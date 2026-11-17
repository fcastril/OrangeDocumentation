[Regresar al Inicio](../README.md)

---

# CARTERA (V2026)

Manuales de las pantallas de Cartera en la nueva versión.

## Inicio del módulo

- Al abrir **Cartera** verá el menú del módulo con los grupos que tiene su perfil. Los grupos sin pantallas disponibles no aparecen. Desde el botón **?** de la pantalla de inicio puede abrir este índice.

## Gerencia

- [Dashboard de Cartera](dashboard.md): la vista de gerencia de la cartera en una pantalla: saldo, vencido y días de cartera con comparación, aging por tramos, terceros con mayor saldo, clientes sobre cupo, cubrimiento y efectividad de cobro; exportar a Excel. Requiere el permiso del menú gerencial.

## Maestros

- [Cobradores](cobradores.md): las personas que hacen la gestión de cobro, su suplente y su tope diario; reglas de asignación por zona, vendedor, saldo o mora, y ausencias. Requiere la fase 2 habilitada.
- [Edades de cartera](edades.md): los tramos de antigüedad con los que se agrupa la cartera por vencer y vencida de la compañía; cómo crear, editar, eliminar, restaurar los valores del legado y exportar los tramos, y qué pasa cuando otro usuario los cambia.
- [Maestros de Cartera por tipo](maestros.md): cómo se organiza el menú **Maestros** en cuentas por cobrar (clientes y vendedores), cuentas por pagar (proveedores y compradores) y configuración de cartera; qué permisos hacen falta para cada uno.
- [Parámetros de cartera](parametros.md): la configuración de la cobranza de la compañía: nivel de cobranza, semáforo de cupo, reparto de cartera y horarios de contacto, con sus valores por validar.

## Movimientos

- [Seguimiento de Cartera](movimientos/seguimiento.md): la lista de clientes (por cobrar) y proveedores (por pagar) con su saldo, vencido y mora a una fecha de corte; registro de gestiones en un panel lateral, **Mis alertas**, semáforo de cupo y exportar a Excel o PDF.
- [Cola de cobro](movimientos/cola.md): a quién cobrar hoy, ordenado por prioridad y con el motivo de cada cliente; vistas Mi cola, Equipo y Sin asignar; exportar a Excel o PDF. Requiere la fase 2.
- [Estado de cuenta por correo](movimientos/estado-cuenta.md): enviar a un cliente o en lote el PDF con sus documentos pendientes, con vista previa, registro de envíos, reintentos y plantilla del correo. Requiere la fase de envío de correo habilitada.
- [Generación de cobros](movimientos/generacion.md): genera los cobros del día (asignaciones, reparto y cola) con vista previa, progreso, historial, deshacer y reintentar. Requiere la fase 2.

## Consultas y reportes

Están en el grupo **Consultas** del menú de Cartera. Cada reporte se consulta con **Consultar** y se exporta a Excel o a PDF con sus propios permisos.

- [Cartera de terceros](reportes/terceros.md): el saldo de cada tercero a una fecha de corte, en resumen o con sus documentos; por cobrar (CxC) o por pagar (CxP), con valores o rangos de edad.
- [Cartera de terceros por sucursal](reportes/sucursales.md): el mismo saldo separado por sucursal, con los documentos sin sucursal agrupados en **Sin sucursal**.
- [Cartera por vendedores](reportes/vendedores.md): el saldo por vendedor (o comprador), con su zona o ciudad; los terceros sin zona ni ciudad aparecen en **Sin ciudad/zona**.

## Accesos desde otros módulos

- **Clientes** y **Vendedores** se abren desde Cartera, pero sus pantallas están en el módulo [Ventas](../ventas/readme.md). **Proveedores** y **Compradores** se abren desde Cartera con las pantallas de [Compras](../compras/readme.md); ver [Maestros de Cartera por tipo](maestros.md).
