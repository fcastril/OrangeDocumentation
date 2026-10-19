[Regresar a Compras](../readme.md)

---

# Órdenes de compra y compras por proveedor

**Módulo**: Compras · **Submódulo**: Consultas/Reportes · **Versión**: V2026 · **Actualizado**: 18/10/2026

---

## Descripción

El informe **Órdenes de compra y compras por proveedor** le muestra, para cada proveedor, cuánto le pidió, cuánto ya recibió, cuánto le falta y cuánto le compró, incluidas las compras **sin orden de compra**.

Sirve para evaluar a cada proveedor: si entrega lo pedido, si entrega de más, cuánto está pendiente y cuánto se compra por fuera de las órdenes.

Puede verlo en dos vistas:

- **Resumido**: una fila por proveedor, con sus totales.
- **Detallado**: proveedor → sus órdenes de compra → las compras de cada orden, y al final las compras sin orden de compra.

Es solo de consulta: no modifica órdenes, compras ni inventario.

---

## Acceso

1. En el menú, entre a **Compras › Consultas/Reportes › Órdenes de compra y compras por proveedor**.
2. Para ver el informe necesita el permiso **Consultar** sobre esta pantalla.
3. Para usar **Exportar Excel** y **Exportar PDF** necesita además el permiso **Exportar**.

Las compras y las órdenes se abren desde el informe solo si tiene permiso para consultarlas.

---

## Pantalla principal

