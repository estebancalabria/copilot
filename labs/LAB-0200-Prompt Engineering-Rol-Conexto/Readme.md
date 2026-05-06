# Lab 0200 — Prompt Engineering

## Contexto y Rol

**Sesión:** 1 · **Duración estimada:** 35 minutos
**Módulo:** 1 — Arquitectura, seguridad y fundamentos
**Patrón:** Rol + Fuente + Contexto + Formato de salida

---

## La situación

Son las 10:47 de la mañana. Abrís Outlook y ahí está: un correo de Martín Ferreyra, Director de Operaciones de uno de tus clientes más importantes. El proyecto de implementación lleva dos semanas de retraso y Martín acaba de enterarse por su propio equipo, no por vos.

El correo no es agresivo. Es peor: es frío, preciso y lleva copia a tu gerente.

Tenés que responder. Y tenés que responder bien.

---

## El correo simulado

En este lab vamos a trabajar con el siguiente correo. Copialo — lo vas a usar como fuente en tus prompts.

---

```
De: Martin Ferreyra <m.ferreyra@grupoatlantida.com>
Para: [Tu nombre] <[tu email]>
CC: Valeria Suárez <v.suarez@tuempresa.com>
Asunto: RE: Proyecto Integración API — Estado de avance
Fecha: Martes, 9:23 AM

Buen día.

Me comunico porque esta mañana mi equipo técnico me informó que
el módulo de integración que debía estar en producción el viernes
pasado todavía no fue entregado. Esta es la segunda vez que se
corre la fecha sin que recibamos una comunicación formal de su parte.

Necesito entender qué está pasando y cuál es el plan concreto
para los próximos días. Grupo Atlántida tiene compromisos internos
que dependen de esta entrega y cada semana de retraso tiene un
impacto operativo real.

Espero su respuesta antes del mediodía.

Martín Ferreyra
Director de Operaciones — Grupo Atlántida
```

---

## Paso 1 — Recuperar el correo desde Copilot en Outlook

Antes de responder, vamos a practicar recuperar contexto desde Copilot.

🌐 **URL:** https://outlook.office.com

1. Abrí Outlook en el navegador.
2. Hacé clic en el ícono de **Copilot** en la barra lateral derecha.
3. Escribí este prompt:

```
Busca el último correo de un cliente que mencione un retraso o demora
en una entrega. Resumime de qué se trata, quién lo envió y cuál es
el tono del mensaje.
```

> **Nota didáctica:** Copilot está consultando tu bandeja real a través de Microsoft Graph. Si no encontrás un correo similar, usá el correo simulado de arriba pegándolo directamente en el chat en los pasos siguientes.

---

## Paso 2 — El prompt malo

Pegá el correo de Martín en el chat de Copilot y escribí este prompt:

```
Ayudame a responder este mail
```

Guardá la respuesta. La vamos a comparar después.

**Observá y anotá:**
- ¿El tono es el adecuado para la situación?
- ¿Propone alguna solución concreta?
- ¿Podrías enviarlo tal cual o necesitaría muchas correcciones?
- ¿Tiene la extensión correcta para un correo ejecutivo?

> **Lo que suele pasar:** Copilot devuelve algo genérico, educado pero vacío. Reconoce el problema pero no propone nada. Podría servir para cualquier industria y para cualquier cliente. No tiene voz, no tiene peso. No lo podrías enviar sin reescribirlo casi completo.

---

## Paso 3 — Deconstruir el problema

¿Por qué falló el primer prompt? Porque le diste a Copilot el mínimo de información posible. El modelo no sabe:

- **Quién sos vos** en esta situación (¿account manager? ¿gerente de proyecto? ¿CTO?)
- **Qué pasó realmente** con el retraso (¿hay una causa? ¿hay un nuevo plan?)
- **Qué tono necesitás** (¿formal? ¿empático? ¿directo?)
- **Qué forma debe tener** la respuesta (¿larga? ¿corta? ¿con fecha concreta?)

Sin esa información, el modelo adivina. Y cuando adivina, promedia. Y lo promediado nunca es lo que necesitás.

---

## Paso 4 — La estructura de un prompt efectivo

Un prompt bien construido tiene cuatro elementos:

