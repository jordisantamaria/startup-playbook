# 02 - Validacion

## La regla de oro: No construyas nada hasta que alguien te diga que lo quiere

Tu objetivo es **reducir incertidumbre con el minimo esfuerzo posible**. Cada experimento debe responder una pregunta concreta.

## Niveles de validacion

### Nivel 1: Validacion del problema (Semana 1-2)

**Objetivo**: Confirmar que el problema existe y es importante.

#### Entrevistas de descubrimiento (Customer Discovery)

Habla con **minimo 15 personas** de tu segmento objetivo.

**Reglas de las entrevistas**:
- NUNCA preguntes "usarias mi producto?" (siempre dicen que si)
- NUNCA describas tu solucion antes de entender su problema
- Pregunta por comportamiento pasado, no futuro
- Busca el dolor real, no el dolor educado

**Guion de entrevista (30 min)**:

```
1. Contexto (5 min)
   - Cuentame sobre tu rol / dia a dia
   - Cual es tu mayor reto en [AREA]?

2. Problema (15 min)
   - Cuando fue la ultima vez que tuviste [PROBLEMA]?
   - Que hiciste para resolverlo?
   - Que soluciones has probado?
   - Cuanto tiempo/dinero gastas en esto?
   - En una escala del 1-10, cuanto te frustra?

3. Solucion actual (10 min)
   - Que usas ahora para manejar esto?
   - Que te gusta/no te gusta de tu solucion actual?
   - Si pudieras tener una varita magica, que cambiarias?
   - Cuanto pagarias por resolver esto completamente?
```

**Senales positivas**:
- La gente se emociona al hablar del problema
- Ya gastan dinero/tiempo intentando resolverlo
- Te piden que les avises cuando tengas algo
- Te refieren a otras personas con el mismo problema

**Senales negativas**:
- "Si, supongo que es un problema..." (tibio)
- No pueden recordar la ultima vez que lo tuvieron
- No han intentado resolver nada (no les importa lo suficiente)

> Ver [Outreach Framework](./outreach-framework.md) para el proceso completo de como conseguir y ejecutar estas entrevistas via LinkedIn DMs.

### Nivel 2: Validacion de la solucion (Semana 2-4)

**Objetivo**: Confirmar que tu enfoque de solucion resuena.

#### Landing page test

Crea una landing page simple que:
1. Describe el problema
2. Presenta tu solucion (sin construirla)
3. Tiene un CTA claro (email waitlist, pre-order, demo call)

**Metricas que importan**:
- **Conversion de visita a signup**: > 5% es buena senal
- **Fuente de trafico**: De donde vienen? Es replicable?
- **Engagement post-signup**: Responden a emails? Quieren hablar?

**Stack rapido para landing**:
- Framer / Carrd / Typedream (sin codigo)
- Tally / Typeform para formularios
- Cal.com para agendar calls

#### Smoke test / Fake door

Pon un boton de "comprar" o "solicitar demo" antes de tener el producto. Mide cuantos clickan.

**Variantes**:
- **Pre-venta**: "Reserva por 50EUR y ten acceso prioritario"
- **Waitlist con referral**: "Invita a 3 amigos y sube de puesto"
- **Concierge MVP**: Haz el servicio a mano para los primeros 5 clientes

### Nivel 3: Validacion del producto (Semana 4-8)

**Objetivo**: Confirmar que la gente usa y paga por tu producto.

#### MVP - Producto Minimo Viable

**Lo que un MVP NO es**:
- Una app completa con 20 features
- Algo que te lleve 3 meses construir
- Algo bonito y pulido

**Lo que un MVP SI es**:
- La solucion mas simple que resuelve el problema core
- Algo que puedas poner en manos de usuarios en 1-2 semanas
- Algo que te de datos reales de uso

**Tipos de MVP** (del mas simple al mas complejo):

| Tipo | Descripcion | Ejemplo | Tiempo |
|------|-------------|---------|--------|
| **Concierge** | Haces el servicio a mano | Revisas facturas manualmente | 1 dia |
| **Wizard of Oz** | Parece automatico pero es manual | Frontend bonito, tu procesas atras | 1 semana |
| **Landing + Typeform** | Captura interes + datos | Formulario que simula el producto | 2 dias |
| **No-code** | Producto real sin codigo | Bubble, Zapier, Airtable | 1-2 semanas |
| **Script/CLI** | Automatizacion basica | Python script que resuelve el core | 3-5 dias |
| **Prototipo coded** | Codigo real, scope minimo | Solo la feature principal | 2-4 semanas |

## Framework de experimentos

Para cada experimento, documenta:

```
## Experimento: [NOMBRE]
- **Hipotesis**: Creemos que [SEGMENTO] tiene el problema de [PROBLEMA]
- **Test**: Vamos a [ACCION] para [OBJETIVO]
- **Metrica**: Mediremos [METRICA]
- **Criterio de exito**: Consideramos validado si [UMBRAL]
- **Timeline**: [X dias]
- **Coste**: [X EUR]

## Resultado:
- **Datos**: [RESULTADOS]
- **Aprendizaje**: [QUE APRENDIMOS]
- **Decision**: Pivotar / Perseverar / Matar
```

## Herramientas de validacion

| Herramienta | Uso | Precio |
|-------------|-----|--------|
| Google Forms / Tally | Encuestas rapidas | Gratis |
| Calendly / Cal.com | Agendar entrevistas | Gratis |
| Carrd | Landing pages | 19$/ano |
| Stripe | Cobrar pre-ventas | Pay-as-you-go |
| Hotjar | Ver como usan tu landing | Gratis tier |
| Google Ads | Trafico para validar | Desde 5$/dia |

## Prompt AI: Disenar experimentos de validacion

```
Estoy validando esta idea de startup:
- Problema: [PROBLEMA]
- Segmento: [SEGMENTO]
- Solucion propuesta: [SOLUCION]

Disenname 5 experimentos de validacion ordenados de menor a mayor esfuerzo.
Para cada uno dame:
1. Que hipotesis valida
2. Como ejecutarlo paso a paso
3. Que metrica medir
4. Cual es el umbral de exito
5. Cuanto tiempo y dinero requiere
6. Que herramientas usar
```

---

**Siguiente**: [03 - AI como Acelerador](../03-ai-como-acelerador/) - Usa AI para ir 10x mas rapido
