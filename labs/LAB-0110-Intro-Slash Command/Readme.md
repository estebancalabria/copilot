# Lab 110 — Slash Context y referencias en Copilot Chat

**Sesión:** 1 · **Duración estimada:** 35 minutos
**Módulo:** 1 — Arquitectura, contexto y productividad
**Patrón:** Context Injection con `/`

---

# Objetivo

Aprender a usar el selector contextual `/` de Microsoft 365 Copilot Chat para insertar contexto explícito dentro de una conversación.

Durante este laboratorio vas a:

✅ crear archivos reales
✅ generar un mail de prueba
✅ crear una reunión de calendario
✅ usar `/` para citar recursos
✅ hacer preguntas sobre ese contexto
✅ entender cómo Copilot usa Microsoft Graph

---

# La idea clave

Los modelos de IA responden mucho mejor cuando reciben contexto explícito.

En Copilot Chat, el símbolo:

```text id="x7m2q5"
/
```

abre un selector contextual conectado a Microsoft Graph.

Desde ahí podés insertar:

* archivos
* correos
* reuniones
* chats
* agentes
* recursos recientes

Copilot usa esos recursos como contexto adicional para responder.

---

# Cómo funciona conceptualmente

```text id="m5q8x1"
Usuario → Copilot → Microsoft Graph → Archivos / Mail / Teams / Calendario
```

El modelo no “adivina” el contexto.

Vos se lo proporcionás explícitamente usando `/`.

---

# Requisitos

* Cuenta Microsoft 365 con Copilot
* Acceso a:

  * OneDrive
  * Outlook
  * Teams
  * Calendario
  * Copilot Chat
* Navegador web

---

# Paso 1 — Abrir Copilot Chat

🌐 **URL:**
[Microsoft 365 Copilot Chat](https://m365.cloud.microsoft/chat?utm_source=chatgpt.com)

Verificá:

* estar logueado con cuenta corporativa
* que Copilot tenga acceso al entorno de trabajo

---

# Paso 2 — Crear un documento de Word

🌐 **URL:**
[Microsoft Word Online](https://www.office.com/launch/word?utm_source=chatgpt.com)

---

# Crear documento

1. Crear un documento nuevo
2. Renombrarlo:

```text id="r8n2m4"
plan-q3-lab
```

3. Escribir este contenido:

```text id="k4x7q1"
Planificación Q3

Objetivos:
- reducir costos operativos
- lanzar nuevo portal web
- automatizar soporte interno

Riesgos:
- retrasos del proveedor
- falta de recursos técnicos
- presupuesto limitado

Equipos involucrados:
- IT
- Comercial
- Producto
```

4. Esperar unos segundos para que sincronice.

---

# Paso 3 — Crear un mail de prueba

🌐 **URL:**
[Microsoft Outlook](https://outlook.office.com?utm_source=chatgpt.com)

---

# Enviar correo

1. Crear un nuevo mail
2. Enviártelo a vos mismo

---

# Asunto

```text id="v5m1x8"
Reunión presupuesto Q3
```

---

# Cuerpo

```text id="n7q3p5"
Hola,

Necesitamos revisar el presupuesto del Q3.

Puntos importantes:
- aumento de costos cloud
- retraso del proveedor
- posible contratación de nuevos recursos

Necesitamos definir acciones esta semana.

Saludos.
```

3. Enviar el correo.

---

# Paso 4 — Crear una reunión de calendario

🌐 **URL:**
[Microsoft Outlook Calendar](https://outlook.office.com/calendar?utm_source=chatgpt.com)

---

# Crear meeting

1. Crear una nueva reunión
2. Título:

```text id="q2x8m6"
Seguimiento proyecto portal web
```

3. Agregar descripción:

```text id="d4n7v1"
Temas:
- avance del desarrollo
- riesgos técnicos
- fechas de entrega
- presupuesto

Pendientes:
- validar proveedores
- revisar arquitectura
```

4. Guardar la reunión.

---

# Paso 5 — Crear conversación en Teams

🌐 **URL:**
[Microsoft Teams](https://teams.microsoft.com?utm_source=chatgpt.com)

---

# Crear chat simple

1. Abrir Teams
2. Abrir un chat con vos mismo o con un compañero
3. Enviar este mensaje:

```text id="f8q2m5"
Necesitamos actualizar el estado del portal web.
Todavía faltan definiciones de arquitectura y testing.
Hay riesgo de retraso.
```

Esperar unos segundos.

---

# Paso 6 — Usar `/` para citar un documento

Volvé a Copilot Chat.

En la caja de texto escribí:

```text id="p7x1m4"
/
```

---

# Qué debería pasar

Copilot abrirá un menú contextual con recursos disponibles desde Microsoft Graph.

Deberías poder ver:

* archivos recientes
* mails
* reuniones
* chats
* agentes
* contenido reciente

---

# Seleccionar el documento

Elegí:

```text id="y3n8q6"
plan-q3-lab
```

---

# Prompt

Después de seleccionar el documento, escribí:

```text id="t6q2v9"
Resumí este documento en 5 bullets ejecutivos.
```

---

# Qué observar

Copilot debería:

✅ leer el documento
✅ entender riesgos
✅ resumir objetivos
✅ generar síntesis contextual

---

# Paso 7 — Citar el mail

Escribí nuevamente:

```text id="u5m9x1"
/
```

Seleccioná el mail:

```text id="r4q7n2"
Reunión presupuesto Q3
```

---

# Prompt

```text id="k8x3m5"
¿Cuáles son los principales riesgos mencionados en este correo?
```

---

# Paso 8 — Citar la reunión

Escribí:

```text id="b1q6v8"
/
```

Seleccioná:

```text id="m7x2n4"
Seguimiento proyecto portal web
```

---

# Prompt

```text id="z5q1m7"
¿Cuáles son las tareas pendientes de esta reunión?
```

---

# Paso 9 — Citar el chat de Teams

Escribí:

```text id="d8m3x2"
/
```

Seleccioná el chat reciente de Teams.

---

# Prompt

```text id="q4n7v5"
Resumí esta conversación y detectá posibles riesgos del proyecto.
```

---

# Lo importante del laboratorio

Con `/` no estás “adjuntando” archivos manualmente.

Estás usando Microsoft Graph para darle contexto explícito al modelo.

Eso significa que Copilot puede trabajar sobre:

* documentos
* mails
* reuniones
* Teams
* recursos corporativos

sin salir del ecosistema Microsoft 365.

---

# Concepto clave

```text id="x2q8m4"
El slash no ejecuta comandos.

Inserta contexto.
```

---

# Preguntas de reflexión

1. ¿Qué diferencia hay entre describir un documento y citarlo?
2. ¿Qué ventajas tiene trabajar con contexto explícito?
3. ¿Qué recursos fueron más útiles: mail, Teams, reuniones o archivos?
4. ¿Qué riesgos existen si el contexto citado es incorrecto o incompleto?

---

# El aprendizaje clave

La calidad de una respuesta de IA no depende solamente del prompt.

Depende también del contexto disponible.

Los usuarios avanzados de Copilot no escriben prompts enormes explicando todo.

Simplemente citan el recurso correcto usando `/`.

---

*Material desarrollado por MCT Esteban Calabria · [https://linkedin.com/in/esteban-calabria](https://linkedin.com/in/esteban-calabria)*
