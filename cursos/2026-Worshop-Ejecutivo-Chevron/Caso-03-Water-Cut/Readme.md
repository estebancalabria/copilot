# Laboratorio: Exploración de Datos con Microsoft 365 Copilot Analyst

## Objetivo

Utilizar el agente Analyst para analizar un conjunto de datos reales de producción petrolera de Vaca Muerta y explorar distintas capacidades de análisis de datos, visualización, detección de anomalías, segmentación, regresión y generación de informes.

## Archivo utilizado

Adjuntar el archivo:

```text
WC01_Datos_produccion_Vaca_Muerta_Neuquen_petroliferos.xlsx
```

---

# Ejercicio 1 - Comprender el dataset

## Objetivo

Explorar la estructura y contenido del archivo.

## Prompt

```text
Analizá el archivo adjunto.

Describí:

- cantidad de filas
- cantidad de columnas
- nombres de las columnas
- significado probable de cada campo
- calidad general de los datos
- posibles limitaciones

Generá un resumen ejecutivo de los datos disponibles.
```

---

# Ejercicio 2 - Visualización y gráficos

## Objetivo

Generar visualizaciones utilizando Python y MatPlotLib.

## Prompt

```text
Analizá este dataset de la Secretaría de Energía.

Cruzá las columnas de producción de crudo y producción de agua.

Calculá el water cut utilizando la fórmula:

Water Cut = Agua / (Petróleo + Agua)

Armá un gráfico mostrando la evolución histórica del water cut por yacimiento.

Utilizá Python y MatPlotLib para generar la visualización.

Explicá qué tendencias observás en el gráfico.
```

---

# Ejercicio 3 - Estadística descriptiva

## Objetivo

Calcular métricas estadísticas relevantes.

## Prompt

```text
Analizá las columnas numéricas del dataset.

Calculá para producción de petróleo y producción de agua:

- promedio
- mediana
- mínimo
- máximo
- percentil 25
- percentil 75
- desviación estándar

Presentá una tabla resumen e interpretá los resultados.
```

---

# Ejercicio 4 - Evolución histórica de la producción

## Objetivo

Analizar tendencias temporales.

## Prompt

```text
Analizá la evolución histórica de la producción.

Generá gráficos que permitan observar:

- evolución del petróleo
- evolución del agua
- cantidad de pozos informados

Indicá si existen tendencias crecientes, decrecientes o períodos estables.
```

---

# Ejercicio 5 - Cálculo del Water Cut

## Objetivo

Construir un indicador derivado.

## Prompt

```text
Calculá el Water Cut mensual utilizando:

Water Cut = Agua / (Petróleo + Agua)

utilizando los volúmenes totales de cada mes.

Generá:

- tabla mensual
- gráfico temporal
- estadísticas del indicador

Describí la evolución observada.
```

---

# Ejercicio 6 - Detección de anomalías

## Objetivo

Encontrar valores atípicos en la serie temporal.

## Prompt

```text
Analizá la serie histórica del Water Cut.

Detectá:

- valores atípicos
- cambios bruscos
- comportamientos inesperados

Indicá:

- fecha
- valor observado
- diferencia respecto a la tendencia

No inventes explicaciones.

Mostrá evidencia basada únicamente en los datos.
```

---

# Ejercicio 7 - Investigación de una anomalía

## Objetivo

Profundizar sobre una anomalía detectada.

## Prompt

```text
Tomá la anomalía más importante detectada.

Investigá:

- cantidad de pozos informados
- empresas involucradas
- áreas involucradas
- diferencias respecto de los meses anteriores y posteriores

Presentá la evidencia encontrada.
```

---

# Ejercicio 8 - Clasificación de pozos

## Objetivo

Segmentar registros según el Water Cut.

## Prompt

```text
Para agosto de 2026 calculá el Water Cut individual de cada pozo.

Clasificá los pozos en:

- Menos de 30%
- Entre 30% y 50%
- Entre 50% y 80%
- Más de 80%

Generá:

- tabla de cantidades
- porcentaje sobre el total
- gráfico de distribución

Describí las características de cada grupo.
```

---

# Ejercicio 9 - Descubrimiento de patrones

## Objetivo

Identificar agrupamientos relevantes.

## Prompt

```text
Analizá el dataset buscando patrones de comportamiento.

Evaluá agrupamientos considerando:

- empresa
- área
- yacimiento
- nivel de Water Cut
- producción de petróleo
- producción de agua

Identificá los grupos más relevantes y describí sus características.
```

---

# Ejercicio 10 - Identificación de los principales productores

## Objetivo

Realizar análisis comparativos.

## Prompt

```text
Identificá:

- las empresas con mayor producción de petróleo
- las empresas con mayor producción de agua
- los yacimientos más productivos

Generá rankings y visualizaciones comparativas.

Explicá las principales diferencias observadas.
```

---

# Ejercicio 11 - Regresión y proyección

## Objetivo

Aplicar modelos predictivos simples.

## Prompt

```text
Utilizá la serie histórica del Water Cut.

Construí un modelo de regresión lineal para analizar la tendencia.

Mostrá:

- ecuación del modelo
- pendiente
- R²
- gráfico de ajuste

Proyectá el comportamiento para los próximos 12 meses.

Explicá los supuestos y limitaciones del modelo.
```

---

# Ejercicio 12 - Validación del modelo

## Objetivo

Evaluar la calidad de una proyección.

## Prompt

```text
Realizá una validación retrospectiva del modelo de regresión.

Utilizá únicamente datos históricos.

Calculá:

- error medio absoluto (MAE)
- error porcentual
- sesgo promedio

Compará los valores proyectados contra los valores reales.

Indicá qué tan confiable resulta la proyección.
```

---

# Ejercicio 13 - Preguntas en lenguaje natural

## Objetivo

Explorar capacidades de análisis ad hoc.

## Prompt

```text
Respondé utilizando únicamente los datos del archivo.

- ¿Qué empresa produjo más petróleo?
- ¿Qué empresa produjo más agua?
- ¿Qué yacimiento presenta mayor Water Cut?
- ¿Cómo evolucionó la cantidad de pozos informados?
- ¿Existen meses con comportamientos inusuales?
- ¿Qué tendencias destacás en los datos?

Justificá cada respuesta con evidencia.
```

---

# Ejercicio 14 - Resumen ejecutivo

## Objetivo

Comunicar hallazgos para la dirección.

## Prompt

```text
Actuá como analista de negocio.

Prepará un informe ejecutivo que incluya:

- situación general observada
- principales tendencias
- anomalías detectadas
- patrones relevantes
- resultados de la proyección
- limitaciones del análisis

Utilizá lenguaje ejecutivo.

No incluyas código.

Máximo una página.
```
