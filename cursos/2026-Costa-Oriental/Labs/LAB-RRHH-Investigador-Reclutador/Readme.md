# Laboratorio: Preselección Inteligente de Candidatos con el Agente Investigador

## Objetivo

Utilizar el Agente Investigador de Microsoft 365 Copilot para analizar múltiples currículums almacenados en OneDrive, identificar los candidatos que mejor se ajustan a una vacante y generar recomendaciones para el proceso de selección.

---

# Escenario

Costa Oriental necesita incorporar un nuevo Supervisor de Operaciones Logísticas.

El área de RRHH ha recibido diversos currículums para la posición y desea utilizar Inteligencia Artificial para:

- Identificar los candidatos más adecuados.
- Detectar fortalezas y debilidades.
- Comparar perfiles de forma objetiva.
- Reducir el tiempo de análisis.
- Preparar entrevistas más efectivas.

Los currículums ya se encuentran almacenados en OneDrive.


---

# Requisitos

- Microsoft 365 Copilot.
- Acceso al Agente Investigador (Researcher).
- Carpeta de OneDrive con los CVs cargados.

---

# Actividad 1

## Preparar la información

Crear una carpeta en OneDrive denominada:

```text
RRHH - CVs Supervisor Operaciones
```

Cargar en dicha carpeta los CVs proporcionados para la actividad.

---

# Actividad 2

## Abrir el Agente Investigador

1. Acceder a Microsoft 365 Copilot.
2. Seleccionar **Agentes**.
3. Abrir **Investigador**.

---

# Actividad 3

## Definir la vacante mediante un prompt

Ingresar el siguiente prompt:

```text
Analiza los currículums disponibles.

Extrae y organiza información factual contenida en cada documento.

Incluye:

- Formación académica.
- Certificaciones.
- Puestos ocupados.
- Sectores de experiencia.
- Tecnologías mencionadas.
- Herramientas utilizadas.
- Idiomas.
- Cantidad de años de experiencia informados.
- Responsabilidades descritas.

Presenta la información en formato tabular.
```

---

# Resultado esperado

El agente debería:

- Leer todos los CVs disponibles.
- Comparar cada perfil con los requisitos.
- Generar un ranking de candidatos.
- Explicar los criterios utilizados.
- Justificar la recomendación.

---

# Actividad 4

## Identificar brechas y riesgos

Ingresar el siguiente prompt:

```text
Para cada candidato recomendado:

- Identifica fortalezas.
- Identifica debilidades.
- Indica riesgos potenciales.
- Detecta competencias faltantes.
- Explica por qué podría o no avanzar en el proceso.
```

---

# Resultado esperado

Obtención de un análisis objetivo similar al realizado por un reclutador experimentado.

---

# Actividad 5

## Generar preguntas de entrevista

Ingresar el siguiente prompt:

```text
Genera una guía de entrevista para los tres candidatos mejor posicionados.

Incluye:

- Preguntas técnicas.
- Preguntas sobre liderazgo.
- Preguntas situacionales.
- Aspectos de riesgo a validar.
- Competencias críticas a evaluar.
```

---

# Resultado esperado

El agente debe generar preguntas específicas para cada perfil analizado.

---

# Actividad 6

## Selección final recomendada

Ingresar el siguiente prompt:

```text
Actúa como responsable de selección.

Considerando toda la información analizada:

- Recomienda un candidato principal.
- Propón dos candidatos de respaldo.
- Explica el razonamiento.
- Resume los factores clave de decisión.
```

---

# Resultado esperado

Generación de un informe ejecutivo de selección que permita acelerar la toma de decisiones.

---

# Discusión Final

Analizar las siguientes preguntas:

1. ¿Cuánto tiempo se hubiera requerido para revisar manualmente todos los CVs?
2. ¿La IA identificó candidatos que probablemente hubieran pasado desapercibidos?
3. ¿Qué ventajas ofrece el análisis comparativo automatizado?
4. ¿Qué validaciones humanas siguen siendo necesarias?
5. ¿Cómo podría utilizarse este mismo proceso para otras posiciones dentro de la empresa?

---

# Aprendizajes Esperados

Al finalizar este laboratorio el participante será capaz de:

- Utilizar el Agente Investigador para analizar grandes volúmenes de currículums.
- Comparar candidatos contra una descripción de puesto.
- Identificar fortalezas y brechas de competencias.
- Generar rankings fundamentados de candidatos.
- Crear guías de entrevista asistidas por IA.
- Reducir tiempos de reclutamiento y selección.
- Mejorar la calidad de las decisiones de contratación.
