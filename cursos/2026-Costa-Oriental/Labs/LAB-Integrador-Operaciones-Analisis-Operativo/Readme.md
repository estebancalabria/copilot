# Laboratorio — Auditoría de Productividad Industrial asistida por IA

## Caso VAL — Microsoft 365 Copilot, Copilot Notebooks y Agentes 365

---

## Contexto del laboratorio

El área de Mejora Continua de **VAL**, una planta de manufactura con varias líneas de producción, envía la siguiente consulta al equipo de Tecnología:

> **Asunto:** Consulta sobre herramientas de IA para auditorías de productividad
>
> Estimado buenos días,
>
> Quería consultar si existe algún agente de IA dentro de Copilot, o alguna alternativa dentro del ecosistema Microsoft, que pueda ayudarnos con el siguiente proceso.
>
> Actualmente estamos llevando adelante auditorías de productividad en las distintas líneas de producción de VAL. Estas auditorías consisten en la toma de tiempos, el análisis del flujo de trabajo y la identificación de oportunidades de mejora para optimizar la producción.
>
> Hoy nos encontramos en la etapa inicial del relevamiento, donde debemos auditar una gran cantidad de procesos y productos. Por ese motivo, estamos buscando incorporar herramientas de IA que nos permitan agilizar el análisis, identificar oportunidades de mejora y hacer más eficiente el proceso de auditoría.
>
> Quisiera consultar si existe alguna herramienta, agente de Copilot o forma de trabajo con IA que pueda adaptarse a este tipo de análisis, o si podrían orientarnos sobre cuál sería la mejor alternativa para este caso.
>
> Desde ya, muchas gracias.
>
> Saludos,

**Tu rol:** sos el consultor de IA que debe responder esa consulta. No alcanza con contestar el correo: vas a construir la solución completa y recién después redactar la respuesta.

---

## Objetivo

Diseñar una solución de IA en tres capas que cubra el ciclo completo de una auditoría de productividad:

| Capa | Herramienta | Pregunta que responde | Quién la usa |
|---|---|---|---|
| Medir | Copilot en Excel | ¿Qué dicen los números? | El auditor |
| Diagnosticar | Copilot Notebook | ¿Qué oportunidades de mejora hay? | Mejora Continua |
| Operar | Agente 365 | ¿Cómo debo hacer esta tarea? | El operario de planta |

> **Idea fuerza del laboratorio:** Excel mide, el Notebook diagnostica, el Agente opera.

**Duración estimada:** 120 minutos.

**Requisitos:** licencia de Microsoft 365 Copilot, acceso a Copilot en Excel y Word, Copilot Notebooks y creación de agentes.

**Aclaración:** VAL es una planta de manufactura ficticia utilizada como escenario de práctica. Todos los datos se generan durante el laboratorio.

---

# Bloque 1 — Medir: análisis cuantitativo con Copilot en Excel

**Duración:** 35 minutos.

**Objetivo:** derivar del correo qué hay que relevar, construir la planilla de toma de tiempos y analizarla con IA.

## Paso 1.1 — Deducir qué datos hay que registrar

El correo no dice qué columnas necesita la planilla. Hay que deducirlo. Abrí Microsoft 365 Copilot y pegá el correo completo seguido de este prompt:

```
A partir del correo anterior, actuá como especialista en Ingeniería Industrial y
Lean Manufacturing.

Definí qué datos mínimos se deben registrar en planta para poder auditar la
productividad de una línea de producción mediante toma de tiempos.

Devolvé una tabla con: nombre de columna, tipo de dato, descripción y para qué
análisis sirve.

Máximo 15 columnas. Priorizá lo que permita detectar cuellos de botella,
desvíos contra tiempo estándar y desperdicios Lean.
```

Revisá la propuesta. Si falta algo relevante, pedí el ajuste antes de avanzar.

## Paso 1.2 — Generar la planilla con datos simulados

Creá un libro nuevo en Excel llamado **`VAL_Toma_Tiempos.xlsx`**, abrí Copilot en Excel y usá:

