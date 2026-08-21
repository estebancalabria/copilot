# Laboratorio: Tablas Dinámicas con el Agente Analyst de Excel

**Módulo relacionado:** 2.0 Integración con Ecosistema 365 / 2.1 Análisis de la información
**Duración estimada:** 30-40 min
**Dataset:** Financial Sample.xlsx (oficial de Microsoft)
**Regla del laboratorio:** todo se resuelve pidiéndoselo a Copilot / al Agente Analyst. No se usan menús de Excel (Insertar, etc.) en ningún paso.

## Objetivo

Que el participante aprenda a resolver análisis de datos completos (tablas dinámicas, gráficos, proyecciones, detección de anomalías) delegando cada paso en el Agente Analyst de Excel, y a evaluar de forma crítica la respuesta que le devuelve.

## Prerrequisitos

- Cuenta de Microsoft 365 corporativa con licencia Copilot activa.
- Excel de escritorio o Excel Web (m365.cloud.microsoft).

---

## Parte 1 — Descarga del dataset

1. [BROWSER] Abrí una pestaña nueva y navegá a:
   `https://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Financial Sample.xlsx`
2. [WINDOWS] Guardá el archivo, idealmente directo en OneDrive.
3. [WINDOWS] Abrí el archivo con Excel.
4. [TAB] Abrí el panel de Copilot (ícono de Copilot en la cinta).

---

## Parte 2 — Qué es Financial Sample: que lo explique Copilot

En vez de que el instructor explique el dataset, se lo pedimos a la herramienta.

**Prompt:**
```
Explicame qué contiene esta planilla: qué representa cada columna,
qué unidad de negocio parece describir, y qué tipo de análisis
permite hacer con estos datos.
```

Lo que debería identificar (y el instructor valida contra la respuesta real de Copilot):

| Columna | Qué representa |
|---|---|
| Segment | Segmento de cliente (Government, Enterprise, Midmarket, Channel Partners, Small Business) |
| Country | País donde se realizó la venta |
| Product | Producto vendido |
| Discount Band | Rango de descuento aplicado (None, Low, Medium, High) |
| Units Sold | Unidades vendidas |
| Manufacturing Price | Costo de fabricación por unidad |
| Sale Price | Precio de venta por unidad |
| Gross Sales | Ventas brutas (antes de descuento) |
| Discounts | Monto descontado |
| Sales | Ventas netas |
| COGS | Costo de la mercadería vendida |
| Profit | Beneficio (Sales - COGS) |
| Date / Month Number / Month Name / Year | Dimensión temporal de cada operación |

> Punto de discusión: si Copilot se equivoca o generaliza mal alguna columna, es el momento de aplicar el "Protocolo de la verdad" — pedirle que lo revise contra los datos reales en vez de asumir que la primera respuesta es correcta.

---

## Parte 3 — Primera tabla dinámica, pedida por prompt

**Prompt:**
```
Necesito una tabla dinámica que muestre el Profit total por Country
y por Segment, con el total general y ordenada de mayor a menor.
Insertala en una hoja nueva.
```

Verificar en el resultado:
- ¿Generó una tabla dinámica real (editable, con lista de campos) o solo un resumen en texto/tabla estática?
- ¿Los totales cierran contra el total general de la columna Profit?
- ¿La ubicó en hoja nueva como se pidió?

---

## Parte 4 — Segunda tabla dinámica, con más variables

**Prompt:**
```
Ahora armá otra tabla dinámica: Sales totales por Product en filas,
por Year en columnas, y agregá el % que representa cada producto
sobre el total general.
```

Punto de discusión: esto es lo que en Excel manual sería "Mostrar valores como % del total general". Evaluar si Copilot lo resolvió bien sin que se lo expliquemos paso a paso, o si hubo que reformular el prompt.

---

## Parte 5 — Gráfico a partir de la tabla dinámica

**Prompt:**
```
A partir de la tabla dinámica de Profit por Country y Segment,
generame un gráfico de barras apiladas que la represente.
```

Comparar contra lo visto en el temario (Módulo 2.0: "Números que se explican solos: generación de gráficos dinámicos").

---

## Parte 6 — Proyección (dónde la IA necesita supervisión)

**Prompt:**
```
Proyectá el Profit del segmento Government para el próximo trimestre,
basándote en la tendencia histórica de los datos.
```

Punto de discusión obligatorio: pedirle a Copilot que explicite los supuestos usados (estacionalidad, si descartó outliers, qué método de proyección aplicó). Esta es la parte del laboratorio donde se muestra que la IA generativa no reemplaza el criterio humano: hay que revisar cómo llegó al número, no solo tomarlo.

---

## Parte 7 — Detección de anomalías

**Prompt:**
```
Revisá la columna Discount Band contra Sales y Profit: ¿hay
combinaciones donde el descuento aplicado no es coherente con el
resto de los datos, o casos que parezcan un error de carga?
```

Este ejercicio conecta con el caso de uso real de Finanzas (controles de consistencia) visto en la propuesta de Costa Oriental.

---

## Cierre

- ¿En qué paso Copilot resolvió más rápido que si lo hubieras hecho a mano?
- ¿En qué paso tuviste que reformular el prompt más de una vez?
- ¿En qué paso NO confiarías en el resultado sin revisarlo (Parte 6 y 7 suelen ser los candidatos)?
