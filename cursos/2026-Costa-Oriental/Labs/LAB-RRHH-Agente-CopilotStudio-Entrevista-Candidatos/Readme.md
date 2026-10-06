# Laboratorio: Guía de entrevista y agente de selección con Microsoft 365 Copilot

## Objetivo

En este laboratorio utilizarás Microsoft 365 Copilot y Copilot Studio para construir un proceso básico de entrevista asistido por IA.

Al finalizar serás capaz de:

- Crear una descripción de puesto utilizando Copilot.
- Generar una guía de entrevista estructurada.
- Crear un agente en Copilot Studio.
- Configurar el agente para realizar preguntas al candidato.
- Obtener un resumen estructurado de las respuestas.
- Comprender cómo podría registrarse la información en Excel mediante Power Platform.

> Importante: el agente ayuda a estandarizar entrevistas. La evaluación del candidato y la decisión de contratación siempre deben ser realizadas por una persona.

---

# Escenario

El área de Recursos Humanos necesita incorporar un Analista de Recursos Humanos Jr.

Para reducir diferencias entre entrevistadores, se utilizará Microsoft 365 Copilot para generar una guía única de preguntas y posteriormente se creará un agente en Copilot Studio capaz de realizar una entrevista inicial.

---

# Descripción del puesto

> Disponen en este repositorio un archivo JD-Analista-RHHH.dox con estos pasos realizados

## Abrir Word

1. Abrí Microsoft Word.
2. Seleccioná **Documento en blanco**.
3. Seleccioná **Guardar**.
4. Asigná el nombre:

```text
JD-Analista-RRHH.docx
```

5. Guardá el archivo en OneDrive para la Empresa o SharePoint Online.

---

## Generar la descripción utilizando Copilot

1. Seleccioná el icono **Copilot** dentro de Word.
2. En el panel de Copilot ingresá el siguiente prompt:

```text
Actuá como responsable de Recursos Humanos.

Generá una descripción de puesto completa para un Analista de Recursos Humanos Jr.

Incluí:

- Nombre del puesto
- Reporte jerárquico
- Objetivo del puesto
- Responsabilidades principales
- Requisitos obligatorios
- Competencias blandas requeridas
- Conocimientos técnicos requeridos
- Requisitos deseables

La descripción debe ser realista para una empresa mediana y estar redactada de manera profesional.

Presentá el resultado en formato estructurado con títulos y viñetas.
```

3. Esperá la respuesta de Copilot.
4. Revisá el contenido generado.
5. Insertá el contenido en el documento.
6. Guardá los cambios.

---

# Paso 2: Generar una guía de entrevista

## Utilizar el documento como contexto

1. Mantené abierto el archivo `JD-Analista-RRHH.docx`.
2. Abrí nuevamente Copilot desde Word.
3. Verificá que Copilot esté utilizando el documento abierto como contexto.

---

## Generar preguntas de entrevista

## Generar la guía de entrevista

1. Abrí Microsoft Word.

2. Creá un **documento en blanco**.

3. Guardalo en OneDrive para la Empresa o SharePoint Online con el siguiente nombre:

```text
Guia-Entrevista-Analista-RRHH.docx
```

4. En la pestaña **Inicio**, seleccioná **Copilot** para abrir el panel lateral.

5. En el cuadro de conversación ubicado en la parte inferior del panel de Copilot, seleccioná **Agregar contenido** o el icono **+**.

6. Seleccioná la opción para agregar un archivo.

7. Buscá y seleccioná el documento creado anteriormente:

```text
JD-Analista-RRHH.docx
```

8. Verificá que el documento aparezca adjunto o referenciado en el cuadro de conversación de Copilot.

9. Sin quitar la referencia al documento, ingresá el siguiente prompt:

```text
Actuá como especialista en selección de Recursos Humanos.

Utilizá exclusivamente la descripción del puesto incluida en el documento JD-Analista-RRHH.docx como fuente de información.

Generá una guía abierta para entrevistar candidatos al puesto de Analista de Recursos Humanos Jr.

La guía no debe ser un cuestionario fijo. Debe servir como marco para que un entrevistador o un agente de IA genere preguntas dinámicamente y profundice según las respuestas del candidato.

Requisitos:

- Identificá las competencias más relevantes para el puesto.
- Explicá qué aspectos deben explorarse en cada competencia.
- Incluí ejemplos de preguntas iniciales.
- Incluí ejemplos de preguntas de seguimiento.
- Indicá en qué situaciones conviene profundizar en una respuesta.
- Permití adaptar las preguntas según la experiencia y las respuestas del candidato.
- Asegurá que durante la entrevista se cubran todas las competencias identificadas.
- No inventes requisitos, conocimientos ni competencias que no aparezcan en la descripción del puesto.
- No evalúes ni clasifiques al candidato.
- Presentá el resultado con títulos claros y una tabla.
- Incluí una columna para registrar observaciones.
```

10. Presioná **Enter** o seleccioná **Enviar**.

11. Esperá la respuesta de Copilot.

12. Revisá que la guía:

    - Esté basada en la descripción del puesto.
    - Defina competencias y temas que deben explorarse.
    - Incluya ejemplos de preguntas iniciales y de seguimiento.
    - Permita profundizar según las respuestas del candidato.
    - No se limite a una lista rígida de preguntas.
    - No incluya requisitos que no aparezcan en la descripción del puesto.

13. Insertá o copiá la respuesta de Copilot en el documento abierto.

14. Guardá los cambios en:

```text
Guia-Entrevista-Analista-RRHH.docx
```

