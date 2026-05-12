# Lab — Crear un agente personal trainer que actualiza Excel automáticamente

**Sesión:** 4 · **Duración estimada:** 45 minutos
**Módulo:** Agentes con Microsoft 365 Copilot
**Patrón:** IA + Automatización + Excel + Memoria operativa

---

# La situación

Hasta ahora usaste Copilot para responder preguntas o resumir información. Pero los agentes modernos pueden hacer algo mucho más potente:

* leer archivos
* interpretar lenguaje natural
* ejecutar acciones
* actualizar datos automáticamente

En este laboratorio vas a crear un agente de fitness y nutrición que actúa como un personal trainer digital:

✅ registra comidas
✅ registra entrenamientos
✅ actualiza un Excel automáticamente
✅ mantiene histórico diario
✅ genera resúmenes semanales

Todo usando lenguaje natural.

---

# Objetivo del laboratorio

Al finalizar este lab vas a tener:

* un Excel conectado en OneDrive
* un agente personalizado en Copilot
* un flujo automático con Power Automate
* actualización automática del Excel desde prompts

---

# Arquitectura final

## Lo que vamos a construir

```text id="r0yqz2"
Usuario → Copilot Agent → Power Automate → Excel Online
```

Ejemplo:

```text id="m9n2x1"
"Hoy hice 45 minutos de natación y comí pollo con arroz."
```

↓

El agente:

* interpreta la comida
* interpreta el ejercicio
* ejecuta el flujo
* agrega una fila en Excel

---

# Requisitos

## Necesitás

* Cuenta Microsoft 365 con Copilot
* Acceso a:

  * Copilot
  * OneDrive
  * Excel Online
  * Power Automate
* Navegador web

---

# Paso 1 — Crear el Excel base

Primero vamos a crear la base de datos del agente.

