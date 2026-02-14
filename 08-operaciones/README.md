# 08 - Operaciones y Escalado

## De startup a empresa: cuando las cosas empiezan a funcionar

Felicidades, tienes producto, usuarios y revenue. Ahora el reto cambia: ya no es sobrevivir, es **escalar sin romperte**.

## Senales de que necesitas escalar operaciones

- Estas diciendo que no a clientes porque no das abasto
- Los bugs y fires te consumen mas tiempo que construir
- Haces todo a mano y no es sostenible
- El equipo crece y la comunicacion se rompe
- Los procesos que funcionaban con 3 personas no funcionan con 10

## Metricas y dashboards

### Metricas que un founder debe revisar semanalmente

```
REVENUE
- MRR (Monthly Recurring Revenue)
- MRR growth rate (mes a mes)
- ARPU (Average Revenue Per User)
- Net Revenue Retention

USUARIOS
- New signups
- Activation rate (% que completa accion clave)
- DAU/WAU/MAU
- Churn rate

UNIT ECONOMICS
- CAC (Customer Acquisition Cost)
- LTV (Lifetime Value)
- LTV/CAC ratio (target: >3)
- Payback period

CASH
- Burn rate mensual
- Runway (meses de cash restantes)
- Revenue vs gastos
```

### Herramientas para dashboards

| Herramienta | Mejor para | Precio |
|-------------|-----------|--------|
| **Metabase** | SQL dashboards, self-hosted | Gratis (OSS) |
| **Posthog** | Product analytics | Gratis hasta 1M eventos |
| **Mixpanel** | Analisis de comportamiento | Gratis tier |
| **Stripe Dashboard** | Revenue metrics | Incluido con Stripe |
| **Google Sheets** | Cuando eres < 10 personas | Gratis |
| **ChartMogul** | SaaS metrics | Desde 99$/mes |

## Procesos esenciales

### 1. Ciclo de desarrollo

```
Sprint semanal (cuando eres 2-5 personas):

Lunes: Planning (30 min)
- Que vamos a hacer esta semana?
- Prioridades basadas en impacto
- Quien hace que

Viernes: Review + Retro (30 min)
- Que se hizo?
- Que aprendimos?
- Que cambiamos para la semana que viene?

Herramientas: Linear, GitHub Issues, o simplemente un doc compartido
```

### 2. Customer support

```
Nivel 1: Self-service
- FAQ, documentacion, videos
- Chatbot con AI (si aplica)

Nivel 2: Soporte humano
- Email o chat
- SLA: responder en < 24h (< 4h para clientes de pago)
- Template de respuestas para problemas comunes

Nivel 3: Escalacion
- Bugs criticos -> equipo de desarrollo
- Churn risk -> founder/account manager

Herramientas: Intercom, Crisp, o simplemente email + Notion
```

### 3. Hiring process

```
1. Define el rol (job description clara)
2. Publica en 2-3 canales relevantes
3. Screening inicial (CV + mini-cuestionario)
4. Entrevista cultura/fit (30 min)
5. Prueba tecnica/practica (pagada, 2-4 horas)
6. Entrevista final con founders
7. Referencia check (2-3 referencias)
8. Oferta

Timeline ideal: < 3 semanas de principio a fin
```

### 4. Decision-making framework

```
Para decisiones reversibles (Type 2):
- Decide rapido (< 1 dia)
- No necesitas consenso
- Mejor pedir perdon que permiso
- Ejemplos: cambiar copy, probar un nuevo canal, feature flags

Para decisiones irreversibles (Type 1):
- Tomalo con calma (1-3 dias)
- Busca input del equipo
- Documenta la decision y el razonamiento
- Ejemplos: despedir a alguien, pivotar el producto, levantar inversion
```

## Cultura de startup

### Principios que funcionan en early stage

1. **Transparencia radical**: Comparte metricas, planes, problemas con todo el equipo
2. **Ownership**: Cada persona es duena de su area, no un ejecutor de tareas
3. **Velocidad**: Sesgo hacia la accion. "Done is better than perfect"
4. **Feedback constante**: Directo, constructivo, y frecuente
5. **Aprendizaje**: Los errores se analizan, no se castigan

### Lo que NO escala (y cuando cambiarlo)

