# Laboratorio: Resumen de Gestión con Cuadernos de Microsoft 365 Copilot

## Objetivo

Generar un informe ejecutivo a partir de múltiples documentos utilizando un Cuaderno de Microsoft 365 Copilot.

---

# Paso 1 - Crear el cuaderno

1. Abrí Microsoft 365 Copilot.
2. En el panel izquierdo seleccioná **Cuadernos**.
3. Hacé clic en **Nuevo cuaderno**.
4. Asigná el nombre:

```text
Horizonte 2027 - Septiembre 2026
```

---

# Paso 2 - Incorporar las fuentes

1. Hacé clic en **Agregar contenido**.
2. Incorporá los archivos:
   - M01
   - M02
   - M03
   - M04
   - M05
   - M06
   - M07
   - M08
   - M09

3. Esperá a que el cuaderno procese los archivos.

---

> [!NOTE]
> Poner instrucciones del ccuaderno

```
Actúa como analista documental y PMO.

Trabaja únicamente con la información contenida en las fuentes incorporadas al cuaderno.

Reglas:

- No inventes información.
- No completes datos faltantes por inferencia.
- Si una información no puede verificarse, indícalo explícitamente.
- Identifica siempre la fuente documental utilizada cuando sea posible.
- Señala contradicciones entre documentos.
- Diferencia claramente hechos, supuestos y observaciones.
- Indica cuando existan varias versiones de un mismo documento.
- Conserva fechas, responsables y estados exactamente como aparecen en las fuentes.
- Si falta información para responder una solicitud, indícalo en lugar de asumirla.

Cuando generes resúmenes o informes:

- Prioriza información confirmada.
- Agrupa contenido relacionado proveniente de varios documentos.
- Identifica riesgos, acuerdos, decisiones y acciones pendientes.
- Señala cualquier dato que requiera validación manual.
```

# Paso 3 - Comprender el contenido

## Objetivo

Verificar qué información contiene el cuaderno.

## Prompt

```text
Resume el contenido del cuaderno.

Indica:

- Qué documentos contiene.
- Qué temas trata.
- Qué documentos parecen estar relacionados entre sí.
- Qué documentos no parecen pertenecer al proyecto.
```

---

# Paso 4 - Detectar inconsistencias

## Objetivo

Identificar problemas en la documentación antes de generar el informe.

## Prompt

```text
Analiza los documentos del cuaderno.

Indica:

- Documentos duplicados.
- Versiones reemplazadas.
- Información incompleta.
- Acuerdos sin responsable.
- Acuerdos sin fecha.
- Información que requiera validación.
```

---

# Paso 5 - Generar el informe ejecutivo

## Objetivo

Crear un borrador consolidado.

## Prompt

```text
Genera un informe ejecutivo de avance para septiembre de 2026 utilizando únicamente la información del cuaderno.

Incluye:

- Resumen ejecutivo
- Hechos relevantes
- Acuerdos
- Riesgos
- Próximos pasos
- Pendientes de información

Indica siempre la fuente cuando sea posible.

Comienza el documento con la palabra BORRADOR.
```

> [!NOTE]
> Para revisar el resultado generar una pagina

---

# Paso 6 - Revisar el resultado

## Objetivo

Validar el trabajo realizado por la IA.

## Prompt

```text
Revisa el informe generado.

Indica:

- Información que no pueda verificarse.
- Acuerdos con datos incompletos.
- Riesgos que requieran seguimiento.
- Posibles errores o inconsistencias.
```

---

# Paso 7 - Mejorar el informe

## Objetivo

Aplicar correcciones.

## Prompt

```text
Actualiza el informe considerando las observaciones detectadas durante la revisión.

Muestra nuevamente la versión completa.
```

---

# Paso 8 - Crear el documento final

## Objetivo

Generar el entregable.

## Prompt

```text
Crea un documento Word con la última versión del informe.

No agregues información nueva.
```

---

---

# Paso 9 - Preparar el contexto para Researcher

## Objetivo

Generar un resumen autocontenido con la información necesaria para realizar posteriormente un análisis estratégico con Researcher.

## Prompt

```text
A partir de toda la información disponible en el cuaderno, genera un resumen ejecutivo autocontenido del proyecto Horizonte 2027.

El resumen debe incluir:

- Objetivo y meta del proyecto.
- Período analizado.
- Estado actual del proyecto.
- Principales hechos e hitos.
- Acuerdos cumplidos.
- Acuerdos abiertos.
- Riesgos vigentes y sus posibles efectos.
- Próximos pasos, con responsables y fechas cuando estén disponibles.
- Información pendiente de confirmar.
- Versiones de documentos utilizadas.

El resultado debe poder comprenderse sin consultar el cuaderno ni los documentos originales.

No agregues información que no figure en las fuentes.

No completes datos faltantes por tu cuenta.

Distingue claramente entre:
- datos confirmados
- fechas estimadas
- información pendiente

Limita la respuesta a un máximo de 800 palabras.
```

## Resultado esperado

Un resumen autocontenido que reúna el contexto necesario para que Researcher pueda analizar el estado del proyecto sin acceder directamente al cuaderno.

---

# Paso 10 - Copiar el contexto

## Objetivo

Trasladar la información consolidada desde el cuaderno hacia Researcher.

## Instrucciones

