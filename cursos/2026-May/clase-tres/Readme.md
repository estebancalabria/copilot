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

# Glosario

* No Deterministicas
