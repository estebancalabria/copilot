# Laboratorio 4: Preparación de Conversaciones Difíciles con un Agente de Microsoft 365 Copilot

## Objetivo

Utilizar Microsoft 365 Copilot y Agent Builder para:

- Crear un agente especializado en conversaciones de liderazgo.
- Preparar conversaciones relacionadas con bajo desempeño, conflictos, planes de mejora y cambios organizacionales.
- Generar guiones adaptados a diferentes situaciones.
- Formular preguntas abiertas.
- Anticipar posibles objeciones o reacciones.
- Obtener recomendaciones de comunicación.
- Evaluar críticamente las respuestas generadas por la IA.

---

# Escenario

Los supervisores y responsables de equipo de Costa Oriental deben mantener conversaciones que pueden resultar difíciles, por ejemplo:

- Comunicar un problema de desempeño.
- Abordar un conflicto entre personas.
- Acordar un plan de mejora.
- Informar un cambio organizacional.
- Tratar incumplimientos de procedimientos.
- Comunicar errores que afectan a la operación o al cliente.

La calidad de estas conversaciones depende de la experiencia y preparación de cada responsable. Una conversación mal planteada puede generar resistencia, afectar el clima laboral o dificultar la resolución del problema.

Costa Oriental decide crear un agente en Microsoft 365 Copilot para ayudar a sus líderes a preparar estas conversaciones de manera profesional, respetuosa y orientada a la mejora.

El agente no tomará decisiones sobre los colaboradores ni reemplazará la intervención de Recursos Humanos. Su función será ayudar al líder a organizar la conversación y considerar diferentes maneras de abordar la situación.

---

# Acceso necesario

Abrir:

- [Microsoft 365 Copilot](https://m365.cloud.boratorio se utilizará el creador de agentes de Microsoft 365 Copilot. No es necesario utilizar Copilot Studio porque el agente proporcionará orientación y generará contenido, pero no ejecutará acciones ni se conectará con sistemas externos.

---

# Parte 1 – Crear el agente

## Paso 1

Abrir https://m365.cloud.microsoft/.

Seleccionar la opción para crear un nuevo agente.

---

## Paso 2

En la sección para describir el agente, utilizar el siguiente prompt:

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

No realices diagnósticos sobre las emociones, intenciones, personalidad o actitud de las personas.

No determines sanciones, promociones, despidos ni otras decisiones laborales.

No inventes hechos que no hayan sido proporcionados por el usuario.

Diferencia claramente los hechos proporcionados, las interpretaciones del usuario y las sugerencias generadas por la IA.

Recuerda siempre que las recomendaciones deben ser revisadas por el líder y, cuando corresponda, por Recursos Humanos.
```

---

# Parte 2 – Revisar la configuración

## Paso 3

Revisar la configuración propuesta por Copilot.

Comprobar los siguientes elementos:

- Nombre del agente.
- Descripción.
- Instrucciones.
- Tono de las respuestas.
- Alcance del agente.
- Restricciones.
- Preguntas sugeridas para comenzar una conversación.

Evitar que el agente se presente como responsable de tomar decisiones sobre empleados.

---

## Paso 4

Agregar las siguientes preguntas sugeridas:

```text
Ayúdame a preparar una conversación por bajo desempeño.
```

```text
Necesito abordar un conflicto entre dos integrantes del equipo.
```

```text
Ayúdame a preparar un plan de mejora.
```

```text
Necesito comunicar un cambio organizacional.
```

```text
Quiero preparar una conversación por incumplimiento de un procedimiento.
```

---

# Parte 3 – Incorporar conocimiento organizacional

## Paso 5

Si el instructor proporciona documentos ficticios o aprobados para el laboratorio, agregarlos como fuentes de conocimiento del agente.

Se pueden utilizar documentos como:

- Valores corporativos.
- Código de conducta.
- Guía de liderazgo.
- Política de Recursos Humanos.
- Procedimiento de evaluación de desempeño.
- Procedimiento para planes de mejora.
- Recomendaciones para proporcionar feedback.
- Normas de seguridad y operación.

No cargar evaluaciones reales, expedientes personales, información médica, sanciones, remuneraciones ni otros datos confidenciales de colaboradores.

---

## Paso 6

Agregar la siguiente instrucción al agente:

```text