1. Revisá el resumen generado en el paso anterior.
2. Verificá que no incluya información inventada.
3. Comprobá que las fechas estimadas estén identificadas como estimadas.
4. Comprobá que los datos faltantes aparezcan como pendientes.
5. Copiá el resumen completo.
6. Salí del cuaderno.
7. Abrí el agente **Researcher** desde Microsoft 365 Copilot.
8. Iniciá una nueva conversación.

> Researcher se utiliza como una experiencia separada. No se invoca desde el cuaderno mediante `@Researcher`.

---

# Paso 11 - Analizar el proyecto con Researcher

## Objetivo

Analizar el estado del proyecto desde la perspectiva de un comité de dirección y contrastarlo con buenas prácticas externas.

## Instrucciones

1. En la conversación nueva con Researcher, pegá el siguiente prompt.
2. Reemplazá `[PEGAR AQUÍ EL RESUMEN]` por el resumen generado en el paso 9.
3. Ejecutá la investigación.

## Prompt

```text
Analiza el siguiente resumen del proyecto Horizonte 2027 desde la perspectiva de un comité de dirección de una empresa de energía.

RESUMEN DEL PROYECTO

[PEGAR AQUÍ EL RESUMEN]

TAREA

Determina si la información disponible permite concluir que el proyecto está bajo control.

Identifica:

1. Preguntas críticas que el comité debería formular antes de aprobar el siguiente hito.

2. Riesgos mencionados cuyo impacto, probabilidad, responsable o plan de mitigación no estén suficientemente documentados.

3. Información faltante necesaria para tomar decisiones.

4. Supuestos del informe que deberían validarse.

5. Posibles señales tempranas de desvíos de plazo, coste o alcance.

6. Acciones de seguimiento recomendadas.

INVESTIGACIÓN EXTERNA

Investiga buenas prácticas actuales relacionadas con:

- gobierno de proyectos
- gestión de riesgos
- control de cronogramas
- gestión de dependencias críticas
- seguimiento de contratistas
- campañas de perforación con múltiples pozos

Compara esas buenas prácticas con la situación descrita en el resumen.

No trates las buenas prácticas externas como hechos específicos del proyecto.

Distingue claramente entre:

- hechos aportados por el resumen
- conclusiones derivadas del análisis
- información obtenida mediante investigación externa
- recomendaciones

PRIORIZACIÓN

Clasifica cada hallazgo según:

- Impacto: Alto, Medio o Bajo.
- Urgencia: Alta, Media o Baja.

Justifica brevemente cada clasificación.

FORMATO

Presenta el resultado como un briefing ejecutivo con estas secciones:

1. Conclusión general sobre el estado del proyecto.
2. Hallazgos prioritarios.
3. Preguntas para el comité de dirección.
4. Riesgos insuficientemente analizados.
5. Información faltante.
6. Comparación con buenas prácticas externas.
7. Acciones de seguimiento recomendadas.
8. Fuentes externas consultadas.

Incluye referencias a las fuentes externas utilizadas.

No inventes datos específicos sobre Horizonte 2027 que no estén incluidos en el resumen.
```

---

# Paso 12 - Revisar la investigación

## Objetivo

Diferenciar los hechos del proyecto de los aportes realizados por Researcher.

## Prompt

```text
Revisa el briefing generado y clasifica sus afirmaciones en cuatro grupos:

1. Hechos provenientes del resumen del proyecto.
2. Conclusiones derivadas del análisis.
3. Información obtenida de fuentes externas.
4. Recomendaciones.

Para cada afirmación indica:

- categoría
- prioridad
- evidencia o fuente
- si requiere validación adicional

No agregues nuevos hallazgos.
```

## Controles

Verificá que:

- Los hechos del proyecto coincidan con el resumen proporcionado.
- Las conclusiones estén claramente identificadas como análisis.
- Las buenas prácticas externas incluyan fuentes.
- Las recomendaciones no se presenten como decisiones aprobadas.
- Researcher no haya inventado fechas, responsables, costes o estados del proyecto.
- Las fuentes externas sean pertinentes para el análisis.

---

# Paso 13 - Preparar el briefing para el comité

## Objetivo

Convertir la investigación en una salida breve para una reunión de dirección.

## Prompt

```text
A partir del análisis anterior, genera una versión final del briefing para el comité de dirección.

Incluye únicamente:

- conclusión general
- cinco hallazgos prioritarios
- cinco preguntas críticas
- cinco acciones de seguimiento recomendadas
- información pendiente necesaria para decidir

Para cada hallazgo indica:

- impacto
- urgencia
- evidencia disponible
- validación pendiente

Distingue los hechos del proyecto de las recomendaciones basadas en buenas prácticas externas.

No agregues información nueva.

Limita el briefing a un máximo de 800 palabras.
```

## Resultado esperado

Un briefing ejecutivo priorizado que complemente el informe de avance con:

- preguntas para la dirección
- riesgos que necesitan mayor análisis
- información pendiente para decidir
- comparación con buenas prácticas externas
- acciones de seguimiento recomendadas

---

# Conclusión del laboratorio

En este laboratorio se utilizaron dos experiencias diferentes:

- **Cuadernos de Microsoft 365 Copilot:** para reunir fuentes, comprender el contenido, detectar problemas documentales y generar el informe de avance.
- **Researcher:** para analizar el resumen consolidado, investigar buenas prácticas externas y preparar preguntas y recomendaciones para el comité de dirección.

El resumen generado en el cuaderno funciona como puente entre ambas experiencias.

Researcher no reemplaza la validación humana ni convierte sus recomendaciones en decisiones aprobadas. La revisión y la decisión final corresponden a las personas responsables.