| Funciona con 3 personas | No funciona con 15 | Solucion |
|-------------------------|-------------------|----------|
| Todo el mundo sabe todo | Info se pierde | Documentar decisiones |
| Comunicacion informal | Ruido, malentendidos | Standups + canales claros |
| Founders hacen soporte | No da tiempo | Contratar soporte |
| Deploy manual | Errores, lentitud | CI/CD automatizado |
| "Ya lo hablamos" | Nadie se acuerda | Escribirlo en Notion/doc |

## Cuando pivotar vs perseverar

### Senales de que debes pivotar

- Churn alto persistente (>10% mensual) despues de 6+ meses
- No puedes explicar por que los usuarios se quedan (no hay "aha moment")
- CAC crece y LTV se estanca
- Los usuarios usan tu producto de forma diferente a la esperada
- No ves un camino claro a 10x en 12 meses
- Tu motivacion se basa en "hemos invertido mucho" (sunk cost fallacy)

### Senales de que debes perseverar

- Algunos usuarios AMAN tu producto (aunque sean pocos)
- Los que se quedan, se quedan mucho tiempo (buena retencion)
- Las metricas mejoran mes a mes (aunque sea poco)
- Los usuarios te dicen exactamente que falta para pagar mas
- Sientes que estas cerca de algo (pero valida con datos, no solo feeling)

### Tipos de pivot

| Tipo | Ejemplo |
|------|---------|
| **Zoom-in** | Una feature se convierte en el producto entero |
| **Zoom-out** | Tu producto se convierte en una feature de algo mas grande |
| **Segmento** | Mismo producto, diferente cliente |
| **Necesidad** | Mismo cliente, diferente problema |
| **Canal** | Mismo producto, diferente canal de distribucion |
| **Tecnologia** | Mismo problema, diferente solucion tecnica |
| **Modelo** | Mismo producto, diferente forma de monetizar |

## Checklist de escalado

Antes de escalar, asegurate de tener:

- [ ] Product-market fit validado (NPS > 40, retencion fuerte)
- [ ] Unit economics positivos (LTV > 3x CAC)
- [ ] Al menos 1 canal de adquisicion predecible y escalable
- [ ] Procesos documentados para las operaciones core
- [ ] Cash/runway para al menos 12 meses
- [ ] Equipo que puede operar sin que los founders hagan todo
- [ ] Infraestructura tecnica que aguanta 10x de usuarios actuales

## Prompt AI: Diagnostico de operaciones

```
Mi startup tiene las siguientes metricas:
- MRR: [MRR]
- Usuarios activos: [NUMERO]
- Equipo: [NUMERO DE PERSONAS]
- Churn mensual: [%]
- CAC: [NUMERO]
- LTV: [NUMERO]
- Burn rate: [NUMERO/MES]
- Runway: [MESES]

Principales problemas:
- [PROBLEMA 1]
- [PROBLEMA 2]
- [PROBLEMA 3]

Analiza mi situacion y dame:
1. Diagnostico: que esta bien y que esta mal
2. Las 3 cosas mas urgentes que deberia hacer
3. Que deberia dejar de hacer
4. Que deberia medir que probablemente no estoy midiendo
5. Recomendacion: escalar, optimizar, o pivotar?
```

---

## Recursos adicionales

### Libros recomendados

| Libro | Autor | Para que fase |
|-------|-------|--------------|
| The Mom Test | Rob Fitzpatrick | Validacion |
| The Lean Startup | Eric Ries | Ideacion a MVP |
| Zero to One | Peter Thiel | Vision estrategica |
| Traction | Gabriel Weinberg | Go-to-market |
| Blitzscaling | Reid Hoffman | Escalado |
| The Hard Thing About Hard Things | Ben Horowitz | Operaciones/liderazgo |
| Venture Deals | Brad Feld | Financiacion |
| Running Lean | Ash Maurya | Validacion + Lean Canvas |

### Podcasts

- **How I Built This** (NPR) - Historias de founders
- **Indie Hackers** - Bootstrapped startups
- **The Twenty Minute VC** - Venture capital
- **Itnig** (ES) - Startups en Espana
- **Lenny's Podcast** - Product y growth

### Newsletters

- **TLDR** - Tech news diario
- **Indie Hackers** - Comunidad + historias
- **Lenny's Newsletter** - Product management
- **The Hustle** - Business y startups

---

**Volver al [indice](../README.md)**