> Al finalizar este paso tendrás dos documentos diferentes: `JD-Analista-RRHH.docx`, que contiene la descripción del puesto, y `Guia-Entrevista-Analista-RRHH.docx`, que contiene la guía abierta que posteriormente utilizará el agente de Copilot Studio.

---

# Paso 3: Revisar la guía generada

Antes de crear el agente verificá:

- Que las competencias provengan de la descripción del puesto.
- Que las preguntas no agreguen requisitos inexistentes.
- Que todas las preguntas sean relevantes para el puesto.
- Que exista una explicación del objetivo de cada pregunta.

> En un entorno real, este sería el momento en que Recursos Humanos valida el contenido antes de utilizarlo con candidatos.

---

# Paso 4: Crear el agente en Copilot Studio

## Abrir Copilot Studio

1. Abrí el navegador.
2. Ingresá a:

[Copilot Studio](https://copilotstudio.microsoft.com)

3. Iniciá sesión con tu cuenta corporativa.
4. Verificá que te encuentres en el entorno correcto.

---

## Crear un nuevo agente

1. En el menú izquierdo seleccioná **Agents** o **Agentes**.
2. Seleccioná **New Agent** o **Nuevo agente**.
3. Completá los siguientes datos:

### Nombre

```text
Entrevistador RRHH
```

### Descripción

```text
Agente para realizar entrevistas iniciales a candidatos para puestos de Recursos Humanos.
```

4. Seleccioná **Create** o **Crear**.

---

# Paso 5: Configurar el comportamiento del agente

## Definir instrucciones

1. Abrí la sección **Instructions** o **Instrucciones**.

2. Ingresá el siguiente texto:

```text
Sos un entrevistador de Recursos Humanos.

Tu función es realizar una entrevista inicial para candidatos al puesto de Analista de Recursos Humanos Jr.

Debés:

- Realizar una pregunta a la vez.
- Esperar la respuesta antes de continuar.
- Mantener un tono profesional y respetuoso.
- No evaluar ni calificar candidatos.
- No tomar decisiones de contratación.
- Registrar mentalmente las respuestas durante la conversación.
- Al finalizar generar un resumen estructurado de todas las respuestas obtenidas.
```

3. Guardá los cambios.

---

# Paso 6: Incorporar conocimiento

## Agregar la descripción del puesto

1. Seleccioná la sección **Knowledge** o **Conocimiento**.
2. Seleccioná **Add Knowledge**.
3. Elegí la opción para agregar archivos.
4. Seleccioná el documento:

```text
JD-Analista-RRHH.docx
```

5. Esperá que finalice la carga.
6. Confirmá que el documento aparezca como origen de conocimiento.

---

## Agregar la guía de entrevista

1. Si guardaste la guía en un documento independiente, agregalo también como conocimiento.
2. Verificá que el agente pueda consultar tanto la descripción del puesto como la guía de preguntas.

---

# Paso 7: Publicar el agente

1. Seleccioná **Publish** o **Publicar**.
2. Confirmá la publicación.
3. Esperá a que el proceso finalice.

---

# Paso 8: Probar la entrevista

## Abrir el área de pruebas

1. Seleccioná **Test** o **Probar**.
2. Iniciá una conversación nueva.

---

## Simular un candidato

Respondé las preguntas como si fueras un postulante real.

Ejemplos:

```text
Tengo dos años de experiencia en procesos de selección.
```

```text
Utilizo Excel para seguimiento de candidatos y reportes.
```

```text
He participado en actividades de onboarding.
```

---

## Verificar el comportamiento

Comprobá que:

- El agente haga una pregunta por vez.
- Utilice información relacionada con el puesto.
- Mantenga una conversación coherente.
- Genere un resumen final.

---

# ¿Quién utiliza este agente?

Este agente está pensado para interactuar directamente con el candidato.

El objetivo no es reemplazar al entrevistador sino:

- Estandarizar preguntas.
- Obtener respuestas consistentes.
- Reducir diferencias de criterio.
- Facilitar revisiones posteriores.

El área de Recursos Humanos continúa siendo responsable de analizar la información obtenida y tomar decisiones.

---

# ¿Por qué utilizar Copilot Studio?

Microsoft 365 Copilot está orientado a asistir a usuarios dentro de aplicaciones como:

- Word
- Excel
- Outlook
- Teams

En este laboratorio se necesita un agente conversacional especializado capaz de:

- Realizar preguntas.
- Mantener una entrevista.
- Recopilar respuestas.
- Generar resúmenes.

Por ese motivo Copilot Studio resulta más adecuado para este escenario.

---

# Desafío opcional: Registro automático en Excel

Las respuestas podrían almacenarse automáticamente en una tabla de Excel.

Ejemplo:

| Candidato | Fecha | Pregunta | Respuesta |
|------------|---------|-----------|-----------|
| Juan Pérez | 06/10/2026 | Experiencia en selección | ... |

O bien:

| Candidato | Fecha | P1 | P2 | P3 | P4 |
|------------|---------|----|----|----|----|
| Juan Pérez | 06/10/2026 | ... | ... | ... | ... |

## Consideraciones

El registro automático en Excel normalmente requiere componentes adicionales de Power Platform como:

- Power Automate
- Conectores de Excel
- Dataverse

Estas integraciones se encuentran fuera del alcance de este laboratorio y no son necesarias para completar la actividad principal.

---

# Resultado esperado

Al finalizar el laboratorio deberías disponer de:

- Un documento de descripción de puesto.
- Una guía de entrevista generada con Copilot.
- Un agente de Copilot Studio configurado.
- Una entrevista de prueba completada.
- Un resumen estructurado de respuestas.

La contratación, evaluación y selección final continúan siendo responsabilidad del equipo de Recursos Humanos.
