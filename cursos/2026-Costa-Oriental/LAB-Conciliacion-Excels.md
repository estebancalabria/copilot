# Laboratorio: Compilación Inteligente de Facturación con Microsoft 365 Copilot Analyst

## Objetivo

Utilizar Microsoft 365 Copilot Analyst para analizar un archivo Excel que contiene información proveniente de múltiples sistemas, interpretar reglas de negocio expresadas en lenguaje natural y generar una propuesta de **FACTURA COMPILADA** lista para revisión por el área de Finanzas.

Este laboratorio busca responder una pregunta concreta:

> ¿Puede Analyst comprender un proceso de facturación complejo, identificar reglas de cálculo, cruzar información entre fuentes y construir automáticamente un reporte consolidado?

---

# Escenario de Negocio

Costa Oriental recibe mensualmente información operativa proveniente de Zonamerica.

La información descargada no puede utilizarse directamente para emitir una factura, ya que existe un contrato particular que establece:

- descuentos específicos;
- porcentajes de facturación diferentes según el servicio;
- prorrateos;
- validaciones;
- cruces con información complementaria;
- correcciones de datos.

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

- Movimientos
- Recargo p/doc.T
- Transformacione
- VERIF.MATRIZ RI
- Estac.playa int
- Habilitación
- Ingreso B/uso
- Egreso paq.pequ

---

### Bajada Wiki

Reporte utilizado como fuente complementaria.

Contiene información que puede no estar disponible en ZA o que debe utilizarse para validar datos.

---

### Premisas del proceso

Documento funcional donde se describen las reglas de negocio que deben aplicarse para generar la factura.

---

# Estructura de los Datos de Entrada

## Hoja: Bajada ZA

Representa la fuente principal de información.

### Campos relevantes

| Campo | Descripción |
|---------|---------|
| Cliente | Cliente informado originalmente |
| Nombre Cliente | Descripción del cliente |
| Fecha | Fecha de la operación |
| Nro.Orden | Número de orden |
| Nro.Orden Asoc. | Orden relacionada |
| Código | Código del servicio |
| Servicio | Servicio realizado |
| Dua | Identificador DUA |
| Importe Dua | Valor asociado al DUA |
| Importe | Importe original informado |
| Cantidad | Cantidad registrada |
| Observaciones | Información complementaria |
| Detalle | Información de detalle |
| Verificador Principal | Responsable de la operación |
| Empresa | Empresa asociada |
| Tipo Operativa | Tipo de operativa |
| Numero | Número de operativa |
| Clase | Clasificación |
| DUA | DUA alternativo |

---

## Hoja: Bajada Wiki

Se utiliza como fuente secundaria para enriquecer y validar información.

### Campos relevantes

| Campo | Descripción |
|---------|---------|
| Dua 6 dig | Clave de cruce |
| Tipo | Tipo de operación |
| Operativa | Operativa asociada |
| Numero | Número de operación |
| Cliente | Cliente asociado |
| Usuaria | Empresa asociada |
| Orden | Referencia operativa |
| DUA | Número completo de DUA |

---

# Reglas de Negocio

Analyst debe identificar e interpretar las reglas descritas en la hoja **Premisas del proceso**.

## Reglas generales

- Crear una nueva hoja denominada **FACTURA COMPILADA**.
- Agregar dos ceros al código de cliente proveniente de ZA.
- Convertir todos los importes calculados a USD utilizando el tipo de cambio almacenado en `Bajada ZA!F1`.
- Generar una columna DUA de 6 dígitos.
- Generar un identificador concatenando diversos campos de la operación.
- Completar información faltante utilizando la hoja Wiki.
- Validar clientes contra Wiki.

---

## Reglas por servicio

### Egreso paq.pequ

- Utilizar el importe original sin modificaciones.

### Estac.playa int

- Aplicar el 70% del importe original.
- Si el importe es cero, distribuir el valor entre registros relacionados.

### Habilitación

- Utilizar el importe original.
- Si el importe es cero, realizar prorrateo entre registros relacionados.

### Ingreso B/uso

- Utilizar el importe original.

### Mov.de vehículo

- Utilizar el importe original.

### Movimientos

- Sumar todos los importes de Movimientos.
- Aplicar un descuento del 7%.
- Dividir el resultado entre la cantidad total de registros Movimientos.
- Asignar el resultado a cada registro de Movimientos.

### Recargo p/doc.T

- Comparar la cantidad de registros contra la cantidad de Movimientos.
- Si representan menos del 30%:
  - asignar importe cero.
- Si superan el 30%:
  - aplicar el 70% del total.
  - distribuir entre todas las filas del servicio.

### Transformacione

- Aplicar el 50% del importe original.

### VERIF.MATRIZ RI

