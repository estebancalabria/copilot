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

# LLM

## Alucinacione

* Tipos de Alucinaciones
  * IA Inventa
     * Ejemplo Real: Un abogado quiso hacer un alegato y la IA hizo un alegato magnifico pero invento jurisprudencia
     * https://metajuridico.com/alucinaciones-ia-derecho-argentino-casos-reales/
     * LA IA interpreto que el usuario queria un ejemplo de alegato bien escritp pero que no era la idea ver que las fuentes sean veridicas
     * A veces la IA te da una respuesta generica y correcta pero que no aplica al caso
  
  * Asume datos que no son correctos / actualizados
     * La respuesta de las IA si no busca en internet se basan en su entrenamiento\
     * Los datos de entrenamiento son de internet y tienen sesgos, errores, inconsistencias, etc
     * Cuando la IA usa su conocimiento puede equivorcarse porque los teras de datos que se usaron para entrenarla pueden tener sus cositas
     * Para evitar esto hay que hacer Grounding
       * Adjuntar archivos con datos que sabes que esta bien
       * Crear un agente con grandes datos de fuente de informacion confiable
       * Especificarle a la IA los recursos web que queres que utilice
  
  * Comete errores de Razonamiento
      * Ejemplo
         * "Tengo que ir a lavar el auto. El lavadero queda a dos cuadras. Me conviene ir en auto o caminando"
         * Obviamente voy a ir en auto, pero la ia respondia que vayas caminando porque es mas cerca
         * Con respecto a esto en general los van corrigiendo y la IA se esta volviendo mas capaz, sobre todo en temas matematicos y de logica donde al principio hacia bastante agua
      
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

* Consiste en decirle a la IA que no me de una respuesta directamente sino que explique su razonamiento
   * Al pedirle esto a la IA primero entiendo mejor en que basa su respuesta
   * Muchas veces si le  pido la respuesta directa comete un error (de razonamiento) pero al pedirle que explique el razonamiento da una respuesta correcta
 
> Esto se venia bien (ahora la Ia ya lo hace bien de primera) con el problema del asesino

* Sin la tecnica

```
En una habitacion hay 3 personas. Uno de ellos es un asesino. Entra una persona nueva a la habitacion y mata al asesino. Cuantos asesinos vivos quedan?
```

> La IA deberia responder 1, pero respondia 0

* Con la tecnica
  
```
En una habitacion hay 3 personas. Uno de ellos es un asesino. Entra una persona nueva a la habitacion y mata al asesino. Cuantos asesinos vivos quedan?. Explicame en detalle paso a paso tu razonamiento y como llegas a la conclusion
```

> Si se lo pedia asi a la IA entonces me daba 1

* Ver noticia de deepseek y china como inventaron el modo "pensamiento profundo" que ahora lo tienen todos y en copilot se llama "Smart"
   * https://moderndiplomacy.eu/2026/02/24/chinas-deepseek-trains-ai-on-u-s-nvidia-chip-despite-export-ban/
* No es para usar siempre ya que todo el razonamiento consume muchos tokens

---

# Agentes

* Al principio hablabamos de LLM en mundo de la IA pero a medida que los usabamos fuimos descubriendo sus limitaciones

* Se les fue inforporando a los LLM caracteristicas agenticas

Angente = LLM + Herramientas (capacidad de buscar web) + Base de Conocimiento (RAG) + System prompt esepcifico

* Podemos decir que un LLM esta pensado para uso genera, mientras que un agente esta especializado en una tarea particular
   * Agente de soporte tecnico
   * Agente de ventas
   * Agente atonomo que busca prospectos en internet

> En la version gratuita de copilot no puedo crear agetnes, lo mas parecido son los proyectos que vamos a ver (una aproximacion)

## Proyecto 

* Vamos a hacer una aproximacion a un agente con un proyecto en la version de copilot individual o nuevo agente en la version de 365
* Usamos estas drecciones como fuentes de informacion:

```
https://raw.githubusercontent.com/estebancalabria/copilot/refs/heads/main/cursos/2026-Jun-SWE-Agro/clase-01/Readme.md
https://raw.githubusercontent.com/estebancalabria/copilot/refs/heads/main/cursos/2026-Jun-SWE-Agro/clase-02/Readme.md
https://raw.githubusercontent.com/estebancalabria/copilot/refs/heads/main/cursos/2026-Jun-SWE-Agro/clase-03/Readme.md
https://raw.githubusercontent.com/estebancalabria/copilot/refs/heads/main/cursos/2026-Jun-SWE-Agro/clase-04/Readme.md
https://raw.githubusercontent.com/estebancalabria/copilot/refs/heads/main/cursos/2026-Jun-SWE-Agro/clase-05/Readme.md
https://raw.githubusercontent.com/estebancalabria/copilot/refs/heads/main/cursos/2026-Jun-SWE-Agro/clase-06/Readme.md
```

* Lo mas parecido a esto es notebooklm
  * https://notebook.google.com/
