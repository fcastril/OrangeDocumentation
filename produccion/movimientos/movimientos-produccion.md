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