- Utilizar el importe original.

### Verific.extendi

- Utilizar el importe original.
- Si el importe es cero:
  - agrupar operaciones relacionadas.
  - distribuir el importe entre las filas correspondientes.

---

## Reglas de Conversión

### Conversión a USD

Todos los importes contractuales deben convertirse a dólares.

Fórmula conceptual:

```text
Importe USD =
Importe Contractual
/
Tipo de Cambio
```

---

### DUA de 6 dígitos

Debe construirse una nueva columna:

- tomar los últimos 6 dígitos de la columna Dua;
- si no existe valor, utilizar la columna DUA.

Ejemplo:

```text
22026546249
```

Resultado:

```text
546249
```

---

### Enriquecimiento desde Wiki

Si una fila posee información faltante:

- completar Tipo Operativa;
- completar Número de Operativa;
- validar Cliente.

---

### Validación de Cliente

Cuando el cliente obtenido desde Wiki sea diferente al cliente de ZA:

- conservar el valor proveniente de Wiki.

---

# Propuesta de Estructura de Salida

El documento original no define explícitamente la estructura de FACTURA COMPILADA.

Como parte del laboratorio, Analyst deberá proponer una estructura consistente con todas las reglas encontradas.

Se propone la siguiente:

| Campo | Origen |
|---------|---------|
| Cliente Original | ZA |
| Cliente Final | ZA + Wiki |
| Nombre Cliente | ZA |
| Fecha | ZA |
| Nro.Orden | ZA |
| Servicio | ZA |
| DUA Original | ZA |
| DUA 6 Dígitos | Calculado |
| Tipo Operativa | ZA / Wiki |
| Número Operativa | ZA / Wiki |
| Importe Original | ZA |
| Regla Aplicada | Calculado |
| Importe Contractual | Calculado |
| Tipo de Cambio | ZA |
| Importe USD | Calculado |
| Identificador Factura | Calculado |
| Estado de Validación | Calculado |

---

# Actividad

## Paso 1

Abrir Microsoft 365 Copilot.

Seleccionar:

```text
Analyst
```

---

## Paso 2

Cargar el archivo:

```text
Control de Inventario - Factura.xlsx
```

---

## Paso 3

Solicitar el análisis general del proceso.

### Prompt

```text
Analiza el archivo Excel.

Identifica:
- las hojas disponibles;
- el propósito de cada una;
- las fuentes de entrada;
- las reglas de negocio.

Resume el proceso de negocio que intenta resolver este archivo.
```

---

## Paso 4

Solicitar la extracción de reglas.

### Prompt

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

## Paso 5

Solicitar el análisis operativo.

### Prompt

```text
Calcula la cantidad de registros existentes por tipo de servicio en la hoja Bajada ZA.

Presenta los resultados ordenados de mayor a menor.
```

---

## Paso 6

Validar una regla contractual real.

### Prompt

```text
Analiza la regla correspondiente a Recargo p/doc.T.

Calcula:

- cantidad de registros Recargo p/doc.T;
- cantidad de registros Movimientos;
- porcentaje resultante.

Determina si corresponde asignar importe cero y explica el cálculo.
```

---

## Paso 7

Diseñar la salida.

### Prompt

```text
Basándote en todas las reglas identificadas, propone la estructura de una hoja FACTURA COMPILADA.

Justifica cada columna propuesta indicando:
- origen del dato;
- finalidad;
- regla asociada.
```

---

## Paso 8

Generar la factura compilada completa.

### Prompt

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

---

## Paso 9

Validar el resultado.

### Prompt

```text
Resume:

- cantidad total de registros procesados;
- cantidad de clientes corregidos;
- cantidad de registros completados desde Wiki;
- excepciones encontradas;
- reglas ambiguas detectadas.
```

---

# Resultado Esperado

Al finalizar el laboratorio, Analyst debería ser capaz de:

✅ Comprender un proceso de facturación documentado en lenguaje natural.

✅ Interpretar reglas complejas por tipo de servicio.

✅ Cruzar información entre múltiples fuentes.

✅ Detectar inconsistencias y ambigüedades.

✅ Proponer una estructura de factura consolidada.

✅ Generar una FACTURA COMPILADA aplicando todas las reglas identificadas.

✅ Explicar cómo se obtuvo cada resultado.

---

# Conclusión

Este laboratorio demuestra cómo Microsoft 365 Copilot Analyst puede actuar como un analista financiero digital capaz de:

- interpretar documentación funcional;
- comprender reglas contractuales;
- enriquecer datos desde múltiples fuentes;
- construir reportes consolidados;
- documentar excepciones y ambigüedades;
- asistir en procesos de facturación complejos con trazabilidad y explicabilidad.
