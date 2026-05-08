# Clase Dos - 8 de Mayo del 2026

# Repaso

* Programa del curso
* Copilot
  * Memria
      * Poder Guardar recuerdos y configurar que sabe copilot de mi
  * Personalizacion
      * Poder configurar como te responde copilot
* Tips
  * Utilizar el modo voz para no economizar contexto
* Prompt Engineering
  * Prompt
      * Contexto
* Glosario

# Enterprise Safety Mode

* Para licencias empresariales (no pasa con la cuenta personal) copilot tiene mucho cuidado de no dar respuestas que puedan herir o ser mal interpretadas.
* No es es opcional viene asi de fabrica y no se puede configurar
* Se cancelan resupestas hostiles o que puedan generar riesgo reputacional

# Prompt Engineering

## Contexto

* **Prompt**
* Conversacion
* Personalizacion
* Memroria
* Historial de Chats (las ultimas converaciones)
* Microsft Graph
  * OneDrive
  * Correos
  * Conversaciones de Teams
* Busquedas web

## Prompt

* Componentes de Un prompt
    * Tarea
    * Contexto
    * Ejemplo
    * Rol/Persona
    * Formato
    * Tono

## Tip

### Agregar al prompt al final
  * "Dame el contenido solamente para copiar y pegar sin acotar nada mas."

### Usar copilto como experto en prompt engineering

```
Actua como experto en prompt engineering y dame una version optima de este prompt
"Quiero que actues como un experto en inversiones inmobiliarias especializado en inversioens en Tucuman. Hay un terreno en la calle Lola Mora Yerba buena. Son 4 lotes. (Entre Salas y Valdez y Lola Mora)  (Numero de padrones 183471  / 72 / 73/ 74). (Busca informacion relevante del terreno en internet si encontras). Tambien cita a un panel de expertos donde cada uno me de algun insight particular de estos terrenos que valga la pena tener en cuenta. Evaluame pros y contras. Devolver el prompt para copiar y pegar sin acotar nada mas"
```

*  Me genero este prompt

```
Quiero que actúes como un experto senior en inversiones inmobiliarias especializado en el mercado de Tucumán, Argentina, con enfoque particular en Yerba Buena. Debes analizar en profundidad un caso específico: un conjunto de 4 lotes ubicados en la calle Lola Mora, entre Salas y Valdez (padrones 183471, 183472, 183473 y 183474).
Tu tarea es:

Investigar y recopilar toda la información pública relevante disponible sobre estos terrenos (ubicación, zonificación, normativa urbanística, servicios disponibles, accesibilidad, entorno, desarrollos cercanos, evolución de precios en la zona, y cualquier dato relevante que encuentres en internet o fuentes abiertas).
Realizar un análisis integral del potencial de inversión considerando:

Usos posibles del suelo
Demanda actual y proyectada en la zona
Perfil del comprador/inversor objetivo
Riesgos regulatorios, económicos y de mercado


Evaluar de manera estructurada los principales pros y contras de la inversión en estos lotes, con argumentos claros, concretos y basados en datos.
Simular un “panel de expertos” compuesto por al menos 4 perfiles distintos (por ejemplo: desarrollador inmobiliario, urbanista, inversor conservador, agente inmobiliario local). Cada experto debe aportar un insight diferencial, específico y no redundante sobre la oportunidad.
Incluir recomendaciones estratégicas accionables: escenarios de inversión (conservador, moderado, agresivo), posibles estrategias de desarrollo o reventa, y puntos clave a validar antes de avanzar.
El análisis debe ser profundo, estructurado, claro y orientado a la toma de decisiones de inversión.
```

## Editar en Pagina

* Contexto.
  * Genero un documento (informe, mail,...)
  * Le pido un cambio especifico a copilot
  * Me regenera TODO el documento
  * Cambio lo que le pedi y ademas otra cosa sin abisar
* Problema
  * Cambia algo que no le pedimos
  * Consumo redundante de tokens al generar lo mismo
* Solucion
  * Cuando tengo un texto que quiero cambiar. Uso Edtiar en pagina

## Tecnicas de Prompting

### Interaccion / Encadenamiento de Prompts (Prompt Chainning)

* Consiste en decirle a la IA que me haga preguntas para tener las repsuesta en la conversacion e ir alrmando el contexto

```
Voy a redactar una propuesta comercial a un cliente nuevo y quiero que me ayudes a consturirla con informacion real. Para hacerlo bien necesito que me hagas preguntas de a una esperando m i respuesta antes de hacer la siguiente.  Cuanto tengas suficiente informacion avisame y genera la respuesta. Empeza con la primer pregunta.
```

* El seccreto de esta tecnica es pedirle a copilot que  me haga las preguntas de a una
* La respuesta en este caso la editamos en la pagina como vimos antes

### Rol / Persona

* Tres solapas del navegador
  * Sin Rol
      * "Hay un terreno en venta en el centro de tucuman. Ayudame a evaluar si me conviene comprarlo."
  * Con Rol
      * Actua como un experto en inversioens inmobiliarias para una empresa que se dedica a organizar proyectos de construcion. Hay un terreno en venta en el centro de tucuman. Ayudame a evaluar si me conviene comprarlo.
  * Panel de expertos
      * Armame un panel de expertos donde cada uno me de su opion es una oracion sobre un tema especifico. Cada experto me data su vision especifica segun su area de expertise.. Hay un terreno en venta en el centro de tucuman. Ayudame a evaluar si me conviene comprarlo. 

### Personalizacion de Salida

* Para esta actividad le voy a pedir a la IA una lista de algo
  * "Haceme una lista de barrios de Yerba Buena, Tucuman. De cada barrio quiero saber poblacion aproximada, costo metro cuadrado aproximado, trasnporte, edificios, actividad comercial. (Busca en internet y si no encontras infromacion estima)"

* Formatos de Salida
  * Tecnicos
      * json, xml
  * Pseudo tecnico
      * HTML
      * Para generar PDFs con formato profesional
      * El HTML lo puedo previsualizar en la misma ventana de copilot
      * Si no me gusta le puedo pedir cambios sin necesidad de saber html (en lenguaje natual)
      * Si bien copilot me puede generar pdfs...
          * Si copio el html en un block de notas con extension .html
          * Le doy doble click
          * Y lo imprimo en pdf
          * Tengo mas contro de como se me ve la salida
          * (Si e lo pido directamente en pdf lo hace como quiere)
  * Planillas de calculo
      * CSV : Comma sepparated values
      * Formato estandar para interactuar con excel
      * Sirve para traerte informacion en tabla desde otros lugares (otros llm)
      * En Copilot es menos util porque le puedo edicr que me genere el excel directamente

# Glorario

* No determinismo : Mismo prompt no da siempre el mismo resultado
* Token
* Grounding
