# Laboratorio 4: Diseño de Encuestas e Indicadores de RRHH con un Agente de Microsoft 365 Copilot

## Objetivo

Utilizar Microsoft 365 Copilot y Agent Builder para:

- Crear un agente especializado en diseño de encuestas de RRHH.
- Reutilizar documentación interna como fuente de conocimiento.
- Generar encuestas alineadas con iniciativas de la organización.
- Definir indicadores y KPIs para medir resultados.
- Crear cuestionarios listos para Microsoft Forms.
- Analizar la calidad de las preguntas generadas por la IA.
- Estandarizar los procesos de medición de programas internos.

---

## Escenario

Costa Oriental desarrolla periódicamente iniciativas destinadas a mejorar la experiencia de los colaboradores, fortalecer la capacitación y acompañar el crecimiento de la organización.

Actualmente, el equipo de RRHH necesita diseñar encuestas para medir el impacto de distintos programas, pero la construcción de cuestionarios, indicadores y criterios de evaluación se realiza de forma manual.

Para agilizar este proceso, se decide crear un agente especializado en Microsoft 365 Copilot que ayude a:

- Diseñar encuestas.
- Definir indicadores.
- Sugerir KPIs.
- Estandarizar escalas de evaluación.
- Generar formularios listos para Microsoft Forms.

---

# Parte 1 – Preparar el conocimiento organizacional

## Paso 1 – Crear documentos de referencia

Crear una carpeta denominada:

**RRHH - Encuestas e Indicadores**

Dentro de la carpeta crear los siguientes documentos Word.

---

## Documento 1

**Programa de Bienestar y Calidad de Vida.docx**

```text
Nombre del programa:
Bienestar y Calidad de Vida Costa Oriental

Objetivo:
Promover hábitos saludables, mejorar el bienestar general de los colaboradores y fortalecer el equilibrio entre la vida personal y laboral.

Actividades realizadas:

- Pausas activas en depósitos y oficinas.
- Charlas sobre hábitos saludables.
- Talleres de gestión del estrés.
- Actividades deportivas.
- Campañas internas de bienestar.

Aspectos que RRHH desea medir:

- Participación.
- Nivel de satisfacción.
- Utilidad percibida.
- Impacto sobre el bienestar.
- Interés en futuras actividades.
```

---

## Documento 2

**Programa de Capacitación Operativa.docx**

```text
Nombre del programa:
Capacitación Operativa Costa Oriental

Objetivo:
Fortalecer las habilidades técnicas y operativas del personal de logística, distribución y depósito.

Temáticas:

- Seguridad operativa.
- Procedimientos de carga y descarga.
- Gestión de inventario.
- Uso de herramientas digitales.
- Atención al cliente.

Aspectos que RRHH desea medir:

- Calidad de la capacitación.
- Aplicación práctica de los contenidos.
- Utilidad para el puesto.
- Satisfacción general.
- Nuevas necesidades de capacitación.
```

---

## Documento 3

**Encuesta Histórica - Capacitación.docx**

```text
Preguntas utilizadas anteriormente:

1. ¿Cómo califica la capacitación recibida?
2. ¿La capacitación fue útil para su trabajo?
3. ¿Considera adecuados los contenidos?
4. ¿Recomendaría esta capacitación?
5. ¿Qué mejoras propondría?
```

---

## Paso 2 – Guardar los documentos

Guardar los documentos en OneDrive o SharePoint.

Verificar que los archivos se encuentren disponibles para ser utilizados como conocimiento del agente.

---

# Parte 2 – Crear el agente

## Paso 3 – Crear un nuevo agente

1. Abrir Microsoft 365 Copilot.
2. Seleccionar **Crear un agente**.
3. Elegir creación mediante lenguaje natural.

---

## Paso 4 – Definir el comportamiento del agente

Utilizar la siguiente descripción:

