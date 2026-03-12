[Regresar a Producción](../readme.md)

---
# MOVIMIENTOS DE PRODUCCIÓN

Permite registrar y consultar los movimientos de producción (entradas y salidas) asociados a una orden de producción.

## Campos principales

- Orden de Producción
- Operación
- Responsable
- Fecha
- Fecha de Entrega (obligatoria)
- Fecha de Entrega Real

## Reglas de validación

- La Fecha de Entrega es obligatoria al crear o editar el movimiento.
- La Fecha de Entrega debe ser mayor que la Fecha del movimiento.

## Consulta de movimientos

En el listado se visualizan los campos:

- Fecha
- Fecha Entrega
- Fecha Entrega Real
- Tipo de movimiento
- Estado

## Relación con Trazabilidad y Reportes

- En Trazabilidad, pestaña Movimientos, se muestran Fecha Entrega y Fecha Entrega Real.
- En Estado de Órdenes de Producción (detallado) se muestra Fecha Entrega.

## Integración SwiftBots (Base de datos externa)

Cuando la compañía tiene configurados los parámetros de automatización, al guardar un movimiento de producción se envía automáticamente la información a la base de datos externa.

### Requisitos previos en Compañías

En Configuración → Compañías (Crear/Editar), diligenciar:

- Url Base de Datos Automatización
- ApiKey Base de Datos Automatización

### Comportamiento de sincronización

- La sincronización se ejecuta desde el guardado del movimiento de producción.
- Se toma siempre el movimiento en **ENTREGA** como fuente del payload.
- Si el guardado en Orange es exitoso y la sincronización externa falla, el movimiento queda guardado y se informa el mensaje de advertencia.

### Datos enviados a la base externa

- Datos de compañía: `idCompany`, `IdentCompany`, `NameCompany`
- Datos del movimiento y operación
- Responsable
- Fechas (movimiento y entrega)
- Cantidades y detalle por referencia/atributos
