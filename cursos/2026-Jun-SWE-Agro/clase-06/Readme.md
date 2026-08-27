# Clase Seis - 27 de Agosto del 2026

# Repaso

* Prompt Engineering
  * Tecnica personalizacion de salida
    * Graficos
        * Mermaid
          * Para generar graficos
          * Tienen generalmente previsualizacion
    * Codigo
        * Se lleva excelente con Python
        * Interprete de codigo en Python
            * Colab para ejecutar el codigo si el interprete no anda
        * HTML
          * Generamos un dashboard
          * Generamos PDFs con formatos
        * MatplotLib
    * Informacion Tabular
        * CSV
          * Es mucho mas eficiente para ver los datos que el excel
    * Markdown
        * Es el lenguaje que usa la IA para generar sus salidas
        * Generar plantillas de las respuestas con Markdown

---

# IA Responsable

* Los que usamos en clase son herramientas para uso particular / domestico
    * ChatGPR
    * Claude
    * Copilot <<< El principal que vimos

* En estas herramientas dejan guardadas las conversaciones
    * Las empresas pueden usar estas conversaciones para
        * Entrenar Modelos
        * Hacer Marketing
        * ...
    
* Esto traer aparejado bastantes cuestiones de privacidad de datos

> Hay que tener cuidado a la hora de utilizar datos sensibles / privados (de terceros) con los LLM domesticos

* Entonces no puedo usar LLM?
    * Todas las empresas tienen versiones individuales / empresariales
    * Cuando vos adquiris un plan empresarial hay un contrato donde las empresas te aseguran que no usan los datos ni para entrenar modelos, ni para marketing, ni nada raro...
    * La otra alternativa es tener instalado en mi empresa en una PC lo suficientemente potente (GPU) mi propia IA con modelo Open Source.

> [!NOTE]
> Ver la ley del GPRD en Europa como referencia para entender para donde va el mundo

---
      
# Prompt Engineering

## Few Shot Prompting

* La IA funciona muchisimo mejor si le doy ejemplos / especifico el criterio
* Vamos a hacer un ejemplo de clasificacion

* Sin la Tecnica (Zero-Shot)
  
```
Mira mis ultimos 20 correos y clasificalos en prioridad alta/media/baja
```

* Con la tecnica

```
Mira mis ultimos 20 correos y clasificalos en prioridad alta/media/baja
Ejemplos:
* Mail de MCT y Salud de mi mama ---> Prioridad Alta
* Mails de dar clases no mct, cuestiones laborales y de trabajo ---> Prioridad media
* Otros correos ---> Prioridad baja
```

## Cadena de Razonamiento (Chain of thoughts)

* 

---

# Agentes

## Proyecto 

