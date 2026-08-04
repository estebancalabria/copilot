# Clase dos - 04 de agosto del 2026

# Repaso

* Hay varias IA
  * ChatGPT (varios modelos)
  * Gemini (varios modelos)
  * Claude (varios modelos)
  * Grok
  * ...
  * Cada modelo se especializa en algo particular
* Copilot
  * Copilot Chat (para uso domestico)
  * Copilot 365 (para uso empresarial)
      * Copilot for Exel
      * Copilot for Word
      * ...
  * Copilot para Imagenes (designer de microsoft)
  * Copilot for Edge
  * Github copilot (para programar y tareas tecnicas)
  * Copilot for Windows
* Copilot Chat
  * Eleccion del modelo (Claude, GPT-X)
  * Historial de Conversaciones
  * Uso de Memoria
  * Utilizar herramientas
    * Busqueda Web
* Creacion de Imagenes
* Glosario
  * Prompt
  * Tokens (palabras o parte de ellas)
  * Alucinacion
  * Grounding

---

# LLM

* Los modelos de lenguaje no aprenden a medida que vamos hablando
* Cuando escribo un prompt la IA me va prediciendo iterativamente el proxito token (palabra) y asi va armando la respuesta
    * https://platform.openai.com/tokenizer
* Hay varios modelos de Lenguaje
  * GTP, Claude, Gemini...
  * Aparece el FOMO (Fear of Missing out)
    * Para ver el estado actual en modelos uso https://arena.ai/

## Alucinaciones

* La IA, al predecir el proximo token estadisticamente y armarme una respuesta que parece coherente y correcta puede estar suponiendo o inventando
* No hay que confiar ciegamente en la respuesta de la IA, es uan herramienta. La respuesta esta para que iteremos sobre ella y no para que la aceptemos ciegamente
  * Para reducir las alucinaciones:
    * Mejorar la calidad de los prompts
    * Agregar mas informacion o contexto a la conversacion
    * Proveer fuentes de datos confiables y verificables (grounding)
      * Mediante archivos adjuntos o referencias para la busqueda web

> [!NOTE]
> Siempre hay que chequear la respuesta de la IA e iterar sobre ella
  
## Copilot Microsoft

* No es un modelo en si sino una pasarela a otros modelos de IA
* (prompt) -> (filtro de seguridad de microsoft) -> (modelo de lenguaje)

---

# Prompt Engineering

* Componentes de un prompt
  * Tarea
  * Contexto
  * Ejemplos
  * Persona
  * Formato
  * Tono
* Existen distnitas tecnicas de prompting que se encagan en produdizar algunos de estos aspectos y son las que vamos a estudiar en las subsiguientes clases

## Contexto

* Todo la informacion que la IA recibe acompaniando al prompt para generar una respuesta

* Idea que tenemos
  * (prompt) -> (LLM)
* Lo que realmente ocurre
  * (prompt)
    * -> (Agrega la ingormaicon de toda la conversacion) 
    * -> (agrega la informacion de la memoria)
    * -> (informacion de las ultimas conversaciones)
    * -> (agrega los archivos adjuntos)
    * -> (usa herramientas para complementar la informacion)
      * -> LLM
* Ejemplo
  * Prompt : "Quien descubrio America?" (masomenos 5 tokens)
    * "El usuario juan perez que segun mi memoria es arquitecto y ..., buscamos en la web actualizaciones obre historia...." (aca hay muchos mas tokens)
      * Al LLM no le llega solamente el prompt que escribi sino todo el contexto adicional que se le agrego 

> [!NOTE]
> Entender como influye y la ia utiliza el contexto para generar una repsuesta es fundamental en prompt engineering

### Tecnica de Prompting : Interaccion o Encadenamiento de prompts

* Consiste en generar una conversacion con la IA que tenga todo el contexto necesario para dar un respuesta mas efectiva

* Sin tecnica
  * "Armame el plan de comidas para hoy"
* Con tecnica
  * "Armame el plan de comidas para hoy. Quiero que me hagas un cuestionario de 10 preguntas rapidas para determinar el mejor plan de comidas para mi persona. Haceme las pregutnas de a una y recien cuadno responda armarmame el mejor plan."
  * https://copilot.microsoft.com/shares/eTQ9UCG1st4tM7UXd2S7z

### Contexto con Herramientas : Conectores

* Ademas de la busqeuda Web copilot permite integracion con otras herramientas
* La version paga de copilot tiene integracion con todo el ecosistema 365 de microsoft
* La version gratuita tiene conectores
  * Si en el mail corportativo no aparece utilizar un mail personal en una ventana de incognito (u otro navegador)
  * Usuario (abajo izquierda) -> Configuracion -> Conectores
  * Habilitar contectores con gmail o outlook (el que mas le guste)

> [!NOTE]
> Hoy la parte de los conectores esta caida, generamente funciona bien. Una vez configurados los conectores

* Pedirle un resumen de mis correos
* Pedirle que me muestre que reuniones tengo hoy y que me agende reuniones

### Agrupar conversaciones por proyecto

* Cada conversacion tiene su propia URL
* Si yo quiero retomar una conersacion previa para no tener que repetir todo el contexto puedo ir a la direccion de la mimsa
* Muy util para no repetir el contexto

* De la misma forma puedo armar proyectos con conversaciones relacionadas para que la IA haga mejor manejor del contexto en relacion a los temas
* Ademas cada proyecto puede tener un grounding basado en archivos, links o contectores para no tener que repetirlo en cada conversacion

---

# Uso Etico de la IA

* Chequear siempre la respuesta de la IA

---

# Glosario

* Token : Palabra o parte de la misma que la IA utiliza para dividir un prompt o ir generando la respuesta
* No deterministica : Dos personas distintas pueden darle a la IA el mismo prompt y la IA generar dos respuestas distintas

---

# Proxima Clase

* Volver a probar lo de los coenectores que hoy no funciono pero es sumamente util