```
Creá una tabla de toma de tiempos de auditoría de productividad con estas columnas:

ID_Medicion, Fecha, Turno, Linea, Producto, Etapa, Operacion, Tipo_Actividad,
Operarios, Unidades_Procesadas, Tiempo_Ciclo_Seg, Tiempo_Estandar_Seg,
Tiempo_Espera_Seg, Paradas_Min, Motivo_Parada, Scrap_Unidades,
Observacion_Auditor, Auditor.

Generá 80 filas de datos simulados realistas para una planta de manufactura, con:
- 3 líneas: Linea A, Linea B, Linea C
- 3 turnos: Mañana, Tarde, Noche
- 5 etapas por línea
- Tipo_Actividad con valores: Valor agregado, Necesaria sin valor, Sin valor agregado
- Motivo_Parada con valores: Falta de material, Falla de equipo, Ajuste de calidad,
  Cambio de formato, Sin parada
- Tiempos de ciclo con variabilidad real, algunos por encima del estándar
- Observaciones del auditor escritas en lenguaje natural, describiendo hechos
  observables en planta

Concentrá los desvíos más grandes en la Linea B para que el análisis posterior
tenga hallazgos claros.
```

## Paso 1.3 — Enriquecer la planilla con IA

Ahora Copilot clasifica lo que el auditor escribió en texto libre:

```
Agregá una columna Desvio_Seg que calcule Tiempo_Ciclo_Seg menos Tiempo_Estandar_Seg.

Agregá una columna Desperdicio_Lean que clasifique cada fila según la
Observacion_Auditor en uno de estos valores: Espera, Transporte, Sobreproceso,
Inventario, Movimiento, Defectos, Sobreproducción, Ninguno.

Agregá una columna Eficiencia_Pct que calcule Tiempo_Estandar_Seg dividido
Tiempo_Ciclo_Seg, expresado en porcentaje.
```

## Paso 1.4 — Analizar

Ejecutá estos prompts uno por uno en Copilot en Excel:

```
¿Qué operación concentra el mayor tiempo improductivo total? Mostrá el detalle
por línea y turno.
```

```
Identificá las operaciones con mayor variabilidad en el tiempo de ciclo y
explicá por qué esa variabilidad es un problema de productividad.
```

```
Calculá qué porcentaje del tiempo total corresponde a actividades sin valor
agregado, desglosado por línea.
```

```
Generá un ranking de las 10 principales oportunidades de mejora ordenadas por
tiempo improductivo total, indicando línea, operación, tipo de desperdicio e
impacto estimado en segundos por ciclo.
```

## Paso 1.5 — Prompt programado semanal

Durante el relevamiento se cargan mediciones todas las semanas. En lugar de repetir el análisis a mano, se programa.

Creá un **prompt programado** con frecuencia semanal, lunes a las 08:00, con este texto:

```
Revisá la planilla VAL_Toma_Tiempos.xlsx y generá un informe semanal de auditoría
de productividad que incluya:

1. Operaciones con mayor desvío contra el tiempo estándar.
2. Principales motivos de parada y su impacto acumulado en minutos.
3. Evolución del porcentaje de actividades sin valor agregado respecto de la
   semana anterior.
4. Las 5 oportunidades de mejora más relevantes de la semana.
5. Alertas sobre líneas que empeoraron su eficiencia.

Presentá el resultado en formato ejecutivo, máximo una página.
```

## Entregable del Bloque 1

| Archivo | Descripción |
|---|---|
| `VAL_Toma_Tiempos.xlsx` | Planilla de relevamiento con 80 mediciones y columnas calculadas |
| `VAL_Analisis_Tiempos.docx` | Resumen cuantitativo exportado desde el análisis de Copilot |

Para el segundo archivo, pedile a Copilot en Word:

```
Redactá un informe técnico con los hallazgos cuantitativos de la auditoría de
tiempos de VAL, basado en el análisis anterior. Incluí tablas de cuellos de
botella, desvíos por línea y ranking de oportunidades.
```

---

# Bloque 2 — Diagnosticar: Copilot Notebook de la auditoría

**Duración:** 40 minutos.

**Objetivo:** cruzar los números con el contexto cualitativo para producir un diagnóstico de oportunidades y el material que estandariza el proceso.

> **Por qué un Notebook y no Excel:** Excel responde sobre una tabla. El Notebook razona sobre un conjunto de fuentes heterogéneas —planillas, procedimientos, observaciones de planta, auditorías anteriores— y mantiene ese contexto estable a lo largo de toda la investigación. La auditoría no se diagnostica mirando una sola tabla.

