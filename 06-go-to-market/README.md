# 06 - Go-to-Market

## Tu producto no se vende solo

Tener un buen producto es necesario pero no suficiente. Necesitas una estrategia clara para llegar a tus primeros usuarios y convertirlos en clientes de pago.

## Los primeros 100 usuarios

### Estrategia: Do things that don't scale

Los primeros usuarios NO se consiguen con growth hacking ni con ads. Se consiguen con trabajo manual, uno a uno.

**Tacticas para los primeros 100**:

| Tactica | Esfuerzo | Efectividad | Coste |
|---------|----------|-------------|-------|
| **Outreach personal** | Alto | Muy alta | Gratis |
| **Tu red de contactos** | Bajo | Alta | Gratis |
| **Comunidades online** | Medio | Media-Alta | Gratis |
| **Product Hunt launch** | Medio | Variable | Gratis |
| **Content marketing** | Alto | Media (largo plazo) | Gratis |
| **Partnerships** | Medio | Alta | Gratis |
| **Cold email** | Medio | Media | Gratis-bajo |
| **Paid ads** | Bajo | Media | 500-2000$/mes |

### 1. Outreach personal (Los primeros 10-20)

```
Paso 1: Lista de 50 personas que podrian ser usuarios
- Contactos directos
- Gente de tus entrevistas de validacion
- Personas que respondieron a tu landing page

Paso 2: Mensaje personalizado (NO mass email)
"Hey [NOMBRE], estoy construyendo [PRODUCTO] que resuelve
[PROBLEMA QUE SABES QUE TIENE]. Basandome en nuestra conversacion
sobre [REFERENCIA PERSONAL], creo que te podria interesar probarlo.
Es gratis durante el beta. Te apuntas?"

Paso 3: Onboarding personal
- Llamada 1:1 de 15 min para setup
- Pregunta QUE espera del producto
- Followup a las 24h, 72h, y 1 semana
```

### 2. Comunidades (Usuarios 20-100)

**Donde estar** (depende de tu segmento):

| Tipo de usuario | Comunidades |
|----------------|-------------|
| Developers | Hacker News, DEV.to, Reddit (r/programming), Discord servers |
| Designers | Dribbble, Behance, Designer News |
| Startups/Founders | Indie Hackers, X/Twitter, Product Hunt |
| Marketing | GrowthHackers, Reddit (r/marketing) |
| B2B General | LinkedIn, Slack communities de industria |
| Espana especifico | Forobeta, Startup Spain Slack, meetups locales |

**Como aportar valor sin ser spam**:
1. Participa genuinamente durante 2-4 semanas ANTES de promocionar nada
2. Responde preguntas, ayuda a otros
3. Comparte tu proceso de construccion (build in public)
4. Cuando menciones tu producto, que sea en contexto de resolver un problema real
5. NUNCA hagas "Hey check out my startup!"

### 3. Product Hunt Launch

**Preparacion (2-4 semanas antes)**:
- Consigue un hunter con reputacion (o hazlo tu)
- Prepara assets: video demo, screenshots, tagline
- Recluta 20-30 amigos para que upvoteen y comenten (no bots)
- Elige martes o miercoles (mejores dias)

**El dia del launch**:
- Publica a las 00:01 PST
- Responde TODOS los comentarios
- Comparte en todas tus redes
- Prepara posts de social media programados

**Post-launch**:
- Top 5 del dia = ~500-2000 visitas
- Top 1 del dia = ~2000-5000+ visitas
- Convierte ese trafico: landing clara con CTA

### 4. Build in Public

Comparte tu proceso de construccion en Twitter/X y LinkedIn:
- Numeros reales (MRR, usuarios, metricas)
- Lecciones aprendidas
- Fracasos y pivots
- Decisiones tecnicas y de negocio

**Por que funciona**:
- Genera confianza y autenticidad
- Crea una audiencia antes de lanzar
- Atrae potenciales cofounders, empleados e inversores
- Accountability publica te mantiene motivado

