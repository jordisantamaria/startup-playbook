# 07 - Stack y Herramientas

## Todo lo que necesitas. Nada mas.

### Producto

| Herramienta | Para que | Precio |
|-------------|----------|--------|
| **[Supastarter](https://supastarter.dev)** | Boilerplate completo (auth, payments, landing, blog, i18n, admin) | $299 one-time |
| **[Vercel](https://vercel.com)** | Deploy con git push | Free tier |
| **[Neon](https://neon.tech)** | Postgres serverless | Free tier (0.5GB) |
| **[Stripe](https://stripe.com)** | Pagos y suscripciones | 2.9% + 30c/tx |
| **[Resend](https://resend.com)** | Emails transaccionales | Free (3k/mes) |
| **[Cloudflare](https://cloudflare.com)** | DNS, CDN, proteccion | Free |
| **Namecheap** | Dominios | ~$10/año |

### AI (tu co-pilot)

| Herramienta | Para que | Precio |
|-------------|----------|--------|
| **Claude Code** | Escribir codigo, tu herramienta principal de build | ~$100/mes (API) |
| **Claude Pro** | Research, copy, estrategia, analisis | $20/mes |
| **[v0.dev](https://v0.dev)** | Generar UI components | Free / $20/mes |
| **[Perplexity](https://perplexity.ai)** | Research con fuentes | Free / $20/mes |

### Analytics y monitoring

| Herramienta | Para que | Precio |
|-------------|----------|--------|
| **[PostHog](https://posthog.com)** | Product analytics, funnels, session replay | Free (1M events/mes) |
| **[Plausible](https://plausible.io)** | Web analytics simple | $9/mes |
| **[Sentry](https://sentry.io)** | Error tracking | Free (5k events/mes) |
| **[BetterUptime](https://betterstack.com)** | Uptime monitoring | Free (10 monitors) |

### Gestion de proyecto

| Herramienta | Para que | Precio |
|-------------|----------|--------|
| **GitHub Issues + Projects** | Tareas, bugs, kanban board | Free |

No uses Notion, Jira, Linear ni nada mas. Cada producto tiene su repo, cada repo tiene sus issues. El Projects board de GitHub es un kanban gratis. Todo en el mismo sitio que tu codigo. Lo que hacen Levels, Marc Lou y Tony Dinh.

### Marketing y presencia (todo gratis)

| Herramienta | Para que | Precio |
|-------------|----------|--------|
| **Twitter/X** | Build in public, tu canal principal | Free |
| **[Product Hunt](https://producthunt.com)** | Launch day | Free |
| **[Indie Hackers](https://indiehackers.com)** | Comunidad, feedback | Free |
| **[Logofa.st](https://logofa.st)** | Logo rapido | Free |
| **[Termly](https://termly.io)** | Privacy policy, terms | Free |
| **[Otter.ai](https://otter.ai)** | Transcribir calls (si hablas con usuarios) | Free (300 min/mes) |

**Cuentas de Twitter/X**: usa dos cuentas separadas.
- Cuenta indie (nombre completo): para build in public, lanzamientos, contenido de producto. Todo en ingles.
- Cuenta personal: para tus intereses personales. No mezcles audiencias — confunde al algoritmo y a los seguidores.

**Cuando crear la cuenta indie**: cuando empieces a construir tu primer producto. No antes. El algoritmo de X favorece cuentas nuevas que publican consistentemente las primeras semanas — si la creas y la dejas vacia, pierdes ese boost.

```
Viernes:         Crea la cuenta
Sabado-domingo:  2-3 tweets del proceso de build (screenshots, decisiones, progreso)
Lunes:           Tweet/thread del launch + link a Product Hunt
Semana 1-2:      Numeros reales, feedback, iteraciones
Despues:         3-5 tweets/semana sobre tu proceso
```

El primer tweet tiene que ser algo real, no "hey estoy aqui". Ejemplo: "Building [X] this weekend. The problem: [1 frase]. Let's see if anyone needs this."

### Comunicacion (cuando crezcas)

| Herramienta | Para que | Cuando |
|-------------|----------|--------|
| **[Loops](https://loops.so)** | Email marketing, newsletter | Cuando tengas 500+ usuarios |
| **[Crisp](https://crisp.chat)** | Chat widget de soporte | Cuando tengas usuarios de pago |

## Coste total

| Momento | Coste |
|---------|-------|
| Setup (dia 0) | $309 (Supastarter + dominio) |
| Mes 1 | ~$120 (solo AI tools) |
| Mes 2+ (con traccion) | ~$175/mes |
| Cuando hay revenue | Stripe se lleva 2.9% + 30c por pago |

Todo lo demas es free tier hasta que tengas revenue para pagarlo.

## Diseño

No necesitas diseñador. La plantilla de Supastarter ya tiene diseño profesional (shadcn/ui, Tailwind).

Tu approach:
- Usa la landing de Supastarter tal cual, cambia el copy y pon screenshot de tu producto en el hero
- Los componentes de shadcn/ui son el estandar actual (los usa Linear, Vercel, etc.)
- Si necesitas algo visual especifico, v0.dev lo genera
- El diseñador solo entra si escalas a empresa con inversion (fase 06-Scale)

## Setup en 1 hora

```bash
# 1. Fork Supastarter
# 2. Instalar
pnpm install

# 3. Copiar env
cp .env.example .env

# 4. Llenar las keys:
#    - DATABASE_URL (Neon dashboard → connection string)
#    - STRIPE_SECRET_KEY (Stripe dashboard → API keys)
#    - RESEND_API_KEY (Resend dashboard → API keys)
#    - AUTH_SECRET (npx auth secret)

# 5. Database
pnpm db:migrate
pnpm db:seed

# 6. Dev
pnpm dev

# 7. Deploy
git push  # Vercel auto-deploys
```
