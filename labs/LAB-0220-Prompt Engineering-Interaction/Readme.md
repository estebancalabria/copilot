# Lab — El interrogatorio: Copilot como consultor

**Sesión:** 2 · **Duración estimada:** 35 minutos
**Módulo:** 2 — Ingeniería de instrucciones
**Patrón:** Modo socrático — Copilot pregunta de a una para construir contexto

---

## La situación

Laura es ejecutiva de cuentas en una empresa de software. Tiene que entregar una propuesta comercial para un cliente nuevo antes del viernes. El problema no es escribirla — es que no sabe bien por dónde empezar. Tiene información dispersa en la cabeza: el nombre del cliente, algo del presupuesto, una idea de lo que necesitan.

La mayoría de los usuarios en esta situación hacen una de dos cosas:

- **Opción A:** Le dan a Copilot toda la información de golpe en un prompt largo y desordenado. El resultado es una propuesta genérica que no refleja nada real.
- **Opción B:** No saben qué poner y le piden a Copilot que "redacte una propuesta". El resultado es peor todavía — Copilot inventa el cliente, el producto y el contexto.

Laura va a usar una tercera opción: **pedirle a Copilot que la entreviste**.

---

## ¿Qué es el modo socrático?

Es una técnica de prompting donde en lugar de darle toda la información a Copilot de entrada, le pedís que te haga preguntas de a una para extraer lo que necesita.

**¿Por qué de a una?** Porque si le pedís que haga todas las preguntas juntas, te devuelve un formulario de 15 ítems y el flujo se rompe. Una pregunta por vez simula una conversación real con un consultor — pensás mejor, respondés con más detalle y el contexto que construís es mucho más rico.

El resultado final es una propuesta que refleja información real tuya, no suposiciones del modelo.

---

## Paso 1 — Activar el modo socrático

🌐 **URL:** https://m365.cloud.microsoft

Abrí Copilot y escribí exactamente este prompt:

```
Voy a redactar una propuesta comercial para un cliente nuevo
y quiero que me ayudes a construirla con información real.

Para hacerlo bien, necesito que me hagas preguntas de a una,
esperando mi respuesta antes de hacer la siguiente.
No me hagas más de una pregunta a la vez.
Cuando tengas suficiente información, avisame y generá la propuesta.

Empezá con la primera pregunta.
```

> **Nota didáctica:** La instrucción clave es *"de a una, esperando mi respuesta"*. Sin esa aclaración, Copilot tiende a listar todas las preguntas juntas. Esa sola frase cambia completamente la dinámica de la conversación — de formulario a entrevista.

---

## Paso 2 — La entrevista

Copilot va a empezar a preguntarte. Respondé con información real de tu trabajo o, si preferís, usá este escenario ficticio como guía:

> **Escenario de referencia:**
> - Cliente: Grupo Meridian, empresa de logística con 300 empleados
> - Problema: sus procesos de seguimiento de envíos son manuales y generan errores
> - Solución que ofrecés: plataforma de gestión de envíos en tiempo real
> - Presupuesto del cliente: entre USD 15.000 y USD 25.000
> - Plazo de implementación deseado: 3 meses
> - Decisor: Gerente de Operaciones
> - Diferencial de tu empresa: soporte 24/7 y migración de datos incluida

Respondé cada pregunta con el nivel de detalle que tendrías en una situación real. No respondas con una sola palabra — si Copilot te pregunta por el cliente, contale el contexto, no solo el nombre.

> **Observá cómo Copilot va construyendo contexto.** Cada respuesta tuya alimenta las preguntas siguientes. Si en algún momento te hace una pregunta que ya respondiste implícitamente, podés decirle: *"Eso ya lo mencioné antes, pasá a la siguiente"*.

---

## Paso 3 — El momento de generación

En algún punto Copilot va a decirte que tiene suficiente información y te va a ofrecer generar la propuesta. Cuando eso pase, pedile que la abra en Canvas:

```
Perfecto. Generá la propuesta y abrila en una página para editar.
```

La propuesta debe incluir al menos:
- Resumen ejecutivo
- Diagnóstico del problema del cliente
- Solución propuesta
- Propuesta de valor y diferenciales
- Inversión y condiciones comerciales
- Próximos pasos

Si falta alguna sección, pedila puntualmente:

```
Falta la sección de próximos pasos. Agregala al final con 3 acciones concretas
y un plazo para cada una.
```

---

## Paso 4 — Comparar con el prompt directo

Ahora vamos a hacer el experimento de control. Abrí una conversación nueva y escribí:

```
Redactá una propuesta comercial para un cliente de logística
que necesita una plataforma de gestión de envíos.
```

**Comparé los dos resultados:**

| Criterio | Modo socrático | Prompt directo |
|---|---|---|
| ¿Menciona el nombre del cliente? | | |
| ¿Refleja el problema real? | | |
| ¿Incluye el presupuesto real? | | |
| ¿Tiene diferenciales reales de tu empresa? | | |
| ¿Lo enviarías a un cliente sin editar? | | |

> **Lo que vas a ver:** la propuesta del prompt directo es genérica, correcta en estructura pero vacía de contenido real. La del modo socrático tiene nombre del cliente, problema específico, cifras reales y diferenciales concretos. Son el mismo modelo, el mismo prompt de generación — la diferencia es el contexto que construiste antes.

---

## Paso 5 — Refinar en Canvas

Con la propuesta socrática abierta en Canvas, practicá al menos dos ediciones quirúrgicas:

**Ajuste de tono:**
```
La sección de "Propuesta de valor" suena muy genérica.
Reescribila destacando específicamente el diferencial del soporte 24/7
y la migración de datos incluida. No toques el resto.
```

**Agregar urgencia:**
```
Agregá al final de "Próximos pasos" una nota breve sobre
la validez de la propuesta (30 días) y un call to action
para agendar una reunión de cierre esta semana.
```

---

## Preguntas de reflexión para el grupo

1. ¿En qué otras situaciones de tu trabajo usarías el modo socrático? (briefings, planes, análisis...)
2. ¿Qué pasaría si le respondés a Copilot con información vaga o incompleta?
3. ¿Cuánto tiempo te llevó construir esta propuesta vs. hacerla desde cero en Word?

---

## El aprendizaje clave

El modo socrático invierte la dinámica habitual. Normalmente vos pensás cómo pedirle algo a Copilot. Acá Copilot te ayuda a pensar qué información necesitás para que el resultado sea bueno.

Es una técnica especialmente poderosa para documentos donde el contexto lo es todo — propuestas, briefings, planes de proyecto, análisis de situación. Cualquier documento donde una respuesta genérica no sirve.

**La calidad del output no depende solo de lo que le pedís. Depende de cuánto contexto real lograste construir antes de pedirlo.**

---

## Próximo lab

**Lab — Productividad en Excel:** llevamos la lógica de construcción progresiva al análisis de datos.

---

*Material desarrollado por MCT Esteban Calabria · https://linkedin.com/in/esteban-calabria*
