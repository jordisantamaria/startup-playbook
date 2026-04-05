# How I Configured Claude Code as My Full Dev Stack — Permissions, Rules, Hooks, and Workflow

> I'm a fullstack developer and indie hacker based in Japan, building AI-powered products. After months of refining my Claude Code setup, here's my complete configuration — from security permissions to custom status lines.

## Why This Matters

Claude Code is powerful out of the box, but the default experience is full of permission prompts that break your flow. Every `git log`, every file read — confirm, confirm, confirm.

I spent time configuring it so I can focus on building, not clicking "Yes" 50 times per session. Here's exactly how.

## 1. Permissions: Allow What's Safe, Block What's Dangerous

The key insight: **allow all read-only and common dev operations, explicitly block destructive ones.**

### Deny list (things that should NEVER run without asking)

```json
{
  "permissions": {
    "deny": [
      "Read(~/.ssh/**)",
      "Read(~/.aws/**)",
      "Read(**/.env*)",
      "Write(~/.ssh/**)",
      "Write(~/.aws/**)",
      "Bash(curl * | bash)",
      "Bash(ssh *)",
      "Bash(scp *)",
      "Bash(nc *)",
      "Bash(rm -rf *)",
      "Bash(git push --force*)",
      "Bash(git reset --hard*)"
    ]
  }
}
```

This protects you from:
- Accidentally exposing secrets (SSH keys, AWS credentials, .env files)
- Remote code execution (`curl | bash`)
- Destructive git operations (force push, hard reset)
- Deleting everything (`rm -rf`)

### Allow list (things that should run without prompts)

```json
{
  "permissions": {
    "allow": [
      "Read",
      "Glob",
      "Grep",
      "Edit",
      "Write",
      "Bash(git status*)",
      "Bash(git diff*)",
      "Bash(git log*)",
      "Bash(git show*)",
      "Bash(git branch*)",
      "Bash(git fetch*)",
      "Bash(git pull*)",
      "Bash(git add*)",
      "Bash(git commit*)",
      "Bash(git push*)",
      "Bash(git checkout*)",
      "Bash(git switch*)",
      "Bash(git stash*)",
      "Bash(cd *)",
      "Bash(pnpm *)",
      "Bash(npx *)",
      "Bash(tsc*)",
      "Bash(node *)",
      "Bash(ls *)",
      "Bash(mkdir *)",
      "Bash(cp *)",
      "Bash(mv *)",
      "Bash(find *)",
      "Bash(grep *)",
      "Bash(gh *)"
    ]
  }
}
```

The result: Claude Code flows like a human pair programmer. It reads files, runs git commands, installs packages — all without interrupting you. But it can never touch your secrets or destroy your work.

**Important**: `git push` is allowed but `git push --force` is denied. The deny list takes priority over the allow list.

## 2. Rules: Teaching Claude How YOU Work

Rules are markdown files in `~/.claude/rules/` that Claude loads every session. Think of them as your coding standards, enforced automatically.

I organize mine by scope:

```
~/.claude/rules/
  common/
    coding-style.md    # Immutability, file organization, error handling
    git-workflow.md     # Commit message format, PR workflow
    security.md         # Mandatory security checks before commits
    testing.md          # 80% coverage minimum, TDD workflow
    code-review.md      # Review checklist, severity levels
    performance.md      # Model selection, context management
    agents.md           # When to use which agent
    patterns.md         # Repository pattern, API response format
  typescript/
    coding-style.md     # TS-specific conventions
    testing.md          # Vitest, Playwright patterns
    security.md         # XSS, injection prevention
```

### Example: My coding style rule

```markdown
# Coding Style

## Immutability (CRITICAL)
ALWAYS create new objects, NEVER mutate existing ones.

## File Organization
MANY SMALL FILES > FEW LARGE FILES:
- 200-400 lines typical, 800 max
- Organize by feature/domain, not by type

## Error Handling
ALWAYS handle errors explicitly at every level.
Never silently swallow errors.
```

Claude follows these rules in every session, across every project. No need to repeat yourself.

## 3. Hooks: Automating the Boring Stuff

