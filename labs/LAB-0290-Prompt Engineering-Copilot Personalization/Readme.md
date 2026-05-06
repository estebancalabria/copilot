# Lab — Instrucciones personalizadas y memoria

**Sesión:** 2 · **Duración estimada:** 30 minutos
**Módulo:** 2 — Ingeniería de instrucciones
**Patrón:** Personalización persistente — Memoria + Instrucciones personalizadas

---

## La situación

Hasta ahora le explicaste a Copilot quién sos y cómo querés que te responda en cada prompt. Eso funciona, pero tiene un problema: tenés que repetirlo cada vez.

Un usuario avanzado no repite. Configura una sola vez y Copilot se adapta solo.

En este lab vas a descubrir que Copilot sabe cosas sobre vos que nunca le contaste directamente — y después le vas a cambiar la personalidad de una forma que no vas a olvidar.

---

## Paso 1 — El roast: qué sabe Copilot de vos

Antes de tocar cualquier configuración, vamos a ver qué tiene Copilot en memoria sobre vos en este momento.

🌐 **URL:** https://m365.cloud.microsoft

1. Abrí Copilot desde el portal de Microsoft 365.
2. Escribí exactamente este prompt:

```
Haceme un roast basado en todo lo que sabés de mí.
Usá lo que recordás de conversaciones anteriores, mis archivos,
mi forma de escribir, mis temas frecuentes — todo.
Sé creativo, directo y un poco despiadado. Máximo 10 líneas.
```

> **¿Qué es un roast?** Es una crítica humorística y exagerada. En este contexto, si Copilot tiene memoria de conversaciones anteriores, va a usar esa información para hacer chistes sobre tus hábitos, tus temas de trabajo o tu forma de pedir cosas. Si no tiene memoria previa, va a ser genérico — y eso también es información útil.

**Compartí el resultado con el grupo.** El que tenga el roast más certero gana el punto.

---

## Paso 2 — Ver qué tiene guardado en memoria

Ahora vamos a inspeccionar formalmente qué recuerda Copilot sobre vos.

```
¿Qué recordás sobre mí de conversaciones anteriores?
Listame todo lo que tenés en memoria: preferencias, temas frecuentes,
forma de trabajo, cualquier dato que hayas guardado.
```

**Observá:**
- ¿Hay datos que reconocés de conversaciones pasadas?
- ¿Hay algo que te sorprende que haya guardado?
- ¿Hay algo incorrecto o desactualizado?

> **Nota didáctica:** La memoria de Copilot funciona de forma similar a la de ChatGPT — extrae información relevante de las conversaciones y la guarda para personalizar futuras respuestas. Esto es muy útil, pero también implica responsabilidad: si le contás algo sensible, puede recordarlo. Los administradores de tenant pueden controlar y deshabilitar esta función desde el admin center.

---

## Paso 3 — Configurar instrucciones personalizadas

Ahora vamos a la configuración real. Acá es donde le decís a Copilot cómo querés que te responda **siempre**, sin tener que pedirlo en cada prompt.

**Cómo acceder:**

1. En Copilot web (m365.cloud.microsoft), hacé clic en los **tres puntos (…)** del menú superior o lateral
2. Seleccioná **Configuración** (Settings)
3. Andá a **Personalización** (Personalization)
4. Seleccioná **Instrucciones personalizadas** (Custom instructions)
5. Editá el campo de texto

> **Si no encontrás la opción:** dependiendo de la versión y configuración del tenant, puede estar en un lugar ligeramente distinto. También podés acceder desde el ícono de perfil → Configuración → Personalización.

**Escribí estas instrucciones como punto de partida:**

```
- Respondeme siempre en español rioplatense, informal.
- Preferí listas con viñetas sobre párrafos largos.
- Cuando resumas documentos, empezá siempre por el punto más importante.
- Evitá frases de relleno como "¡Claro!" o "¡Por supuesto!".
- Si no sabés algo, decilo directamente sin rodeos.
- Mi rol es [completá con tu rol real].
- Trabajo principalmente en [completá con tu área o industria].
```

Guardá los cambios.

---

## Paso 4 — Verificar que las instrucciones funcionan

Abrí una conversación nueva y escribí un prompt neutro, sin dar ninguna instrucción de formato:

```
Explicame en qué consiste la gestión del cambio organizacional.
```

**Verificá:**
- ¿Usó el formato que pediste (viñetas)?
- ¿Evitó las frases de relleno?
- ¿El tono coincide con lo que configuraste?

Si algo no se aplicó, ajustá las instrucciones y volvé a probar. Las instrucciones personalizadas se pueden iterar exactamente igual que los prompts.

---

## Paso 5 — El experimento: Copilot que responde en poema

Ahora la parte que no vas a olvidar. Vamos a cambiar las instrucciones personalizadas para que Copilot responda en un formato completamente distinto.

**Volvé a Configuración → Instrucciones personalizadas y reemplazá todo con esto:**

```
Respondé siempre en forma de poema con rima consonante.
No importa la pregunta — la respuesta debe ser un poema.
Mantené la información correcta pero expresala en verso.
Máximo 12 líneas por respuesta.
```

Guardá. Abrí una conversación nueva y escribí:

```
¿Cuáles son las mejores prácticas para gestionar un proyecto de software?
```

> **Lo que vas a ver:** Copilot va a responderte con las mejores prácticas reales de gestión de proyectos... pero en poema con rima. La información es correcta, el formato es completamente distinto. Eso demuestra que las instrucciones personalizadas no cambian lo que sabe el modelo — cambian cómo lo expresa.

Probá una segunda pregunta cualquiera para confirmar que el comportamiento persiste:

```
Resumime los beneficios de trabajar con metodologías ágiles.
```

**Compartí el poema con el grupo.** El más creativo o el más absurdo gana.

---

## Paso 6 — Restaurar las instrucciones

Antes de terminar el lab, volvé a Configuración → Instrucciones personalizadas y configurá las instrucciones reales que querés usar en tu trabajo diario.

Como punto de partida, podés usar este prompt para que el propio Copilot te ayude a escribirlas:

```
Ayudame a escribir un bloque de instrucciones personalizadas para Copilot.
Mi rol es [tu rol], trabajo en [tu industria o área], mis tareas más frecuentes
son [listá 2 o 3]. Quiero que las respuestas sean [tono y formato que preferís].
Generá las instrucciones listas para copiar y pegar.
```

---

## Preguntas de reflexión para el grupo

1. ¿Qué te sorprendió del roast? ¿Copilot sabía más o menos de lo que esperabas?
2. ¿Qué instrucciones personalizadas serían más útiles para tu trabajo real?
3. ¿Qué riesgos ves en que Copilot guarde memoria en un entorno corporativo?

---

## El aprendizaje clave

La mayoría de los usuarios de Copilot escriben las mismas instrucciones de formato en cada prompt. Eso es trabajo repetido. Las instrucciones personalizadas y la memoria existen para que configures el comportamiento del modelo una sola vez y lo olvides — igual que configurás la firma automática del correo.

La diferencia entre un usuario básico y un usuario avanzado no está en los prompts que escribe. Está en los prompts que **ya no necesita escribir**.

---

## Próximo lab

**Lab — Productividad en Word:** ahora que Copilot ya sabe cómo querés que te responda, vamos a llevarlo a las apps de M365.

---

*Material desarrollado por MCT Esteban Calabria · https://linkedin.com/in/esteban-calabria*
