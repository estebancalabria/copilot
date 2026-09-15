# Laboratorio 1 — De export crudo de WIS a tabla de equipos

## Objetivo

Que el participante entienda por qué el export de WIS separa la identificación de un equipo en tres lecturas independientes (Serial, IMEI, IMEI2), y que use Copilot para consolidarlas en una tabla de un renglón por equipo, con una validación de cantidad incorporada.

## Materiales del laboratorio

- **Pedido_RU_160.xlsx** — export crudo de WIS. Es el único archivo de trabajo del laboratorio; todo el ejercicio se resuelve sobre este Excel.
- Copilot con acceso al archivo (Excel con Copilot, o Copilot Chat con el documento adjunto).

> **Nota para el instructor:** el archivo contiene SSCC, GTIN e IMEI reales de un pedido de un cliente. Si el laboratorio se va a dictar a un grupo externo o se va a dejar como material descargable, conviene anonimizar los valores antes (reemplazar por SSCC/IMEI ficticios manteniendo la misma estructura).

## Contexto de negocio

Cada iPhone o iPad con línea celular tiene tres identificadores distintos:

- **Serial Number**: identifica la unidad física.
- **IMEI**: identifica el módem de la línea 1.
- **IMEI2**: identifica el módem de la línea 2 (son equipos dual SIM).

El fabricante imprime los tres en la etiqueta de la caja madre, alineados en tres columnas: la fila 1 de la columna de seriales corresponde al mismo equipo que la fila 1 de IMEI y la fila 1 de IMEI2. Es una alineación por posición, no un dato explícito — no hay ningún campo que diga "este serial va con este IMEI".

Cuando el operador recibe la mercadería, escanea esos tres bloques de códigos de barra por separado. WIS guarda cada escaneo como una lectura independiente atada al SSCC del pallet, sin unirlas en un registro por equipo. Eso es lo que se ve en el Excel: por cada pallet hay tres líneas sueltas (V3 = serial, V4 = IMEI, V6 = IMEI2), separadas por una fila vacía del siguiente pallet.

**Antes de abrir el Excel**, conviene mostrar esto con el caso real de Startech:

1. Mostrar la foto de la **etiqueta de envío de la caja** (SSCC, GTIN, Customer PO, cantidad de bultos declarada) para bajar el problema a algo tangible: esto no es un ejercicio abstracto, es una caja real que llegó a un depósito.
2. Cerrar con la foto de la **hoja de Serial Numbers / IMEI/MEID Numbers / IMEI2 Numbers** en tres columnas. Esta imagen confirma que la alineación por fila es la convención real del fabricante — no un supuesto inventado para este laboratorio, sino la misma lógica que hay que reconstruir en el Excel.

**Qué se quiere lograr:** una tabla con un renglón por equipo físico —SSCC, GTIN, MPN, Serial, IMEI, IMEI2— en vez de tres listas sueltas por pallet.

## Paso a paso

### Paso 1 — Reconocer el patrón en el archivo crudo

Abrir Pedido_RU_160.xlsx y señalar la estructura junto con el grupo:

- Cada pallet ocupa 3 líneas seguidas, separadas del siguiente pallet por una fila vacía.
- La línea que empieza con `V3` trae los 10 números de serie del pallet.
- La línea que empieza con `V4` trae los 10 IMEI.
- La línea que empieza con `V6` trae los 10 IMEI2.
- Las tres líneas repiten el mismo SSCC, GTIN, MPN y QTY del pallet al principio.

### Paso 2 — Redactar el prompt con contexto de negocio

La clave del paso es que el prompt no solo pida "ordename esto", sino que le dé a Copilot la regla de negocio completa:

```
Tengo un export de WIS con lecturas de recepción de equipos. Cada bloque de 3 líneas
corresponde a un mismo pallet: la línea V3 trae los números de serie, la línea V4 los
IMEI, la línea V6 los IMEI2, todas separadas por comas junto con el SSCC, GTIN, MPN y
QTY del pallet. Se asume que la posición de cada valor dentro de la lista corresponde
al mismo equipo físico (posición 1 de V3 = posición 1 de V4 = posición 1 de V6).

Armá una tabla con una fila por equipo, con columnas SSCC, GTIN, MPN, Serial, IMEI,
IMEI2. Antes de armarla, verificá que la cantidad de valores en V3, V4 y V6 coincida
entre sí y con el QTY declarado, y avisame si algún bloque no cierra.
```

### Paso 3 — Ejecutar y revisar el resultado

Correr el prompt en Copilot (Excel o Chat, con el archivo adjunto) y revisar con el grupo:

- ¿La tabla tiene un renglón por equipo (10 por pallet) y no por lectura?
- ¿Mantuvo correctamente el SSCC/GTIN/MPN de cada pallet en todos sus renglones?
- Pedirle que explique cómo hizo el cruce, para confirmar que aplicó la regla de posición y no inventó una relación.

### Paso 4 — Validar integridad de los datos

Revisar la respuesta a la verificación pedida en el prompt: ¿reportó algún pallet donde la cantidad de seriales, IMEI o IMEI2 no coincide con el QTY declarado? Si el archivo de ejemplo cierra perfecto, es un buen momento para preguntarle al grupo qué haría Copilot si no cerrara, y probar a mano rompiendo un dato (borrar un IMEI de un bloque) para ver si lo detecta.

### Paso 5 — Discusión de cierre

Pregunta para el grupo: ¿qué pasa si el orden de las tres listas no viniera garantizado por el fabricante o por WIS? El método funciona porque confiamos en una convención, no en una relación explícita en los datos. Vale la pena que el grupo lo diga en voz alta antes de llevarse el laboratorio como una receta automática.