Hooks are shell commands that run on specific events. Three I use:

### Session evaluation (on stop)

```json
{
  "hooks": {
    "Stop": [
      {
        "hooks": [
          {
            "type": "command",
            "command": "node ~/.claude/plugins/.../evaluate-session.js",
            "async": true
          }
        ]
      }
    ]
  }
}
```

Automatically evaluates the session quality when Claude stops — useful for tracking how productive each session was.

### Desktop notifications

```json
{
  "Notification": [
    {
      "hooks": [
        {
          "type": "command",
          "command": "notify-send 'Claude Code' 'Needs your attention'",
          "async": true
        }
      ]
    }
  ]
}
```

When Claude needs input, I get a desktop notification. No more staring at the terminal waiting.

## 4. Custom Status Line

I built a Starship-style status line that shows:
- Current directory
- Git branch
- Model name
- Context window usage (color-coded: green < 50%, yellow < 80%, red > 80%)

```bash
#!/usr/bin/env bash
input=$(cat)
cwd=$(echo "$input" | jq -r '.workspace.current_dir // ""')
model=$(echo "$input" | jq -r '.model.display_name // ""')
used=$(echo "$input" | jq -r '.context_window.used_percentage // empty')

# Git branch
branch=$(git -C "$cwd" symbolic-ref --short HEAD 2>/dev/null)

# Color-coded context usage
used_int=$(printf '%.0f' "$used")
if [ "$used_int" -ge 80 ]; then
  ctx_color='\033[31m'  # red
elif [ "$used_int" -ge 50 ]; then
  ctx_color='\033[33m'  # yellow
else
  ctx_color='\033[32m'  # green
fi

printf '\033[34m%s\033[0m \033[35m%s\033[0m \033[36m[%s]\033[0m %bctx:%s%%\033[0m' \
  "$cwd" "$branch" "$model" "$ctx_color" "$used_int"
```

The context usage indicator is crucial — when it hits 80%+, I know I need to wrap up or start a new session.

## 5. Skills: Reusable Workflows

Skills are slash commands you define once and use forever:

```
~/.claude/skills/
  commit/SKILL.md          # /commit — smart commit messages
  commit-push-pr/SKILL.md  # /commit-push-pr — full PR workflow
  pr/SKILL.md              # /pr — create GitHub PR
  issue/SKILL.md           # /issue — create GitHub issue
```

Instead of explaining "commit this, push it, create a PR with a good description" every time, I just type `/commit-push-pr`.

## 6. Environment Tuning

```json
{
  "env": {
    "MAX_THINKING_TOKENS": "10000",
    "CLAUDE_AUTOCOMPACT_PCT_OVERRIDE": "50"
  },
  "language": "spanish",
  "attribution": {
    "commit": "",
    "pr": ""
  }
}
```

- **MAX_THINKING_TOKENS**: Caps extended thinking to avoid burning tokens on simple tasks
- **AUTOCOMPACT at 50%**: Compresses conversation history earlier, keeping more room for actual work
- **Language**: Claude responds in Spanish (my native language) while code stays in English
- **Attribution disabled**: No "Co-Authored-By: Claude" in commits

## 7. Plugins

```json
{
  "enabledPlugins": {
    "everything-claude-code@everything-claude-code": true,
    "frontend-design@claude-plugins-official": true,
    "typescript-lsp@claude-plugins-official": true
  }
}
```

- **Everything Claude Code**: Adds 100+ specialized agents, skills, and tools
- **Frontend Design**: UI generation capabilities
- **TypeScript LSP**: Type-aware code intelligence

## The Result

Before this setup: constant permission prompts, no consistency across projects, manual repetitive workflows.

After: Claude Code works like a senior dev who knows my standards, follows my conventions, and never asks permission for safe operations. I focus on building products, not configuring tools.

The full `settings.json` is about 130 lines. It took a few sessions to get right, but now every new project inherits the same workflow automatically.

---

*I'm building two products in Japan: [paopaoanime.com](https://paopaoanime.com) (anime streaming schedule) and an AI business Japanese trainer. Follow the journey on X: [@jordisantadev](https://x.com/jordisantadev)*
