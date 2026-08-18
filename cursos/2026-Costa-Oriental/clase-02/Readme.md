# Clase Dos - 18 de Agosto 2026

# Repado

* Roadmap
* Modelos de Lenguaje
  * ChatGPT -> Redaccion
  * Claude -> Cuestiones Tecnica
  * Copilot -> No es un modelo de lenguaje, es una pasarela a ChatGPT que el medio le agrega contoles empresariales
* Agentes
  * LLM + Fuentes de Informacion + Herramientas + Objetivo puntual
* Copilot
  * Personalizacion de Salida
      * Cada uno la va ajustando mediante las instrucciones personalizadas como quiere que le responda
      * No hay un ajust universal
      * Ejemplo utiles de personalizaciones
          * Protocolo de la verdad
  * Memoria
      * Contexto de la conversacion, utiliza toda la conversacion mas las conversaciones reciente
      * Recuerda cosas puntuales de quien le habla
      * La puedo consultar y pedirle a la IA que recuerde cosas especificas
* Glosario
  * Alucinaciones
  * Grounding
  * Prompt
  * Prompt Engineerings
  * Token
 
---

# Prompts

## Contexto

(prompt)  ---> (+contexto)  ---> LLM
(prompt)  ---> (+Intstrucciones Personalizadas) (+memoria) (+conversacion/recientes) (+herramienta) ---> LLM
"Que clima hace hoy" --->  "El usuario Juan Perez que vive en Montevideo y tiene 30 anios y utimamente hablo esto (...) y segun openwheather hace 30 grados  --> LLM

---

# Copilot

## Diferencias ente Copilot empresarial y Domestio

* El copilot empresarial se accede en:
    * https://www.office.com/
    * https://m365.cloud.microsoft/
    * Este tiene el acuerdo de proteccion de datos empresarial
* Es distinto al copilto domestico
  * https://copilot.microsoft.com/

## Editar en Paginas

* Primero le pedimos a la IA

```
Redactame un correo para solicitar presupuesto por pallets y cajas. Un mail con cierta extension.
```

* Sirve para
  * Hacer cambios puntuales
  * Gastar menos tokens
  * Estar seguro que la IA solo modifica exactamente lo que le pedi y nada mas

<img width="1101" height="235" alt="image" src="https://github.com/user-attachments/assets/34af1474-76a6-4f53-a31d-c913b8f36b2d" />

* En otros llm
  * En copilot se llama Paginas, pero en ChatGPT se llama "Canvas editable"
  * En copilot se llama Paginas, pero en Claude se llama "Artefacto"

## Generacion de Imagen

* Copilot permite utilizar ademas de un modelo de generacion de texto, modelos de generacion de imagenes

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/b7cc8f14-07b2-4fc7-a24f-2f087344fb2d" />

* En biblioteca tambien quedan las imagenes generadas


### Bilblioteca

* Tanto las imagenes generadas con IA como las Paginas quedan guardadas en la biblioteca para poder consultarlas y seguir editandolas luego

---

## Agentes

* Si algun agente no aparece como el @Word
* Poner el @ e ir a la opcion "Obtener Agentes"
* Ahi agregar el Agente de Word
  
### Integrar con Agentes de Office

* Con el @ en una conversacion le puedo pedir a un agente que se encargue de resolver el prompt en cuestion
  * @Word
  * @Excel

* En la conversacion donde genere un documento
```
@Word. Me podes generar un word con el documento
```
---

## Agendar programaciones

* Puedo ejecutar periodicamente ciertos promps en forma automatica
* Me puede mandar un correo una vez que se finaliza
  * Los lunes pido normativas nuevas del mercao cambiario
  * Todos los dias que me haga una investigacion sobre potenciales clientes
 
* A mi me aparece asi abajo del prompt
  
<img width="765" height="190" alt="image" src="https://github.com/user-attachments/assets/df119751-d09e-4d63-8150-df4c33d42a4e" />

* A ustedes les aparece asi 

<img width="1254" height="719" alt="image" src="https://github.com/user-attachments/assets/ebe1cfb9-462d-4637-a69c-1e1e35d1838c" />

* Voy a administar las programaciones aca

<img width="399" height="400" alt="image" src="https://github.com/user-attachments/assets/aedd502a-b5f5-4411-991c-f04a5d783ab5" />

* Una cuestion que me parece muy util es adjuntarle un archivo de One Drive a la programacion y en prompt al momento de ejecutarse va a utilizar la ultima version del archivo
   * Es una forma de parametrizar el prompt de programacion

* Ejemplos de uso
  * Indicadores
  * Archivos que se van cargando
  * Distribucion de clientes

---

# Proxima Clase

* Editar el prompt
* Guardar los prompts
* Cuadernos / Noteebooks
