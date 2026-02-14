# 05 - Pactos y Acuerdos Legales

## La conversacion incomoda que TIENES que tener

El 62% de startups que fracasan por problemas de equipo podrian haberse salvado con acuerdos claros desde el dia 1. Estas conversaciones son incomodas ahora, pero mucho menos que un juicio despues.

**Regla de oro**: Si no esta escrito, no existe.

## Documentos esenciales

### 1. Pacto de socios (Shareholders Agreement)

**Que es**: El documento mas importante de tu startup. Define las reglas del juego entre los socios.

**Cuando hacerlo**: ANTES de escribir la primera linea de codigo juntos.

**Que debe incluir**:

```
1. ESTRUCTURA DE EQUITY
   - Porcentaje de cada socio
   - Vesting schedule (tipico: 4 anios, cliff de 1 anio)
   - Que pasa con el equity si alguien se va

2. ROLES Y RESPONSABILIDADES
   - Quien es CEO (y que poder tiene)
   - Que decide cada uno
   - Que decisiones requieren unanimidad

3. DEDICACION
   - Full-time / Part-time / Timeline para transicion
   - Clausula de no competencia
   - Clausula de exclusividad

4. DECISIONES Y DEADLOCK
   - Como se toman decisiones del dia a dia
   - Como se resuelven desacuerdos
   - Mecanismo de desempate
   - Mediacion/arbitraje

5. SALIDA DE UN SOCIO
   - Vesting y cliff
   - Good leaver vs Bad leaver
   - Derecho de adquisicion preferente (right of first refusal)
   - Drag-along y Tag-along
   - Valoracion en caso de salida

6. PROPIEDAD INTELECTUAL
   - Todo el IP pertenece a la empresa
   - Cesion de PI previa (si aplica)
   - Inventos futuros durante la relacion

7. FINANCIACION
   - Aportaciones iniciales de capital
   - Reglas para futuras rondas
   - Derechos de anti-dilucion

8. CONFIDENCIALIDAD
   - Obligacion de confidencialidad
   - Duracion post-salida
   - Que se considera confidencial
```

### 2. Vesting y cliff

**Que es vesting**: Tu equity se "gana" progresivamente durante un periodo de tiempo.

**Standard de la industria**:
- **Periodo**: 4 anios
- **Cliff**: 1 anio (no recibes nada hasta cumplir 1 anio)
- **Frecuencia**: Mensual despues del cliff

**Ejemplo**: Tienes 25% de equity con vesting 4 anios y cliff 1 anio
- Mes 0-11: 0% (cliff)
- Mes 12: 6.25% de golpe (1 anio / 4 anios = 25%)
- Mes 13-48: ~0.52% cada mes

**Por que es esencial**:
- Protege contra alguien que se va a los 3 meses con un gran porcentaje
- Alinea incentivos a largo plazo
- Los inversores lo exigen (y desconfian si no lo tienes)

**Good leaver vs Bad leaver**:

| Situacion | Good leaver | Bad leaver |
|-----------|-------------|------------|
| Definicion | Se va por razones legit (salud, acuerdo mutuo) | Se va de mala manera, incumple acuerdos |
| Equity vesteado | Lo mantiene | Lo pierde (total o parcialmente) |
| Equity no vesteado | Vuelve al pool | Vuelve al pool |
| Precio de recompra | Valor de mercado | Precio nominal |

### 3. Acuerdo de confidencialidad (NDA)

**Cuando usarlo**:
- Antes de compartir info sensible con potenciales cofounders
- Con freelancers y empleados
- Con potenciales inversores (aunque muchos no lo firman)

**Que cubrir**:
- Definicion de informacion confidencial
- Excepciones (info publica, desarrollo independiente)
- Duracion (tipico: 2-5 anios)
- Consecuencias de incumplimiento

**Nota**: Las ideas no se protegen con NDA. La ejecucion si.

### 4. Cesion de propiedad intelectual (IP Assignment)

**Critico**: Todo lo que se crea para la startup pertenece a la empresa, no a la persona.

**Incluye**:
- Codigo
- Disenos
- Marcas y logos
- Bases de datos y datasets
- Documentacion
- Inventos y patentes

**Cuidado con**: Codigo creado ANTES de la startup que se usa en ella. Necesitas una licencia o cesion explicita.

### 5. Acuerdo de prestacion de servicios

