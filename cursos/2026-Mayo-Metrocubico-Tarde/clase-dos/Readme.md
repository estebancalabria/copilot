# Clase Dos - 11 de Mayo del 2026

# Repaso

* Programa
* Prommpt Engineering
  * Instrucciones Personalizadas
  * Memoria
  * Usar a ChatGPT como experto en prompt Enginnering
  * Utilizar el modo Voz

# Canvas / Editar en una pagina

* Problema
    * Generar un informe/documento, pedirle que cambie algo..
    * Cambia lo que le pedi pero cambia tambien cosas que no le pedi
* Solucion
    * Usar canvas/ editar en pagina
 
```
Quiero escribir un mail informando a la oficina que no voy a ir a trabajar porque no me siento bien.
```

* Puse editar en pagina y fui cambiando solamente los parrados que deseo

```

Asunto: Aviso de ausencia por motivos de salud
Hola, espero que estés muy bien. ¿Cómo estás?
Les escribo para informarles que hoy no voy a poder asistir al trabajo porque no me encuentro bien de salud. Desde anoche me siento realmente mal y, a pesar de haber intentado descansar y mejorar, hoy no estoy en condiciones de rendir ni de presentarme a trabajar de manera responsable. Prefiero priorizar mi recuperación para poder volver en mejores condiciones y cumplir correctamente con mis tareas. Retomaré mis actividades apenas me sienta mejor.
Lamento mucho los inconvenientes que esto pueda generar y les pido disculpas por no poder estar presente hoy. Realmente espero que sea algo excepcional y que no vuelva a repetirse. Quedo totalmente a disposición para colaborar en lo que esté a mi alcance y avisaré cualquier novedad.
Saludos,
           MCT Esteban Calabria

```
# Prompt Engineering

## Tips

* Peditle a la ia "Dame el contenido para copiar y pegar sin acotar nada mas"

## Prompt

* Componentes
    * Tarea
    * Contexto <<<< Mucho muy importante
    * Ejemplos
    * Persona/Rol
    * Formato
    * Tono

### Contexto

* Prompt
    * Tip del modo voz
* Conversacion
* Conversaciones pasadas
* System Prompt
    * DE FABRICA : Intrucciones del fabricante le da la Ia y condiciona su forma de responder
        * Enterprise Safety Mode (No habla ni en broma, ni de politica, ni de ofensa)
    * PUEDO CAMBIAR: Instrucciones Personalizadas que vimos la clase pasada
* Memoria
* Uso de Herramientas
    * Busqueda web (para obtener informacion)
    * Microsft Graph
        * OneDrive
        * Mails
        * Conversarciones de team
        * ...

#### Tecnicas de prompting Contexto : Interaccion

* Consiste en encadenar prompts (por ejemplo haciendo que copilot me haga preguntas a mi) para generar una conversacion con todo el contexto relevante que preciso y luego recien cuando tenga todo ahi si me de uan respuesta
  * Importante. Decirle que me haga las preguntas DE A UNA

```
Voy a redactar una propuesta comercial a un cliente nuevo y quiero que me ayudes con informacion real.
Para hacerlo bien necesito que me hagas preguntas de a una esperando mi respuesta antes de la siguiente.
 Cuando tengas suficiente infromacion genera la propuesta.
Las preguntas que se respondan con un texto corto o que sean multiple choice. Empeeza con la primer pregunta.
```

* Copilot te va generando preguntas de a una

--- 

### Rol / Persona

* Tres solapas
    * Sin Rol
      * Se vende un terreno en Yerbabuena, Tucuman en Altos Verde 3. Decime si me conviene comprarlo
    * Con Rol
      * Actua como un esperto en operaciones inmibiliarias con mucha experiencia y realiza una  analisis profesional.Se vende un terreno en Yerbabuena, Tucuman en Alto Verde 3. Decime si me conviene comprarlo
    * Panel de expertos
      * Se vende un terreno en Yerbabuena, Tucuman en Alto Verde 3. Decime si me conviene comprarlo. Armes un panel de expertos donde cada uno me haga su analisis corto con pros, contras y cuestiones a considerar.


# Glosario

* Grounding 
