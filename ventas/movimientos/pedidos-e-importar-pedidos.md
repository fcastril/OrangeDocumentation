[Regresar a Ventas](../readme.md)

---

# Pedidos e Importar Pedidos

Este manual describe el flujo funcional para crear, editar, consultar e importar pedidos desde archivo Excel.

## Ubicacion

- Ruta: Ventas > Movimientos > Pedidos.

## Proposito

- Registrar pedidos manualmente.
- Consultar pedidos existentes.
- Importar el detalle del pedido desde Excel.
- Mantener trazabilidad del documento con su idMovimiento.

## Flujo general de Pedidos

1. Ingresar a Ventas > Movimientos > Pedidos.
2. Crear un nuevo pedido o abrir uno existente.
3. Completar encabezado del documento.
4. Agregar detalle manualmente o importar detalle desde Excel.
5. Guardar y validar totales.

## Campos principales del encabezado

- Tipo de Movimiento.
- Prefijo y Consecutivo.
- Fecha.
- Cliente.
- Sucursal del cliente.
- Vendedor.
- Fecha de entrega.
- Dias de plazo.
- Documento de referencia.
- Observaciones.

## Importar Pedidos desde Excel

La importacion se realiza desde el modal de importacion en la pantalla de Pedidos.

### Requisitos previos

- El encabezado del pedido debe estar completo.
- Debe seleccionar un archivo Excel valido.
- Se recomienda descargar y usar la plantilla oficial.

### Descargar plantilla

Desde la opcion de Pedidos, usar la accion Descargar Plantilla Importar Pedidos.

Columnas esperadas en el archivo:

1. Referencia
2. Atributo Principal
3. Atributo Secundario
4. Porcentaje Descuento
5. Codigo IVA
6. Bodega
7. Centro de Costos
8. Cantidad
9. ValorUnitario

### Validar archivo

1. Abrir el modal de importacion.
2. Seleccionar archivo.
3. Pulsar Validar.
4. Revisar resultados en la tabla de previsualizacion.

Reglas de validacion principales:

- La referencia debe existir.
- El atributo principal y secundario deben existir.
- La combinacion Referencia + Atributos debe existir en MvtoAtributos.
- Codigo IVA debe existir.
- Bodega debe existir.
- Centro de Costos debe existir.
- Cantidad debe ser mayor a 0.
- ValorUnitario debe ser mayor a 0.
- Porcentaje Descuento debe estar entre 0 y 100 y no puede ser 100.

Si una fila contiene errores, se muestran en la columna Errores y mediante tooltip por campo.

### Importar archivo

1. Con el archivo validado, pulsar Importar.
2. El sistema envia encabezado + detalle validado al endpoint de importacion.
3. El procedimiento retorna el resultado con formato OK|idMovimiento|...
4. Si la importacion es exitosa:
- Se toma el idMovimiento retornado.
- Se actualiza la URL del navegador al pedido importado.
- Se recarga la pantalla para mostrar el documento real creado/actualizado.

### Resultado esperado

- El usuario queda ubicado en el pedido importado.
- El formulario muestra el idMovimiento definitivo.
- El detalle del pedido queda persistido y visible.

## Mensajes comunes

- No se recibieron detalles para importar.
- Debe validar el archivo antes de importar.
- No hay detalles validados para importar.
- Error al importar el pedido.
- La importacion finalizo, pero no se recibio idMovimiento para recargar la pantalla.

## Recomendaciones operativas

- Validar primero el encabezado antes de abrir el modal de importacion.
- Corregir todas las filas con error antes de importar.
- Confirmar que la URL final corresponda a /_MV_Pedidos/CrearEditar/{idMovimiento}.
- Si el documento ya existe, confirmar que el id importado coincide con el esperado.
