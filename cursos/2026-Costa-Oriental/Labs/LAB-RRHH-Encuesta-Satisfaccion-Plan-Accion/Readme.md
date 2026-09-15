# Laboratorio 3: Generación de Planes de Acción a partir de Encuestas con Microsoft 365 Copilot

## Objetivo

Utilizar Microsoft 365 Copilot para:

- Diseñar una encuesta para medir la satisfacción de los participantes en los programas de Costa Oriental.
- Crear automáticamente la estructura de la encuesta.
- Generar datos ficticios para simular las respuestas recibidas.
- Analizar los resultados con Copilot para Excel.
- Detectar problemas, tendencias y oportunidades de mejora.
- Convertir los hallazgos en un plan de acción.
- Elaborar un informe ejecutivo para los responsables del programa.

---

# Escenario

Costa Oriental desarrolla programas, talleres y charlas dirigidos a colaboradores, clientes y otros grupos de interés.

Después de cada actividad se recopilan opiniones de los participantes, pero las preguntas, los criterios de evaluación y el análisis de los resultados no siempre siguen un formato estandarizado.

El área responsable desea utilizar Microsoft 365 Copilot para crear una encuesta modelo, analizar las respuestas y generar planes de acción basados en los resultados obtenidos.

En este laboratorio se trabajará con un programa ficticio denominado:

```text
Programa de Capacitación en Operaciones Logísticas Seguras
```

---

# Parte 1 – Diseñar la encuesta con Copilot

## Paso 1

Abrir Microsoft 365 Copilot Chat.

Utilizar el siguiente prompt:

```text
Trabajo en Costa Oriental, una empresa logística y de distribución.

Necesito evaluar un programa denominado "Programa de Capacitación en Operaciones Logísticas Seguras".

Diseña una encuesta estandarizada para conocer la opinión de los participantes.

La encuesta debe permitir evaluar:

- Calidad general de la actividad.
- Claridad de los contenidos.
- Utilidad de los conocimientos adquiridos.
- Aplicabilidad en el puesto de trabajo.
- Desempeño del facilitador.
- Calidad de los materiales.
- Duración de la actividad.
- Organización.
- Probabilidad de recomendar la actividad.
- Comentarios y sugerencias.

Utiliza preguntas con una escala de valoración del 1 al 5 cuando corresponda.

Incluye también preguntas para identificar:

- Área del participante.
- Cargo o función.
- Modalidad de participación.
- Aspectos más valorados.
- Aspectos que deberían mejorarse.

Devuelve la encuesta completa e indica el tipo de respuesta recomendado para cada pregunta.
```

---

## Resultado esperado

Copilot generará una propuesta completa de encuesta, incluyendo preguntas de valoración, selección y respuesta abierta.

Revisar la propuesta y comprobar que las preguntas permitan medir tanto la satisfacción como la utilidad y aplicabilidad de la actividad.

---

# Parte 2 – Crear la encuesta en Microsoft Forms

## Paso 2

Abrir Microsoft Forms.

Seleccionar la opción para crear un nuevo formulario con Copilot.

Utilizar el siguiente prompt:

```text
Crea una encuesta para evaluar el "Programa de Capacitación en Operaciones Logísticas Seguras" de Costa Oriental.

Incluye preguntas para conocer el área, cargo y modalidad de participación.

Evalúa del 1 al 5:

- Calidad general.
- Claridad de los contenidos.
- Utilidad.
- Aplicabilidad en el puesto.
- Desempeño del facilitador.
- Calidad de los materiales.
- Duración.
- Organización.
- Probabilidad de recomendación.

Agrega preguntas abiertas para identificar los aspectos más valorados, las oportunidades de mejora y las sugerencias de los participantes.
```

---

## Paso 3

Revisar la encuesta generada por Copilot.

Comprobar:

- La redacción de las preguntas.
- Los tipos de respuesta.
- La escala utilizada.
- El carácter obligatorio u opcional de cada pregunta.
- El orden lógico de las secciones.
- La ausencia de preguntas duplicadas o ambiguas.

Realizar los ajustes que se consideren necesarios.

---

# Parte 3 – Preparar los datos de ejemplo

## Paso 4

Desde Microsoft Forms, abrir la pestaña de respuestas y utilizar la opción para exportar los resultados a Excel.

Si la encuesta todavía no tiene respuestas, crear un libro de Excel utilizando la misma estructura de columnas generada por el formulario.

Guardar el archivo como:

```text
Encuesta-Programa-Operaciones-Logisticas-Seguras.xlsx
```

---

## Paso 5

Abrir Copilot en Excel.

Utilizar el siguiente prompt:

```text
Completa esta tabla con 100 respuestas ficticias de participantes del "Programa de Capacitación en Operaciones Logísticas Seguras" de Costa Oriental.

Distribuye las respuestas entre participantes de:

- Depósito.
- Transporte.
- Operaciones.
- Administración.
- Atención al Cliente.

Incluye diferentes cargos y modalidades de participación.

Genera valoraciones realistas entre 1 y 5.

No utilices las mismas puntuaciones para todos los participantes.

Incluye resultados positivos y negativos que permitan identificar tendencias y oportunidades de mejora.

Completa también las respuestas abiertas con comentarios ficticios coherentes con las puntuaciones asignadas.
```

---

## Objetivo

Obtener un conjunto de datos de prueba que permita realizar el análisis completo sin proporcionar previamente a Copilot cuáles deberían ser los resultados.

---

# Parte 4 – Analizar los resultados en Excel

## Paso 6

En Copilot para Excel, utilizar el siguiente prompt:

```text
Analiza los resultados de esta encuesta.

Identifica:

- Promedio de cada aspecto evaluado.
- Aspectos con mayor valoración.
- Aspectos con menor valoración.
- Diferencias relevantes entre áreas.
- Diferencias según la modalidad de participación.
- Tendencias generales.
- Resultados atípicos que deberían revisarse.

Basa todas las conclusiones exclusivamente en los datos de la tabla.
```

---

## Paso 7

Solicitar a Copilot una representación visual de los resultados:

```text
Crea las visualizaciones más apropiadas para mostrar:

- La valoración promedio de cada aspecto.
- La comparación de resultados por área.
- La comparación según la modalidad de participación.
- Los tres aspectos mejor valorados.
- Los tres aspectos con mayores oportunidades de mejora.

Agrega títulos claros a los gráficos.
```

---

## Preguntas para discusión

- ¿Qué aspectos recibieron las valoraciones más bajas?
- ¿Los resultados son iguales en todas las áreas?
- ¿La modalidad de participación afecta la valoración?
- ¿Qué resultados requieren atención inmediata?
- ¿Qué información aportan los gráficos que no se observa fácilmente en la tabla?

---

# Parte 5 – Analizar los comentarios abiertos

## Paso 8

Utilizar el siguiente prompt:

```text
Analiza las respuestas abiertas de la encuesta.

Agrupa los comentarios por temas recurrentes.

Para cada tema indica:

- Cantidad de comentarios relacionados.
- Opiniones positivas.
- Opiniones negativas.
- Sugerencias realizadas por los participantes.
- Ejemplos representativos, sin incluir nombres ni datos personales.

Diferencia claramente los hallazgos obtenidos de los comentarios y las conclusiones generadas por la IA.
```

---

## Paso 9

Profundizar el análisis con el siguiente prompt:

```text
Compara los comentarios abiertos con las puntuaciones numéricas.

Identifica:

- Comentarios que confirman las puntuaciones.
- Comentarios que contradicen las puntuaciones.
- Problemas recurrentes que no resultan evidentes al observar únicamente los promedios.
- Posibles causas que deberían ser investigadas.

No presentes las posibles causas como hechos confirmados.
```

---

## Objetivo

Combinar información cuantitativa y cualitativa para obtener una visión más completa de la experiencia de los participantes.

---

# Parte 6 – Identificar hallazgos prioritarios

## Paso 10

Utilizar el siguiente prompt:

```text
Actúa como especialista en evaluación de programas.

Basándote exclusivamente en los resultados de la encuesta, identifica los principales hallazgos.

Para cada hallazgo indica:

- Evidencia encontrada.
- Área o grupo afectado.
- Impacto potencial.
- Cantidad estimada de participantes afectados, cuando pueda calcularse con los datos.
- Prioridad: Alta, Media o Baja.
- Justificación de la prioridad asignada.

Separa los hallazgos respaldados directamente por los datos de las hipótesis que requieren validación adicional.
```

---

## Objetivo

Priorizar problemas y oportunidades utilizando criterios verificables, evitando que el plan de acción se base únicamente en opiniones generales.

---

# Parte 7 – Generar el plan de acción

## Paso 11

Utilizar el siguiente prompt:

```text
Convierte los hallazgos prioritarios en un plan de acción para mejorar futuras ediciones del "Programa de Capacitación en Operaciones Logísticas Seguras".

Para cada acción incluye:

- Hallazgo que origina la acción.
- Acción recomendada.
- Objetivo.
- Responsable sugerido.
- Prioridad.
- Plazo de implementación.
- Recursos necesarios.
- Indicador KPI.
- Meta esperada.
- Método de verificación.
- Riesgo de no implementación.

Presenta el resultado en formato de tabla.

No propongas acciones que no estén relacionadas con los hallazgos obtenidos de la encuesta.
```

