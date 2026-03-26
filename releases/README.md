[Regresar al Inicio](../README.md)

---

# Releases Orange ERP

## 2026-03

### Implementaciones

- **Cierre Contable Anual (Contabilidad → Procesos):** Se implementa la ejecución del cierre anual usando el proceso de Cierres Contables con parámetros de año, tipos de movimiento y cuentas PUC (actual/anterior). Incluye selectores con búsqueda/paginación (Select2), validación previa de parámetros obligatorios y control para evitar cierres duplicados del mismo año/tipos de movimiento con base en movimientos contables. Ver manual: [Cierre Contable Anual](../contabilidad/procesos/cierre-contable-anual.md).
- **Observaciones en Órdenes de Producción (API):** Se habilita el endpoint para registrar observaciones sobre una OP existente, incluyendo **relevancia**, **fecha/hora del servidor** y respuesta JSON estandarizada. Cuando el usuario se resuelve desde el token, el texto guardado deja trazabilidad visible del reportante dentro de la observación. Ver manual: [Órdenes de Producción](../produccion/movimientos/ordenes-produccion.md).
- **Accesos Directos (Favoritos por usuario/empresa):** Se implementa la marcación de opciones favoritas desde el menú lateral mediante estrella (activa/inactiva por color), persistencia por **usuario + empresa**, visualización en el dashboard principal como **recuadros grandes** (ícono superior y texto inferior), y barra compacta de favoritos en el resto de vistas. Incluye validación de compañía activa para evitar guardar favoritos en una empresa incorrecta.
- **Inventarios Físicos (Consulta/Reporte):** Se implementa la nueva opción de consulta en Inventarios para revisar encabezados y detalle de conteos físicos en modo solo lectura. Ver manual: [Inventarios Físicos](../inventarios/consultas/inventarios-fisicos.md).
- **Comparativo de Inventarios Físicos:** Se implementa la opción en Inventarios → Procesos con filtros por fecha de corte y bodega, tabla paginada, exportación a Excel y exportación a PDF. Ver manual: [Comparativo de Inventarios Físicos](../inventarios/procesos/comparativo-inventarios-fisicos.md).
- **Movimientos y trazabilidad de Producción:** Se incorporan los campos **Fecha de Entrega** y **Fecha de Entrega Real** en consultas de movimientos, se agrega **Fecha de Entrega** al formulario de Movimientos de Producción con validación (obligatoria y mayor a la fecha del movimiento), y se añade **Fecha de Entrega** en el reporte de Estado de Órdenes. Ver manuales: [Movimientos de Producción](../produccion/movimientos/movimientos-produccion.md), [Trazabilidad](../produccion/consultas-reportes/trazabilidad.md), [Estado Órdenes de Producción](../produccion/consultas-reportes/estado-ordenes-produccion.md).
- **Integración SwiftBots (WhatsApp ↔ Producción):** Se agregan en Compañías los campos **UrlBaseDatosAutomatizacion** y **ApiKeyBaseDatosAutomatizacion**, se implementa sincronización desde Movimientos de Producción hacia base externa vía API y se toma siempre el movimiento en **ENTREGA** como origen del payload.
- **UI de operaciones con ícono y color (Producción/Inventarios):** Se estandariza la visualización de operaciones para mostrar ícono Font Awesome y texto con color configurado en Operaciones. El ajuste aplica en **Operaciones**, **Referencias (tab Operaciones)**, **Movimientos de Producción**, **Trazabilidad**, **Estado de Órdenes de Producción** y **Reporte Órdenes Producción Resumen**. Ver manuales: [Operaciones](../produccion/maestros/operaciones.md), [Referencias](../inventarios/maestros/referencias.md), [Movimientos de Producción](../produccion/movimientos/movimientos-produccion.md), [Trazabilidad](../produccion/consultas-reportes/trazabilidad.md), [Estado Órdenes de Producción](../produccion/consultas-reportes/estado-ordenes-produccion.md), [Reporte Órdenes Producción Resumen](../produccion/consultas-reportes/reporte-ordenes-produccion-resumen.md).
- **Estado de Órdenes de Producción (resumen visual por operación):** Se agrega resumen por operación integrado al formulario en formato de chips redondeados con color de fondo por operación, ícono y texto en blanco en negrita. Cada chip muestra **Cantidad** y **Lotes**, y se actualiza dinámicamente según los filtros y búsquedas aplicados en la tabla resumida.
- **Impresión PDF en Movimientos de Producción:** En el formato de impresión (`PrintMovts`) se incorpora **Fecha de Entrega** junto a la **Fecha** del encabezado para facilitar lectura operativa; además se resalta el valor en mayor tamaño, negrilla y color azul.
- **Consulta Gantt de Producción:** Se implementa y ajusta la consulta Gantt con resumen por operación (ícono/color, cantidad y lotes), tabla principal de responsables paginada a 10 registros, calendario inferior con eje de fechas y scroll, y visualización de OP en formato **OP-Consecutivo**. Además, se adiciona la línea vertical de **Fecha de Corte** en el calendario y se mejora el detalle en la primera columna a un formato de 2 líneas (información de OP y línea de fechas/cantidad), para evitar recortes de información en tablas pequeñas. Ver manual: [Gantt de Producción](../produccion/consultas-reportes/gantt.md).