Para freelancers y colaboradores no-socios:

```
- Scope del trabajo (bien definido)
- Timeline y entregables
- Compensacion y forma de pago
- Propiedad intelectual (todo es de la empresa)
- Confidencialidad
- Clausulas de terminacion
```

## Escenarios criticos que debes cubrir

### Que pasa si un cofounder quiere irse?

```
Escenario 1: Se va en el cliff (< 1 anio)
-> Pierde todo el equity no vesteado
-> Si fue good leaver, puede quedarse con lo vesteado
-> Si fue bad leaver, pierde todo

Escenario 2: Se va despues del cliff
-> Mantiene el equity vesteado (si good leaver)
-> El equity no vesteado vuelve al pool
-> Derecho de recompra por la empresa a precio justo
-> Non-compete de 12-24 meses
```

### Que pasa si entran inversores?

```
- Dilucion proporcional para todos
- Clausula de anti-dilucion para founders (negociable)
- Nuevos derechos para inversores:
  * Puesto en el board
  * Derechos de informacion
  * Derechos de veto en decisiones clave
  * Liquidation preferences
```

### Que pasa si no os poneis de acuerdo (deadlock)?

```
Opciones (definir de antemano):
1. CEO tiene voto de desempate
2. Mediacion externa (mediador acordado)
3. Arbitraje vinculante
4. Russian roulette: uno ofrece comprar la parte del otro,
   y el otro puede aceptar O comprar al mismo precio (ultimo recurso)
```

## Cuanto cuesta la parte legal

| Documento | DIY | Abogado startup | Bufete grande |
|-----------|-----|-----------------|---------------|
| Pacto de socios | Template online | 1.000-3.000 EUR | 5.000-15.000 EUR |
| Constitucion SL | 500-800 EUR | 800-1.500 EUR | 2.000-5.000 EUR |
| Contratos freelancer | Template | 300-800 EUR | 1.500-3.000 EUR |
| NDA | Template gratis | 200-500 EUR | 1.000-2.000 EUR |

**Recomendacion**: El pacto de socios merece un abogado. Para el resto, empieza con templates y revisa con abogado cuando haya dinero en juego.

**Recursos para templates** (Espana):
- [Legal Hackers](https://legalhackers.es)
- [Pacto de Socios template de SeedRocket](https://www.seedrocket.com)
- Y Combinator tiene templates en ingles: [ycombinator.com/documents](https://www.ycombinator.com/documents)

## Constituir la empresa

### Cuando constituir

- **NO constituyas** solo porque tienes una idea
- **Constituye cuando**: Vayas a cobrar a alguien, recibir inversion, o contratar
- **Opcion intermedia**: Autonomo + acuerdo de colaboracion hasta que valides

### Donde constituir (si estas en Espana)

| Opcion | Pros | Contras | Coste |
|--------|------|---------|-------|
| **SL (Espana)** | Sencillo, conocido, 1EUR de capital | Lenta de crear (2-4 semanas), burocracia | 500-1500 EUR |
| **SLU (unipersonal)** | Solo un socio | Mismos contras que SL | 500-1500 EUR |
| **Delaware C-Corp** | Standard para VCs americanos | Complejo de mantener, doble imposicion | 1000-3000 USD |
| **Estonia e-Residency** | 100% online, rapido | Fiscalidad compleja si vives en Espana | 200 EUR + 500/anio |

**Recomendacion**: Empieza con SL espanola. Si levantas ronda con VCs americanos, ya hablaran de flip a Delaware.

## Prompt AI: Revisar acuerdos

```
Actua como un abogado mercantil experto en startups.
Estoy redactando un [TIPO DE DOCUMENTO] para mi startup.

Contexto:
- Somos [N] cofounders
- Split de equity: [SPLIT]
- Uno es CEO, otro es CTO
- Estamos en fase de [FASE]
- Estamos en [PAIS]

Revisame este borrador y dimme:
1. Que clausulas faltan que son criticas
2. Que clausulas son ambiguas o problematicas
3. Que escenarios no estan cubiertos
4. Que recomendarias cambiar
5. Red flags que ves

IMPORTANTE: Esto es orientativo. Siempre revisare con un abogado real.

[PEGA TU BORRADOR AQUI]
```

---

**Siguiente**: [06 - Go-to-Market](../06-go-to-market/) - Hora de conseguir usuarios
