[Regresar a la documentación V2026](../../README.md)

---

# 📦 Ficha del cliente · Referencias vendidas

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Clientes-blue)
![Static Badge](https://img.shields.io/badge/Opcion-FichaReferenciasVendidas-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261025-yellow)

---

## 📋 Descripción

La pestaña **Referencias vendidas** muestra **lo que el cliente nos ha comprado**, de **mayor a menor**, para ver qué productos rotan y cuáles se enfrían. También reparte lo vendido por **bodega, grupo, subgrupo, línea y talla**.

Es una pantalla de **consulta**: no crea, no edita ni elimina nada.

> 📘 Para el uso general de tablas (orden, paginación y exportación) vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Las ventas se muestran **netas**: las devoluciones **restan**. Los valores no incluyen impuestos y ya tienen descuentos aplicados.

> 💡 Los documentos **no se abren desde aquí**. Desde cada referencia puede ver los documentos y líneas en que se vendió, pero no abrirlos.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Maestros**, haga clic en **Clientes**.
3. Busque el cliente y ábralo en **Editar** (ficha).
4. Haga clic en la pestaña **Referencias vendidas**.

La pestaña solo aparece si su perfil puede **consultar ventas por clientes y referencias**. Si no la ve, pida ese permiso a su administrador.

---

## 🖥️ Pantalla principal

![Resumen de referencias vendidas](../recursos/img/ficha-referencias-vendidas/01-resumen.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **Desde** y **Hasta** | Rango de fechas de las ventas. Por defecto es el **último mes**. Puede ampliarlo para ver más historia. |
| **Ordenar por** | **Valor neto** (por defecto) o **Cantidad**. Cambia el orden de la lista. |
| **Consultar** | Vuelve a calcular con el rango y el orden elegidos. La pantalla no se actualiza sola. |
| **Tarjetas de totales** | **Referencias**, **Cantidad neta** (ventas menos devoluciones) y **Valor neto** (sin impuestos, con descuentos). |
| **Lista de referencias** | Una referencia por fila o tarjeta, de mayor a menor, con cantidad y valor. |
| **Ver documentos de…** | Abre el detalle de esa referencia (ver más abajo). |

Al pie de la consulta aparece cuándo se calculó (**«Del … al …, ordenado de mayor a menor por …, calculado a las …»**).

### Mayor a menor

La lista siempre va de **mayor a menor** según la métrica elegida:

- Con **Valor neto**, arriba están las referencias que más dinero representan.
- Con **Cantidad**, arriba están las que más unidades representan.

Cambie la métrica en **Ordenar por** y pulse **Consultar** si lo necesita. Las dos vistas se pueden comparar para encontrar productos con mucho volumen y poco valor, o al revés.

![Ordenada por cantidad](../recursos/img/ficha-referencias-vendidas/02-por-cantidad.png)

### Devoluciones

Las devoluciones de venta **restan** de la cantidad y del valor de la referencia. Una referencia con más devoluciones que ventas puede quedar con cantidad neta negativa.

![Referencias con devoluciones](../recursos/img/ficha-referencias-vendidas/03-con-devoluciones.png)

---

## 🔎 Ver los documentos de una referencia

1. Haga clic en **Ver documentos de** la referencia (o en su fila).
2. Aparece **Documentos y líneas de** esa referencia en el periodo, con:
   - **Documento**, **Fecha**, **Cantidad**, **Valor neto** y **Descuento** de cada línea.
   - Las devoluciones aparecen con **Devolución: resta**.
3. Para cerrar, haga clic en **Cerrar**.

![Detalle de una referencia](../recursos/img/ficha-referencias-vendidas/04-detalle.png)

---

## 📊 Indicadores del periodo

Debajo de la lista están los **Indicadores del periodo**. Cada barra muestra la **parte del total** que aporta ese grupo, con el mismo orden de mayor a menor:

| Indicador | Qué agrupa |
|-----------|------------|
| **Por bodega** | Lo vendido desde cada bodega. |
| **Por grupo** | Grupos de referencias. |
| **Por subgrupo** | Subgrupos dentro de cada grupo. |
| **Por línea** | Líneas de producto. |
| **Por talla** | Tallas de las referencias. |

Cada grupo muestra su cantidad o valor neto y su **porcentaje del total**. Si hay más grupos de los visibles, use **Ver detalle (+n)** para verlos todos y **Ver menos** para volver.

Si en el periodo no hubo ventas, aparece **Sin ventas en el periodo**.

---

## 🗓️ Rango de fechas

- Por defecto se consulta el **último mes**.
- Para ver ventas anteriores, cambie **Desde** y pulse **Consultar**.
- Si el rango no tiene ventas, aparece **Este cliente no tiene ventas entre el … y el …**. Amplíe el rango para ver ventas anteriores.

![Rango sin ventas](../recursos/img/ficha-referencias-vendidas/05-vacio-por-rango.png)

---

## 🔄 Cambios de otros usuarios (en vivo)

Esta pantalla **no se actualiza sola**. Si se registran ventas o devoluciones mientras la consulta está abierta, pulse **Consultar** para recalcular.

---

## ❓ Preguntas frecuentes

**¿Por qué una referencia no aparece?**
No se vendió en el rango de fechas. Amplíe **Desde** o revise que la venta no sea anterior al último mes.

**¿Por qué la cantidad neta es menor que la vendida?**
Porque las devoluciones restan. Compare con el detalle de la referencia para ver las devoluciones.

**¿Los valores incluyen IVA?**
No. El valor neto va sin impuestos y con los descuentos aplicados.

**¿Puedo abrir la factura de una venta desde aquí?**
No. Los documentos se muestran para consulta; la pantalla de cada documento llegará con su módulo.

**¿Por qué no veo esta pestaña?**
Su perfil no tiene el permiso de consulta de ventas por clientes y referencias.

---

## 🛠️ Errores comunes

| Mensaje | Qué hacer |
|---------|-----------|
| **No tiene permiso para ver esta información** | Su perfil no tiene el permiso necesario. Consulte con su administrador. |
| **No se pudo cargar el detalle** | Vuelva a elegir la referencia o pulse **Reintentar**. |
| **Esta referencia ya no está disponible para este cliente** | Las ventas pudieron cambiar. Pulse **Consultar**. |
| **La fecha inicial no puede ser posterior a la final** | Corrija el rango de fechas. |

---

## 🧷 Relacionado

- [Ficha del cliente · Pedidos y sus Facturas de Despachos](ficha-pedidos.md)
- [Ficha del cliente · Remisiones y sus Facturas de Venta](ficha-remisiones.md)
- [Ficha del cliente · Facturas de Venta y sus Recibos de Caja](ficha-facturas.md)
