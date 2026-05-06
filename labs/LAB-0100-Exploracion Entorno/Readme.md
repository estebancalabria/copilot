# Lab 1A — Exploración del entorno

**Sesión:** 1 · **Duración estimada:** 30 minutos  
**Módulo:** 1 — Arquitectura, seguridad y fundamentos

---

## Objetivo

Acceder a Microsoft Copilot desde tres superficies distintas (web, Teams y mobile), explorar qué información del entorno ya tiene disponible el modelo, y documentar en tiempo real qué datos propios puede ver Copilot hoy.

> **¿Para qué sirve este lab?**  
> Antes de usar Copilot para trabajar, es fundamental entender *qué ve* el modelo. Copilot no es un chatbot genérico — tiene acceso a tu correo, tus archivos, tu calendario y tus conversaciones de Teams a través de **Microsoft Graph**. Este lab te hace consciente de ese contexto antes de empezar a hacer prompts.

---

## ¿Qué es Microsoft Graph?

**Microsoft Graph** es la API central de Microsoft 365. Funciona como el sistema nervioso de todo el ecosistema: conecta usuarios, correos, archivos, calendarios, chats de Teams, tareas y más bajo un único punto de acceso.

Cuando le hacés una pregunta a Copilot sobre "mis correos de esta semana" o "el documento que edité ayer", Copilot no adivina — consulta Microsoft Graph en tiempo real con tus permisos. Esto significa que Copilot **solo ve lo que vos tenés permiso de ver**. Nada más, nada menos.

```
[Vos] → [Copilot] → [Microsoft Graph] → [Correo / Archivos / Calendario / Teams]
```

---

## Preparación previa (antes de empezar)

Asegurate de tener a mano:

- [ ] Tu usuario y contraseña de Microsoft 365
- [ ] El celular con la app **Microsoft 365** o **Copilot** instalada
- [ ] Un navegador moderno (Edge recomendado, Chrome funciona igual)

---

## Paso 1 — Acceder a Copilot desde la web

🌐 **URL:** https://copilot.microsoft.com

1. Abrí el navegador y navegá a https://copilot.microsoft.com
2. Si no estás logueado, hacé clic en **Iniciar sesión** e ingresá con tu cuenta corporativa de Microsoft 365.
3. Verificá que en la esquina superior derecha aparezca tu nombre/avatar. Si aparece una cuenta personal (Outlook.com, Hotmail), cerrá sesión y volvé a ingresar con la cuenta corporativa.

> **⚠️ Diferencia importante:** Copilot en modo personal (sin sesión corporativa) no tiene acceso a Microsoft Graph. No ve tus archivos ni correos. Es un chatbot genérico. Cuando iniciás sesión con tu cuenta M365 + licencia Copilot, se activa el modo "Work" — ese es el que usamos en este taller.

4. Fijate que en la barra inferior del chat aparezca un ícono de **complementos** o que el chat diga algo como *"Tengo acceso a tu organización"*. Esa es la señal de que Graph está conectado.

---

## Paso 2 — Tu primer prompt de contexto

En el chat de Copilot web, escribí exactamente este prompt:

```
¿Qué archivos he modificado o revisado recientemente? Listame los últimos 5 con fecha y tipo de documento.
```

Observá la respuesta:
- ¿Aparecen archivos reales tuyos?
- ¿Las fechas son correctas?
- ¿Reconocés los nombres de los documentos?

> **Nota didáctica:** Si Copilot dice que no tiene acceso a tus archivos o devuelve una respuesta genérica, puede significar que la licencia Copilot for M365 no está activa en tu cuenta, o que OneDrive/SharePoint están vacíos. Avisale al instructor.

---

## Paso 3 — Crear un archivo de prueba en OneDrive

Para asegurarnos de que Copilot tiene algo que ver en tiempo real, vamos a crear un archivo.

