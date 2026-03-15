# 03 - Build

## MVP en un finde

Tu stack: Supastarter ($299, one-time) + Claude Code + Vercel. Con esto tienes auth, payments, landing, blog, email, i18n ya hechos. Tu solo añades la feature core.

## El finde

### Viernes noche (2-3h)

```
1. Fork de Supastarter
2. pnpm install && cp .env.example .env
3. Crea cuentas (si no las tienes): Vercel, Neon, Stripe, Resend
4. Llena las env vars
5. pnpm dev — ya tienes app con auth + payments + landing
6. Define el scope: ¿cual es la UNA feature que resuelve el problema?
```

### Sabado (8-10h)

```
1. Implementa la feature core con Claude Code
2. No hagas: onboarding fancy, settings, admin panel, notificaciones
3. Si haces: la funcionalidad que resuelve el problema
4. Conecta Stripe: al menos 1 plan de pago
5. Test manual: funciona el flow completo? signup → usar → pagar?
```

### Domingo (6-8h)

```
Manana:
1. Landing page: edita el copy de Supastarter
   - Hero: problema en 1 frase + solucion + CTA
   - Features: 3-4 bullets de lo que hace
   - Pricing: 1-2 planes, simple
   - FAQ: 3-4 preguntas obvias
2. Deploy a Vercel: git push

Tarde:
3. Dominio: compra en Namecheap/Cloudflare (~$10)
   O usa el .vercel.app para validar primero
4. Prepara assets para Product Hunt:
   - Logo (Logofa.st, 2 min)
   - Tagline (1 frase)
   - Descripcion (3-4 parrafos)
   - Screenshots / GIF del producto
5. Programa el post de PH para manana a las 00:01 PST
```

## Reglas del MVP

### SI hacer

- La feature que resuelve el problema core
- Auth (ya viene con Supastarter)
- Cobrar (Stripe ya integrado)
- Landing page con copy claro
- Deploy publico

### NO hacer

- Admin panel
- Onboarding wizard de 5 pasos
- Sistema de notificaciones
- Dashboard con graficos
- Tests automatizados (si, en serio — es un MVP)
- Soporte multi-idioma (usa ingles, mercado global)
- App movil
- Integraciones con 10 servicios
- Dark mode custom (el de Supastarter ya viene)

### Scope check

Si dices "necesito hacer X antes de lanzar", preguntate:

```
¿El usuario puede resolver su problema SIN esta feature?
├── SI → No la hagas. Lanza sin ella
└── NO → Hacela. Pero solo esa
```

## Claude Code como co-pilot

Tu no escribes todo el codigo. Claude Code escribe, tu diriges:

```
Workflow:
1. Describe la feature en lenguaje natural
2. Claude Code implementa
3. Tu revisas y ajustas
4. Repite

Ejemplo:
"Crea una pagina /dashboard que muestre una lista de [ENTIDAD] del usuario logueado.
Cada item muestra nombre, fecha, y un boton para editar.
Usa los componentes de shadcn/ui que ya estan en el proyecto.
El data viene de la tabla [TABLA] en Drizzle."
```

Con este workflow un dev experimentado puede construir un MVP completo en 16-20 horas.

## Herramientas de build

| Herramienta | Para que | Cuando usarla |
|-------------|----------|---------------|
| **Claude Code** | Escribir codigo, debuggear, refactorizar | Todo el finde |
| **v0.dev** | Generar componentes UI rapido | Si necesitas una UI especifica |
| **Supastarter** | El boilerplate base | Setup inicial |
| **Vercel** | Deploy | Cada git push |
| **Neon** | Base de datos | Ya configurado con Supastarter |