| Elemento | Pregunta que responde | Ejemplo |
|---|---|---|
| **Rol** | ¿Quién sos en este contexto? | "Sos un Account Manager senior de una empresa de software" |
| **Fuente** | ¿Con qué información trabajás? | "Basate en el correo que te pego a continuación" |
| **Contexto** | ¿Qué está pasando realmente? | "El retraso se debió a un problema técnico ya resuelto. El nuevo plazo es el viernes" |
| **Formato** | ¿Cómo debe verse la respuesta? | "Redactá un correo de no más de 120 palabras, tono formal pero empático" |

---

## Paso 5 — El prompt bueno

Ahora reescribí el prompt con la estructura completa. Pegá el correo de Martín y luego este prompt:

```
Sos un Account Manager senior de una empresa de desarrollo de software B2B.

Basate en el correo del cliente que te pego a continuación.

Contexto: el retraso se debió a un problema técnico en el entorno
de integración del cliente que ya fue resuelto por nuestro equipo.
El nuevo plazo de entrega confirmado es el próximo viernes.
El cliente tiene copia a tu gerente, por lo que la respuesta
debe ser profesional y transmitir control de la situación.

Redactá una respuesta de no más de 120 palabras. Tono formal y empático.
Que reconozca el impacto, explique brevemente la causa sin excusas,
confirme el nuevo plazo y proponga una llamada de seguimiento para hoy o mañana.

[CORREO DEL CLIENTE]
```

Guardá esta respuesta junto a la del Paso 2.

---

## Paso 6 — Comparar los dos outputs

Poné los dos resultados lado a lado y evaluá:

| Criterio | Prompt malo | Prompt bueno |
|---|---|---|
| ¿Reconoce el impacto en el cliente? | | |
| ¿Explica la causa? | | |
| ¿Propone una acción concreta? | | |
| ¿Tiene el tono correcto? | | |
| ¿Lo enviarías tal cual? | | |

> **El momento clave:** La diferencia no está en la IA. Está en la calidad de la instrucción. Copilot es tan bueno como el prompt que recibe.

---

## Paso 7 — Iteración: refiná sin reescribir

El prompt bueno ya funciona. Ahora practicamos iterar sobre la respuesta sin volver a escribir todo desde cero.

Probá estos prompts de refinamiento uno por uno:

**Refinamiento 1 — Tono:**
```
La respuesta está bien pero suena demasiado corporativa.
Reescribila con el mismo contenido pero con un tono más directo y humano,
sin perder la formalidad.
```

**Refinamiento 2 — Extensión:**
```
Reducila a no más de 80 palabras manteniendo los tres puntos clave:
causa del retraso, nuevo plazo y propuesta de llamada.
```

**Refinamiento 3 — Foco:**
```
Agregá una línea al inicio que reconozca específicamente
que la comunicación de nuestra parte no fue la adecuada.
Sin sonar defensivo.
```

> **Nota didáctica:** Iterar es parte del proceso. Un buen usuario de Copilot no espera el prompt perfecto a la primera — construye la respuesta en capas, igual que lo haría con un colaborador humano.

---

## Preguntas de reflexión para el grupo

1. ¿En qué otras situaciones de tu trabajo cotidiano podrías aplicar esta estructura?
2. ¿Qué elemento de los cuatro (rol, fuente, contexto, formato) te cuesta más definir?
3. ¿Cuánto tiempo te hubiera llevado escribir ese correo sin Copilot?

---

## Resumen del lab

El prompt malo le da a Copilot el problema. El prompt bueno le da el problema, el contexto, la voz y la forma esperada del resultado. La diferencia entre los dos no es técnica — es la diferencia entre delegar y saber delegar.

| Elemento | Lo que aporta |
|---|---|
| Rol | Le da identidad y criterio al modelo |
| Fuente | Ancla la respuesta en datos reales |
| Contexto | Elimina las suposiciones del modelo |
| Formato | Define exactamente qué necesitás |

---

## Próximo lab

**Lab 1C — Prompt vs. búsqueda:** ahora que dominás la estructura de un prompt, vamos a comparar cuándo conviene usar Copilot y cuándo una búsqueda tradicional en SharePoint.

---

*Material desarrollado por MCT Esteban Calabria · https://linkedin.com/in/esteban-calabria*
