# Lab — Canvas: Copilot como coautor

**Sesión:** 2 · **Duración estimada:** 35 minutos
**Módulo:** 2 — Ingeniería de instrucciones
**Patrón:** Edición quirúrgica — Canvas / Editar en página

---

## La situación

Rodrigo es gerente de proyectos en una empresa de software. Pasó 20 minutos construyendo con Copilot un informe ejecutivo de 6 secciones sobre el estado de un proyecto. El informe quedó muy bien — casi perfecto.

Casi. La sección de conclusiones suena demasiado optimista. Rodrigo quiere que sea más realista y directa.

Sin pensar, escribe en el chat:

```
Reescribí el informe con conclusiones más realistas y directas.
```

Copilot regenera **todo el informe desde cero**.

Las cinco secciones que estaban perfectas ahora son distintas. El tono cambió. Un párrafo que Rodrigo había ajustado a mano desapareció. Tiene que volver a revisar todo.

Perdió 15 minutos y un trabajo que ya estaba hecho.

**Ese error tiene nombre: prompt de regeneración total. Y es evitable.**

---

## El problema: tokens, contexto y cambios no deseados

Cuando le pedís a Copilot que "reescriba el informe", el modelo interpreta que tiene que producir un documento nuevo completo. Eso implica:

- **Consumo innecesario de tokens** — procesás 6 secciones cuando solo necesitabas tocar 1
- **Pérdida de ediciones manuales** — cualquier cambio que hayas hecho a mano en el texto desaparece
- **No-determinismo** — el modelo no genera dos veces lo mismo; la nueva versión va a diferir en frases, estructura y tono aunque no quieras que cambie
- **Tiempo perdido** — revisás todo de nuevo cuando solo había un problema puntual

La solución es el **Canvas**.

---

## ¿Qué es el Canvas de Copilot?

El Canvas (también llamado "Editar en una página" en algunas versiones de Copilot) es un espacio de edición colaborativa donde el documento existe como un objeto persistente — no como una respuesta de chat.

La diferencia es fundamental:

| Chat normal | Canvas |
|---|---|
| Copilot genera una respuesta nueva cada vez | Copilot trabaja sobre el texto existente |
| Cambiar algo = regenerar todo | Cambiar algo = tocar solo esa parte |
| Tus ediciones manuales se pierden | Tus ediciones manuales se preservan |
| Es un chatbot | Es un coautor |

---

## Paso 1 — Generar el informe base en Canvas

🌐 **URL:** https://m365.cloud.microsoft

1. Abrí Copilot desde el portal M365.
2. Escribí este prompt para generar el informe inicial:

```
Generá un informe ejecutivo sobre el estado de un proyecto de implementación
de software para un cliente del sector financiero. El proyecto lleva 4 meses,
tiene un retraso de 2 semanas y el equipo está trabajando para recuperarlo.

El informe debe tener exactamente estas 6 secciones:
1. Resumen ejecutivo
2. Estado actual del proyecto
3. Principales logros del período
4. Riesgos identificados
5. Plan de recuperación
6. Conclusiones

Tono profesional, dirigido a un comité de dirección. Extensión: 400 palabras aprox.
```

3. Cuando Copilot genere la respuesta, buscá el botón **"Editar en una página"** o **"Abrir en Canvas"** que aparece debajo del texto generado. Hacé clic ahí.

> **Nota didáctica:** Si no aparece el botón automáticamente, podés pedirlo explícitamente escribiendo: *"Abrí esto en una página para editar"*. El Canvas no siempre se activa solo — a veces hay que pedirlo.

---

## Paso 2 — Explorar el Canvas

Una vez en el Canvas, observá la interfaz:

- El documento aparece como un texto editable, no como un mensaje de chat
- Podés hacer clic en cualquier parte y editar directamente como en Word
- El chat de Copilot sigue disponible en el panel lateral
- Las instrucciones que escribís ahora aplican **sobre el documento abierto**, no generan una respuesta nueva

Tomá 2 minutos para leer el informe generado. Identificá mentalmente:
- ¿Qué secciones están bien?
- ¿Cuál cambiarías?
- ¿Hay alguna frase que querrías ajustar?

---

## Paso 3 — Edición quirúrgica: cambiar solo una sección

Vamos a demostrar la diferencia entre el prompt peligroso y el prompt quirúrgico.

