# 03 - AI como Acelerador

## La ventaja injusta del founder tecnico en 2025-2026

AI no reemplaza el trabajo duro, pero te permite hacer en horas lo que antes costaba semanas. La clave es saber **donde** aplicarlo y **donde no**.

## Mapa de AI por fase de startup

### Ideacion y Research

| Tarea | Herramienta AI | Como usarla | Ahorro estimado |
|-------|---------------|-------------|-----------------|
| Analisis de mercado | Claude / ChatGPT | Research profundo de competencia, tendencias, tamanio de mercado | 2-3 dias -> 2-3 horas |
| Analisis de competencia | Perplexity AI | Buscar y comparar competidores con fuentes actualizadas | 1 dia -> 30 min |
| Brainstorming | Claude | Generar y evaluar ideas con frameworks estructurados | - |
| Analisis de tendencias | Perplexity + Claude | Identificar tendencias emergentes en tu sector | 1 dia -> 1 hora |

### Validacion

| Tarea | Herramienta AI | Como usarla |
|-------|---------------|-------------|
| Guiones de entrevista | Claude | Genera guiones adaptados a tu segmento |
| Analisis de entrevistas | Claude | Transcribe (Whisper) + analiza patrones |
| Copy de landing page | Claude / Copy.ai | Genera variantes de copy para A/B test |
| Encuestas | Claude | Disena preguntas sin sesgo |
| Analisis de feedback | Claude | Categoriza y encuentra patrones en feedback |

### Desarrollo de producto

| Tarea | Herramienta AI | Como usarla |
|-------|---------------|-------------|
| Codigo | Claude Code / Cursor / Copilot | Desarrollo acelerado 3-5x |
| Diseno UI | v0.dev / Galileo AI | Genera componentes y layouts |
| Arquitectura | Claude | Disena sistemas, elige tech stack |
| Testing | Claude Code | Genera tests automaticamente |
| Documentacion | Claude | Genera docs tecnicas y de usuario |
| Prototipado | Bolt.new / Lovable | MVP funcional en horas |

### Marketing y Ventas

| Tarea | Herramienta AI | Como usarla |
|-------|---------------|-------------|
| Contenido blog/social | Claude | Genera contenido adaptado a tu voz |
| SEO | Claude + Surfer SEO | Research de keywords + contenido optimizado |
| Emails | Claude | Secuencias de cold outreach personalizadas |
| Ads copy | Claude | Variantes de anuncios para testing |
| Social media | Claude + Canva AI | Contenido visual + copy |

### Operaciones

| Tarea | Herramienta AI | Como usarla |
|-------|---------------|-------------|
| Analisis financiero | Claude | Modelos financieros, proyecciones |
| Legal | Claude | Borradores iniciales (siempre revisar con abogado) |
| Procesos | Claude | Documenta y optimiza workflows |
| Customer support | Claude API | Chatbot para soporte tier 1 |

## Workflows concretos con AI

### Workflow 1: Research de mercado en 2 horas

```
Paso 1: Prompt de contexto (Claude/Perplexity)
"Analiza el mercado de [SECTOR] en [REGION]. Incluye:
- Tamanio de mercado (TAM/SAM/SOM)
- Principales players y su posicionamiento
- Tendencias de los ultimos 2 anios
- Gaps y oportunidades no cubiertas
- Regulaciones relevantes
Usa datos verificables y cita fuentes."

Paso 2: Analisis de competencia
"Para estos 5 competidores: [LISTA]
Crea una tabla comparativa con:
- Pricing
- Features principales
- Target audience
- Puntos fuertes/debiles
- Reviews de usuarios (que se quejan?)
- Tecnologia que usan (BuiltWith, Wappalyzer)"

Paso 3: Oportunidades
"Basandote en el analisis anterior, identifica:
- 3 nichos desatendidos
- 3 funcionalidades que nadie ofrece bien
- 3 modelos de negocio alternativos
- El angulo de posicionamiento mas prometedor para un nuevo entrante"
```

### Workflow 2: De idea a landing page en 1 dia

```
Manana:
1. Refina propuesta de valor con Claude (30 min)
2. Genera copy de landing con Claude (1 hora)
3. Genera estructura/wireframe con v0.dev (30 min)

Tarde:
4. Monta la landing en Framer/Carrd (2 horas)
5. Configura analytics (Plausible/Umami) (30 min)
6. Genera variantes de ads copy con Claude (30 min)
7. Lanza campania de Google/Meta Ads (30 min)
```

### Workflow 3: MVP tecnico en 1 semana con Claude Code

```
Dia 1: Arquitectura y setup
- Usa Claude para definir tech stack y arquitectura
- Scaffold del proyecto con Claude Code
- Setup de base de datos y auth

Dia 2-3: Core features
- Desarrolla la feature principal con Claude Code
- Itera rapido: describe lo que quieres, revisa, ajusta

Dia 4: Integraciones
- APIs externas, pagos (Stripe), email (Resend)
- Claude Code maneja la integracion

Dia 5: Polish y deploy
- UI refinement con v0.dev + Claude Code
- Deploy a Vercel/Railway
- Testing basico

Dia 6-7: Buffer
- Bugs, ajustes, onboarding flow
```

### Workflow 4: Contenido y SEO en piloto automatico

```
1. Research de keywords con Claude + herramienta SEO
2. Genera calendario de contenido (20 posts)
3. Usa Claude para generar borradores
4. Tu editas y anade tu voz personal (CRITICO)
5. Publica con consistencia 2-3x por semana

Prompt para generar contenido:
"Escribe un post de blog/LinkedIn sobre [TEMA] para [AUDIENCIA].
Tono: [casual/profesional/tecnico]
Longitud: [500-800 palabras]
Incluye: datos concretos, ejemplo practico, CTA
Objetivo: [educar/generar leads/SEO]
Keywords: [LISTA]"
```

## Donde NO usar AI (o usarla con cuidado)

| Area | Por que tener cuidado |
|------|----------------------|
| **Entrevistas con usuarios** | La empatia humana es irremplazable. AI puede preparar el guion pero TU hablas |
| **Decisiones estrategicas** | AI te da input, pero la decision final es tuya |
| **Contratos legales** | Usa AI para borradores, pero SIEMPRE revisa con abogado |
| **Relaciones con inversores** | Los inversores invierten en personas, no en AI |
| **Cultura de empresa** | Se construye con acciones, no con prompts |
| **Datos financieros criticos** | Verifica siempre. AI alucina numeros |

## Stack AI recomendado para founders

| Necesidad | Herramienta | Coste |
|-----------|-------------|-------|
| AI general | Claude Pro | 20$/mes |
| Coding | Claude Code / Cursor | 20-100$/mes |
| Research con fuentes | Perplexity Pro | 20$/mes |
| Prototipado UI | v0.dev | Gratis/20$ |
| MVP rapido | Bolt.new / Lovable | Gratis/20$ |
| Automatizaciones | Make / Zapier + AI | Gratis/20$ |
| Imagenes/branding | Midjourney / DALL-E | 10-30$/mes |
| Transcripciones | Whisper (local) / Otter.ai | Gratis/16$ |

**Coste total**: ~100-150$/mes para un stack AI completo de founder.

---

**Siguiente**: [04 - Equipo y Colaboradores](../04-equipo-y-colaboradores/) - No puedes hacerlo todo solo
