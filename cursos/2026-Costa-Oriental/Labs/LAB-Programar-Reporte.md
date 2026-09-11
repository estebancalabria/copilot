# Laboratorio: Reportes automáticos con Scheduled Prompts de Copilot

## Paso 1
Enviar un mail con el subject **"RV: PROGRAMACION 01-09-2026"** y citar el contenido:

> Buenas Tardes chicos,
> Para mañana nos estaría faltando los PL de:

| | | | | |
|---|---|---|---|---|
| EMZ | 578067 | INTERNATIONAL | 28 | 32 |
| EMZ | 578067 | INTERNATIONAL | 4 | |
| EMZ | 578087 | INTERNATIONAL | | 2 |
| EMZ | | SIEA | | |
| EMZ | | SIEA | | |
| EMZ | 577609 | FIVISA | | 10 |
| EMZ | | SONY | | |
| EMZ | 578066 | STRTECH | | 1 |
| EVI | 106796 | INTERNATIONAL | | 3 |
| EVI | 106799 | INTERNATIONAL | | 4 |
| EMZ | 577945 | GRAPHTEC | | 16 |
| EMZ | 578008 | BRAY | | 1 |

> Muchas gracias!!

## Paso 2
Enviar un mail con el subject **"RV: PROGRAMACION 02-09-2026"** y citar el contenido:

> Buenas tardes!
> Les pido nos envíen los PL

| | | | | | |
|---|---|---|---|---|---|
| EMZ | 578143 | INTERNATIONAL | | 797 | 1 |
| EMZ | | SIEA | | | |
| EMZ | 578017 | CARLA BESOLA PAOLINO | | 143691 | 2 |
| EMZ | 577950 | EXPEDITORS - ZOETIS | | 143679 | 3 |

> Muchas gracias!

## Paso 3
Enviar un mail con el subject **"Re: PROGRAMACION 03-09-2026"** y citar el contenido:

> Buenas tardes,
> Para mañana estaría faltando solamente un PL:
>
> 578050
> GRAPHTEC
>
> Saludos!

## Paso 4
Enviar un mail con el subject **"Re: PROGRAMACION 04-09-2026"** y citar el contenido:

> Buenas tardes,
> Les dejo el listado de los PL necesarios para mañana:
>
> 578302 INTERNATIONAL
> 578141 CENTRO DIST. MITUTOYO
> 578130 SONY UY
> 577693 ARUGUAY S.A. - PY
> 578090 INTERNATIONAL
>
> Gracias,
> Saludos!

## Paso 5
Probar el siguiente prompt directamente en el chat de Copilot:

> Analizá los correos cuyo asunto contenga el texto "PROGRAMACION DD-MM-AAAA" (incluidas las variantes con prefijo "RV:" o "Re:") y considerá únicamente aquellos cuya fecha en el asunto corresponda a la semana calendario anterior.
>
> De esas conversaciones, tomá la respuesta del equipo de Control de Inventarios que informa los packings pendientes de envío a Zona.
>
> Generá un reporte consolidado con: fecha de programación, número de packing, cliente/observación informada y cantidad de veces que cada packing aparece durante la semana. Ordená los resultados por fecha.

## Paso 6
Pasar el mouse por arriba del prompt ejecutado en el paso anterior y seleccionar la opción para programarlo (Schedule this prompt).

## Paso 7
Completar la configuración de la programación (frecuencia semanal, día y hora) y guardar.
