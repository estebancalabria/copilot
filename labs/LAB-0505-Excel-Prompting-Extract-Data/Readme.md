# Laboratorio — De la Factura Comercial al Reporte de Control Mensual

**Caso de uso (hoja ADM Logística):** *"Conversión de documentos a Excel y/o generar reportes"*
**Técnica:** Prompt engineering

## Contexto

Administración Logística recibe periódicamente facturas comerciales y packing lists de distintos proveedores, cada uno con su propio formato, y necesita volcar esos datos a una planilla para poder trabajarlos, además de armar un resumen para elevar a un responsable. Hoy eso se hace a mano: alguien abre cada documento y tipea los datos.

En este laboratorio vas a usar prompt engineering para resolver exactamente eso: convertir documentos con formato variable en un Excel estructurado, y generar un reporte a partir de esos datos — sin escribir una sola línea de código.

## Objetivo

Al finalizar este laboratorio vas a poder:
- Extraer datos estructurados desde documentos no tabulares (PDF) usando un prompt bien especificado.
- Consolidar información proveniente de múltiples fuentes con formatos distintos entre sí, en un único archivo Excel.
- Generar un reporte ejecutivo a partir de datos ya procesados.

## Materiales

- 3 facturas comerciales / packing lists en PDF (ya las tenés):
  - `doc1_commercial_invoice_shenzhen.pdf` — Shenzhen Top Textiles Co., Ltd.
  - `doc2_invoice_packing_americanautoparts.pdf` — American Auto Parts Corp.
  - `doc3_factura_industrias_metalicas.pdf` — Industrias Metálicas del Sur S.A.
- Copilot (o la herramienta de IA que uses en el curso) con capacidad de leer archivos adjuntos y generar archivos descargables

> Nota: los tres documentos representan proveedores distintos, con estructura y presentación diferente entre sí — a propósito, para que el ejercicio de extracción no sea un simple copiar y pegar.

---

## Paso 1 — Extracción a Excel

Subí los tres PDF a la conversación y pedile a la IA que extraiga los datos a un archivo Excel con columnas fijas.

**Prompt sugerido:**

```
Extraé los datos de las 3 facturas adjuntas en una única tabla, con exactamente
estas columnas: Documento de origen, Proveedor, SKU, Descripción, Cantidad,
Peso total (kg), Precio FOB unitario (USD), Total FOB (USD).

Si algún dato no está declarado en el documento, dejá la celda vacía y no
inventes ni estimes el valor.

Generame el resultado como un archivo Excel (.xlsx) descargable, con los
encabezados en la primera fila. No lo muestres solo como texto en el chat.
```

**Punto de discusión:** notá que el prompt es explícito en cuatro cosas: (1) nombra cada columna exacta, (2) da una instrucción clara para datos faltantes ("no inventes"), (3) especifica que el resultado tiene que ser un archivo descargable —no una tabla pegada en el chat— y (4) el formato de ese archivo. Sacá cualquiera de esas partes y probá de nuevo — vas a ver cómo cambia (o falla) el resultado. Si la herramienta que usás no genera archivos directamente (por ejemplo, un chat de solo texto), pedí el resultado en formato CSV y guardalo vos como `.csv`, que Excel abre sin problema.

**Resultado esperado:** un archivo Excel con 15 filas (5 ítems x 3 documentos).

---

## Paso 2 — Reporte ejecutivo

Con el Excel ya generado, pedile un reporte de una página que resuma la operativa del mes.

**Prompt sugerido:**

```
Con los datos del Excel generado en el paso anterior, redactá un reporte
ejecutivo de una página para elevar al responsable de Administración
Logística. Debe incluir:
1. Cantidad de documentos procesados y proveedores involucrados.
2. Peso total y monto total FOB del mes, discriminado por proveedor.
3. Un párrafo de cierre con la conclusión general de la operativa.

Usá un tono formal y directo, sin tecnicismos innecesarios.

Generame el resultado como documento Word (.docx) descargable, listo para
enviar por correo.
```

**Resultado esperado:** un documento Word de una página, con las cifras derivadas correctamente del Excel del Paso 1 (no inventadas ni recalculadas de memoria).

---

## Cierre y reflexión

- ¿Qué pasó cuando le diste al modelo instrucciones vagas en el Paso 1 (por ejemplo, "extraeme los datos de las facturas") en vez del prompt estructurado? Probalo y compará.
- Revisá el Excel generado línea por línea contra los PDF originales: ¿hay algún dato mal extraído o mal interpretado?
- Pensá en un documento real que manejes en tu trabajo (no necesariamente una factura) al que le podrías aplicar este mismo esquema de dos pasos: extracción a Excel → reporte.

---

## Extensión opcional — Otro caso de uso: controles de Finanzas

Los tres PDF que usaste tienen, a propósito, dos inconsistencias insertadas: un ítem sin peso declarado (batería 12V, documento de American Auto Parts) y un precio FOB fuera de rango (bulones M12, documento de Industrias Metálicas del Sur). No hace falta usarlas para este laboratorio — pertenecen a otro caso de uso del relevamiento, el de **controles automáticos de Finanzas** (concordancia VIA/DUA, operativas masivas, volumen marítimo, variaciones de cadastro).

Si querés explorar ese caso de uso por separado, con el Excel del Paso 1 como insumo, el prompt sería:

```
Revisá la tabla y marcá cualquier ítem que presente una posible
inconsistencia: datos faltantes, peso en cero, o un precio FOB unitario
que se aparte significativamente del resto de los ítems similares.
Para cada anomalía, explicá brevemente por qué la marcaste.
```

Pero tratalo como un laboratorio aparte, no como parte de este.
