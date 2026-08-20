# Clase Cuatro - 20 de agosto del 2026

# Repaso

* Herramientas
  * Speech-To-Texto (Voz-a-Texto)
    * Taqtic
* Copilot
  * Integracion con herramientas
      * Integracion con el correo
  * Pages
    * Editar un texto parcialmente para redaccion
* Prompt Engineering
  * Tips
      * PEdir el contenido para copiar y pegar
      * Modo dictado o por voz
        * Contexto
      * Usar a la IA como experto en Prompt Engineering : Previo a darle a la IA un prompt, pedirle en otra ventana que mejore/genere el promtp "Como si fuera un experto...
  * Prompt
      * Tarea, Contexto, Ejemplo, Rol/Persona, Formato, Tono
      * Contexto
        * Prompt + Conversacion + Conversaciones Recientes + Memoria + Conectores + Adjuntos + Busqueda Web

# Prompt Engineering

## Biblioteca de Prompts

* Consiste en tener un repositorio de plantillas de los prompts que mas me sirven en mi trabajo / dia a dia

## Cotexto

### Tecnica de Prompting : Interaccion

* AKA : Prompt Chainning
* Generar una conversacion con la IA que tenga todo el contexto necesario (encadenando prompts) antes de hacerle la pregunta

> [!NOTE]
> Lo vimos en la clase2, lo repasamos rapidamente

* Sin Tecnica
  * "Mi heladera funciona mal, el freezer hace escarcha. Decime como solucionarlo"
* Con la tecnica
  * "Mi heladera funciona mal, el freezer hace escarcha. Decime como solucionarlo. Haceme 10 preguntas de a una para tener todo el contexto necesario para darme una recomendacion precisa."

> [!NOTE]
> Aplicar el patron de interaccion para un caso real de uso en su trabajo y comparar las respuestas sin aplicar y aplicando el patron

## Persona

### Tecnica Personificacion

* El famoso promtp de decirle a la IA "Actua como si fueras..."
* Si le decimos a la IA que genere un prompt como un experto la aplica siempre


* Ejercitacion : Abrimos 4 solapas de copilot
  * Sin la tecnica
    * "Tengo una reunion con el cliente mas importante de mi empresa. Vamos a ver el tema de desviaciones sobre operaciones con lo previsto. Dame tips de como encarar la reunion."
  * Dandonle un rol
      * "Actua como un experto en negociaciones, relaciones empresariales, como mas de 20 anios mejorando las relaciones entre empresa-cliente y logrando mejorar la impagen de la empresa y manejando cualquier cuestionamiento o inquietud que el cliente pueda tener. Tengo una reunion con el cliente mas importante de mi empresa. Vamos a ver el tema de desviaciones sobre operaciones con lo previsto. Dame tips de como encarar la reunion.."
  * Personifique a alguien relevante
      * Eres Elon Musk. Tengo una reunion con el cliente mas importante de mi empresa. Vamos a ver el tema de desviaciones sobre operaciones con lo previsto. Dame tips de como encarar la reunion.
  * Citar un panel de experto
      * Tengo una reunion con el cliente mas importante de mi empresa. Vamos a ver el tema de desviaciones sobre operaciones con lo previsto. Dame tips de como encarar la reunion. Quiero que reunas un panel de expertos en distitas areas donde cada uno en una oracion me de un tip desde su punto de vista.

* Ejemplos
  * https://github.com/estebancalabria/Intro-Ia/tree/main/Prompt%20Engineering/Patrones%20de%20Prompting/Persona
 
* 

# Glosario

* Alucinaciones
* Grounding / Anclaje
* No Determiniso
  * Ante el mismo prompt identico la ia me suele dar tespuestas disitintas