🌐 **URL:**
[Microsoft Excel Online](https://www.office.com/launch/excel?utm_source=chatgpt.com)

---

## Crear archivo

1. Abrí Excel Online
2. Creá un libro nuevo
3. Guardalo como:

```text id="v7k1d4"
fitness-tracker.xlsx
```

---

## Crear tabla

En la hoja 1 creá esta tabla:

| Fecha | Comida | Calorias | Proteina | Ejercicio | Duracion | Observaciones |
| ----- | ------ | -------- | -------- | --------- | -------- | ------------- |

---

## IMPORTANTE

Seleccioná toda la tabla y hacé:

```text id="t5h8c9"
Insertar → Tabla
```

Excel Online necesita una tabla formal para que Power Automate pueda escribir filas.

---

## Renombrar tabla

En “Diseño de tabla”:

```text id="k3p7n6"
TablaFitness
```

---

# Paso 2 — Crear el flujo automático

Ahora vamos a crear la automatización que actualiza Excel.

🌐 **URL:**
[Microsoft Power Automate](https://make.powerautomate.com?utm_source=chatgpt.com)

---

# Crear flujo

## 1. Crear

Hacé clic en:

```text id="q4w6e8"
Create → Instant cloud flow
```

Nombre:

```text id="j2u5f1"
RegistrarFitness
```

---

## 2. Trigger

Elegí:

```text id="s8m3r0"
When an HTTP request is received
```

> Dependiendo de la licencia, puede variar el nombre del trigger.

---

# Paso 3 — Agregar acción de Excel

## Nueva acción

Buscá:

```text id="z6x1a4"
Excel Online (Business)
```

Elegí:

```text id="n7b2v5"
Add a row into a table
```

---

# Configurar conexión

## Archivo

Seleccioná:

```text id="f9c4y7"
fitness-tracker.xlsx
```

## Tabla

```text id="u3l8o2"
TablaFitness
```

---

# Mapear columnas

Asigná:

| Excel         | Valor         |
| ------------- | ------------- |
| Fecha         | fecha         |
| Comida        | comida        |
| Calorias      | calorias      |
| Proteina      | proteina      |
| Ejercicio     | ejercicio     |
| Duracion      | duracion      |
| Observaciones | observaciones |

---

# Paso 4 — Guardar y copiar URL

Guardá el flujo.

Power Automate te va a generar una URL HTTP.

Copiala.

La vamos a usar desde el agente.

---

# Paso 5 — Crear el agente en Copilot

🌐 **URL:**
[Microsoft 365 Copilot](https://m365.cloud.microsoft/chat?utm_source=chatgpt.com)

---

# Crear agente

## Ir a

```text id="b8v5m2"
Agents → Create agent
```

---

# Nombre del agente

```text id="p1x7k4"
Fitness Coach AI
```

---

# Descripción

```text id="w6n2c9"
Asistente de fitness y nutrición que registra comidas y ejercicios automáticamente en Excel.
```

---

# Paso 6 — Configurar instrucciones

Pegá estas instrucciones:

```text id="a4d8f0"
Sos un personal trainer y asistente nutricional.

Tu trabajo es:

- Registrar comidas diarias
- Registrar ejercicios
- Estimar calorías y proteínas
- Mantener histórico diario
- Detectar fatiga o sobreentrenamiento
- Responder siempre en español

Cuando el usuario describa una comida o entrenamiento:

1. Extraé:
- comida
- ejercicio
- duración
- observaciones

2. Estimá:
- calorías
- proteínas

3. Ejecutá la acción de registro.

4. Confirmá el registro al usuario.
```

---

# Paso 7 — Crear acción conectada

Ahora conectamos el agente con Power Automate.

## Agregar acción

Dentro del agente:

```text id="e5g1u7"
Actions → Add action
```

Elegí:

```text id="h2r9c3"
Power Automate Flow
```

Seleccioná:

```text id="d7q4w1"
RegistrarFitness
```

---

# Paso 8 — Probar el agente

Abrí el chat del agente y escribí:

```text id="c8m5n0"
Hoy comí:
- 2 huevos
- arroz
- pollo

Entrené:
- 40 minutos de natación
- 15 minutos de calistenia
```

---

# Resultado esperado

El agente debería:

✅ interpretar la información
✅ calcular valores estimados
✅ ejecutar el flujo
✅ insertar una fila en Excel
✅ responder algo como:

```text id="y3t6k8"
Registro actualizado correctamente.

Resumen:
- Calorías estimadas: 850
- Proteínas estimadas: 62g
- Ejercicio: natación + calistenia
```

---

# Paso 9 — Verificar Excel

Volvé a:

[Excel Online](https://www.office.com/launch/excel?utm_source=chatgpt.com)

Abrí:

```text id="o7v2m4"
fitness-tracker.xlsx
```

Verificá que apareció una nueva fila automáticamente.

---

# Paso 10 — Experimentar

Probá prompts distintos:

```text id="i9p4e6"
Hoy descansé pero comí bastante mal:
pizza, helado y gaseosa.
```

o:

```text id="l5x8d2"
Hice 100 piletas y después cené lentejas con huevo y palta.
```

---

# Desafío opcional

Intentá agregar:

* gráfico semanal
* cálculo automático de peso
* dashboard
* alertas de sobreentrenamiento
* integración con Teams
* recordatorio diario automático

---

# Preguntas de reflexión

1. ¿Qué diferencia hay entre un chatbot y un agente?
2. ¿Qué parte agrega más valor: el modelo o la automatización?
3. ¿Qué otros procesos reales podrían automatizarse con esta arquitectura?
4. ¿Qué riesgos existen si el agente modifica datos automáticamente?

---

# El aprendizaje clave

El salto más importante de la IA moderna no es que “responda preguntas”.

Es que puede:

* interpretar lenguaje natural
* tomar decisiones simples
* ejecutar acciones reales
* actualizar sistemas automáticamente

Cuando conectás un LLM con herramientas como Excel y Power Automate, dejás de tener un chatbot.

Empezás a tener un agente operativo.

---

# Próximo lab

**Lab — Analista financiero con Copilot + Excel + Agentes**

Vamos a construir un agente que:

* analiza KPIs
* detecta anomalías
* genera insights
* actualiza dashboards automáticamente

---

*Material desarrollado por MCT Esteban Calabria · [https://linkedin.com/in/esteban-calabria](https://linkedin.com/in/esteban-calabria)*

