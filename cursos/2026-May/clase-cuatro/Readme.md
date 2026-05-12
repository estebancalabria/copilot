# Clase Cuatro - 12 de Mayo del 2026

# Repaso

* Prompt Engineering
  * Personalizacion de Salida
    * Markdown
      * Me servia para escribir una plantilla de como quiero exactamente la respuesta
    * Mermaid
      * Me servia para generar Graficos
* Copilot para Analisis de Datos
  * Copilot en Excel
    * Tablas dinamicas (Pivot Tables)
    * Graficos dinamicos (Pivot Graph)
  * Agente Analista
    * Ejecuta scripts de datos en python para analizar los dataset

---

# Modo Profesional vs Modo Web

* Cambia el enfoque de como hace el grounding de la informacion
 * Modo Profesional : Prioriza los documentos de la empresa y las apps corporativas con microsft Graph
 * Modo Web : Prioriza la busqueda web para generar una respuesta

---

# Copilot en Word

* Abrimos la aplicacion de work
* Hacemos click en el iconito de Copilot
* Le ponemos este prompt

```
Crea un resumen de reunion con un cliente de la empresa ABC sobre la realizacion de una construccion sobre un terreno que tienen ellos. Incluye asistente, fecha de hoy, tres puntos discutidos, dos compromisoso asumidos y proximos pasos 
```

> [!NOTA]
> Una vez generado el documento al igual que haciamos con el "Edit in page" (Canvas) se puede modificar un parrafo concreto, seleccionandolo y diciendole a copilot que lo modifique en el menu contextual

---

# Distintos modelos de Lenguaje

* Microsoft es socio accionario de OpenAI
* Y utiliza por detras en copilot varios modelos de esa empresa

* (Prompt)
  * --> (Enterprise Safety Mode / System Prompt / Controles.../ Eleccion del modelo)
    * --> (Modelo elegido como GPT 5)

* Si no le pongo nada MS elije el modelo mas apropiado segun el prompt

* Tipos de Modelos
 * OpenAI
    * Fast : Dan una respuesta rapida, poseen llamadas a herramientas (busqueda web)
    * Razonamiento/Thinking : Se utilizan para generar razonamientos logicos para escenarios logica/matematica/razonamientos
  * Anthropic
    * Opus : Mas preparado para tareas tecnicas

---

# Repaso (Usar Copilot como prompt engineering)

* En una solapa aparte

```
Quiero que actues como un experto en envio de correos institucionales y prompt enginenieering. Quiero que para cada prompt que requiera envio de correo me redactes un prompt para anexar teniendo en cuenta que a mi me gusta primero preguntar a las personas como anden e incluir algun detalle de la persona en ese correo.
```

* Me genero esta propuesta

```
Actúa como un experto en redacción de correos institucionales, con un tono profesional, cercano y humano.

Quiero redactar un correo que cumpla con estas condiciones:

1. Siempre comenzar saludando de forma cordial y preguntando cómo está la persona.
2. Incluir un detalle personalizado sobre el destinatario si se dispone (por ejemplo: trabajo reciente, proyecto, contexto compartido, equipo, etc.).
3. Mantener un tono profesional pero cálido (ni demasiado formal ni demasiado informal).
4. Ir al punto del mensaje con claridad.
5. Mostrar empatía, predisposición y buena actitud.
6. Cerrar el correo de forma amable, abierta y disponible.

Contexto del correo:
- Objetivo: [explicar para qué es el mail]
- Destinatario: [nombre y rol]
- Relación con el destinatario: [ej: colega, cliente, superior]
- Detalles personales relevantes a incluir: [ej: proyecto en el que está, curso, situación, etc.]
- Contenido principal del mensaje: [lo que querés comunicar]
- Tono deseado adicional: [ej: más formal, más cercano, más insistente, más comercial]

Redacta el correo listo para copiar y pegar, sin explicaciones adicionales.
```

---

# Referenciar documentos en Copilot

* Con la / (slash command) puedo activar referenciar
  * Documentos
  * Contactos
  * Mails
  * Conversaciones
* Automaticamente lo incluye en el contexto de la conversacion

---

# Galeria de Prompts

> [!NOTE]
> Solo modo profesional

* Cuanto uno estudia prompt engineering es probable que muchas veces repita prompts similares
* Puedo pasarle por arriba a un prompt y en el menu contextual guardarlo en la galeria de prompts
* Arriba se puede acceder en los ... a la galeria de prompts
  * Prompts probados que son de Microsoft
  * Tus propios prompts que guardase antes
* Probemos por ejemplo el prompt "Mantenerse Informado"
* En la parte de mis prompts puedo ver mis prompts guardados
* Los prompts se pueden compartir
* En la galeria de indicaciones arriba en la ruedita se peude ver los prompts compartidos
  
---

# Agendar Prompts

* En Copilot se pueden automatizar prompts
 * Ejemplo
    * Todos los lunes a las 5 de la tarde hacer esta busqueda en intenet y hace me un informe
    * Todos los martes a las 3 haceme un resumen con las tareas pendientes que recibi por mail

> [!NOTE]
> Solo me funciono en el modo profesional

```
Quiero que me hagas un informe con todos los terrenos que estan dispoibles para la venta en Yerba Buena, Tucuman
```

* Al pasarle por arriba al prompt tenemos la opcion de Agendar prompts para que ejecute automaticamente

---

# Creacion de Agentes