![Órdenes de compra y compras por proveedor, vista resumida](../recursos/img/informes/pr-01-resumido.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral. |
| **Del … al …** | Periodo de las **órdenes**. Por defecto, los **últimos 90 días** hasta hoy. |
| **Vista del informe** | **Resumido** o **Detallado**. |
| **Exportar Excel** / **Exportar PDF** | Descarga el resultado con los mismos filtros. Ver *Exportar*. |
| **Filtros** | Proveedor, Comprador, Tipo de orden de compra, Recepción, Solo vencidas e Incluir anuladas. Ver *Filtros*. |
| **Consultar** | Ejecuta el informe con los filtros elegidos. |
| Totales | Cifras de **todo el filtro**, no solo de la página. |

> El informe **no se consulta solo**. Si cambia un filtro, pulse **Consultar**.

---

## Filtros

| Filtro | Qué hace |
|--------|----------|
| **Desde** / **Hasta** | Fecha de la orden. El rango no puede superar **366 días**. |
| **Proveedor** | Solo esos proveedores. Puede elegir varios (máximo 50). |
| **Comprador** | Solo las órdenes de ese comprador. |
| **Tipo de orden de compra** | Solo ese tipo de orden. |
| **Recepción** | **Todas**, **Pendientes** (sin recibir y parciales), **Sin recibir**, **Parciales**, **Realizadas** (recepción total) o **Con exceso**. |
| **Solo vencidas** | Solo las órdenes con saldo cuya fecha de entrega ya pasó. |
| **Incluir anuladas** | Muestra las órdenes anuladas, marcadas. No suman a los totales. |

---

## Vistas

### Resumido

Una fila por proveedor y al final el **TOTAL GENERAL**.

| Columna | Qué significa |
|---------|---------------|
| **Órdenes** | Cuántas órdenes tiene el proveedor en el periodo. |
| **Pedido** | Cantidad y valor pedidos. |
| **Recibida** | Cantidad recibida, neta: las devoluciones restan. |
| **Saldo** | Lo que falta por recibir. |
| **Exceso** | Lo que se recibió de más. |
| **Valor pendiente** | Valor estimado de lo que falta por recibir. |
| **Compras** | Cuántas compras cumplieron las órdenes del proveedor. |
| **Comprado neto** | Compras menos devoluciones de esas órdenes. |
| **Devoluciones** | Valor de las devoluciones. |
| **Compras sin OC** | Cuántas compras **sin orden de compra** tiene y su valor neto. |

### Detallado

![Detallado por proveedor](../recursos/img/informes/pr-02-detallado.png)

Cada proveedor tiene:

1. Sus **órdenes de compra**, con la misma recepción y saldo del informe de órdenes de compra.
2. En cada orden, el botón **Ver compras**, que abre el detalle de las compras que la cumplieron.
3. Al final, el bloque **Compras sin OC de [proveedor]**, con sus documentos.

### Reglas de atribución

- Una orden se cuenta en el **proveedor de la orden**.
- Una compra sin orden se cuenta en el **proveedor de la compra**.
- Si una compra cumple una orden de **otro proveedor**, se cuenta en el proveedor de la **orden**. En el detalle aparece marcada como **proveedor distinto**.
- **Valor** es el subtotal de las líneas, **sin IVA ni retenciones** del encabezado.
- Las compras **anuladas no suman**.
- Una compra que cumple una orden, pero cae **fuera del rango de fechas** de la orden, no suma en la fila del proveedor. Se ve en el detalle de la orden.

---

## Ver las compras de una orden

1. En el detalle, pulse **Ver compras** en la fila de la orden.
2. Se abre el panel **Compras de la orden**, con la recepción por variante y las compras que la cumplieron.
3. Las devoluciones restan. Las compras anuladas aparecen marcadas y no suman.
4. Pulse **Cerrar el detalle** para volver.

Para el detalle completo, vea el [informe de órdenes de compra](ordenes-compra.md#ver-las-compras-de-una-orden).

![Detalle de una orden con una compra de otro proveedor](../recursos/img/informes/pr-03-proveedor-distinto.png)

---

## Exportar a Excel y a PDF

Con el permiso **Exportar** verá **Exportar Excel** y **Exportar PDF**. Descargan el informe con **los mismos filtros** y la misma vista.

| Formato | Límite | Qué incluye |
|---------|--------|-------------|
| **Excel** (.xlsx) | Hasta **50.000 filas**. | Una fila por proveedor, con sus órdenes y su bloque de compras sin OC, y el **TOTAL GENERAL**. |
| **PDF** | Hasta **4.000 filas**. Se imprime en horizontal. | Encabezado con la empresa, los filtros, el usuario y la fecha y hora; **subtotales por proveedor** y **TOTAL GENERAL**. |

Si el resultado supera el límite, no se descarga nada: *Hay demasiadas filas para exportar a Excel (máximo 50.000). Acota los filtros.* o *El PDF admite hasta 4.000 filas; filtra más o usa Excel.*

---

## Estados de la pantalla

| Situación | Qué ve |
|-----------|--------|
| Antes de consultar | *Elige los filtros y consulta*. |
| Sin resultados | *No hay resultados para los filtros elegidos*. |
| Error al consultar | *No se pudo consultar el informe*, con **Reintentar**. Sus filtros se conservan. |
| Sin permiso | *No tiene permiso para ver este informe*. |

---

## Preguntas frecuentes

**¿Por qué una compra aparece en un proveedor y su orden en otro?**
La orden manda. La compra se cuenta en el proveedor de la orden y en el detalle aparece **proveedor distinto**.

**¿Por qué el proveedor tiene compras sin OC?**
Son compras registradas sin orden de compra. Es normal y se cuentan aparte, en el bloque **Compras sin OC**.

**¿Por qué no veo una orden anulada?**
Active **Incluir anuladas**. La orden aparece marcada, sin saldo, y no suma a los totales.

**¿Por qué el proveedor no aparece?**
Revise el rango de fechas y los filtros. El rango se aplica a la **fecha de la orden**.

---

## Otros informes de Compras

- [Informe de órdenes de compra](ordenes-compra.md)
- [Compras por tipo de movimiento](tipo-movimiento.md)
- [Compras por tipo y referencia](tipo-referencia.md)
- [Órdenes de compra y compras por comprador](compradores.md)

[Regresar a Compras](../readme.md)