---

## Paso 12

Solicitar una priorización del plan:

```text
Clasifica las acciones propuestas utilizando los siguientes criterios:

- Impacto esperado.
- Urgencia.
- Cantidad de participantes afectados.
- Esfuerzo de implementación.
- Riesgo operativo.

Organiza las acciones en:

- Acciones inmediatas.
- Acciones de corto plazo.
- Acciones de medio plazo.

Justifica la clasificación utilizando los resultados de la encuesta.
```

---

# Parte 8 – Definir indicadores de seguimiento

## Paso 13

Utilizar el siguiente prompt:

```text
Define indicadores para realizar el seguimiento del plan de acción.

Para cada indicador incluye:

- Nombre del indicador.
- Objetivo que mide.
- Fórmula de cálculo.
- Fuente de datos.
- Frecuencia de medición.
- Responsable sugerido.
- Valor inicial obtenido de la encuesta.
- Meta esperada.
- Criterio para considerar cumplida la acción.

Utiliza únicamente valores iniciales que puedan calcularse con los datos disponibles.
```

---

## Objetivo

Asegurar que las acciones propuestas puedan medirse y verificarse en futuras ediciones del programa.

---

# Parte 9 – Realizar el análisis completo en Microsoft 365 Copilot Chat

## Paso 14

Guardar el archivo de Excel y cargarlo en Microsoft 365 Copilot Chat.

Utilizar el siguiente prompt:

```text
Analiza el archivo de resultados de la encuesta del "Programa de Capacitación en Operaciones Logísticas Seguras" de Costa Oriental.

Realiza un análisis completo que incluya:

1. Resumen general de los resultados.
2. Aspectos mejor valorados.
3. Aspectos con mayores oportunidades de mejora.
4. Diferencias entre áreas.
5. Diferencias según la modalidad de participación.
6. Temas recurrentes en los comentarios.
7. Hallazgos prioritarios.
8. Recomendaciones.
9. Indicadores de seguimiento.

Basa las conclusiones exclusivamente en la información disponible en el archivo.

Cuando una posible explicación no pueda comprobarse con los datos, identifícala como una hipótesis que requiere validación.
```

---

# Parte 10 – Elaborar un informe ejecutivo

## Paso 15

Continuar la conversación con Copilot utilizando el siguiente prompt:

```text
A partir del análisis anterior, genera un informe ejecutivo para los responsables de programas de Costa Oriental.

El informe debe incluir:

- Resumen ejecutivo.
- Objetivo de la evaluación.
- Principales resultados.
- Fortalezas del programa.
- Oportunidades de mejora.
- Diferencias relevantes entre grupos.
- Análisis de los comentarios.
- Acciones prioritarias.
- Indicadores de seguimiento.
- Próximos pasos.

Utiliza un tono profesional, claro y orientado a la toma de decisiones.

Diferencia los datos observados, las conclusiones y las recomendaciones.
```

---

# Parte 11 – Validar las respuestas de Copilot

## Paso 16

Verificar que las conclusiones generadas por Copilot coincidan con los datos del archivo.

Revisar especialmente:

- Los promedios informados.
- Las comparaciones entre áreas.
- Las comparaciones por modalidad.
- La cantidad de respuestas analizadas.
- Los porcentajes mencionados.
- La relación entre los comentarios y las recomendaciones.
- Los valores iniciales asignados a los indicadores.
- La correspondencia entre hallazgos y acciones.

Si se detecta una conclusión que no puede comprobarse, utilizar el siguiente prompt:

```text
Indica qué filas, columnas y cálculos del archivo respaldan esta conclusión.

Si la conclusión no puede demostrarse con los datos disponibles, corrígela o elimínala.
```


---

# Aprendizajes Esperados

Al finalizar este laboratorio, el alumno será capaz de:

- Diseñar encuestas estandarizadas con Microsoft 365 Copilot.
- Crear encuestas con Microsoft Forms.
- Generar datos ficticios para realizar pruebas.
- Analizar resultados cuantitativos con Copilot para Excel.
- Analizar comentarios abiertos.
- Detectar tendencias y oportunidades de mejora.
- Priorizar hallazgos según su impacto.
- Convertir resultados de encuestas en planes de acción.
- Definir indicadores para medir la implementación de las acciones.
- Elaborar informes ejecutivos con Microsoft 365 Copilot.
- Validar las conclusiones generadas por la IA antes de utilizarlas.
