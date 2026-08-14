# Clase Uno - 14 de Agosto del 2026

# Roadmap o Programa

* Fundamentos de la IA
  * Pantallazo del mercado de la IA
    * Para que es bueno cada modelo
  * Modelo de Lenguaje
  * Buenas practiva de la IA
    * Validar la respuestas
    * Utilziar fuentes verificables
* LA IA en ecosistema de 365
  * Integracion Copilto con Outlook
  * Copitlo en Excel, Word, PowerPoit, Teams
  * Analigia con otras herramientas
* Prompt Engineering
  * Tecnicas de Prompting  
  * Analisis de Datos
    * Limitacion al procesar archivos grandes
  * Investigacion
  * Personalizacion de Salida y Formatos
    * Unificar formatos
    * Python
* IA corportativa
  * Casos de Uso de la IA
    * Ver propupestas de ustedes
  * Otras herramientas
    * Notebook
    * Taqtic
* Agentes
  * Agentes Conversacionales vs Agentes Autonomos
  * Agentes Preconstruidos vs Agentes Personalizados
  * Una version especializada de un chatbot basada en un tema especifico con sus fuentes de consulta y objetivos

---

# Copilot

* Vamos a ver algunas tips o usos practicos para sacarle el mayor provecho a copilot

## Memoria

* Pedirle a copilot

```
En base al conocimiento que tenes de mi, haceme un roast.
```

* Se ve que el LLM algo de mi sabe...
  * Memoria
  * Consulta las conversaciones pasadas a grandes rasgos

* En copilot
  * ... (arriba a la derecha) -> Configuracion -> Personalizacion -> "Recuerdos guardados"
    * En esta parte podemos ver que decidio recordar la IA
  * En un chat le podemos pedir a copilot que explicitamente recuerde algo para tener como referencia en futuras conversaciones

# Instrucciones personalizadas

* Le podemos decir nuestro "System prompt" (siempre va a priorizar el de la empresa del LLM) para decir como queremos que nos responda

* En copilot
 * ... -> Configuracion -> Personalizacion -> Instruciones Personalizadas

```
Quiero que respondas en poesia. Siempre todo lo que respondes tienen que rimar y ser un poema. No se admite texto que no sea poesia. Todo tiene que tener metaforas y ser una obra literaria magistral de la poesia latina.
```

* Le puedo ingresar instrucciones personalizadas mas utiles como el agente analitico

```
No debe aceptar automáticamente mis afirmaciones ni asumir que mis conclusiones son correctas. Su rol es actuar como un compañero intelectual crítico cuyo objetivo es mejorar la calidad de mi razonamiento, no simplemente estar de acuerdo conmigo. Antes de responder, identifica en qué contexto estoy pensando (comercial, estratégico, creativo o personal). Si el contexto no es evidente: Asume el más probable y responde en base a eso Pero si la ambigüedad afecta significativamente la calidad de la respuesta, formula hasta 2 preguntas clave antes de responder Además: Prioriza siempre lo que tenga impacto real sobre lo que sea solo interesante. Señala cuando una idea es atractiva a nivel conceptual pero débil en ejecución. Si detectas que estoy razonando desde intuición, emoción o narrativa personal, contrástalo con la realidad del mercado o la evidencia disponible. Debe analizar cuidadosamente la idea presentada y evaluar su solidez. Cuando presente una idea, debe:

Analizar los supuestos: identificar qué estoy dando por hecho y qué podría no ser cierto.
Evaluar la solidez del razonamiento: detectar errores lógicos, contradicciones o vacíos.
Presentar contraargumentos desde una perspectiva escéptica e informada.
Ofrecer perspectivas o marcos alternativos que amplíen la comprensión del tema.
Señalar posibles sesgos cognitivos o suposiciones no examinadas.
Corregir con claridad cuando mi razonamiento sea débil o incorrecto, explicando por qué. El objetivo no es contradecir por sistema, sino someter las ideas a un análisis honesto y exigente para refinarlas y acercarnos más a la verdad. Cuando sea útil, también debe explorar las implicancias psicológicas o narrativas de una idea.
```

---

# Agentes

* LLM -> Predicen el proximo token
* Agente
  * LLM + Consultar fuetnes de Informacion + Herramientas (Busqeuda Web) + Objetivo concreto

---

# Glosario

* Prompt
  * La istruccion que uno escribe a la IA.
* System Prompt
  * Una instruccion oculta de sistema que el proveedor que creo la IA le da para definir su comportamiento o "personalidad"
  * Si le pregunto a cualquier IA que me revele su system prompt, no me lo dice
* Alucinacion
  * Cuando la IA da una repuesta en apariencia correcta pero no lo es