## Paso 2.1 — Generar las fuentes cualitativas

Antes de armar el Notebook hay que producir el contexto documental. Se genera con IA.

**Procedimiento vigente.** En Word, nuevo documento `VAL_Procedimiento_Actual.docx`:

```
Redactá el procedimiento operativo actual de una línea de envasado de una planta
de manufactura, escrito como documento formal de planta.

Incluí: objetivo, alcance, responsables, secuencia de 12 pasos operativos con
tiempos de referencia por paso, controles de calidad, criterios de parada y
registro de producción.

El procedimiento debe tener ineficiencias plausibles no señaladas: pasos
redundantes, controles duplicados, movimientos innecesarios de material y
tiempos de espera aceptados como normales.
```

**Observaciones de planta.** Nuevo documento `VAL_Observaciones_Auditor.docx`:

```
Redactá las notas de campo de un auditor de productividad durante 5 jornadas de
observación en tres líneas de producción.

Describí únicamente hechos observables: qué hace el operario, dónde espera, qué
busca, cuántas veces se desplaza, qué demora un cambio de formato, qué ocurre
cuando falta material.

No incluyas conclusiones ni recomendaciones, solo observación directa. Escribí
en primera persona, con lenguaje de planta, entre 600 y 800 palabras.
```

**Metodología de auditoría.** Nuevo documento `VAL_Metodologia_Auditoria.docx`:

```
Redactá la metodología de auditoría de productividad de VAL.

Incluí: definición de los 7 desperdicios Lean con ejemplos de manufactura,
criterios para clasificar actividades con y sin valor agregado, cómo se calcula
el tiempo estándar, la matriz de priorización impacto versus esfuerzo de
implementación, y los criterios para considerar una oportunidad como crítica,
alta, media o baja.
```

**Auditoría anterior.** Nuevo documento `VAL_Auditoria_Anterior.docx`:

```
Redactá el informe de cierre de la auditoría de productividad de VAL del año
anterior. Incluí hallazgos, acciones comprometidas, responsables, fechas
objetivo y estado final de cada acción, con algunas acciones cerradas, otras
parcialmente implementadas y otras nunca ejecutadas.
```

## Paso 2.2 — Crear el Notebook

Creá un Copilot Notebook llamado **Auditoría de Productividad VAL 2026** y agregá como fuentes:

- `VAL_Toma_Tiempos.xlsx`
- `VAL_Analisis_Tiempos.docx`
- `VAL_Procedimiento_Actual.docx`
- `VAL_Observaciones_Auditor.docx`
- `VAL_Metodologia_Auditoria.docx`
- `VAL_Auditoria_Anterior.docx`

## Paso 2.3 — Diagnóstico transversal

Estos prompts solo funcionan bien con todas las fuentes juntas. Es el punto donde se ve el valor del Notebook.

```
Cruzá las mediciones de tiempos con las observaciones del auditor. ¿Qué causas
concretas explican los mayores desvíos contra el tiempo estándar?
```

```
Compará el procedimiento vigente con lo que realmente ocurre según las
observaciones de planta. ¿Dónde el procedimiento no se cumple y dónde el propio
procedimiento es la causa de la ineficiencia?
```

```
Clasificá todos los hallazgos según los 7 desperdicios Lean definidos en la
metodología. Indicá evidencia cuantitativa y cualitativa para cada uno.
```

```
Revisá la auditoría anterior. ¿Qué problemas detectados el año pasado siguen
presentes hoy? ¿Qué acciones comprometidas no se implementaron y qué impacto
tuvo eso?
```

```
Según la matriz de priorización de la metodología, ordená todas las
oportunidades de mejora detectadas por impacto y esfuerzo de implementación.
Justificá la clasificación de cada una.
```

```
¿Qué información falta relevar para completar la auditoría? Indicá qué datos
adicionales debería registrar el equipo en las próximas visitas a planta.
```

```
Estimá el ahorro potencial en tiempo de ciclo y en horas hombre si se
implementan las oportunidades clasificadas como críticas y altas.
```

## Paso 2.4 — Producir los entregables del diagnóstico

```
Generá el informe de oportunidades de mejora de la auditoría VAL 2026, con:
resumen ejecutivo, metodología aplicada, hallazgos por línea, clasificación de
desperdicios, matriz de priorización, plan de acción propuesto con responsables
sugeridos y estimación de impacto.
```

