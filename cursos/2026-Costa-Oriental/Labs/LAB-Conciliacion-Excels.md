# Laboratorio: Compilación Inteligente de Facturación con Microsoft 365 Copilot Analyst

## Objetivo

Utilizar Microsoft 365 Copilot Analyst para analizar un archivo Excel que contiene información proveniente de múltiples sistemas, interpretar reglas de negocio expresadas en lenguaje natural y generar una propuesta de **FACTURA COMPILADA** lista para revisión por el área de Finanzas.

Este laboratorio busca responder una pregunta concreta:

> ¿Puede Analyst comprender un proceso de facturación complejo, identificar reglas de cálculo, cruzar información entre fuentes y construir automáticamente un reporte consolidado?

---

# Escenario de Negocio

Costa Oriental recibe mensualmente información operativa proveniente de Zonamerica.

La información descargada no puede utilizarse directamente para emitir una factura, ya que existe un contrato particular que establece:

* descuentos específicos;
* porcentajes de facturación diferentes según el servicio;
* prorrateos;
* validaciones;
* cruces con información complementaria;
* correcciones de datos.

Actualmente estas tareas se realizan manualmente.

El objetivo es evaluar si Analyst es capaz de comprender el proceso y generar automáticamente una propuesta de factura compilada.

---

# Archivo Utilizado

## Control de Inventario - Factura.xlsx

El archivo contiene tres hojas:

### Bajada ZA

Reporte operativo descargado desde Zonamerica.

Contiene el detalle de todos los servicios realizados durante el período.

Ejemplos de servicios:

* Movimientos
* Recargo p/doc.T
* Transformacione
* VERIF.MATRIZ RI
* Estac.playa int
* Habilitación
* Ingreso B/uso
* Egreso paq.pequ

### Bajada Wiki

Reporte utilizado como fuente complementaria.

Contiene información que puede no estar disponible en ZA o que debe utilizarse para validar datos.

### Premisas del proceso

Documento funcional donde se describen las reglas de negocio que deben aplicarse para generar la factura.

---

# Estructura de los Datos de Entrada

## Hoja: Bajada ZA

Representa la fuente principal de información.

| Campo                 | Descripción                     |
| --------------------- | ------------------------------- |
| Cliente               | Cliente informado originalmente |
| Nombre Cliente        | Descripción del cliente         |
| Fecha                 | Fecha de la operación           |
| Nro.Orden             | Número de orden                 |
| Nro.Orden Asoc.       | Orden relacionada               |
| Código                | Código del servicio             |
| Servicio              | Servicio realizado              |
| Dua                   | Identificador DUA               |
| Importe Dua           | Valor asociado al DUA           |
| Importe               | Importe original informado      |
| Cantidad              | Cantidad registrada             |
| Observaciones         | Información complementaria      |
| Detalle               | Información de detalle          |
| Verificador Principal | Responsable de la operación     |
| Empresa               | Empresa asociada                |
| Tipo Operativa        | Tipo de operativa               |
| Numero                | Número de operativa             |
| Clase                 | Clasificación                   |
| DUA                   | DUA alternativo                 |

## Hoja: Bajada Wiki

Se utiliza como fuente secundaria para enriquecer y validar información.

| Campo     | Descripción            |
| --------- | ---------------------- |
| Dua 6 dig | Clave de cruce         |
| Tipo      | Tipo de operación      |
| Operativa | Operativa asociada     |
| Numero    | Número de operación    |
| Cliente   | Cliente asociado       |
| Usuaria   | Empresa asociada       |
| Orden     | Referencia operativa   |
| DUA       | Número completo de DUA |

---

# Reglas de Negocio

Analyst debe identificar e interpretar las reglas descritas en la hoja **Premisas del proceso**:

* Crear una nueva hoja denominada **FACTURA COMPILADA**.
* Agregar dos ceros al código de cliente proveniente de ZA.
* Convertir los importes calculados a USD utilizando el tipo de cambio almacenado en `Bajada ZA!F1`.
* Generar el **DUA de 6 dígitos** tomando los últimos 6 dígitos de `Dua`; si no existe, utilizar `DUA`.
* Generar un identificador concatenando los campos definidos por el proceso.
* Completar desde Wiki los datos faltantes de **Tipo Operativa** y **Número de Operativa**.
* Validar el **Cliente** contra Wiki y conservar el valor de Wiki cuando sea diferente al de ZA.
* Para **Egreso paq.pequ**, utilizar el importe original.
* Para **Estac.playa int**, aplicar el 70% del importe; si es cero, prorratear entre los registros relacionados.
* Para **Habilitación**, utilizar el importe original; si es cero, prorratear entre los registros relacionados.
* Para **Ingreso B/uso** y **Mov.de vehículo**, utilizar el importe original.
* Para **Movimientos**, sumar los importes, aplicar un descuento del 7%, dividir el resultado entre la cantidad de registros y asignarlo a cada registro.
* Para **Recargo p/doc.T**, comparar su cantidad de registros con la de Movimientos: si representa menos del 30%, asignar importe cero; si supera el 30%, aplicar el 70% del total y distribuirlo entre sus registros.
* Para **Transformacione**, aplicar el 50% del importe original.
* Para **VERIF.MATRIZ RI**, utilizar el importe original.
* Para **Verific.extendi**, utilizar el importe original; si es cero, agrupar las operaciones relacionadas y distribuir el importe entre las filas correspondientes.
* Convertir cada **Importe Contractual** a USD mediante `Importe Contractual / Tipo de Cambio`.
* Marcar como **REVISAR** cualquier caso en el que las reglas no permitan determinar el resultado sin inventar información.

