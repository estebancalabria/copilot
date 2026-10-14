# Caso 4 - Presentación al Directorio

## Objetivo

Crear una presentación para el Directorio utilizando una cadena de trabajo compuesta por:

1. Investigación
2. Documento base
3. Esquema
4. Presentación

La idea no es mostrar que la IA crea diapositivas.

La idea es mostrar cómo cada documento alimenta al siguiente y cómo se controla la calidad del resultado en cada etapa.

---

# Paso 1 - Entender el problema

## Acción

Abrir PD01.

Leer la solicitud recibida del Directorio.

## Qué dice el profesor

- "Antes de abrir Copilot necesitamos entender el problema."
- "El Directorio no nos pidió una investigación."
- "No nos pidió un documento."
- "No nos pidió una presentación."
- "Nos pidió una recomendación."
- "La pregunta que tenemos que responder es cómo asegurar la capacidad de transporte necesaria para Horizonte 2027."
- "Todo lo que hagamos a continuación tiene que ayudarnos a responder esa pregunta."

## Resultado esperado

Todos entienden qué decisión debe tomarse.

---

# Paso 2 - Realizar la investigación

## Acción

1. Abrir Microsoft 365 Copilot.
2. Crear un chat nuevo.
3. Seleccionar Researcher.
4. Adjuntar PD01.

## Qué dice el profesor

- "Ahora vamos a investigar el contexto externo."
- "Todavía no vamos a utilizar información interna."
- "Primero queremos entender qué está ocurriendo fuera de la empresa."
- "Por eso solamente voy a adjuntar el pedido del Directorio."

## Prompt

```text
Contexto:
Asume que eres la directora de Administración y Finanzas de Auren Patagonia Energía.

La Secretaría del Directorio te pidió una presentación sobre capacidad de transporte para Horizonte 2027.

Preparas el material base para construir posteriormente esa presentación.

Tarea:

Investiga exclusivamente fuentes públicas publicadas entre el 01/09/2025 y el 11/10/2026 sobre:

1. El anuncio del Gobierno de Neuquén sobre exigir capacidad de transporte para nuevas concesiones.
2. La infraestructura de transporte de petróleo de Vaca Muerta:
   - Oldelval
   - Duplicar
   - Duplicar Norte
   - VMOS
3. La ampliación del Gasoducto Perito Moreno.
4. Opciones para operadores que no poseen capacidad propia.

Formato:

1. Resumen ejecutivo.
2. Situación regulatoria.
3. Transporte de petróleo.
4. Transporte de gas.
5. Opciones para operadores.
6. Diferencias entre fuentes.
7. Fuentes utilizadas.

Restricciones:

- Utiliza solamente información pública.
- Cada dato debe incluir fecha y enlace.
- No inventes datos.
- Si existen diferencias entre fuentes muéstralas.
- Si algo es un anuncio y no una norma, indícalo.
- Encabeza el documento con la palabra BORRADOR.
```

## Qué dice el profesor mientras trabaja

- "Researcher trabaja durante varios minutos porque realiza una investigación de múltiples pasos."
- "No está respondiendo solamente con lo que conoce."
- "Está buscando, comparando y organizando información."

## Resultado esperado

Un informe de investigación con fuentes y referencias.

---

# Paso 3 - Revisar la investigación

## Acción

Leer la investigación.

Abrir varios enlaces.

Comprobar los datos más importantes.

## Qué dice el profesor

- "La investigación parece terminada."
- "Pero todavía no es un entregable."
- "Ahora vamos a validarla."
- "La IA acelera la búsqueda."
- "La validación sigue siendo humana."

### Revisar el anuncio de Neuquén

- "Quiero verificar si estamos viendo una norma o solamente un anuncio."
- "Esa diferencia puede cambiar completamente una decisión."

### Revisar capacidades de transporte

- "También voy a comprobar que las cifras provengan de fuentes reales."
- "Si dos fuentes indican valores distintos, quiero ver ambas."

## Resultado esperado

Un informe validado.

---

