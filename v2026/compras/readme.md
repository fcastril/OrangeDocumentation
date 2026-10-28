[Regresar al Inicio](../README.md)

---

# COMPRAS (V2026)

Manuales de las pantallas de Compras en la nueva versión.

## Dashboard

- [Dashboard gerencial de Compras](dashboard-gerencial.md): órdenes de compra abiertas, saldo, vencidas y en tránsito; compras, devoluciones y neto del periodo frente al anterior; rankings de proveedores, referencias y tipos de movimiento, con drill-down y exportación a Excel.

## Informes

Consultas de solo lectura del menú **Consultas/Reportes**. Todos exportan a Excel y a PDF con los mismos filtros (con el permiso *Exportar*).

- [Informe de órdenes de compra](informes/ordenes-compra.md): qué se pidió, qué se recibió y qué falta por recibir, con las compras que cumplen cada orden.
- [Compras por tipo de movimiento](informes/tipo-movimiento.md): compras y devoluciones netas por tipo de movimiento, resumido o detallado por documento.
- [Compras por tipo y referencia](informes/tipo-referencia.md): compras y devoluciones por referencia dentro de cada tipo de movimiento.
- [Órdenes de compra y compras por proveedor](informes/proveedores.md): pedido, recepción, saldo y compras de cada proveedor, con las compras sin orden de compra.
- [Órdenes de compra y compras por comprador](informes/compradores.md): lo mismo por comprador, incluido el grupo «Sin comprador».

## Movimientos

- [Compras y devoluciones](movimientos/compras-devoluciones.md): registro de compras y devoluciones a proveedores, con cruce de órdenes de compra, autorización de administrador, cerrar, anular, eliminar e imprimir.
- [Importar compras y devoluciones desde Excel](movimientos/compras-devoluciones-importar.md): carga de muchos documentos desde una hoja de Excel, con vista previa y resultado.
- [Importar factura electrónica](movimientos/compras-devoluciones-importar-factura-electronica.md): carga de facturas electrónicas de la DIAN (XML o ZIP) para crear compras abiertas con sus adjuntos.

## Maestros

- [Proveedores](maestros/proveedores.md): incluye la pestaña **Cartera** (saldos de cada proveedor a una fecha de corte, documentos, historia y exportación a Excel).
  - Envío a SIIGO: el proveedor se envía solo al guardar y el botón **Enviar a SIIGO** sirve para reenviarlo (sección *Enviar a SIIGO* del manual).
- [Compradores](maestros/compradores.md)
- [Cartera de proveedores](maestros/cartera-proveedores.md): manual de la pestaña Cartera de Proveedores (Saldos, documentos, historia y Dashboard), con acceso por la opción Cartera Terceros.
- [Importar referencias compradas a un proveedor](maestros/proveedores-importar-referencias.md): trae al catálogo del proveedor lo que se le compró o gastó, con el código con el que el proveedor identifica cada referencia y el último valor.
- [Inventario del proveedor](maestros/proveedores-inventario.md): pestaña Inventario y rotación de la ficha del proveedor (existencias de las referencias que maneja, vista A o B, exportes a Excel y PDF).
- [Rotación del proveedor](maestros/proveedores-rotacion.md): modo Rotación de la pestaña Inventario y rotación de la ficha del proveedor (rotación, días de inventario, cobertura y clase de cada referencia, exportes a Excel y PDF).
- [Reposición del proveedor](maestros/proveedores-reposicion.md): modo Reposición de la pestaña Inventario y rotación de la ficha del proveedor (semáforo de reposición, sugerido de compra y exportes a Excel y PDF).

## Movimientos

- [Órdenes de compra](movimientos/ordenes-compra.md): crear, editar, cerrar, anular o eliminar órdenes, estados de documento y de recepción, impresión, adjuntos y el inventario en tránsito.
