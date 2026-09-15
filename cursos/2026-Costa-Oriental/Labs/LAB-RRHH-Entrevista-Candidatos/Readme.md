# Laboratorio: Guía de entrevista y registro de respuestas con Microsoft 365 Copilot

## Objetivo

A partir de una descripción de puesto, utilizar Microsoft 365 Copilot para:

- Generar una guía estructurada de preguntas de entrevista.
- Crear una planilla de evaluación con una escala de 1 a 5.
- Construir en Copilot Studio un agente que realice la entrevista.
- Registrar cada respuesta en una tabla de Excel.

El objetivo es estandarizar el proceso de entrevista y reducir las diferencias de criterio entre entrevistadores. La evaluación y la decisión final siempre estarán a cargo de una persona.

## Prerrequisitos

- Licencia activa de Microsoft 365 Copilot.
- Acceso a Microsoft Word y Microsoft Excel.
- Acceso a Microsoft Copilot Studio.
- Permisos para crear agentes y conexiones.
- Acceso al conector Excel Online (Business).
- OneDrive para la Empresa o SharePoint Online.
- Permisos de edición sobre los archivos utilizados en el laboratorio.

---

## Paso 1: Preparar la descripción del puesto

1. Abrí Microsoft Word.
2. Creá un documento nuevo.
3. Guardalo con el nombre:

   `JD-Analista-RRHH.docx`

4. Copiá la siguiente descripción:

### Descripción del puesto

**Puesto:** Analista de Recursos Humanos Jr.  
**Reporta a:** Coordinador de Talento

**Responsabilidades:**

- Brindar soporte en procesos de selección.
- Coordinar entrevistas.
- Cargar y realizar el seguimiento de candidatos en el ATS.
- Colaborar en procesos de onboarding.

**Requisitos:**

- Entre uno y dos años de experiencia en Recursos Humanos.
- Manejo de Microsoft Excel.
- Buena comunicación oral y escrita.
- Proactividad.

**Deseable:**

- Conocimiento de herramientas de inteligencia artificial generativa aplicadas a Recursos Humanos.

5. Guardá el documento en OneDrive para la Empresa o SharePoint Online.

---

## Paso 2: Abrir Copilot con el documento como contexto

1. Mantené abierto `JD-Analista-RRHH.docx`.
2. En la cinta de Word, seleccioná **Copilot**.
3. Verificá que Copilot esté trabajando con el documento abierto como contexto.

> Si el documento no está almacenado en OneDrive o SharePoint, algunas funciones de Copilot pueden no estar disponibles.

---

## Paso 3: Generar la guía de entrevista

En el panel de Copilot de Word, ingresá el siguiente prompt:

```text
Actuá como especialista en selección de Recursos Humanos.

A partir exclusivamente de la descripción de puesto incluida en este documento, generá una guía de entrevista para el puesto de Analista de Recursos Humanos Jr.

Requisitos de la guía:

- Definí tres competencias clave relacionadas con el puesto.
- Creá un total de ocho preguntas.
- Agrupá las preguntas por competencia.
- Para cada pregunta, explicá brevemente qué aspecto busca evaluar.
- No agregues requisitos que no estén presentes en la descripción del puesto.
- Presentá el resultado con títulos y una tabla clara.
