# Lab — Crear un agente analista inmobiliario con Copilot

**Sesión:** 4 · **Duración estimada:** 35 minutos
**Módulo:** Agentes con Microsoft 365 Copilot
**Patrón:** Agente con conocimiento (Knowledge Agent)

---

# La situación

Una de las capacidades más potentes de los agentes modernos no es solamente conversar. Es entender información empresarial.

En este laboratorio vas a crear un agente inmobiliario inteligente capaz de analizar un portfolio de proyectos de construcción usando lenguaje natural.

El agente no va a programarse. Tampoco vamos a entrenar un modelo.

Simplemente vamos a:

* crear un dataset
* subirlo a Microsoft 365
* conectarlo como conocimiento del agente
* hacer preguntas en lenguaje natural

---

# Objetivo del laboratorio

Al finalizar este lab vas a tener:

✅ un Excel con proyectos inmobiliarios
✅ un agente conectado al archivo
✅ análisis inteligente en lenguaje natural
✅ detección de riesgos y patrones
✅ insights ejecutivos automáticos

---

# Lo que vamos a construir

## El usuario podrá preguntar:

```text id="k4m8q1"
"¿Qué proyectos tienen más riesgo de sobrecosto?"
```

```text id="t7x2v5"
"¿Qué barrios concentran más inversión?"
```

```text id="r3n6p8"
"¿Cuáles están más demorados?"
```

```text id="d1v9m4"
"Generame un resumen ejecutivo del portfolio."
```

Y el agente responderá usando el Excel como fuente de conocimiento.

---

# Arquitectura

```text id="f5q2x7"
Excel → Agente Copilot → Análisis en lenguaje natural
```

---

# Requisitos

## Necesitás

* Cuenta Microsoft 365 con Copilot
* Acceso a:

  * Excel Online
  * OneDrive
  * Copilot Web
* Navegador web

---

# Paso 1 — Crear el dataset inmobiliario

🌐 **URL:**
[Microsoft Excel Online](https://www.office.com/launch/excel?utm_source=chatgpt.com)

---

# Crear archivo

1. Abrí Excel Online
2. Creá un libro nuevo
3. Guardalo como:

```text id="x7m2d9"
proyectos-inmobiliarios.xlsx
```

---

# Paso 2 — Generar datos con Copilot

Abrí una pestaña nueva con:

[Microsoft 365 Copilot Chat](https://m365.cloud.microsoft/chat?utm_source=chatgpt.com)

Escribí este prompt:

```text id="q2v7n5"
Generame 30 filas ficticias de proyectos inmobiliarios
en desarrollo en Argentina en formato tabla.

Columnas:
- Proyecto
- Barrio
- Metros cuadrados
- Porcentaje avance
- Costo actual USD
- Costo estimado USD
- Estado
- Riesgo
- Fecha estimada entrega

Quiero variedad realista:
- algunos proyectos demorados
- algunos con sobrecosto
- distintos barrios
- distintos tamaños
```

---

# Paso 3 — Copiar los datos a Excel

1. Copiá la tabla generada
2. Pegala en Excel
3. Ajustá columnas si hace falta

---

# Paso 4 — Convertir a tabla

Esto es importante.

1. Seleccioná todos los datos
2. Hacé:

```text id="b5x1q8"
Insertar → Tabla
```

---

# Paso 5 — Crear el agente

🌐 **URL:**
[Microsoft 365 Copilot](https://m365.cloud.microsoft/chat?utm_source=chatgpt.com)

---

# Crear agente

1. Ir a:

```text id="v8n4m2"
Agents → Create Agent
```

---

# Nombre

```text id="a6p3x7"
Real Estate Analyst
```

---

# Descripción

```text id="z9q1m5"
Agente especializado en análisis de proyectos inmobiliarios y detección de riesgos.
```

---

# Paso 6 — Configurar instrucciones

Pegá estas instrucciones:

```text id="e3r7k1"
Sos un analista inmobiliario senior.

Tu trabajo es analizar proyectos de construcción,
detectar riesgos, identificar patrones y generar
resúmenes ejecutivos.

Cuando analices datos:

- Detectá sobrecostos
- Detectá proyectos demorados
- Compará barrios
- Identificá tendencias
- Generá insights accionables
- Respondé siempre en español
- Usá tablas cuando sea útil
- Priorizá el análisis ejecutivo
```

---

# Paso 7 — Agregar conocimiento

Ahora vamos a conectar el Excel.

## Dentro del agente:

Ir a:

```text id="m2x8v4"
Knowledge → Add knowledge
```

---

# Agregar archivo

Seleccionar:

```text id="j7d1q6"
proyectos-inmobiliarios.xlsx
```

---

# Esperar indexación

Dependiendo del tenant, puede tardar unos minutos.

---

# Paso 8 — Probar el agente

Abrí el chat del agente y probá preguntas.

---

# Ejercicio 1 — Riesgos

```text id="t4m9x2"
¿Qué proyectos tienen más riesgo de sobrecosto?
```

---

# Ejercicio 2 — Demoras

```text id="y6q3v8"
¿Cuáles parecen más demorados?
```

---

# Ejercicio 3 — Inversión

```text id="c8r1p5"
¿Qué barrios concentran más inversión?
```

---

# Ejercicio 4 — Resumen ejecutivo

```text id="u5n7k3"
Generame un resumen ejecutivo del portfolio inmobiliario.
```

---

# Ejercicio 5 — Insight avanzado

```text id="d2x6m9"
¿Qué patrones o problemas estructurales detectás?
```

---

# Lo importante del laboratorio

El agente:

✅ NO fue entrenado
✅ NO usa machine learning personalizado
✅ NO requiere código

Simplemente:

* recibe contexto
* interpreta lenguaje natural
* razona sobre documentos

---

# Experimento opcional

Agregá más archivos:

* contratos PDF
* presupuestos
* reportes Word
* planos
* informes financieros

Y preguntá:

```text id="h1q8v6"
"¿Qué inconsistencias encontrás entre los documentos?"
```

---

# Preguntas de reflexión

1. ¿Qué diferencia hay entre buscar información y conversar con un agente?
2. ¿Qué ventajas tiene usar lenguaje natural sobre filtros tradicionales?
3. ¿Qué riesgos existen si el agente interpreta mal datos empresariales?
4. ¿Qué procesos reales podrían usar este patrón?

---

# El aprendizaje clave

La revolución de los agentes no está solamente en “hablar con IA”.

Está en que ahora la IA puede trabajar sobre información empresarial real usando lenguaje natural.

El usuario ya no necesita:

* saber SQL
* crear dashboards complejos
* construir filtros avanzados

Puede simplemente preguntar.

Y el agente razona sobre los datos.

---

# Próximo lab

**Lab — Agente operativo con Power Automate**

Ahora vamos a dar el siguiente paso:

```text id="n8m2q4"
Que el agente no solo analice información…
sino que además modifique sistemas automáticamente.
```

---

*Material desarrollado por MCT Esteban Calabria · [https://linkedin.com/in/esteban-calabria](https://linkedin.com/in/esteban-calabria)*
