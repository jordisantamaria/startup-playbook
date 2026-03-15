# 09 - Tooling y Stack

## El stack completo para lanzar un SaaS en un finde

No necesitas mas que esto. Cada herramienta tiene free tier suficiente para validar. Solo pagas cuando hay traccion.

## Stack de producto

| Area | Herramienta | Precio | Para que |
|------|-------------|--------|----------|
| **Boilerplate** | [Supastarter](https://supastarter.dev) | $299 one-time | Auth, payments, orgs, email, i18n, admin, landing, blog — todo listo |
| **Alternativa** | [Shipfast](https://shipfa.st) | $199 one-time | Mas simple que Supastarter, sin multi-tenant ni i18n |
| **Alternativa gratis** | [next-saas-stripe-starter](https://github.com/mickasmt/next-saas-stripe-starter) | Gratis | Basico pero funcional, shadcn/ui |
| **Deploy** | [Vercel](https://vercel.com) | Free tier | Deploy automatico con git push, CDN global |
| **Base de datos** | [Neon](https://neon.tech) | Free tier (0.5GB) | Postgres serverless, branching para dev |
| **Alternativa DB** | [Supabase](https://supabase.com) | Free tier (500MB) | Postgres + auth + storage + realtime |
| **Dominio** | Namecheap / Cloudflare | ~$10/año | |
| **DNS + CDN** | [Cloudflare](https://cloudflare.com) | Free | DNS rapido, proteccion DDoS, cache |

## Stack de pagos

| Area | Herramienta | Precio | Para que |
|------|-------------|--------|----------|
| **Pagos** | [Stripe](https://stripe.com) | 2.9% + 30c por tx | Suscripciones, one-time, checkout |
| **Alternativa** | [Lemon Squeezy](https://lemonsqueezy.com) | 5% + 50c por tx | Merchant of Record (ellos manejan taxes/IVA) |

**Cuando elegir cada uno**:
- **Stripe**: mas barato, mas control, mas trabajo con taxes
- **Lemon Squeezy**: mas caro, pero se encarga de todo el tax/VAT compliance. Ideal si vendes globalmente y no quieres complicarte

## Stack de comunicacion

| Area | Herramienta | Precio | Para que |
|------|-------------|--------|----------|
| **Email transaccional** | [Resend](https://resend.com) | Free (3k/mes) | Magic links, verificacion, notificaciones |
| **Email marketing** | [Loops](https://loops.so) | Free (1k contactos) | Newsletters, onboarding sequences, waitlist |
| **Alternativa email** | [Resend Audiences](https://resend.com/audiences) | $0-25/mes | Si ya usas Resend, unifica transaccional + marketing |
| **Chat/soporte** | [Crisp](https://crisp.chat) | Free (2 seats) | Widget de chat en tu app |
| **Alternativa soporte** | [Intercom](https://intercom.com) | $39/mes | Mas completo pero mas caro |

## Stack de analytics y monitoring

| Area | Herramienta | Precio | Para que |
|------|-------------|--------|----------|
| **Product analytics** | [PostHog](https://posthog.com) | Free (1M events/mes) | Funnels, retention, feature flags, session replay |
| **Web analytics** | [Plausible](https://plausible.io) | $9/mes | Alternativa a Google Analytics, privacy-first |
| **Alternativa analytics** | [Umami](https://umami.is) | Free (self-host) | Open source, self-hosted |
| **Error tracking** | [Sentry](https://sentry.io) | Free (5k events/mes) | Errores en produccion con stack traces |
| **Uptime** | [BetterUptime](https://betterstack.com/uptime) | Free (10 monitors) | Te avisa si tu app se cae |

## Stack de marketing

| Area | Herramienta | Precio | Para que |
|------|-------------|--------|----------|
| **Landing (si no usas Supastarter)** | [Framer](https://framer.com) | Free / $5/mes | Landing pages sin codigo |
| **Legal** | [Termly](https://termly.io) | Free | Privacy policy, terms of service auto-generados |
| **OG Images** | [Vercel OG](https://vercel.com/docs/og-image-generation) | Free | Previews dinamicas en redes sociales |
| **Logo rapido** | [Logofa.st](https://logofa.st) | Free | Logo decente en 2 minutos |
| **Social scheduling** | [Buffer](https://buffer.com) | Free (3 canales) | Programar posts en Twitter/LinkedIn |
| **Feedback** | [Canny](https://canny.io) | Free | Feature requests y roadmap publico |

## Stack de AI (para el founder)

| Area | Herramienta | Precio | Para que |
|------|-------------|--------|----------|
| **AI general** | Claude Pro | $20/mes | Research, copy, estrategia, analisis |
| **Coding** | Claude Code | $100/mes (API) | Desarrollo acelerado 5-10x |
| **Research con fuentes** | [Perplexity Pro](https://perplexity.ai) | $20/mes | Buscar info con fuentes verificables |
| **Prototipado UI** | [v0.dev](https://v0.dev) | Free / $20/mes | Genera componentes React desde texto |
| **Transcripciones** | [Otter.ai](https://otter.ai) | Free (300 min/mes) | Transcribir calls de validacion |

## Coste total para validar

| Fase | Coste |
|------|-------|
| **Dia 0** | $299 (Supastarter) + $10 (dominio) = **$309** |
| **Mes 1** | Todo en free tiers = **$0** adicional |
| **Mes 2-3** (si hay traccion) | Vercel Pro $20 + Loops $25 + Plausible $9 = **~$54/mes** |
| **Herramientas AI** | Claude $20 + Claude Code ~$100 = **~$120/mes** |

**Total primer mes**: ~$430 (con AI incluido). Despues ~$175/mes hasta que haya revenue.

## Decisiones de stack que NO importan (ahora)

No pierdas tiempo decidiendo:
- Postgres vs MySQL (usa Postgres, fin)
- AWS vs GCP vs Vercel (usa Vercel, fin)
- React vs Vue vs Svelte (Supastarter usa Next.js, fin)
- Tailwind vs CSS modules (Tailwind, fin)
- Jest vs Vitest (el que traiga el boilerplate, fin)

Estas decisiones solo importan a escala. Cuando tengas ese problema, sera un buen problema.

## Setup en 1 hora

```
1. Compra Supastarter Solo ($299)
2. Fork/clone el repo
3. Crea cuenta en:
   - Vercel (deploy)
   - Neon (database)
   - Stripe (pagos)
   - Resend (emails)
   - PostHog (analytics)
4. Copia .env.example, llena las keys
5. pnpm install && pnpm dev
6. Ya tienes app con auth + payments + landing + blog
7. Customiza: logo, colores, copy de la landing
8. Deploy a Vercel: git push
```

---

**Siguiente**: [10 - Ecosistema Indie](../10-ecosistema-indie/) - Donde aprender, a quien seguir, como entrar en la comunidad
