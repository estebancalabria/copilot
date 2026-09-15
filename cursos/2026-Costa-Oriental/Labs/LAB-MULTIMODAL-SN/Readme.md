# Laboratorio 2 — Lectura de números de serie por foto cuando el código de barras está dañado

## Objetivo

Que el participante use Copilot para transcribir series, IMEI e IMEI2 a partir de una foto (cuando el código de barras no se puede escanear), y aprenda a pedirle que señale baja confianza en vez de inventar un dígito.

## Materiales del laboratorio

- **Foto de la etiqueta de la caja** (envío a Startech: SSCC, GTIN, Customer PO, Ship Date, cantidad de bultos declarada).
- **Foto de la hoja de Serial Numbers / IMEI/MEID Numbers / IMEI2 Numbers** (tres columnas alineadas por fila).
- Copilot con capacidad de leer imágenes (Copilot Chat con la foto adjunta).

> **Nota para el instructor:** las fotos son de un cliente real (Startech) con SSCC e IMEI reales. Si el laboratorio se dicta a un grupo externo o queda como material descargable, conviene usar fotos anonimizadas o un mock antes de distribuirlo.

## Contexto de negocio

En recepción, lo normal es escanear el código de barras de la caja y que el sistema capture SSCC, GTIN, serial e IMEI automáticamente. El problema aparece cuando ese código de barras llegó dañado, arrugado o tapado por otra etiqueta (como pasó con el caso Startech) y no hay forma de escanearlo. Ahí la única opción es leer los datos a mano de la hoja impresa — algo lento y con riesgo de error si el operador transcribe un IMEI de 15 dígitos a ojo.

La alternativa es sacarle una foto a la hoja y que Copilot la transcriba. Esto reemplaza la lectura manual, pero no elimina el riesgo de error: ahora el riesgo pasa de "el operador transcribe mal un dígito" a "Copilot lee mal un dígito borroso y lo completa con uno plausible". Con un serial number un error así se nota rápido, pero con un IMEI un solo dígito mal leído genera un número que parece válido y no lo es — la línea deja de funcionar y nadie se entera hasta que el equipo se activa. Por eso el laboratorio no se trata solo de "que lea la foto", sino de que declare cuándo no está seguro en vez de arriesgar un dígito.

## Paso a paso

### Paso 1 — Presentar el escenario

Mostrar la foto de la etiqueta de la caja y explicar la situación: código de barras dañado o tapado, no se puede escanear, la caja trae declarados SSCC, GTIN, Customer PO y una cantidad de bultos (CTN: 10 of 10 / Count: 10).

### Paso 2 — Adjuntar las dos fotos y pedir transcripción + validación en un mismo prompt

Subir a Copilot Chat **las dos fotos juntas** — la etiqueta de la caja y la hoja de Serial/IMEI/IMEI2 — con un prompt que le pida usar una para controlar a la otra:

```
Adjunto dos fotos. La primera es la etiqueta de envío de una caja, que declara la
cantidad de equipos que debería contener (buscá campos como CTN o Count). La segunda
es una hoja con tres columnas: Serial Numbers, IMEI/MEID Numbers e IMEI2 Numbers,
donde cada fila corresponde a un mismo equipo (el serial de la fila 1 va con el IMEI
de la fila 1 y el IMEI2 de la fila 1).

Necesito que:
1. Leas la etiqueta de la caja y me digas qué cantidad de equipos declara.
2. Transcribas la hoja de series en una tabla con columnas Serial, IMEI, IMEI2,
   respetando el orden de las filas. Si algún dígito no se ve con claridad o el
   número te queda con una cantidad de caracteres distinta a la esperada (10 para
   Serial, 15 dígitos para IMEI e IMEI2), no lo completes a tu criterio: marcá esa
   celda como "revisar" en vez de inventar el dígito.
3. Compares la cantidad de filas de la tabla contra la cantidad declarada en la
   etiqueta y me digas si coinciden.
```

### Paso 3 — Revisar el resultado con el grupo

- ¿Leyó bien la cantidad declarada en la etiqueta de la caja?
- ¿Transcribió las 10 filas de la hoja de series?
- ¿Marcó alguna celda como "revisar"? Si no marcó ninguna, preguntarle directamente cuán segura está de cada IMEI, para ver si al insistir cambia de opinión — es una forma de mostrar que la confianza declarada no siempre es estable.
- ¿El propio Copilot reportó si la cantidad transcripta coincide con la declarada? Si no coincide, hay que decidir si falta una fila en la foto o si Copilot descartó alguna por baja confianza — dos causas distintas que requieren acciones distintas.
- Comparar a ojo un par de valores contra la foto para confirmar que no hay errores silenciosos que Copilot no haya señalado.

### Paso 4 — Discusión de cierre

Preguntas para el grupo:

- ¿Qué proceso debería existir para las celdas marcadas como "revisar"? (por ejemplo, doble chequeo manual antes de cargar el dato al sistema).
- Este método es un parche para cuando falla el escaneo normal, no un reemplazo. ¿En qué otros puntos de la recepción convendría seguir escaneando en vez de fotografiar?