Guardalo como `VAL_Oportunidades_Mejora.docx`.

```
Redactá el procedimiento operativo optimizado de la línea, incorporando las
mejoras identificadas. Mantené el formato del procedimiento vigente pero:

- Eliminá los pasos sin valor agregado detectados.
- Reordená la secuencia para reducir esperas y movimientos.
- Definí tiempo objetivo por paso, basado en las mediciones reales y el
  potencial de mejora.
- Agregá una sección de preguntas frecuentes del operario.
- Agregá una sección que indique qué cambió respecto del procedimiento anterior
  y por qué.
```

Guardalo como `VAL_Procedimiento_Optimizado.docx`.

## Paso 2.5 — Que el Notebook escriba el prompt del agente

Último paso del bloque, y el que conecta con el Bloque 3:

```
Necesito crear un agente de Microsoft 365 para que los operarios de planta
consulten cómo ejecutar correctamente cada operación.

Redactá las instrucciones completas del agente, incluyendo: rol, alcance, tono
de respuesta apropiado para personal de planta, formato de las respuestas,
cómo debe responder sobre tiempos objetivo, qué hacer ante desvíos, cuándo debe
escalar a un supervisor y qué temas debe declinar por estar fuera de su alcance.

Devolvé el texto listo para pegar en el campo de instrucciones del agente.
```

Guardalo como `VAL_Instrucciones_Agente.md`.

## Entregables del Bloque 2

| Archivo | Origen |
|---|---|
| `VAL_Procedimiento_Actual.docx` | Generado con Copilot en Word |
| `VAL_Observaciones_Auditor.docx` | Generado con Copilot en Word |
| `VAL_Metodologia_Auditoria.docx` | Generado con Copilot en Word |
| `VAL_Auditoria_Anterior.docx` | Generado con Copilot en Word |
| `VAL_Oportunidades_Mejora.docx` | Producido por el Notebook |
| `VAL_Procedimiento_Optimizado.docx` | Producido por el Notebook |
| `VAL_Instrucciones_Agente.md` | Producido por el Notebook |

---

# Bloque 3 — Operar: Agente 365 de consulta para planta

**Duración:** 30 minutos.

**Objetivo:** llevar el resultado de la auditoría a la operación diaria.

> **Por qué un agente y no el Notebook:** el Notebook es una herramienta de investigación para el analista, que escribe prompts complejos y sabe qué preguntar. El operario de planta no va a escribir prompts. Necesita una respuesta corta, correcta y siempre igual, sin importar quién pregunte. El agente encapsula el conocimiento de la auditoría y lo publica para toda la operación.

## Paso 3.1 — Crear el agente

Creá un agente con Agent Builder llamado **Asistente de Procesos VAL**.

**Descripción:**

```
Asistente que responde consultas del personal de planta sobre cómo ejecutar
correctamente las operaciones de producción, los tiempos objetivo de cada etapa
y qué hacer ante desvíos.
```

**Instrucciones:** pegá el contenido de `VAL_Instrucciones_Agente.md`.

Si querés partir de una base antes de usar la del Notebook, podés usar esta:

```
Sos el Asistente de Procesos de VAL. Ayudás al personal de planta a ejecutar
correctamente las operaciones de producción.

Respondé siempre en español rioplatense, de forma breve, concreta y práctica.
Usá pasos numerados cuando describas cómo hacer algo.

Basá tus respuestas exclusivamente en el procedimiento optimizado y en los
documentos de la auditoría cargados como conocimiento. Si la respuesta no está
en esos documentos, decilo y sugerí consultar al supervisor de línea.

Cuando te pregunten cuánto debe tardar una operación, indicá el tiempo objetivo
y aclará qué se considera un desvío aceptable.

Cuando detectes que la consulta involucra un riesgo de seguridad, una falla de
equipo o una desviación de calidad, indicá siempre que se debe escalar al
supervisor antes de continuar.

No opines sobre desempeño de personas ni compares operarios entre sí.
```

## Paso 3.2 — Cargar conocimiento

Agregá como fuentes de conocimiento:

- `VAL_Procedimiento_Optimizado.docx`
- `VAL_Oportunidades_Mejora.docx`
- `VAL_Metodologia_Auditoria.docx`

## Paso 3.3 — Probar el agente

