# Transcripción — Reunión de Kickoff: Implementación Sistema de Control de Cadastros

**Fecha:** martes 3 de marzo de 2026, 10:00 hs
**Modalidad:** Presencial / Sala de reuniones 2
**Participantes:**
- Marcela Risso (Líder de Proyecto, Administración Logística)
- Fabiana Zetoulian (Finanzas)
- Nicolas Tilve (Operaciones)
- Ignacio Gil (Sistemas / Desarrollo)
- Valentina Cuñetti (QA / Control de Calidad)

---

**Marcela Risso:** Buenos días a todos, gracias por venir. La idea de hoy es arrancar formalmente el proyecto de automatización del control de cadastros y pedidos de venta que veníamos charlando con Fabiana. Quiero que salgamos de acá con un cronograma claro, con responsables y fechas.

**Fabiana Zetoulian:** Perfecto. Del lado de Finanzas, lo primero que necesitamos es relevar los cuatro controles que ya veníamos haciendo manualmente: concordancia de VIA y DUA, operativas masivas, volumen marítimo y modificaciones de cadastros. Calculo que el relevamiento y la documentación de las reglas actuales nos puede llevar una semana, del 4 al 10 de marzo.

**Marcela Risso:** De acuerdo. Anoto: "Relevamiento de reglas de control", del 4 al 10 de marzo, a cargo de Fabiana.

**Ignacio Gil:** Una vez que tengamos ese relevamiento, desde Sistemas podemos empezar el diseño técnico. Necesitamos entender de dónde sale la data: ODOO por un lado y DIM por otro. Le calculo unos cinco días hábiles a partir del 11 de marzo, o sea que terminaríamos el 17.

**Marcela Risso:** "Diseño técnico de integración ODOO–DIM", del 11 al 17 de marzo, a cargo de Ignacio.

**Nicolas Tilve:** Desde Operaciones queremos sumarnos en paralelo con el tema de los cadastros de mercadería, porque nosotros somos los que después analizamos las variaciones significativas junto con Administración. Podemos empezar a definir los umbrales de variación aceptables la misma semana que arranca Ignacio, del 11 al 14 de marzo, es más corto.

**Marcela Risso:** Anotado: "Definición de umbrales de variación en cadastros", del 11 al 14 de marzo, a cargo de Nicolas.

**Ignacio Gil:** Con el diseño cerrado, el desarrollo del módulo de control automático lo estimo en tres semanas. Arrancaríamos el 18 de marzo y estaríamos cerrando el 7 de abril.

**Marcela Risso:** "Desarrollo del módulo de control automático", del 18 de marzo al 7 de abril, a cargo de Ignacio y su equipo.

**Valentina Cuñetti:** Yo necesito al menos una semana antes de terminar el desarrollo para preparar los casos de prueba, así que puedo arrancar el 31 de marzo con el armado de los casos, en paralelo con la última parte del desarrollo. Eso lo tengo listo para el 4 de abril.

**Marcela Risso:** "Preparación de casos de prueba", del 31 de marzo al 4 de abril, a cargo de Valentina.

**Valentina Cuñetti:** Y ya con el módulo cerrado, las pruebas funcionales en sí las estimo en una semana, del 8 al 14 de abril.

**Marcela Risso:** "Pruebas funcionales (QA)", del 8 al 14 de abril, a cargo de Valentina.

**Fabiana Zetoulian:** En paralelo a esa semana de pruebas, nosotros en Finanzas queremos hacer una validación en paralelo con el proceso manual, para comparar resultados antes de confiar ciegamente en el sistema. Lo hacemos la misma semana, del 8 al 14 de abril.

**Marcela Risso:** "Validación en paralelo (manual vs. automático)", del 8 al 14 de abril, a cargo de Fabiana.

**Ignacio Gil:** Si todo sale bien en las pruebas, el pase a producción y la puesta en marcha los podemos hacer el 15 y 16 de abril.

**Marcela Risso:** "Pase a producción", 15 al 16 de abril, a cargo de Ignacio.

**Nicolas Tilve:** Y para que esto no se caiga en un mes, propongo una capacitación breve al equipo de Administración Logística y Operaciones antes de que el sistema quede como único método de control. La podemos hacer el 17 de abril, medio día.

**Marcela Risso:** "Capacitación a usuarios finales", 17 de abril, a cargo de Nicolas.

**Marcela Risso:** Perfecto, entonces con esto ya tenemos el esqueleto del proyecto. Cierro la reunión: cualquier corrimiento de fecha me lo avisan a mí directamente así actualizo el cronograma. Nos vemos la semana que viene para el primer seguimiento.

**Fin de la reunión — 10:47 hs**

---