### Bugs

- **Trazabilidad de Órdenes de Producción (Movimientos):** Se corrige la inconsistencia entre la cantidad del encabezado y el detalle. Ahora ambas vistas calculan y muestran la cantidad con el mismo criterio para evitar diferencias.
- **Referencias (Atributos):** Se corrige el BUG que ocurría al eliminar atributos en Referencias.


## Tabla de contenidos

- [2026-03](#2026-03)
- [2026-02](#2026-02)
- [2026-01](#2026-01)
- [2025-11](#2025-11)
- [2022-05](#2022-05)
- [2022-04](#2022-04)
- [2022-03](#2022-03)
- [2022-02](#2022-02)
- [2022-01](#2022-01)
- [2021-12](#2021-12)
- [2021-11](#2021-11)
- [2021-10](#2021-10)
- [2021-09](#2021-09)
- [2021-08](#2021-08)
- [2021-07](#2021-07)
- [2021-06](#2021-06)

---

## 2026-02

### Información

- **Copiar Referencias (Inventarios):** Se habilita duplicar referencias tipo R con validación de código en tiempo real, copiando atributos, materiales, proveedores, consumos y operaciones.
- **Cálculo de costos y precios (Inventarios):** Se mejora el cálculo automático usando **Costo Calculado** y el porcentaje **PorCostoCalculado** configurado en compañías.
- **Congelar/Descongelar Órdenes (Producción):** Botón dual con cambio visual por estado, confirmaciones y registro en logs.
- **Correcciones generales:** Ajustes en modal de referencias (loading), tipo de documento 44 en terceros, bloqueo en consultas de ventas, carga en movimientos de producción y reporte de pedidos por referencia.

## 2026-01

### Información

- **Precios de venta en referencias:** Implementación del cálculo a partir de **Costo Calculado** y porcentajes de precios configurados por empresa.
- **Fórmula:** Precio = CostoCalculado / (1 - PorcentajePrecio/100).
- **Bugs corregidos:** Multiplicador en movimientos de producción (entrada), velocidad de matriz de tallas, recarga en cierre de ventas, cálculo/acumulación de pre-nómina, anulación de ventas, exportación de clientes y carga de pedidos/detalle en ventas.

## 2025-11

### Implementaciones

- Se agrega la cantidad total en movimientos en la trazabilidad de órdenes de producción.

### Bugs

- Se organiza para que no se dupliquen los adjuntos en referencias al crear.
- Se verifica error al crear referencias (ya existían).
- Se bloquea el botón de guardar en movimientos para evitar duplicados por error.

## 2022-05

### Información

- Se implementa el reporte de cartera por sucursales.
- Se corrige informe detallado de ventas por referencias y tipos de movimiento.
- Se agrega botón (ojo) en consulta de movimientos de inventario.
- Se corrige bug en consulta de empleados, clientes y terceros.

### Actividades pendientes

- Totales de inventarios por atributo principal y secundario.
- Exportar informes de contabilidad a Excel.
- Espejo de movimientos.
- Reportes de programación y explosión de materiales de producción.
- Tipos de cliente (online, mayorista), factura electrónica desatendida.
- Consulta de asientos contables con filtros y mejoras de velocidad en informes/consultas.
- Revisar anulados en trazabilidad y retención por horticultura.

## 2022-04

### Información

- Se corrige afectación contable en tesorería con valores a favor.
- Se organiza lista de ventas por tipos de movimiento cuando usan mismo documento de referencia.
- Se corrige bug de guardado de órdenes de producción.
- Se corrige informe resumido de ventas por tipos de movimiento.
- Se agrega botón (ojo) en consulta de movimientos de inventario.

### Actividades pendientes

- Totales de inventarios por atributo principal y secundario.
- Exportar informes de contabilidad a Excel.
- Espejo de movimientos.
- Reportes de programación y explosión de materiales de producción.
- Tipos de cliente (online, mayorista), reporte de cartera por sucursal y factura electrónica desatendida.
- Consulta de asientos contables con filtros y mejoras de velocidad en informes/consultas.
- Revisar anulados en trazabilidad.

## 2022-03

### Implementaciones

- Dashboard de ventas: ticket diario por bodega.
- Certificados de retefuente.
- Campo existencia en traslados y en entradas/salidas.
- Consecutivo y código tipo de movimiento en reportes de ventas.
- Cantidad de unidades en reporte de ventas por tipo de movimiento.
- Texto de Habeas Data en impresiones de ventas.

### Bugs

- Se corrige guardado en asientos contables y tesorería.
- Se corrige manejo de decimales en facturación electrónica.
- Se corrige bug de cuadres de caja.
- Se organizan consultas de órdenes de producción para no repetir por atributos.
- Se organiza reporte de producción respecto a cantidades.

### Actividades pendientes

- Totales de inventarios por atributo principal y secundario.
- Exportar informes de contabilidad a Excel.
- Espejo de movimientos.
- Reportes de programación y explosión de materiales de producción.
- Tipos de cliente (online, mayorista), plan separe, cartera por sucursal y factura electrónica desatendida.
- Consulta de asientos contables con filtros y mejoras de velocidad en informes/consultas.
- Consulta (ojo) en movimientos de inventarios e informes de rotación/ventas mes a mes.

## 2022-02

### Implementaciones

- Implementar cuadre de caja.
- Manejo de cliente por defecto.
- Ajuste en consulta de valores para cuadre de caja (2022-02-25).

### Bugs

- Se corrige guardado doble en órdenes de producción.
- En ventas, traer cliente por defecto.
- Permitir modificar cantidades en órdenes de producción.
- Ajuste de asientos contables en ventas por descuentos.

### Actividades pendientes

- Texto de Habeas Data en ventas.
- Existencia en traslados y entradas/salidas.
- Ticket promedio por bodega.
- Certificados de retefuente.
- Totales de inventarios por atributos.
- Exportar contabilidad a Excel y espejo de movimientos.
- Reportes de programación/explosión de materiales.
- Tipos de cliente, plan separe, cartera por sucursal, factura electrónica desatendida.
- Filtros en asientos contables, velocidad de consultas, anulados en trazabilidad y API de nómina electrónica con Alegra.

## 2022-01

### Implementaciones

- Restricción para no modificar ventas/compras/gastos con recibo de caja o egreso asociado.
- IVA descontable en referencias para compras y gastos.
- Campos para nómina electrónica en conceptos, empleados y compañías.
- Saldo de cartera en recibos de caja y egresos.
- Consulta de listas de precios.
- Mensaje de alerta en observaciones.
- Creación de clientes desde movimientos.

### Bugs

- Ajuste en guardado de fecha efectiva en recibos de caja y egresos.
- Permite usar ENTER al buscar en movimientos, referencias y terceros.

### Actividades pendientes

- Modificar cantidades / guardado doble en órdenes de producción.
- Cliente por defecto en ventas.
- Totales de inventarios por atributos.
- Texto Habeas Data.
- Exportar contabilidad a Excel.
- Cuadre de caja, plan separe, cartera por sucursal, ticket promedio por bodega.
- Factura electrónica desatendida, certificados de retención, filtros en asientos contables y espejo de movimientos.

## 2021-12

### Información

- Registro consolidado existente en histórico con el mismo contenido operativo documentado para 2021-10.

### Implementaciones

- Columna consecutivo y tipo de movimiento en selección de facturas para recibos de caja y egresos.
- Campos fecha efectiva y total factura en consulta de recibos de caja y egresos en clientes/proveedores.
- Título en reporte de cartera por terceros con sucursal y observaciones.
- Título en consulta de recibos de caja y egresos para mostrar observaciones.
- Obligatoriedad de órdenes de producción según configuración.
- Botón para nuevo registro al vender sin salir del formulario.
- Consulta de facturas en proveedores.

### Bugs

- Ajustes en tablas de consulta de recibos de caja y egresos para mostrar facturas/formas de pago correctamente.
- Corrección en creación de recibos/egresos al seleccionar factura y valor a abonar.
- Bloqueo de modificación para documentos con meses cerrados aunque no cambie fecha.
- Ajuste de carga de gastos.

## 2021-11

### Información

- Registro consolidado existente en histórico con el mismo contenido operativo documentado para 2021-10.

### Implementaciones

- Columna consecutivo y tipo de movimiento en selección de facturas para recibos de caja y egresos.
- Campos fecha efectiva y total factura en consulta de recibos de caja y egresos en clientes/proveedores.
- Título en reporte de cartera por terceros con sucursal y observaciones.
- Título en consulta de recibos de caja y egresos para mostrar observaciones.
- Obligatoriedad de órdenes de producción según configuración.
- Botón para nuevo registro al vender sin salir del formulario.
- Consulta de facturas en proveedores.

### Bugs

- Ajustes en tablas de consulta de recibos de caja y egresos para mostrar facturas/formas de pago correctamente.
- Corrección en creación de recibos/egresos al seleccionar factura y valor a abonar.
- Bloqueo de modificación para documentos con meses cerrados aunque no cambie fecha.
- Ajuste de carga de gastos.

## 2021-10

### Implementaciones

- Columna consecutivo y tipo de movimiento en selección de facturas para recibos de caja y egresos.
- Campos fecha efectiva y total factura en consulta de recibos de caja y egresos en clientes/proveedores.
- Título en reporte de cartera por terceros con sucursal y observaciones.
- Título en consulta de recibos de caja y egresos para mostrar observaciones.
- Obligatoriedad de órdenes de producción según configuración.
- Botón para nuevo registro al vender sin salir del formulario.
- Consulta de facturas en proveedores.

### Bugs

- Ajustes en tablas de consulta de recibos de caja y egresos para mostrar facturas/formas de pago correctamente.
- Corrección en creación de recibos/egresos al seleccionar factura y valor a abonar.
- Bloqueo de modificación para documentos con meses cerrados aunque no cambie fecha.
- Ajuste de carga de gastos.

## 2021-09

### Implementaciones

- Informe de movimiento contable para exportación.
- Proceso de recálculo de contabilidad.
- Consulta de recibos de caja y egresos en clientes y proveedores.
- Consulta de facturas y detalle de facturas en clientes y proveedores.

### Bugs

- Totales en cartera respecto a recibos de caja.
- Traslados con bodega destino.
- Observaciones en terceros.
- Organización de saldo/estado de cartera en facturas.
- Precios en reporte de inventarios con atributos.
- Opción de consulta de recibos/egresos en terceros.
- Corrección al guardar OPs editadas para no duplicar registros.

## 2021-08

### Implementaciones

- Manejo de clientes por defecto en ventas (configurable en tipos de movimiento).
- Implementación del reporte de remisiones.

### Bugs

- Corrección al crear terceros con contactos.
- Evitar repetición de detalles en órdenes de producción.
- Mejora de búsqueda de proveedores en asientos contables.
- Ajuste de impresión de tercero en comprobante de asientos contables.
- Cuentas contables en grupos dejan de ser obligatorias.
- Ajuste en manejo de clientes y sucursales en ventas.

## 2021-07

### Implementaciones

- Cambio de precios en bloque en referencias.
- Manejo de contactos en terceros.

### Bugs

- Corrección en actualización de referencias.
- Corrección en edición de detalles de órdenes de producción.
- Corrección en consulta del reporte de trazabilidad de órdenes de producción.
- Ajustes en consulta de precios (especialmente insumos).
- Descuentos adicionados al cambio de precios en bloque.
- Mejora de matriz de tallas en ventas y entradas/salidas.

## 2021-06

### Implementaciones

- Trazabilidad de órdenes de producción.
- Orden de producción en compras/devoluciones y causación de gastos.
- Identificador de versión enlazado a notas de release.
- Reporte de estados de órdenes de producción.
- Movimientos de producción: permanecer en formulario después de guardar.
- Asientos contables: razón social del tercero en impresión.
- Consulta de asientos contables por "CODIGOMOVIMIENTO-CONSECUTIVO".

### Bugs

- Ajuste de cálculo de descuentos para transmisión de facturación electrónica.
- Remisiones en observación de factura electrónica.
- Pedidos: precio según lista de precios.
- Trazabilidad y movimientos de producción con consultas/traslados correctos.
- Consulta de terceros en movimientos de producción.
- Impresión de tesorería con anticipos sin error.
- Corrección en importaciones/asientos contables al importar terceros.
- Validación de código de referencia sin espacios iniciales/finales.
- Ajuste en conceptos de nómina (provisiones y apropiaciones).
- Consulta adecuada de responsables en movimientos de producción.
- Homologación inventarios por referencia y reporte por bodega.
- Mejora de concurrencia al exportar/imprimir prenómina.
- Corrección en consulta de inventarios por bodega.
- Corrección en creación de maestro de gastos.