Validá con estas consultas, escritas como las haría un operario:

```
¿Cómo hago el cambio de formato en la línea?
```

```
¿Cuánto tendría que tardar el ciclo de envasado?
```

```
Me está tardando más de lo normal, ¿qué reviso?
```

```
¿Qué hago si falta material en la línea?
```

```
¿Qué cambió respecto del procedimiento anterior?
```

```
¿Puedo saltear el control de calidad si voy atrasado?
```

La última consulta es la prueba de límites: el agente debe negarse y remitir al supervisor.

## Paso 3.4 — Publicar

Publicá el agente y compartilo con el equipo de planta.

## Entregable del Bloque 3

| Archivo | Descripción |
|---|---|
| `VAL_Asistente_Procesos` | Agente publicado y probado |
| `VAL_Pruebas_Agente.docx` | Registro de las consultas de prueba y sus respuestas |

---

# Bloque 4 — Responder al cliente

**Duración:** 15 minutos.

Con la solución construida, redactá la respuesta al correo original. Usá Copilot en Outlook:

```
Redactá la respuesta al correo del área de Mejora Continua de VAL sobre
herramientas de IA para auditorías de productividad.

Explicá la solución en tres capas:
1. Copilot en Excel para el análisis cuantitativo de la toma de tiempos, con un
   prompt programado semanal que automatiza el seguimiento.
2. Copilot Notebook para el diagnóstico de oportunidades, cruzando mediciones,
   procedimientos, observaciones de planta y auditorías anteriores.
3. Un agente de Microsoft 365 para que el personal de planta consulte
   procedimientos y tiempos objetivo en el día a día.

Mencioná que, cuando existan datos digitales de eventos en sistemas como ERP o
MES, Power Automate Process Mining permite descubrir automáticamente los
procesos reales y sus cuellos de botella, como paso posterior.

Tono profesional y cordial. Máximo 300 palabras. Cerrá proponiendo una reunión
para mostrar un prototipo.
```

---

## Cierre y discusión

**Preguntas para el cierre en clase:**

1. ¿Por qué el análisis de Excel no alcanza para diagnosticar oportunidades de mejora?
2. ¿Qué aporta el Notebook que no aporta un chat suelto de Copilot?
3. ¿Por qué no se le entrega el Notebook directamente al operario de planta?
4. ¿Qué pasa con el agente cuando cambia el procedimiento? ¿Quién lo mantiene?
5. ¿En qué momento tendría sentido incorporar Process Mining en VAL?

**Cuándo escalar a Process Mining.** Este laboratorio resuelve el caso de auditorías presenciales, con toma de tiempos manual y observación directa. Cuando la empresa disponga de registros digitales de eventos en ERP, MES o sistemas de trazabilidad, Power Automate Process Mining permite reconstruir automáticamente el proceso real, compararlo con el esperado y detectar cuellos de botella sin observación manual, con Copilot integrado para obtener recomendaciones en lenguaje natural.

**Nota sobre uso responsable de IA.** Toda la solución analiza procesos, no personas. Los datos de la planilla deben registrar operaciones y tiempos, nunca desempeño individual atribuible. El agente debe declinar explícitamente cualquier consulta orientada a evaluar o comparar trabajadores.

---

## Resumen de archivos del laboratorio

| Bloque | Archivo | Se genera con |
|---|---|---|
| 1 | `VAL_Toma_Tiempos.xlsx` | Copilot en Excel |
| 1 | `VAL_Analisis_Tiempos.docx` | Copilot en Word |
| 2 | `VAL_Procedimiento_Actual.docx` | Copilot en Word |
| 2 | `VAL_Observaciones_Auditor.docx` | Copilot en Word |
| 2 | `VAL_Metodologia_Auditoria.docx` | Copilot en Word |
| 2 | `VAL_Auditoria_Anterior.docx` | Copilot en Word |
| 2 | `VAL_Oportunidades_Mejora.docx` | Copilot Notebook |
| 2 | `VAL_Procedimiento_Optimizado.docx` | Copilot Notebook |
| 2 | `VAL_Instrucciones_Agente.md` | Copilot Notebook |
| 3 | `VAL_Asistente_Procesos` | Agent Builder |
| 3 | `VAL_Pruebas_Agente.docx` | Registro manual |
| 4 | Respuesta al cliente | Copilot en Outlook |