# Paso 4 - Corregir la investigación

## Acción

Pegar el siguiente prompt.

## Qué dice el profesor

- "Ahora vamos a hacer una segunda pasada."
- "No estamos aceptando automáticamente la primera versión."
- "Estamos refinando el trabajo."

## Prompt

```text
Revisa el informe y aplica las siguientes reglas:

1. Elimina cualquier dato sin fuente o sin fecha.
2. Distingue claramente anuncios de normas.
3. Si dos fuentes difieren:
   - muestra ambas cifras,
   - indica cuál utilizas,
   - explica el criterio.
4. Agrega una sección llamada "Cálculo de control" donde muestres los cálculos explícitamente.
5. No agregues información nueva.
```

## Resultado esperado

Versión corregida de la investigación.

---

# Paso 5 - Generar el documento base

## Acción

Abrir un chat nuevo.

Adjuntar:

- Investigación validada.
- PD01.
- PD03.

## Qué dice el profesor

- "Hasta ahora trabajamos con el contexto externo."
- "Ahora vamos a incorporar el estado real del proyecto."
- "La idea es construir un documento que combine ambas perspectivas."

## Prompt

```text
Utilizando exclusivamente los documentos adjuntos:

- Solicitud del Directorio
- Investigación validada
- Estado de Horizonte 2027

Genera un documento ejecutivo que incluya:

1. Pedido del Directorio.
2. Situación regulatoria.
3. Transporte de petróleo.
4. Transporte de gas.
5. Estado de Horizonte 2027.
6. Datos faltantes.
7. Decisión propuesta.
8. Fuentes.

Reglas:

- Cada cifra debe incluir una fuente.
- Si un dato no existe escribe exactamente "Sin dato".
- No estimes información.
- No agregues presupuesto.
- Distingue anuncios de normas.
- Encabeza el documento con BORRADOR.
```

## Qué dice el profesor al revisar

- "Quiero comprobar que la IA no complete huecos inventando."
- "Si un dato no existe, debe decir 'Sin dato'."

## Resultado esperado

Documento base para toma de decisión.

---

# Paso 6 - Crear el esquema de la presentación

## Acción

Usar el documento base generado.

## Qué dice el profesor

- "Antes de construir una presentación vamos a construir el mensaje."
- "Primero contenido."
- "Después diseño."

## Prompt

```text
Utiliza exclusivamente el documento base.

Genera un esquema para una presentación de 8 diapositivas.

Para cada diapositiva incluye:

- Título.
- Entre 3 y 5 viñetas.
- Una sección llamada "Notas del orador".

Diapositivas:

1. Portada.
2. Decisión solicitada.
3. Situación regulatoria.
4. Transporte de petróleo.
5. Transporte de gas.
6. Estado de Horizonte 2027.
7. Riesgos y datos faltantes.
8. Próximos pasos.

No agregues información nueva.
Mantén los textos "Sin dato" donde corresponda.
```

## Resultado esperado

Documento de Word con la estructura de la presentación.

---

# Paso 7 - Generar PowerPoint

## Acción

1. Abrir la plantilla PowerPoint.
2. Seleccionar Create Presentation From File.
3. Elegir el esquema generado.

## Qué dice el profesor

- "Ahora PowerPoint va a utilizar el esquema como materia prima."
- "Las instrucciones ya están dentro del documento."
- "Por eso dedicamos tiempo a construirlo correctamente."

## Resultado esperado

Presentación inicial generada por Copilot.

---

# Paso 8 - Revisar la presentación

## Acción

Ejecutar este prompt:

```text
Indica qué diapositivas contienen cifras o fechas.

Para cada una:

- identifica la fuente utilizada,
- indica si la fuente aparece en las notas del orador.
```

## Qué dice el profesor

- "La presentación parece terminada."
- "Pero todavía no está aprobada."
- "Voy a comprobar que cada dato pueda rastrearse hasta una fuente verificable."
- "Una presentación rápida no necesariamente es una presentación confiable."

## Resultado esperado

Presentación validada y lista para revisión humana.