---

# Actividad

## Paso 1 — Analizar el archivo

Abrir Microsoft 365 Copilot y seleccionar **Analyst**.

Cargar el archivo:

```text
Control de Inventario - Factura.xlsx
```

Utilizar el siguiente prompt:

```text
Analiza el archivo Excel.

Identifica:
- las hojas disponibles;
- el propósito de cada una;
- las fuentes de entrada;
- las reglas de negocio.
```

---

## Paso 2 — Identificar las reglas de negocio

Utilizar el siguiente prompt:

```text
Analiza la hoja "Premisas del proceso".

Identifica todas las reglas de negocio.

Clasifícalas en:
- reglas generales;
- reglas por servicio;
- reglas de validación;
- reglas de integración con Wiki.
```

---

## Paso 3 — Diseñar la estructura del Excel unificado

Utilizar el siguiente prompt:

```text
¿Cuál sería la estructura propuesta del Excel unificado resultante?
```

Analyst deberá proponer las columnas necesarias para consolidar la información de las diferentes fuentes y aplicar las reglas identificadas.

---

## Paso 4 — Generar la factura compilada

Utilizar el siguiente prompt:

```text
Genera la hoja FACTURA COMPILADA completa.

Para cada registro:

- aplica las reglas contractuales identificadas;
- calcula el Importe Contractual;
- calcula el Importe USD;
- genera el DUA de 6 dígitos;
- completa datos faltantes desde Wiki;
- valida el cliente contra Wiki;
- registra qué regla fue aplicada.

Si encuentras ambigüedades, márcalas como REVISAR sin inventar información.
```

El resultado debe ser una hoja **FACTURA COMPILADA** que consolide la información de las fuentes y aplique las reglas de negocio identificadas.

---

## Paso 5 — Generar una herramienta reutilizable

Una vez generado el resultado, solicitar a Analyst que transforme el proceso en una herramienta que pueda utilizarse nuevamente con nuevos archivos Excel.

Utilizar el siguiente prompt:

```text
A partir del análisis realizado y de las reglas de negocio identificadas, genera un archivo HTML autocontenido y descargable que permita reproducir este proceso.

La herramienta debe:

- permitir al usuario cargar un archivo Excel con la estructura de entrada utilizada en este laboratorio;
- leer las hojas Bajada ZA, Bajada Wiki y Premisas del proceso;
- aplicar las reglas de negocio identificadas;
- generar la hoja FACTURA COMPILADA con la misma estructura y lógica definida en este laboratorio;
- realizar los cálculos, cruces, validaciones, prorrateos y conversiones a USD;
- identificar y marcar como REVISAR los registros que presenten ambigüedades o datos insuficientes;
- permitir descargar el resultado como un archivo Excel.

El HTML debe funcionar directamente desde el navegador, sin necesidad de instalar Python, Node.js ni otro software.

Incluye una interfaz sencilla para:

1. cargar el archivo Excel;
2. ejecutar el procesamiento;
3. visualizar un resumen de los resultados;
4. descargar el Excel generado.

Utiliza únicamente procesamiento local en el navegador. No envíes los datos del archivo a servicios externos.

Entrega el HTML como un archivo descargable y verifica que el código generado sea funcional.
```

El objetivo de este paso es obtener una herramienta que permita **reutilizar el proceso con nuevos archivos**, sin tener que repetir manualmente los prompts del laboratorio.

---

# Resultado Esperado

Al finalizar el laboratorio, Analyst debería ser capaz de:

* Comprender un proceso de facturación documentado en lenguaje natural.
* Interpretar reglas complejas por tipo de servicio.
* Cruzar información entre múltiples fuentes.
* Detectar inconsistencias y ambigüedades.
* Proponer una estructura de Excel unificado.
* Generar una **FACTURA COMPILADA** aplicando las reglas identificadas.
* Documentar qué regla fue aplicada a cada registro.
* Marcar para revisión los casos que no puedan resolverse de forma confiable.
* Generar una herramienta HTML reutilizable para automatizar el proceso con nuevos archivos.

---

# Conclusión

Este laboratorio demuestra cómo Microsoft 365 Copilot Analyst puede pasar de **analizar información y aplicar reglas de negocio** a **generar una solución reutilizable para automatizar el proceso**.

El flujo completo permite:

* interpretar documentación funcional;
* comprender reglas contractuales;
* combinar información de múltiples fuentes;
* construir un reporte consolidado;
* documentar excepciones y ambigüedades;
* generar una **FACTURA COMPILADA**;
* transformar el proceso en una herramienta reutilizable.
