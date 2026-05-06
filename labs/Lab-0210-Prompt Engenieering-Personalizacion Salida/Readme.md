# Lab — Personalización de salida

**Sesión:** 2 · **Duración estimada:** 45 minutos
**Módulo:** 2 — Ingeniería de instrucciones
**Patrón:** Formatos de salida — JSON · XML · HTML · CSV · Markdown · Mermaid

---

## La situación

Sofía trabaja en el área de marketing de **NovaTech Store**, una tienda online de gadgets y electrónica. Esta semana tienen que lanzar una nueva sección del catálogo con los 8 productos más vendidos de la temporada.

El problema: cada área de la empresa necesita esa misma información en un formato diferente.

| Área | Qué necesita | Para qué |
|---|---|---|
| Desarrollo web | JSON | Importar al sistema de ecommerce |
| Sistemas / ERP | XML | Sincronizar con el inventario |
| Comercial | PDF prolijo | Entregar al cliente en reunión |
| Ventas | CSV | Abrir en Excel y trabajar los precios |
| Marketing | Markdown con plantilla exacta | Documentación interna de producto |
| Dirección | Diagrama Mermaid | Vista rápida de categorías y precios |

Sofía tiene Copilot. Va a resolver todo esto sin tocar una sola hoja de cálculo manualmente.

---

## Paso 1 — Buscar los productos en la web

Lo primero es tener los datos. En lugar de inventarlos, vamos a pedirle a Copilot que los busque en internet.

Abrí Copilot en https://copilot.microsoft.com y escribí este prompt:

```
Buscá en la web los 8 gadgets de electrónica más vendidos o mejor valorados
del momento. Para cada uno necesito:
- Nombre del producto
- Marca
- Categoría (auriculares, smartwatch, cámara, etc.)
- Precio aproximado en USD
- Característica principal
- Valoración promedio (sobre 5)
- Disponibilidad (en stock / sin stock)
- Un párrafo breve de descripción

Presentá los resultados como una lista numerada clara.
```

> **Nota didáctica:** Copilot tiene acceso a búsqueda web en tiempo real. No está generando datos de memoria — está consultando fuentes actuales. Verificá que los productos y precios sean reales y recientes. Si algún dato parece inventado, pedile que cite la fuente.

Guardá esta lista. La vamos a usar como fuente en todos los pasos siguientes.

---

## Paso 2 — Formato JSON (para el sistema de ecommerce)

El equipo de desarrollo necesita los datos en JSON para importarlos al backend de la tienda.

Con la lista del Paso 1 en el chat, escribí:

```
Tomá la lista de productos que generaste y convertila a formato JSON.
Cada producto debe ser un objeto con estos campos:
id, nombre, marca, categoria, precio_usd, caracteristica_principal,
valoracion, disponibilidad, descripcion.
El resultado debe ser un array JSON válido.
```

