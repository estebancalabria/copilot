# Laboratorio 4: Preparación de Conversaciones Difíciles con un Agente de Microsoft 365 Copilot

## Objetivo

Utilizar Microsoft 365 Copilot y Agent Builder para:

- Crear un agente especializado en conversaciones de liderazgo.
- Preparar conversaciones relacionadas con bajo desempeño, conflictos, planes de mejora y cambios organizacionales.
- Generar guiones adaptados a distintas situaciones.
- Formular preguntas abiertas que favorezcan el diálogo.
- Anticipar posibles objeciones o reacciones.
- Obtener recomendaciones de comunicación profesional.
- Evaluar críticamente las respuestas generadas por la IA.

---

## Escenario

Los supervisores, jefes de área y responsables de equipo de Costa Oriental deben afrontar periódicamente conversaciones complejas con colaboradores. Algunos ejemplos incluyen:

- Comunicar problemas de desempeño.
- Abordar conflictos entre integrantes de un equipo.
- Definir planes de mejora.
- Comunicar cambios organizacionales.
- Tratar incumplimientos de procedimientos.
- Analizar errores que afectan la operación o la satisfacción del cliente.

La calidad de estas conversaciones influye directamente en el clima laboral, la motivación de las personas y la efectividad de las acciones correctivas.

Para ayudar a los líderes a prepararse mejor, Costa Oriental decide crear un agente especializado en Microsoft 365 Copilot que actúe como asistente para la preparación de conversaciones difíciles.

> **Importante:** El agente no reemplaza la intervención humana ni las decisiones de Recursos Humanos. Su función es asistir en la preparación de la conversación, ayudando al líder a estructurar su comunicación de forma profesional, respetuosa y orientada a la mejora.

---

# Parte 1 – Crear el agente

## Paso 1 - Crear un nuevo agente

1. Acceder a Microsoft 365 Copilot.
2. Seleccionar **Crear un agente**.
3. Elegir la opción para definir el agente mediante lenguaje natural.

---

## Paso 2 - Definir el comportamiento del agente

Introducir la siguiente descripción:

```text
Crea un agente denominado "Coach de Conversaciones de Liderazgo".

El agente estará dirigido a supervisores, responsables de equipo y gerentes de Costa Oriental, una empresa logística y de distribución.

Su función será ayudar a preparar conversaciones profesionales relacionadas con:

- Bajo desempeño.
- Conflictos laborales.
- Incumplimiento de procedimientos.
- Planes de mejora.
- Errores operativos.
- Cambios organizacionales.
- Desarrollo profesional.

Antes de generar una recomendación, el agente debe solicitar información sobre:

- Situación que se necesita abordar.
- Objetivo de la conversación.
- Hechos concretos disponibles.
- Impacto observado.
- Relación del usuario con la persona involucrada.
- Conversaciones anteriores relacionadas con el problema.
- Resultado que se espera alcanzar.

Después debe generar:

- Objetivo sugerido para la conversación.
- Guion de apertura.
- Explicación estructurada del problema.
- Preguntas abiertas.
- Posibles reacciones u objeciones.
- Recomendaciones para responder.
- Acuerdos que podrían proponerse.
- Próximos pasos.
- Recomendaciones de seguimiento.
- Errores de comunicación que deberían evitarse.

Utiliza un tono profesional, respetuoso, neutral y orientado a la mejora.

No realices diagnósticos sobre emociones, personalidad, actitudes o intenciones de las personas.

No determines sanciones, promociones, despidos ni otras decisiones laborales.

No inventes hechos que no hayan sido proporcionados por el usuario.

Diferencia claramente:
- Hechos proporcionados por el usuario.
- Interpretaciones realizadas por el usuario.
- Recomendaciones generadas por la IA.

Recuerda que todas las recomendaciones deben ser revisadas por el líder y, cuando corresponda, por Recursos Humanos.
```

---

# Parte 2 – Revisar la configuración del agente

## Paso 3 - Validar la configuración generada

---

## Paso 4 - Agregar preguntas sugeridas

Configurar las siguientes preguntas iniciales:

- Ayúdame a preparar una conversación por bajo desempeño.
- Necesito abordar un conflicto entre dos integrantes del equipo.
- Ayúdame a preparar un plan de mejora.
- Necesito comunicar un cambio organizacional.
- Quiero preparar una conversación por incumplimiento de un procedimiento.

---

# Parte 3 – Incorporar conocimiento organizacional

## Paso 5 - Crear una guía organizacional con el Agente Investigador

Antes de agregar conocimiento al agente, se creará un documento que servirá como base de conocimiento.

1. Abrir Microsoft 365 Copilot.
2. Utilizar el Agente Investigador.
3. Solicitar la creación de una guía de buenas prácticas para conversaciones difíciles en entornos logísticos.

Ejemplo de prompt:

```text
Genera una guía para supervisores y responsables de equipo de una empresa logística.

La guía debe incluir:
- Cómo preparar conversaciones por bajo desempeño.
- Cómo abordar conflictos laborales.
- Cómo comunicar errores operativos.
- Cómo acordar planes de mejora.
- Cómo comunicar cambios organizacionales.
- Buenas prácticas de escucha activa.
- Técnicas de feedback constructivo.
- Errores frecuentes que deben evitarse.

Redacta el contenido como un documento interno de referencia para líderes.
```

1. Revisar y validar el contenido generado.
2. Guardar el resultado en un documento Word denominado:

**Guía de Conversaciones de Liderazgo - Costa Oriental.docx**

1. Volver al agente **Coach de Conversaciones de Liderazgo**.
2. Agregar el documento como fuente de conocimiento.

> Importante: Utilizar únicamente documentación genérica o aprobada para capacitación. No cargar evaluaciones reales, expedientes de personal, información médica, remuneraciones ni otros datos sensibles de colaboradores.

---

## Paso 6 - Agregar una instrucción adicional

Incorporar la siguiente instrucción complementaria:

```text
Cuando recibas una solicitud, comienza siempre diferenciando claramente:

1. Hechos proporcionados por el usuario.
2. Suposiciones o interpretaciones realizadas por el usuario.
3. Recomendaciones generadas por la IA.

Si la información es insuficiente para preparar la conversación, solicita aclaraciones antes de generar recomendaciones.

Promueve prácticas de liderazgo basadas en respeto, escucha activa, objetividad y mejora continua.

Recuerda que tu función es ayudar a preparar conversaciones y no evaluar ni determinar el desempeño de las personas.
```

---

# Parte 4 – Probar el agente

## Paso 7 - Simulación de una conversación difícil

Utilizar el siguiente escenario de ejemplo:

```text
Soy supervisor de depósito.

Uno de mis colaboradores ha cometido errores repetidos en el control de mercadería durante las últimas tres semanas.

Ya hablamos informalmente dos veces sobre el problema pero la situación continúa.

Necesito preparar una conversación para acordar mejoras y reducir los errores operativos.
```

Analizar:

- Qué información solicita inicialmente el agente.
- Cómo diferencia hechos e interpretaciones.
- Qué preguntas abiertas propone.
- Qué posibles objeciones anticipa.
- Qué recomendaciones de comunicación proporciona.

---

# Resultado esperado

Al finalizar el laboratorio, los participantes habrán creado un agente de Microsoft 365 Copilot capaz de asistir en la preparación de conversaciones difíciles de liderazgo, ayudando a estructurar reuniones complejas de manera profesional, objetiva y alineada con las buenas prácticas de gestión de personas, sin reemplazar el criterio del líder ni los procesos de Recursos Humanos.