**Primero: editá manualmente una línea.** Hacé clic en el resumen ejecutivo y cambiá una palabra o frase a mano. Recordá qué cambiaste.

**Segundo: pedile a Copilot que modifique solo las conclusiones:**

```
Reescribí solo la sección de Conclusiones.
El tono debe ser más directo y realista — reconocer el retraso
sin sonar alarmista, y cerrar con un compromiso concreto del equipo.
No toques ninguna otra sección.
```

**Verificá:**
- ¿Solo cambió la sección de Conclusiones?
- ¿La edición manual que hiciste en el resumen sigue intacta?
- ¿Las otras 5 secciones quedaron igual?

> **Este es el momento clave del lab.** Si la respuesta a las tres preguntas es sí, el Canvas funcionó como coautor. Si algo cambió que no debía, lo discutimos con el grupo.

---

## Paso 4 — Más operaciones quirúrgicas

Practicá estas instrucciones una por una. Cada una debe tocar solo la parte indicada:

**Agregar contenido puntual:**
```
Agregá una tabla debajo de la sección "Riesgos identificados"
con tres columnas: Riesgo, Probabilidad (alta/media/baja) y Acción mitigadora.
Completala con datos coherentes con el resto del informe.
```

**Cambiar el tono de una parte:**
```
La sección "Estado actual del proyecto" suena demasiado técnica.
Reescribila para que sea comprensible para un lector no técnico,
sin cambiar los datos ni la extensión.
```

**Resumir una sección:**
```
Reducí la sección "Principales logros del período" a no más de 3 bullets.
Conservá solo los logros más relevantes.
```

**Cambiar formato:**
```
Convertí el "Plan de recuperación" en una tabla con columnas:
Acción, Responsable, Fecha límite.
```

---

## Paso 5 — El experimento del prompt peligroso

Ahora vamos a reproducir el error de Rodrigo para ver qué pasa.

Con el documento abierto en Canvas y después de todos los cambios que hiciste, escribí en el chat lateral:

```
Reescribí el informe completo mejorando el tono general.
```

**Observá qué pasa:**
- ¿Regeneró todo desde cero?
- ¿Tus ediciones manuales desaparecieron?
- ¿Las tablas y bullets que agregaste siguen?

> **El aprendizaje:** "Mejorar el tono general" suena inocente pero es un prompt de regeneración total. Copilot no sabe qué partes querés preservar — asume que todo está disponible para reescribir. **Siempre especificá qué sección, qué cambio y qué no debe tocarse.**

---

## Reglas de oro del Canvas

Antes de cerrar el lab, anotá estas reglas:

**✅ Prompts seguros en Canvas:**
- "Reescribí solo la sección X"
- "Agregá [contenido] debajo de [título]"
- "Cambiá el tono de este párrafo"
- "Resumí esta sección en N puntos"
- "Eliminá [parte específica] y reemplazala por..."

**⚠️ Prompts peligrosos en Canvas:**
- "Mejorá el informe"
- "Reescribilo con mejor tono"
- "Hacelo más profesional"
- "Actualizalo" (sin especificar qué)
- Cualquier instrucción que aplique a "el documento" sin delimitar la sección

**La regla simple:** si no dice explícitamente qué sección tocar, Copilot toca todo.

---

## Preguntas de reflexión para el grupo

1. ¿En qué documentos de tu trabajo cotidiano usarías el Canvas?
2. ¿Cuántas veces regeneraste algo innecesariamente antes de conocer esto?
3. ¿Qué diferencia ves entre editar en Canvas vs. editar directamente en Word con Copilot?

---

## El aprendizaje clave

El Canvas no es una función de formato — es un cambio de paradigma. Pasás de usar Copilot como una máquina de generar texto a usarlo como un coautor que trabaja sobre lo que ya existe. Eso cambia completamente cómo iterás, cómo preservás tu trabajo y cuánto tiempo invertís en revisiones.

Un prompt mal dirigido no solo consume tokens — destruye trabajo hecho. La edición quirúrgica es la habilidad que separa a quien usa Copilot de quien lo aprovecha.

---

## Próximo lab

**Lab — Productividad en Excel:** ahora que sabés cómo preservar y editar documentos, llevamos esa lógica a los datos.

---

*Material desarrollado por MCT Esteban Calabria · https://linkedin.com/in/esteban-calabria*
