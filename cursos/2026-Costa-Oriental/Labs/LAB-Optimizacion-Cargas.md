# Laboratorio: Optimización de Carga de Camiones mediante IA

## Escenario

Bray Uruguay prepara embarques para su planta de Brasil.

Cada embarque se documenta mediante un **Packing List**, que contiene:

- Productos incluidos (SKU)
- Cantidades
- Peso
- Volumen
- Dimensiones de los cajones
- Cantidad de bultos (cajones)

Antes de despachar un camión, el área logística necesita determinar:

- Si la carga cumple las restricciones operativas.
- Si conviene consolidar varios embarques en un mismo camión.
- Si existen riesgos de sobrepeso o exceso de bultos.
- Cuál es la mejor alternativa para transportar la mercadería.

Para realizar el análisis se utilizará el **Agente Analista**.

---

## Objetivos

Al finalizar este laboratorio el alumno será capaz de:

- Analizar información logística mediante IA.
- Interpretar Packing Lists.
- Identificar restricciones operativas.
- Realizar consultas complejas sobre archivos Excel.
- Obtener recomendaciones automáticas para la planificación del transporte.

---

## Archivos utilizados

- 143599 Brasil.xls
- 143600 Brasil.xls
- 143698 Brasil_mod.xls
- 143699 Brasil.xls
- Brasil Mock.xls

---

## Restricciones operativas

Todos los análisis deberán considerar las siguientes reglas:

- Peso máximo permitido por camión: **35.000 Kg**
- Cantidad máxima permitida: **70 cajones**

---

# Parte 1 - Comprender el negocio

## ¿Qué es un Packing List?

Un Packing List es un documento logístico que describe exactamente qué productos serán enviados.

Contiene información como:

- SKU
- Descripción
- Cantidad
- Peso
- Volumen
- Dimensiones
- Cajón donde se encuentra cada producto

La información del Packing List se utiliza para planificar la carga y el transporte.

---

## ¿Qué significa consolidar carga?

Consolidar significa combinar varios embarques en un mismo vehículo para aprovechar mejor la capacidad disponible.

La decisión debe considerar:

- Peso total
- Volumen total
- Cantidad de cajones
- Restricciones operativas

---

# Parte 2 - Analizar un Packing List

## Paso 1

Abrir Microsoft 365 Copilot.

## Paso 2

Crear un nuevo chat con el **Agente Analista**.

## Paso 3

Adjuntar:

- 143599 Brasil.xls

## Paso 4

Enviar el siguiente prompt:

```text
Analiza este Packing List.

Genera un resumen ejecutivo indicando:

- Peso total
- Volumen total
- Cantidad de cajones
- Riesgos operativos identificados

Verifica además si la carga cumple los siguientes límites:

- Máximo 35.000 Kg
- Máximo 70 cajones
```

## Resultado esperado

El agente identifica automáticamente:

- Peso de la carga
- Volumen total
- Cantidad de cajones
- Cumplimiento de restricciones

---

# Parte 3 - Comparar varias alternativas de carga

## Paso 5

Adjuntar simultáneamente:

- 143599 Brasil.xls
- 143600 Brasil.xls
- 143698 Brasil_mod.xls
- 143699 Brasil.xls

## Paso 6

Enviar el siguiente prompt:

```text
Compara los cuatro Packing Lists.

Genera una tabla comparativa con:

- Peso total
- Volumen total
- Cantidad de cajones

Indica cuáles cumplen las restricciones operativas.

Ordena las opciones desde la más conveniente
hasta la menos conveniente para transportar.
```

## Resultado esperado

El agente genera una comparación completa de las alternativas disponibles.

---

# Parte 4 - Análisis de consolidación

## Paso 7

Utilizando los mismos cuatro archivos, ejecutar la siguiente consulta:

```text
Actúa como planificador logístico.

Analiza si es posible consolidar
más de un Packing List en el mismo camión.

Considera las siguientes restricciones:

- Peso máximo: 35.000 Kg
- Máximo 70 cajones

Indica:

- Qué combinaciones son posibles.
- Qué combinaciones no son posibles.
- Justifica cada decisión.
```

## Resultado esperado

El agente evalúa automáticamente si la suma de pesos y cajones permite combinar embarques.

---

# Parte 5 - Detección de una situación problemática

## Paso 8

Adjuntar:

- Brasil Mock.xls

## Paso 9

Enviar el siguiente prompt:

```text
Analiza este Packing List.

Determina si cumple las siguientes reglas:

- Peso máximo permitido: 35.000 Kg
- Máximo permitido: 70 cajones

Explica los riesgos logísticos asociados
a cualquier incumplimiento detectado.
```

## Resultado esperado

El agente identifica automáticamente excesos de capacidad y riesgos operativos.

---

# Parte 6 - Recomendación logística

## Paso 10

Sobre el mismo archivo, ejecutar:

```text
Actúa como consultor logístico.

Propón una estrategia para transportar esta carga.

Considera:

- Peso máximo permitido
- Cantidad máxima de cajones
- Minimizar riesgos operativos

Presenta una recomendación ejecutiva para la gerencia.
```

---

# Preguntas para discusión

1. ¿Qué ventajas aporta la IA frente a una revisión manual?
2. ¿Qué información fue necesaria para tomar decisiones logísticas?
3. ¿Qué riesgos operativos detectó el agente?
4. ¿En qué casos confiarías en la recomendación de la IA?
5. ¿Qué otros datos podrían mejorar el análisis?
