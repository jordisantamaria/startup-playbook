# Dos metodologias: elige tu approach

Hay dos escuelas opuestas para validar una idea. Ambas funcionan, pero para escenarios distintos.

## Metodologia 1: "Ship Fast" (Pieter Levels — MAKE)

**Filosofia**: No valides, lanza. El mercado te dira si funciona.

**El proceso**:
1. Detecta un problema que TU tienes
2. Construye la solucion minima en dias (no semanas)
3. Lanza en Product Hunt, Hacker News, DevHunt, Twitter
4. Si la gente paga, sigue. Si no, siguiente idea
5. Repite hasta que algo pegue

**Principios clave**:
- Cobra desde el dia 1
- No hables con nadie antes de lanzar — tu eres el usuario
- Automatiza todo, sin equipo
- Build in public: documenta el proceso en Twitter
- No te encariñes con ninguna idea
- Un finde = un MVP

**Referentes**:
- Pieter Levels (@levelsio) — Nomad List, RemoteOK, PhotoAI. $3M+/año solo
- Marc Lou (@marc_louvion) — Shipfast, lanza un SaaS al mes
- Tony Dinh (@tdinh_me) — TypingMind, BlackMagic

**Libro**: [MAKE](https://readmake.com) de Pieter Levels

**Stack tipico**: Supastarter/Shipfast + Vercel + Stripe + Resend

## Metodologia 2: "Habla primero" (Rob Fitzpatrick — The Mom Test)

**Filosofia**: No construyas nada hasta que alguien te diga que lo quiere y pagaria por ello.

**El proceso**:
1. Identifica un segmento con un problema
2. Habla con 15-20 personas del segmento (customer discovery)
3. Valida que el problema existe y es importante
4. Enseña tu solucion propuesta (wireframe, no codigo)
5. Si 7/10 dicen "pagaria por esto", construye
6. Entrega a esas mismas personas como primeros usuarios

**Principios clave**:
- Nunca preguntes "usarias mi producto?" (siempre dicen que si)
- Pregunta por comportamiento pasado, no futuro
- Busca el dolor real, no respuestas educadas
- El problema tiene que ser top 3 prioridades del usuario
- Si nadie se emociona hablando del problema, no hay negocio

**Referentes**:
- Rob Fitzpatrick — The Mom Test
- Y Combinator — "Talk to users" como mandamiento
- Steve Blank — Customer Development

**Libro**: [The Mom Test](https://www.momtestbook.com) de Rob Fitzpatrick

## Cuando usar cada una

| Criterio | Ship Fast (Levels) | Habla Primero (Mom Test) |
|----------|-------------------|-------------------------|
| **Tu eres el usuario target** | SI | No necesario |
| **Entiendes el problema de primera mano** | SI | Puede que no |
| **El mercado es B2C** | Ideal | Funciona |
| **El mercado es B2B** | Arriesgado | Ideal |
| **No conoces el sector** | NO | SI |
| **Tienes red de contactos en el sector** | No importa | Muy util |
| **Tiempo disponible** | Un finde | 2-4 semanas |
| **Riesgo de perder tiempo** | Bajo (pierdes un finde) | Bajo (pero mas lento) |

## Decision rapida

```
¿Tienes TU MISMO el problema que quieres resolver?
├── SI → Ship Fast (Levels)
│   Construye en un finde, lanza, mira si pagan
│
└── NO → Habla Primero (Mom Test)
    Habla con 15 personas del segmento antes de escribir una linea de codigo
```

## Approach hibrido (recomendado para la mayoria)

No son excluyentes. Puedes combinar lo mejor de ambas:

1. **Identifica un problema** (tuyo o de un sector que conoces)
2. **3-5 conversaciones rapidas** (no 15) para confirmar que otros tambien lo tienen
3. **Construye MVP en un finde** con Supastarter
4. **Lanza** en Product Hunt / Hacker News / Twitter
5. **Mide**: si la gente paga, sigue. Si no, siguiente

La diferencia con Levels puro: esas 3-5 conversaciones te evitan construir algo que solo tu quieres. La diferencia con Mom Test puro: no pierdes 4 semanas hablando antes de construir.

## Senales de que elegiste mal

**Elegiste Ship Fast pero debias haber hablado primero**:
- Lanzas y nadie entiende para que sirve
- 0 signups despues de una semana en Product Hunt
- La gente prueba pero no vuelve (el problema no es real para ellos)

**Elegiste Mom Test pero debias haber lanzado**:
- Llevas 3 semanas hablando y aun no has escrito codigo
- Las entrevistas son cada vez mas "refinadas" pero no empiezas
- Te da miedo lanzar algo imperfecto (procrastinacion disfrazada de validacion)