**Observá:**
- ¿Los tipos de datos son correctos? (números como números, no como texto)
- ¿La estructura es consistente en los 8 productos?
- ¿El JSON es válido? (podés verificarlo en https://jsonlint.com)

> **¿Para qué sirve JSON?** Es el formato estándar de intercambio de datos en aplicaciones web. Cualquier sistema moderno de ecommerce, CRM o ERP puede importar y exportar JSON. Si alguna vez integraste una API, trabajaste con JSON.

---

## Paso 3 — Formato XML (para el ERP de inventario)

El sistema de inventario es más antiguo y solo acepta XML. Mismo dataset, otro formato.

```
Ahora convertí el mismo catálogo a formato XML.
Usá la etiqueta raíz <catalogo> y cada producto dentro de una etiqueta <producto>.
Respetá los mismos campos que el JSON anterior.
```

**Compará con el JSON:**
- ¿Qué formato te parece más legible a simple vista?
- ¿Cuál ocupa más espacio?
- ¿En qué casos usarías uno u otro?

> **Nota didáctica:** XML fue el estándar dominante antes de que JSON lo desplazara en aplicaciones web. Hoy conviven: JSON domina en APIs modernas, XML sigue siendo común en sistemas legacy, SAP, EDI y documentos estructurados como Word o Excel internamente.

---

## Paso 4 — Formato HTML para PDF (para la reunión comercial)

El equipo comercial tiene una reunión con un cliente mañana y necesita un catálogo visualmente prolijo para entregar impreso o en PDF.

```
Generá un archivo HTML único, profesional y elegante con el catálogo completo
de los 8 productos. Debe incluir:
- Logo ficticio de "NovaTech Store" en el encabezado
- Una card por producto con nombre, marca, precio, valoración y descripción
- Tabla de especificaciones técnicas por producto
- Colores corporativos: azul marino y blanco
- Pie de página con fecha y nombre de la empresa
El HTML debe ser autónomo (sin dependencias externas) y verse bien al imprimir.
```

**Para convertirlo a PDF:**
1. Copiá el HTML generado en un archivo `.html` y abrilo en el navegador
2. Presioná `Ctrl + P` (imprimir)
3. En destino, seleccioná **Guardar como PDF**
4. Listo — tenés un catálogo PDF profesional generado 100% con Copilot

> **El truco del Ctrl+P:** No necesitás saber HTML para generar documentos PDF con formato. Copilot escribe el HTML, vos lo convertís a PDF en 10 segundos. Este flujo reemplaza horas de trabajo en Word o InDesign para documentos de entrega rápida.

---

## Paso 5 — Formato CSV (para el equipo de ventas en Excel)

El equipo de ventas quiere la lista en Excel para poder filtrar, ordenar y trabajar los precios.

```
Convertí el catálogo a formato CSV (comma separated values).
La primera fila debe ser el encabezado con los nombres de las columnas.
Usá coma como separador y comillas dobles para campos que contengan comas
o texto largo.
```

**Para abrirlo en Excel:**
1. Copiá el CSV en un archivo `.csv`
2. Abrilo directamente desde Excel
3. O pegá el contenido directamente en el **chat de Copilot dentro de Excel** para que cree el libro automáticamente

> **Bonus:** Si tenés Copilot embebido en Excel (requiere licencia M365 + Copilot), podés pegarle el CSV en el chat y pedirle: *"Creá una tabla con estos datos y aplicá formato de tabla con filtros"*. En 5 segundos tenés el libro listo.

---

## Paso 6 — Markdown con plantilla exacta (para documentación interna)

Este es el paso más importante del lab. El equipo de marketing quiere documentar cada producto con un formato **exacto y consistente** — siempre igual, sin importar quién lo escriba o cuándo.

### Primero: definí la plantilla

La clave es decirle a Copilot exactamente cómo querés la respuesta **antes** de pedirle que la genere. Esto se llama **plantilla de salida** y es una de las técnicas más poderosas de prompt engineering.

Escribí este prompt:

```
Quiero que uses esta plantilla exacta de Markdown para documentar cada producto.
No agregues ni quites secciones. Respetá los títulos, el orden y el formato
tal cual están definidos:

---
# [Nombre del producto]

> [Descripción en un párrafo]

## Ficha técnica

* Marca: **[Marca]**
* Categoría: **[Categoría]**
* Precio: **USD [Precio]**
* Valoración: **[X.X / 5]**
* Disponibilidad: *[En stock / Sin stock]*

## Por qué lo recomendamos

> [Una razón de compra en una oración, orientada al beneficio del usuario]

## Ideal para

* [Perfil de usuario 1]
* [Perfil de usuario 2]
* [Perfil de usuario 3]

---

Ahora generá la ficha completa del primer producto de la lista usando
esta plantilla. No uses ningún otro formato.
```

**Luego pedí el resto:**
```
Generá la ficha del segundo producto con la misma plantilla exacta.
```

> **¿Por qué es tan importante la plantilla?** Sin plantilla, cada vez que pedís una ficha de producto Copilot decide el formato — y nunca es igual dos veces. Con la plantilla, el resultado es predecible, consistente y listo para copiar en cualquier sistema de documentación (Notion, Confluence, GitHub, SharePoint). **Reducís el no-determinismo del modelo.**

**Bonus — Copiar a Word con formato:**
Copiá el Markdown generado y pegalo en Word. Si tu versión de Word soporta Markdown (M365 actualizado), va a respetar los títulos, negritas y listas automáticamente.

---

## Paso 7 — Diagrama Mermaid (para la presentación a dirección)

La dirección quiere una vista rápida de cómo se distribuye el catálogo por categoría y rango de precio. Sin tablas — un diagrama.

```
Tomá el catálogo de 8 productos y generá un diagrama Mermaid de tipo pie chart
que muestre la distribución de productos por categoría.
Luego generá un segundo diagrama de barras (xychart-beta) que muestre
el precio de cada producto.
```

**Para visualizarlo:**
1. Copiá el código Mermaid generado
2. Pegalo en https://mermaid.live
3. El diagrama se renderiza en tiempo real

> **Nota didáctica:** Mermaid es un estándar para generar diagramas a partir de texto. GitHub, Notion, GitLab y muchas wikis corporativas lo renderizan nativamente. Si trabajás con documentación técnica, Mermaid te ahorra horas de trabajo en Visio o Draw.io.

---

## Comparativa final

Al terminar el lab, completá esta tabla con tu experiencia:

| Formato | Tiempo estimado sin Copilot | Tiempo con Copilot | ¿Para qué lo usarías en tu trabajo? |
|---|---|---|---|
| JSON | | | |
| XML | | | |
| HTML → PDF | | | |
| CSV | | | |
| Markdown | | | |
| Mermaid | | | |

---

## Preguntas de reflexión para el grupo

1. ¿Cuál de los seis formatos te parece más aplicable a tu trabajo diario?
2. ¿Qué pasaría si le pedís el Markdown sin plantilla? ¿El resultado sería el mismo?
3. ¿En qué casos el CSV con Copilot reemplaza trabajo que hoy hacés manualmente?

---

## El aprendizaje clave

El dato es el mismo. Lo que cambia es el destinatario y su sistema. Copilot no solo genera contenido — transforma y adapta información al formato que cada receptor puede consumir. Eso es lo que distingue a un usuario avanzado de uno básico: saber pedirle al modelo la forma exacta que necesitás.

---

## Próximo lab

**Lab 3A — Word: de acta a informe:** ahora que dominás los formatos de salida, vamos a aplicar esa misma lógica dentro de las apps de Microsoft 365.

---

*Material desarrollado por MCT Esteban Calabria · https://linkedin.com/in/esteban-calabria*