🌐 **URL:** https://onedrive.live.com  
*(o desde el portal M365: https://www.microsoft365.com → OneDrive)*

1. Abrí OneDrive en una pestaña nueva.
2. Hacé clic en **+ Nuevo → Documento de Word**.
3. Escribí algunas líneas de texto libre — puede ser cualquier cosa, por ejemplo:

   ```
   Reunión de planificación Q3
   Temas: presupuesto, recursos humanos, lanzamiento de producto.
   Responsables: equipo comercial y producto.
   ```

4. El archivo se guarda automáticamente. Fijate el nombre que le asigna (por defecto "Documento") — podés renombrarlo a algo reconocible como `prueba-lab-copilot`.
5. Cerrá la pestaña de Word.

---

## Paso 4 — Verificar que Copilot ya lo ve

Volvé a la pestaña de Copilot web (https://copilot.microsoft.com) y escribí:

```
¿Qué dice el documento que acabo de crear en OneDrive? Se llama "prueba-lab-copilot".
```

> **¿Qué esperamos ver?** Copilot debería poder leer el contenido del archivo que acabás de crear. Esto demuestra en tiempo real que Microsoft Graph está operando — Copilot consultó tu OneDrive y encontró el archivo sin que vos se lo "mandaras" ni adjuntaras nada.

---

## Paso 5 — Explorar el contexto de correo

Ahora vamos a ver qué sabe Copilot de tu bandeja de entrada.

En el mismo chat, escribí:

```
¿De quién recibí correos esta semana? Dame un resumen de los remitentes más frecuentes y los temas principales.
```

Luego probá este segundo prompt:

```
¿Tengo alguna reunión pendiente para los próximos 3 días? ¿De qué tratan?
```

> **Nota didáctica:** Copilot está consultando Exchange Online (tu correo) y el calendario de Microsoft 365 a través de Graph. No está accediendo a ningún servidor externo — todo queda dentro del tenant de tu organización, bajo las políticas de seguridad de Entra ID.

---

## Paso 6 — Acceder desde Microsoft Teams

🌐 **URL:** https://teams.microsoft.com  
*(o desde la app de escritorio de Teams)*

1. Abrí Teams.
2. En el panel izquierdo, buscá el ícono de **Copilot** (puede estar fijado o en la sección "Más aplicaciones").
3. Abrí Copilot dentro de Teams y escribí:

   ```
   Resumí las últimas conversaciones de Teams que tuve esta semana. ¿Hay algo pendiente de responder?
   ```

> **¿Qué cambia respecto a la versión web?** El Copilot dentro de Teams tiene acceso adicional al historial de chats y reuniones del tenant. Es la misma IA, pero con más contexto de colaboración disponible.

---

## Paso 7 — Acceder desde el celular

En tu smartphone:

1. Abrí la app **Microsoft Copilot** (disponible en App Store y Google Play) o la app de **Microsoft 365**.
2. Iniciá sesión con tu cuenta corporativa.
3. Escribí este prompt:

   ```
   ¿Cuál fue lo último que trabajé? Dame un resumen rápido de mi actividad de hoy.
   ```

> **Nota:** La experiencia mobile es idéntica en capacidad a la web. Sirve especialmente para consultas rápidas fuera de la computadora — revisar un documento antes de una reunión, buscar un correo en el taxi, etc.

---

## Paso 8 — Documentar lo que descubriste

En el chat de Copilot (en cualquier superficie), escribí este prompt final:

```
Hacé un resumen de todo lo que pudiste ver de mi entorno en esta conversación: archivos, correos, calendario y chats. Presentalo como una lista organizada por categoría.
```

Copiá esa respuesta en un documento o en el chat del equipo — es tu **mapa de contexto personal de Copilot**.

---

## Preguntas de reflexión para el grupo

Al terminar el lab, el instructor abre una discusión breve:

1. ¿Qué te sorprendió de lo que Copilot podía ver?
2. ¿Hay algo que esperabas que viera y no vio?
3. ¿Qué implicancias de privacidad interna identificás? (¿Puede un compañero preguntarle a Copilot por tus archivos?)

> **Spoiler de la pregunta 3:** No. Copilot respeta los permisos de Microsoft 365. Si un archivo no es compartido con alguien, Copilot no se lo va a mostrar aunque le pregunten. El modelo opera siempre dentro del scope de permisos del usuario autenticado.

---

## Resumen del lab

| Superficie | Lo que exploraste |
|---|---|
| Copilot Web | Archivos recientes, documento de OneDrive creado en tiempo real |
| Copilot en Teams | Historial de chats y reuniones |
| Copilot Mobile | Actividad reciente, acceso desde cualquier lugar |
| Correo y calendario | Remitentes frecuentes, reuniones próximas |

---

## Próximo lab

**Lab 1B — Anatomía de un prompt:** ahora que sabés qué ve Copilot, vas a aprender a pedirle las cosas de forma que obtengas exactamente lo que necesitás.

---

*Material desarrollado por MCT Esteban Calabria · https://linkedin.com/in/esteban-calabria*
