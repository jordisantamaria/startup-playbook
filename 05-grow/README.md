# 05 - Grow

## De los primeros pagos a $5-10k MRR — todo organico

Si has llegado aqui, alguien ha pagado. Ahora el objetivo es crecer sin gastar en ads.

## Tus 3 canales (no necesitas mas)

### 1. Build in Public (Twitter/X)

Tu canal principal. Documenta todo:
- Numeros reales (MRR, usuarios, signups, churn)
- Decisiones de producto (que construyes y por que)
- Lecciones aprendidas (errores, pivots)
- Stack tecnico (a los devs les encanta esto)
- Updates semanales

**Cadencia**: 3-5 tweets por semana. No necesitas mas.

**El loop**: documentas → la gente sigue → algunos prueban tu producto → algunos pagan → documentas los numeros → mas gente sigue → ...

Es marketing pero no se siente como marketing porque estas siendo genuino.

### 2. SEO (trafico gratuito de Google)

La estrategia mas poderosa a medio-largo plazo. Pieter Levels genera la mayoria de su trafico via SEO.

**SEO basico (contenido)**:
- Identifica 5-10 keywords que tu target busca en Google
- Escribe posts de blog optimizados (Supastarter ya trae blog con MDX)
- Ejemplo: si tu producto es un "invoice tracker", escribe "best invoice tracking tools 2026", "how to track freelance invoices"
- Usa Claude para generar borradores, tu editas y adds tu voz

**SEO programatico (avanzado)**:
- Genera paginas automaticamente desde tu base de datos
- Ejemplo (Levels): Nomad List genera una pagina por cada ciudad. Miles de paginas indexadas
- Ejemplo: si tu producto tiene datos, crea paginas tipo "/best-[cosa]-in-[lugar]"
- Cada pagina es un punto de entrada desde Google

**Timeline**: el SEO tarda 2-3 meses en dar resultados. Empieza ya pero no dependas de el al principio.

### 3. Comunidades del nicho

No spam. Participa genuinamente y menciona tu producto cuando es relevante:
- Responde preguntas donde tu producto es la solucion
- Comparte aprendizajes utiles sin vender
- Si alguien tiene el problema que tu resuelves, sugiere tu producto naturalmente

## Iteracion de producto

Mientras creces, mejora el producto basado en feedback de usuarios que pagan:

```
1. Habla con los que pagan (email, chat, call corta)
2. ¿Que les falta? ¿Que les frustra?
3. Construye lo que piden los que pagan, no lo que sugieren los que no pagan
4. Ship rapido, 1-2 features por semana
5. Anuncia cada update en Twitter (contenido gratis)
```

## Metricas que importan

| Metrica | Target | Como medir |
|---------|--------|-----------|
| **MRR** | Cualquier crecimiento mensual positivo | Stripe dashboard |
| **Churn** | <5% mensual | Stripe / PostHog |
| **Signups/semana** | Tendencia creciente | PostHog |
| **Fuentes de trafico** | Saber de donde vienen | Plausible / PostHog |

No midas 20 metricas. Estas 4 son suficientes.

## Lo que NO hacer para crecer

- No gastes en ads (todavia)
- No contrates community manager
- No crees newsletter antes de tener 500+ usuarios
- No hagas partnerships / integraciones todavia
- No optimices conversion rate con <1000 visitas/mes (no tienes datos suficientes)

## Milestone: $5k MRR

Cuando llegues a ~$5k MRR consistente, tienes un negocio real. Aqui decides:

```
¿Quiero seguir creciendo?
├── No, $5-20k/mes esta bien → Quédate solo. Lifestyle business. Has ganado
└── Si, quiero ir a mas → Lee 06-Scale
```
