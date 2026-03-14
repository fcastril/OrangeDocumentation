[Regresar a Producción](../readme.md)

---
# GANTT DE PRODUCCIÓN

Permite visualizar la ocupación de responsables por órdenes y operaciones en una línea de tiempo.

## Filtros

- Fecha de Corte: filtro principal de consulta.
- Botón Consultar: ejecuta la búsqueda (la primera carga consulta automáticamente).

## Resumen superior

La pantalla muestra un resumen general con:

- Total OPs.
- Total Cantidad.
- Resumen por operación en chips con ícono y color configurados.
- Cada chip incluye Cantidad y Lotes.

## Tabla principal (Responsables)

La tabla principal resume por responsable:

- Responsable.
- OPs.
- Total Cantidad.
- Fecha Inicial Asignada.
- Fecha Máxima Entrega.
- Operación Principal (ícono + color).

Configuración actual:

- Paginación de 10 registros por página.
- Botón Ver para abrir el detalle de calendario del responsable.

## Calendario inferior

Al seleccionar un responsable se muestra el calendario con:

- Escala de fechas (eje de calendario) para visualizar el rango temporal.
- Barras por asignación con color de la operación.
- Texto de barra en formato OP-Consecutivo y Documento Referencia.
- Tooltip con detalle de OP, operación, cantidad, inicio y fin.
- Scroll vertical en la sección para facilitar navegación cuando hay muchas asignaciones.

## Visualización de operación

La visualización de operación usa la configuración del maestro de Operaciones:

- Ícono Font Awesome.
- Color configurado.
- En el resumen se muestra solo la descripción de operación (sin código).