```text
Crea un agente denominado "Diseñador de Encuestas RRHH".

Este agente ayudará al área de Recursos Humanos de Costa Oriental a diseñar encuestas e indicadores para medir programas, iniciativas y actividades internas.

Antes de generar una encuesta debe solicitar:

- Nombre de la iniciativa.
- Objetivo del programa.
- Público destinatario.
- Información que se desea medir.
- Cantidad máxima de preguntas.

Luego debe generar:

- Objetivos de medición.
- Indicadores sugeridos.
- KPIs recomendados.
- Escalas de valoración.
- Preguntas cerradas.
- Preguntas abiertas.
- Recomendaciones para Microsoft Forms.

Cuando exista documentación relacionada deberá utilizarla como referencia.

No debe evaluar personas ni emitir juicios sobre colaboradores.

Debe enfocarse exclusivamente en la medición de programas e iniciativas organizacionales.

Todas las recomendaciones deberán estar orientadas a la mejora continua y a la obtención de información útil para la toma de decisiones.
```

---

# Parte 3 – Incorporar conocimiento

## Paso 5 – Agregar archivos al agente

Incorporar como fuentes de conocimiento:

- Programa de Bienestar y Calidad de Vida.docx
- Programa de Capacitación Operativa.docx
- Encuesta Histórica - Capacitación.docx

Publicar el agente.

---

# Parte 4 – Configurar preguntas sugeridas

## Paso 6 – Agregar preguntas iniciales

Configurar las siguientes preguntas:

```text
Ayúdame a diseñar una encuesta para medir una capacitación.

Necesito definir indicadores para un programa interno.

Genera una encuesta para evaluar una iniciativa de bienestar.

¿Qué KPIs debería utilizar para medir participación y satisfacción?

Genera un formulario listo para Microsoft Forms.
```

---

# Parte 5 – Probar el agente

## Escenario 1 – Programa de Bienestar

Enviar el siguiente prompt:

```text
Necesito medir el impacto del programa Bienestar y Calidad de Vida.

Genera:

- Objetivos de medición.
- KPIs.
- Indicadores.
- Encuesta de 10 preguntas.
- Escala de satisfacción.
```

Validar:

- Indicadores propuestos.
- Calidad de las preguntas.
- Relación con la documentación cargada.

---

## Escenario 2 – Capacitación Operativa

Enviar el siguiente prompt:

```text
Necesito medir la efectividad del programa de Capacitación Operativa.

Genera:

- KPIs recomendados.
- Encuesta.
- Escala de valoración.
- Preguntas abiertas.
- Sugerencias de mejora.
```

Analizar:

- Cómo reutiliza la información interna.
- Cómo propone las métricas.
- Qué información considera relevante.

---

# Parte 6 – Generar un formulario para Microsoft Forms

## Paso 7 – Crear la estructura del formulario

Enviar el siguiente prompt:

```text
Genera una versión lista para Microsoft Forms basada en la encuesta del Programa de Bienestar.

Incluye:

- Título.
- Descripción.
- Tipo de pregunta.
- Opciones de respuesta.
- Escalas de valoración.
```

---

## Paso 8 – Crear el formulario

1. Acceder a Microsoft Forms.
2. Crear un formulario nuevo.
3. Copiar la estructura generada por el agente.
4. Revisar el cuestionario.
5. Publicar el formulario.

---

# Resultado esperado

Al finalizar el laboratorio los participantes habrán creado un agente especializado en RRHH capaz de:

- Diseñar encuestas organizacionales.
- Reutilizar documentación interna de Costa Oriental.
- Generar indicadores y KPIs.
- Estandarizar criterios de medición.
- Crear formularios listos para Microsoft Forms.
- Reducir el tiempo necesario para diseñar procesos de relevamiento y análisis de información.

Asimismo, los participantes comprenderán cómo Microsoft 365 Copilot puede actuar como asistente para la generación de instrumentos de medición reutilizando el conocimiento corporativo disponible en OneDrive y SharePoint.
