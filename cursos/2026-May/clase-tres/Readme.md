# Clase Tres - 11 de Mayo del 2026

# Repaso

* Prompt Engimeering
  * Formula de Prompts = Tarea + Contexto + Rol + Ejemplo + Formato + Tono
  * Patrones de Prompting
    * Rol
    * Personalizacion de Salida
      * Html => Pdf
      * CSV => Interactuar con Planillas
      * JSON, XML = > Tecnicos

---

# Prompt Engineering

## Personakizacion de Salida : Markdown

* Problemas
  * Decile a la IA exactamente como quiero la salida
  * Definir un formato que se repete cuando copio el contenido a Word
* Solicion
 * Utilizar Markdown para definir una plantilla para la salida
    * https://es.wikipedia.org/wiki/Markdown

* Sin personalizacion de Salida
```
Dame una lista de los barrios de YerbaBuena tucuman.
```

* Plantilla

```
# Barrio

## Caracteristicas

* Poblacion : [POBBLACION ESTIMADA]
* Extension : [Extension ESTIMADA]
* Tipos de Viviendas :  [TIPOS VIVIENDA]
* Precio Metro Cuadrado : **[PRECIO ESTIMADA]**

## Lugares de Interes

* [Lugar 1]
* [Lugar 2]
*...
* [Lugar N]

* Descripcion

> [Descripcion del barrio]

```

* Puedo poner que lo interprete

```
Dame la lista de barrios tradicionales siguiendo esta plantilla "# Barrio

## Caracteristicas

* Poblacion : [POBBLACION ESTIMADA]
* Extension : [Extension ESTIMADA]
* Tipos de Viviendas :  [TIPOS VIVIENDA]
* Precio Metro Cuadrado : **[PRECIO ESTIMADA]**

## Lugares de Interes

* [Lugar 1]
* [Lugar 2]
*...
* [Lugar N]

* Descripcion

> [Descripcion del barrio]" Devolveme el contenido para copiar y pegar sin acotar nada mas. Dar valores estimados. No mostrar el markdown sino mostrarlo interpretado.
```

* Si lo copio al word me respeta titulo 1, bullets, etc

> Markdown es el lenguaje que ya utiliza la IA para generar las salidas con formato. Podemos aprovechar este formato tambien para darle indicaciones exactas a la IA como quiero la salida

---

# Personalizacion de Salida : Mermaid

* Problema
  * Como genero diagramas con la IA
* Solucion
  * Generar los diagramas utilizando el lenguaje mermaid
    * https://mermaid.live/edit

```
Actua como un experto en construccion y desarrollo de proyectos imbobiliarios. Generame un memaid que muestre un  gant de un proyecto de construccion donde tengo un terreno y quiero construir una casa. Tengo un terreno de 100 metros cuadrados. 
```

* Otro prompt : Flowchart

```
Busca informacion en internet. Queiro que me armes en mermaid un diagrama de flowchart con el organigrama de la empresa metrocubico.
```

* Otro Prompt : Pie

```
Dame un diagrama mermadi de tipo pie donde se vean los 5 barrios mas importantes de tucuman y el precio del metro cuadriado
```

---

# Herramientas de 365

# Excel

* Conceptos claves
  * Tabla dinamica (Pivot Table)
  * Grafico dinamico (Pivot Graph)
  * Segmentadores (Slicers)

* GEnerar un documento de Excel nuevo
* Abrir copilot

```
Generarme 100 filas con datos de prueba. Tengo una lista de todos los proyectos inmobiliarios en desarrollo en San Miguel de tucuman. Quiero ubicacion terreno (direccion), barrio, metros cuadrados, Pocentaje de finalizacion, costo actual, costo estimado, (Hay varios proyectos en cada barrio)
```

## Tablas Dinamicas (Pivot Table)

* Partir de los datos generados con Copilot pidamos una "pivot Table"

```
Generame una hoja nueva donde se vea una tabla dinamica (pivot table) para representar e interactuar con los datos
```

## Grafico Dinamico (Pivot Chart)

```
Generame una hoja nueva donde se vea un grafico dinamico (pivot Chart) para representar e interactuar con los graficos
```

## Dashboard

```
Crear un dashboard inmobiliario interactivo usando tablas dinamicas, graficos dinamicos y segementadores (slices)
```

---

# Agentes

## Agentes incoporados en 365 : Angente Analista

```
Haceme un analisis de todos los datos del doumento. Decime particularmente cuales son los proyectos que se estan yendo de control. Ademas de ellos quiero una analisis detallado de todo mi documento
```

* El agente analista tiene la capacidad de tomar documentos de excel y ejecutar codigo en python para hacer un analisis (tipo data science)

# Glosario

* No Deterministicas
