# Clase Cuatro - 26 de Mayo del 2026

# Repaso

* Prompt Engineering
  * Personalizacion de Salida
    * Markdown
      * Generar plantillas de la respuesta exacta
    * Mermaid
      * Lenguaje estandar que usa la IA para graficos/Diagramas
* Tipos de Modelo de Lenguaje
    * GPT (thinking/Fast)
    * Opus
* Agentes Precompilados
  * Copilot For Excel
    * Pivot Tables
    * Pivot Chart
    * Dashboard

---

# Agentes Precompilaodos  

## Agente Analista

* Problema
  * Al analizar los datos de una planilla (excel) con copilot toma solamente las primeras 40 filas
* Solcuion
  * Utilizar Agente Analista
    * Codifica analisis de datos en python sin necesidad de saber nada del lenguaje
    * Puedo utilizar liberias de python como pandas y matplot lib
      * https://matplotlib.org/stable/gallery/index

* Prompt Generalista
```
Generame un insight de los datos en el siguiente archivo 
```

* Prompt mas especifico (mirando los graficos de ejemplo en matplot lib : https://matplotlib.org/stable/gallery/index)
```
Armame con matplotlib un stacked bar chart donde se vea por cada tipo de proyecto el costo actual y el costo estimado en la misma barra.
```

## Agente Prompt Coach

* Experto en prompt engineering que me redacta los promps como si fuera un experto

```
Rol: Actúa como analista de compras y mercado para construcción en Argentina, con foco en Tucumán.
Objetivo: Realizar una investigación de mercado y elaborar un Top 10 de proveedores recomendados por rubro de materiales de construcción en Yerbabuena, Tucumán y alrededores (San Miguel de Tucumán, Tafí Viejo, El Manantial, Lules, etc.), priorizando menor costo total del proyecto (precio + flete + tiempos + condiciones comerciales) sin descuidar calidad mínima razonable.
1) Alcance geográfico

Zona principal: Yerbabuena, Tucumán
Radio: hasta 30–50 km o “alrededores” (incluye localidades cercanas cuando mejoren precio/flete)

2) Rubros a cubrir (mínimo)
Organiza el Top 10 por rubros (pueden repetirse proveedores si dominan más de un rubro, pero intenta diversificar):

Áridos (arena, piedra, ripio)
Cementos / cal / adhesivos
Hierro y mallas (acero, varillas, alambres)
Ladrillos/bloques (cerámicos, HCCA, etc.)
Hormigón elaborado (si aplica)
Sanitarios y griferías
Electricidad (cables, térmicas, cañerías, tableros)
Plomería/gas (caños, conexiones)
Aberturas (aluminio/PVC/madera) y vidrios
Terminaciones (pisos/revestimientos, yeso/durlock, pintura, impermeabilizantes)

3) Criterios para “mejores proveedores”
Evalúa y puntúa cada proveedor con una escala 1–5 (o 1–10) usando:

Precio estimado (referencias públicas / rangos)
Costo de flete y distancia a Yerbabuena
Variedad y stock
Condiciones comerciales (descuentos por volumen, cuenta corriente, financiación)
Reputación (reseñas Google / redes / referencias)
Tiempo de entrega
Calidad/garantías
Atención a obras (si trabajan con constructoras/arquitectos)

4) Fuentes (obligatorio)

Prioriza fuentes verificables y actuales: webs oficiales, Google Maps, redes verificadas, marketplaces locales.
Para cada proveedor incluye links a: sitio/redes + ubicación (si existe).
Si no hay precios publicados, infórmalo y sugiere cómo cotizar (WhatsApp, formulario, llamada).

5) Entregable en formato tabla + resumen
Devuelve:
A) Tabla principal con columnas:

Rubro
Proveedor (nombre)
Localidad
Distancia aprox. a Yerbabuena (si posible)
Qué vende (1 línea)
Señales de buen precio (ej.: mayorista, descuentos obra, combos, etc.)
Puntaje total + subpuntajes (Precio, Flete, Stock, Condiciones, Reputación)
Contacto/links (web, redes, Google Maps si aplica)

B) Top 10 final “recomendado para abaratar obra”

Lista priorizada (1 al 10) con breve justificación.

C) Estrategia de compra para ahorrar
Incluye recomendaciones prácticas:

Qué rubros conviene comprar “cerca” vs “más lejos”
Cómo negociar por volumen
Alternativas equivalentes (ej.: bloque HCCA vs ladrillo cerámico)
Cómo reducir desperdicio (medidas estándar, cortes, etc.)

6) Preguntas y supuestos (solo si faltan datos)
Si faltan datos críticos, asume valores razonables y decláralos en “Supuestos”.
No pidas más de 3 aclaraciones.
```

## Agente Investigador

* Caracteristica
  * Realiza una investigacion (+100 sitios web segun el problema)
  * Utiliza el prompt (Cadena de Razonamiento) para planificar la mejor forma de encarar la investigacion y mostrar la informacion
 
---

# Cuadernos

* Serian como los proyectos en ChatGPT / Claude
* Son una forma de Agrupar conversaciones
* Compartir contexto entre conversaciones
* Compartir fuentes de informacion entre conversaciones
* Similar/Inspirado en NotebookLM

> [!NOTE]
> Un paso previo a la confeccion de un agente

* Son un area de chats colaboratibos y Abiertos que se pueden modificr sobre la marcha y mantienen el contexto de varias conversaciones

---

# Crear

* Copilot tiene la opcion de crear
  * Imagenes
  * Videos
  * Presentaciones
* MS tiene un clon de Canvas
  * https://designer.microsoft.com/

# Proxima Clase

* Desarrollo de Agentes
  * Conectar nuestro agente con aplicaciones externas como Canva