## Pricing: Como cobrar

### Principios de pricing

1. **Cobra desde el dia 1** (o lo mas pronto posible)
2. **Cobra mas de lo que crees** (siempre puedes bajar, subir es dificil)
3. **Pricing simple** (maximo 3 tiers)
4. **Ancla al valor** que generas, no a tu coste

### Modelos de pricing

| Modelo | Mejor para | Ejemplo |
|--------|-----------|---------|
| **Freemium** | Productos con efecto de red o virales | Slack, Notion |
| **Free trial** | SaaS con valor claro que se demuestra en dias | HubSpot |
| **Flat rate** | Productos simples con un caso de uso | Basecamp |
| **Per seat** | Herramientas de equipo | Figma |
| **Usage-based** | APIs, infraestructura | AWS, Stripe |
| **Tiered** | Diferentes segmentos con diferentes necesidades | La mayoria |

### Template de pricing page

```
TIER GRATIS (si aplica)
- Limite de uso claro
- Suficiente para probar, no para usar en serio
- Sin soporte

TIER PRO / INDIVIDUAL
- Para individuos o equipos pequenos
- La mayoria de features
- Soporte por email
- Precio: 15-49$/mes (B2C) o 29-99$/mes (B2B)

TIER BUSINESS / TEAM
- Para equipos y empresas
- Todas las features
- Soporte prioritario
- Integraciones avanzadas
- Precio: 49-199$/mes por equipo

TIER ENTERPRISE
- "Contacta con ventas"
- Custom features
- SLA, SSO, compliance
- Account manager dedicado
```

### Cuando ofrecer gratis vs pagar

```
Ofrece gratis si:
- Tu producto tiene efecto de red
- Necesitas masa critica para que funcione
- El coste marginal por usuario es ~0
- La conversion free->paid es tu motor de crecimiento

Cobra desde el inicio si:
- Tu producto genera valor inmediato y claro
- El segmento puede y esta acostumbrado a pagar
- No tienes financiacion y necesitas revenue
- Quieres validar willingness to pay
```

## Metricas que importan

### Embudo basico

```
Visitantes -> Signups -> Activacion -> Retencion -> Revenue -> Referral

Metricas clave:
- Visitas a landing/web
- Conversion a signup: >5% es bueno
- Activacion (completa accion clave): >40%
- Retencion D7 (vuelve a la semana): >25%
- Retencion D30: >10%
- NPS: >40
```

### Metricas de negocio (cuando ya cobras)

| Metrica | Que es | Target early stage |
|---------|--------|-------------------|
| **MRR** | Monthly Recurring Revenue | Cualquier numero > 0 al principio |
| **Churn** | % de usuarios que se van al mes | <5% mensual |
| **CAC** | Coste de adquirir un cliente | < LTV/3 |
| **LTV** | Lifetime value del cliente | > 3x CAC |
| **Payback** | Meses para recuperar CAC | <12 meses |

## Prompt AI: Estrategia de Go-to-Market

```
Mi startup:
- Producto: [DESCRIPCION]
- Segmento objetivo: [SEGMENTO]
- Pricing: [MODELO Y PRECIO]
- Diferenciador: [POR QUE SOMOS MEJORES]
- Presupuesto marketing: [PRESUPUESTO/MES]
- Mi red actual: [TAMANO Y TIPO DE RED]

Disenname una estrategia de go-to-market para los primeros 6 meses:

Mes 1-2: Los primeros 100 usuarios
Mes 3-4: De 100 a 500 usuarios
Mes 5-6: De 500 a 2000 usuarios

Para cada fase dame:
1. Canales principales (max 2-3 por fase)
2. Tacticas concretas con pasos de ejecucion
3. Presupuesto estimado
4. Metricas y KPIs
5. Riesgos y plan B
```

---

**Siguiente**: [07 - Financiacion](../07-financiacion/) - De donde sale el dinero
