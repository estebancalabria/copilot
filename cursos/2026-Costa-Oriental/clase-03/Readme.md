# Clase Tres - 21 de Agosto del 2026

# Repaso

* Prompt Engenieering
  * Contexto
* Agentes
  * Invocar a un agente con el @
  * @Word, @Excel
* Copilot
  * Editar en Paginas
      * Es util
      * Cuando trabajo sobre un entregable (mail/informe/analisis) crear un draft/borrador y editarlo como paginas
      * Canvas / Artefacto
  * Generacion de Imagenes
  * Programacion de Prompts
      * Se integra muy bien con el agente preconfigurado "Investigador/Researcher"
      * Intereso mucho

# Agentes de 365

## Lineamientos generales

* Recomedacion
  * Cambio Cultura Organizacional : Para poder sacarle el maximo provecho a la herramientas de IA recomiento una sincronizacion via One Drive los documentos con los que se trabajan dia a dia para usarlos como contexto de la IA

## Excel

* Verificar la presencia del Agente e excel en la herramienta

* Descargar el excel desde : https://github.com/estebancalabria/copilot/blob/main/data/Financial%20Sample.xlsx

* IR a https://excel.cloud.microsoft/

  > [!WARN]
  > Este excel tiene 700 filaes. Para trabajar en excel es mas eficiente usar el agetne embebido. En la interfaz de copilot directamete adjuntar el excel y hacerle preguntas no me asegura que copilot lo procese entero. El analista en excel esta preparado para recorrer todo el document

* Cargar el documento en excel y abrir copilot

```
Explicame que contiene esta plantilla; que representa cada columna, que unididad de negocio describbe y que analisis puedo hacer con estos datos
```

* Caracteristicas del Chat
  * Elegir el modo de interaccion : Ask, Edit, Plan
  * Trabajar con OneDrive para cruzar facilmente excels u otros documentos
  * Conector con muchisimas herramientas

---
 
### Tablas Dinamicas (Pivot Tables)

* Generar una tabla dinamica
```
Necesito una tabla dinamica que muestre el Profit total por Country y por Segment, con el total generaly ordenada de mayor a menor. Insertarla en una hoja nueva.
```

* Generar otra tabla dinamica
```
Arma otra tabla dinamica: Sales totales por product en filas, por year en columnas y agrega el % que representa cada producto sobre el total general. Generame un libro nuevo con la nueva tabla
```

> [!NOTA]
> Vericar como al modificar los datos duros se modifcan el contenido de las tablas dinamicas

----

### Grafficos / Pivot Charts

* Generar un grafico

```
A partir de la tabla dinamica Profit por Pais y segmento generame un grafico de barras apilada que la represente. Incluir el grafico en un libro nuevo al lado del libro que tiene la tabla dinamica
```

* Generar otro grafico

```
A partir de la tabla dinamica de Sales por product y year, crea un grafico dinamico (PivotChart) de columnas agrupadas. Quiero que product este en el eje y year permita coparar la venta entre los disntintos anios. Generar un libro nuevo con el grafico
```

> [!NOTE]
> Distintos tipos de datos en Excel
> https://support.microsoft.com/en-us/Excel/available-chart-types-in-office

* Grafico Map Chart

```
Me podes agrupar las ventas por pais sacar el total de ventas por pais y mostrarlas en un libro nuevo en un map chart.
```
> [!NOTE]
> Este para mi caso, masomenos, a Fabiana le andubo mucho mejor

---

### Ciencia de Datos en Excel

* AKA: Proyecciones, MAchine Lerning

* Casos uso
  * Regresion / Proyeccion
  * Clasificacion
  * Deteccion de anomalias

> [!NOTE]
> Esta es la parte mas util del agente de excel, pero si es para revision

* Regresion / Proyeccion
```
En un libro nuevo proyecta el profit del segmento Goverment para el proximo trimestre basandote en la tendencia historica de los datos
```

 * Deteccion de anomalias
```
Revisa la columna Discount contra los Sales y Profit y busca combinaciones donde el descuento aplicado no es coherente con el resto de los datos, cosas que parezcan un error de carga. Generame un libro nuevo indicando la fila original donde se detecto la anomalia y pintame con color rojizo la fila con anomalia en los datos originales.
```

* Clasificacion
```
Clasifica cada operacion segun su nivel de rentabilidad, Alta, Media, Baja.  Utiliza Profit y el margen de rentabilidad (Profit / Sales) para definir la clasificacion. Explica que criterios y umbrales vas a  utilizar y luego agrega una columna "NivelRentabilidad" con la clasificacion y marcame con verde las columnas con clasificacion Alta
```

---

### Modo plan (Para pensar un problema)

* Ejecutar este prompt en el modo Plan
```
Analiza el dataset y proponeme 5 preguntas de negocio que consideres importante para responder con estos datos
Para cada pregunta decime que informacion usas, que analisis realizarias,  que visualizacion recomendarias, que decision de negocio podrian tomar. No modifiques el chiovo. Quiero revisar y ver el plan solamente
```

> [!NOTA]
> Este prompt vale oro y se puede reutilizar. Recomiendo tenerlo a mano

* Me arroja este informe
```
```
