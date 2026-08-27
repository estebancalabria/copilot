# Procedimiento Operativo Punto a Punto
## PO-LOG-014 — Recepción, Control y Despacho de Mercadería Importada

**Cliente:** Costa Oriental S.A.
**Área responsable:** Administración Logística / Operaciones
**Versión:** 1.2
**Vigencia:** desde 01/03/2026
**Reemplaza a:** PO-LOG-011 (v1.1)

---

### 1. Objetivo
Establecer la secuencia de pasos para la recepción, control documental, cubicación y despacho de mercadería importada que ingresa al depósito de Costa Oriental, garantizando la trazabilidad desde el arribo del contenedor hasta la facturación al cliente final.

### 2. Alcance
Aplica a todas las operativas de tipo marítimo y masivo gestionadas por Administración Logística, con intervención de Operaciones, Finanzas y Sistemas según corresponda.

---

### 3. Procedimiento

**Paso 1 — Aviso de arribo**
Responsable: Administración Logística
El agente marítimo notifica el arribo del contenedor vía correo electrónico o EDI. Se registra la fecha estimada de arribo (ETA) en el sistema DIM.
Duración estimada: 1 hora.

**Paso 2 — Verificación de documentación de ingreso**
Responsable: Administración Logística
Se controla que el Conocimiento de Embarque (B/L), la factura comercial y el packing list estén completos y coincidan con lo declarado en el Pedido de Venta de ODOO.
Duración estimada: 2 horas.
*Depende de: Paso 1.*

**Paso 3 — Control de concordancia VIA/DUA**
Responsable: Finanzas
Se verifica que el tipo de VIA declarado (marítimo, aéreo, terrestre) coincida con el tipo de DUA generado. Ante inconsistencia, se retiene el trámite hasta su corrección.
Duración estimada: 1 hora.
*Depende de: Paso 2.*

**Paso 4 — Coordinación de descarga**
Responsable: Operaciones
Se agenda la cuadrilla y el equipamiento (autoelevadores, grúas) para la descarga del contenedor en el muelle asignado.
Duración estimada: 3 horas.
*Depende de: Paso 3.*

**Paso 5 — Descarga física y cubicación**
Responsable: Operaciones
Se descarga la mercadería y se mide (largo, ancho, alto, volumen) cada pallet o carga suelta. Se compara contra el cadastro declarado.
Duración estimada: 4 horas.
*Depende de: Paso 4.*

**Paso 6 — Control de cadastro por variaciones**
Responsable: Operaciones + Administración Logística
Si el volumen real difiere significativamente del cadastro declarado, se abre una consulta conjunta para analizar la causa antes de continuar.
Duración estimada: 2 horas (solo si aplica; en caso contrario, se omite).
*Depende de: Paso 5.*

**Paso 7 — Control de operativa masiva (si corresponde)**
Responsable: Finanzas
Para operativas clasificadas como "masivo", se aplica el control específico de consistencia de volumen agregado antes de habilitar la facturación.
Duración estimada: 1 hora.
*Depende de: Paso 5. Puede ejecutarse en paralelo al Paso 6.*

**Paso 8 — Ingreso a WMS**
Responsable: Operaciones
Se registra el ingreso definitivo de la mercadería al sistema de gestión de depósito (WMS), con ubicación de rack asignada.
Duración estimada: 1 hora.
*Depende de: Pasos 6 y 7.*

**Paso 9 — Validación final del Pedido de Venta**
Responsable: Administración Logística
Se corrobora que el Pedido de Venta en ODOO quede consistente con lo efectivamente recibido, ajustando manualmente si hubo diferencias.
Duración estimada: 1 hora.
*Depende de: Paso 8.*

**Paso 10 — Habilitación para facturación**
Responsable: Finanzas
Con el Pedido de Venta validado, se libera la operativa para su inclusión en la facturación de fin de mes.
Duración estimada: 30 minutos.
*Depende de: Paso 9.*

**Paso 11 — Despacho o almacenamiento final**
Responsable: Operaciones
Según instrucción del cliente, la mercadería se despacha a destino final o queda almacenada en el depósito bajo el rack asignado.
Duración estimada: 2 horas.
*Depende de: Paso 10.*

---

### 4. Excepciones
- Si en el Paso 3 se detecta inconsistencia VIA/DUA no resuelta en 24 hs, el procedimiento se escala a Gerencia de Administración.
- Si en el Paso 6 la variación de cadastro supera el 10% del volumen declarado, se notifica al cliente antes de continuar con el Paso 8.

### 5. Registros
Toda la secuencia queda documentada en DIM (control documental) y ODOO (Pedido de Venta), con historial de cambios disponible para auditoría.

---

*Documento de uso interno — Costa Oriental S.A. / Administración Logística*
