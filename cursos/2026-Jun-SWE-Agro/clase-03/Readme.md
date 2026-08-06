# Clase Tres - 6 de agosto del 2026

# Repaso

* LLM
  * Existen Varias IA
    * Arena.ai
      * Ranking de modelos de IA
  * Copilot no es un modelo
    * Es una pasarela que direcciona el prompt a el mejor modelo segun microsoft para respoderlo
    * Dependiendo el modo que use MS puede elegir un modelo distinto
        * Por ejemplo el modo "Razonamiento Profundo" utilizaba Claude
* Prompt Engineering
  * Contexto
      * (prompt) -> (Le agrega cosas: Memoria / herramientas (busqueda web) / Ultimas conversaciones) -> (filtros de Seguridad) -> (LLM(
      * Tecnicas de Prompting
        * Prompt Chainning o Interaccion
      * Proyectos para agrupar conversaciones
        * No aparece a todos
        * Usando el mail de la emprea
* Glosario
  * Grounding
      * Anclar la respuesta de la IA con fuentes verificables
  * Tokens
      * Una palabra o parte de e ella que puede ser del prompt o de la respuesta. Es la unidad de medida de la IA.

---

# Trucos y tips

* Utilizar arena.ai para generar videos casi ilimitados (no encontre el limite)
  * Lo unico que no puedo elegir el modelo

---

# Casos de Uso empresariales
 
##  Uso de la IA con reuniones

* Grabar la reunion con celular o aplicacion tipo teams
* Transcribir la reunion con una herramienta como Tactiq
    * https://tactiq.io/es
    * Podemos ver mas herramientas de trasncripcion en : https://www.instagram.com/p/DBzb-kHxqae/?img_index=1
    * Si tenes teams directamente el teams si lo tenes habilitado te hacer la trasncripcion y no tenes que instalar nada
* Cargar la conversacion en copilot para hacerme preguntas

```
Tengo esta conversacion. Quiero que me la resumas, me digas como me fue como instructor y me des un plan de accion para seguir
```

---

# Features de Copilot

## Uso de "Pages" 

* Problema
  * Muchas veces le pido a copilot que me redacte un mail, un texto/propuesta para presetnar un cliente, un informe para un jefe
  * La respuesta de la IA esta bien, pero hay cosas puntuales que quiero cambiar y se lo pido a la IA
  * La IA efectivamente cambia lo que le pedi pero altera otras partes del documento sin que yo se lo pida ni me entere
  * Me obliga a volver a chequear todo
* Solucion
  * Editar la respuesta de la ia en una pagina
  * TE permite hacer ediciones con IA o manualmente
  * Me aparece un chat de IA en la derecha para pregutnas o cambios generales
  * En la parte de biblioteca me quedan guardadas todas las paginas que cree
  * Permite exportar la pagina como pdf o word
  * Permite exportar el documento con otros
      * https://copilot.microsoft.com/shares/pages/d6sZvBP2rnNAjvbhpogtj

> [!NOTE]
> OJO que tal vez con un mail empresarial no les deje ver el link por una cuestio de seguridad y haya que usar un mail personal


```
Soy de la empresa SMW agro y quiero redactar un texto para mostar a un potencial cliente donde se destaquen las fortalezas de mi organizacion y que sea persuasivo para que contraten nuestros servicios. Investitar fortalezas de SMW en linea.
```

> [!NOTE]
> Probar el mismo prompt con el modo buscar y el modo razonamiento profundo

```
Devolver solamente el mensaje persuasivo como para copiar y pegar sin acotar nada mas y que sea mas largo.
```



---

# Prompt Engineering

## Tips

### Pedirle solamente el conetido

* Decirle como parte del prompt
  * "Devolver solamente el <OBJETIVO> para copiar y pegar sin acotar nada mas

### Usar el modo dictado para mejores prompts

* Tipo Para el contexto
  * Escribir prompts "largos" explicando todo lo que te venga a la cabeza utilizando el modo dictado

* No es lo mismo esto:

```
Haceme un mail para pedirle un aumento a mi jefe
```

* Que usando el modo dictado

```
Necesito escribir un mail para pedirle un aumento a mi jefe, pero necesito que sea un mail persuasivo. Además, considera que mi jefe es de Racing y siempre que le hablo de Racing se emociona. Quiero que el mail sea súper persuasivo y apele a su fibra sensible y su emocionalidad como empleado. Quiero que utilices todas las técnicas de persuasión que se te ocurran y que el que lea el mail no se pueda negar. Generame el correo, por favor.
```

### Usar lectura en voz alta

* Para las respuestas largas se puede usar la lectura en voz alta para no tener que leer

<img width="266" height="32" alt="image" src="https://github.com/user-attachments/assets/6034852f-d9dd-433f-917d-20da8c9da664" />


### Usar a Copilot como experto en prompt engineering

* La idea es agarrar y escribir un prompt como a mi me salga y pedirle a Copilot que me lo mejore
* "Actua como experto en prompt engineering y mejorame este prompt <PROMPT>

```
Actua como experto en prompt engineering quiero que me mejores este prompt "Soy de la empresa SMW agro quiero que  me hagas una investigacion de mercado sobre la competencia y que venjas tengo que tengo que tener en cuenta quiero un informe util que me permita conocer el mercado y accionar. Devolver el prompt para copiar y pegar sin acotar nada mas."
```

* Me devuelve el prompt mejorado

```
Actúa como un analista senior de inteligencia de mercado especializado en el sector agroindustrial. Soy de la empresa SMW Agro y necesito que realices una investigación de mercado completa sobre nuestra competencia directa e indirecta. Incluye: análisis de competidores, productos y servicios que ofrecen, precios, posicionamiento, estrategias comerciales, canales de venta, ventajas competitivas, debilidades, tendencias del mercado, oportunidades y amenazas. Quiero un informe claro, accionable y orientado a decisiones estratégicas que me permita entender el mercado y definir acciones concretas para mejorar nuestra competitividad.
```

---

## Prompt

* Formula para prompts
  * https://www.instagram.com/p/C5MDsQiR5cG/?img_index=1
  * Tarea, Contexto, Persona/Rol, Ejemplo, Formato y Tono

## Contexto

### Conectores de Microsoft

* El uso de herramientas

#### Mail de GMAL
  
```
Revisa mis mails y haceme una lista de mails sin responder. Priorizame seguns su contenido cuales son mas urgentes de respoder
```

```
Mandame un mail a mi mismo esteban.calabria@gmail.com con una frase inspiradora
```

> [!NOTE]
> Por un tema de permisos no pudieron probarlo con el mail de outlook

#### Calendar de Google

```
Que tengo agendado en mi calendario hoy?
```

```
Crear un evento en mi calendario hoy a las 13:00 que sea estudiar para el Az-500
```

---

# Uso resposable de la IA

* Principios IA Responsable e MS
  * https://www.microsoft.com/en-us/ai/principles-and-approach

---

# Proxima clase

* Tecnica de prompting Rol/Persona en detalle
