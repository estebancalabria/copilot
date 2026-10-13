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

# Reflexión final

## Prompt

```text
¿Qué información faltaría para convertir este borrador en un informe listo para ser enviado a la dirección?
```
