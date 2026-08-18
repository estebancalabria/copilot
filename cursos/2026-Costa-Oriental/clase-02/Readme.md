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

# Generacion de Imagen

* Copilot permite utilizar ademas de un modelo de generacion de texto, modelos de generacion de imagenes

![Uploading image.png…]()



