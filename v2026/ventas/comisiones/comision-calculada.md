[Regresar a Ventas](../readme.md)

---

# Comisión calculada

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Comisiones-blue)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## Descripción

**Comisión calculada** muestra cuánto le corresponde comisión a un vendedor en un periodo, con las reglas que están vigentes **hoy**. Para cada línea indica qué regla se aplicó: de referencia, de cliente, general del vendedor o de la compañía.

Es solo una **consulta**. No liquida, no paga, no guarda resultados y no congela el periodo: cada vez que consulta, el cálculo se hace de nuevo.

Las reglas se configuran en la pestaña **Comisiones** de la [ficha del vendedor](../vendedores/ficha-comisiones.md).

> Para el uso general de las tablas y la ayuda vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## Acceso

1. En el menú principal, haga clic en **Ventas**.
2. Abra la opción **Comisión calculada** dentro del módulo Ventas.

Para ver la pantalla necesita el permiso **Consultar** sobre **Comisión calculada**.

---

## Pantalla principal

![Comisión calculada con resultado](../recursos/img/vendedores-comisiones/10-comision-calculada.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral. |
| **Vendedor** | Vendedor al que se calcula la comisión. Es obligatorio. Busque por código o nombre. |
| **Desde** y **Hasta** | Periodo del cálculo. Por defecto es el mes en curso. Máximo 366 días y sin fechas futuras. |
| **Regla aplicada** | Filtra las líneas por la regla usada: **Todas**, **Referencia**, **Cliente**, **General** o **Compañía**, y **Sin regla**. |
| **Consultar** | Calcula con los filtros elegidos. Cambiar un filtro **no consulta** hasta que pulse el botón. |
| **Exportar Excel** | Descarga el resultado. Ver [Exportar a Excel](#exportar-a-excel). |
| **Comisión total** y tarjetas | Comisión de ventas, comisión de recaudo y comisión total del periodo. |
| **Calculado a las [hora] con las reglas vigentes** | Indica cuándo se calculó. |
| **Actualizar** | Vuelve a calcular con las reglas vigentes en ese momento. |

### Las secciones de resultado

El resultado se divide en dos secciones:

- **Ventas**: una línea por cada factura o devolución de la línea de venta. Muestra documento, fecha, cliente, referencia, base, porcentaje, **regla aplicada** y comisión.
- **Recaudo**: una línea por cada cruce entre un recibo y una factura. Muestra recibo, factura, cliente, fecha del recibo, vencimiento, **edad en días**, tramo, base, porcentaje, **regla aplicada** y comisión.

Las devoluciones aparecen con base y comisión **negativas**.

Cada sección tiene su propia tabla, con buscador por cliente (escriba al menos 2 letras) y sus encabezados para ordenar.

### Totales

- Los totales de cada sección y el **total general** se calculan sobre **todo el filtro**, no solo sobre la página que ve.
- Al pie de cada tabla aparece **Total del filtro**, con la base y la comisión.
- Las cifras se muestran con 2 decimales.

### Comisión por regla aplicada

Una tabla resume cuánta comisión vino de cada regla, por sección. Permite ver de un vistazo si la comisión depende de excepciones o de la tarifa general.

---

## Líneas sin regla

Si alguna línea no tuvo ninguna regla vigente, aparece el aviso **Hay líneas sin regla**, con el texto: **[n] líneas no tienen ninguna regla vigente y comisionan 0 %. Configure la tarifa general del vendedor o la de la compañía.**

Pulse **Ver solo esas líneas** para filtrar la tabla y revisar solo esos casos. Las líneas aparecen con la regla **Sin regla**.

Para corregirlas, vaya a la pestaña **Comisiones** del vendedor y configure la tarifa general o la escala general, o la de la compañía.

![Comisión calculada con líneas sin regla](../recursos/img/vendedores-comisiones/11-comision-lineas-sin-regla.png)

---

## Estados y mensajes

| Mensaje | Qué significa o qué hacer |
|---------|---------------------------|
| **Elija un vendedor y un periodo** | Pantalla inicial. Elija el vendedor y pulse **Consultar**. |
| **Calculando la comisión…** | El cálculo está en curso. Espere. |
| **El cálculo tarda más de lo normal.** | Se sigue procesando; la pantalla se actualizará sola. |
| **Sin ventas ni recaudo en el periodo** | El vendedor no tiene movimientos comisionables entre esas fechas. Cambie el periodo y consulte de nuevo. |
| **Sin líneas de venta** / **Sin líneas de recaudo** | No hay líneas de esa sección con el filtro elegido. |
| **Elija un vendedor.** | El vendedor es obligatorio. |
| **Escriba la fecha.** | Falta **Desde** o **Hasta**. |
| **La fecha no puede ser futura.** | Elija hoy o una fecha anterior. |
| **«Desde» no puede ser posterior a «Hasta».** | Corrija las fechas. |
| **El periodo no puede superar 366 días.** | Acorte el periodo. |
| **La consulta supera el máximo de líneas por sección. Acorte el periodo y consulte de nuevo.** | Use un periodo más corto. |
| **El servidor rechazó el filtro. Revise el vendedor y el periodo.** | Revise el vendedor y las fechas, y consulte otra vez. |
| **Este tercero tiene más de un registro de vendedor en la compañía; no se puede calcular su comisión.** | Pida a su administrador que revise el dato del vendedor. |
| **[n] reglas se ignoraron porque su cliente o referencia ya no existe.** | Revise las reglas del vendedor en la pestaña **Comisiones**. |
| **No se pudo cargar el detalle** | Pulse **Reintentar** o consulte de nuevo. |
| **Su rol no puede consultar la comisión calculada. Pida el acceso a un administrador.** | Su perfil no tiene el permiso de la consulta. |

---

## Exportar a Excel

1. Calcule el resultado con el vendedor y el periodo que necesite.
2. Pulse **Exportar Excel**.
3. El archivo trae las secciones **Ventas** y **Recaudo**, una fila de **TOTAL** y el encabezado de la compañía, los filtros usados, su usuario y la fecha.

Si el resultado supera **50.000 líneas**, el sistema no exporta. Acorte el periodo y vuelva a exportar.

El botón **Exportar Excel** solo aparece si su perfil tiene permiso para exportar esta consulta.

![Exportar la comisión calculada a Excel](../recursos/img/vendedores-comisiones/12-comision-exportar.png)

---

## Qué ve cada permiso

| Permiso | Qué ve |
|---------|--------|
| Consultar **Comisión calculada** | La consulta completa, sin el botón de exportar. |
| Consultar y **Exportar** en **Comisión calculada** | Además, el botón **Exportar Excel**. |
| Sin Consultar | La pantalla muestra que no tiene permiso. No se calcula nada. |

---

## Cambios de otros usuarios

El resultado **no se guarda**: dos personas pueden consultar al mismo tiempo sin afectarse. Si cambia una regla en la pestaña **Comisiones** después de calcular, el resultado mostrado no cambia hasta que pulse **Actualizar**. La hora de **Calculado a las** le indica qué tan reciente es.

---

## Preguntas frecuentes

**¿Esta consulta paga o liquida la comisión?**
No. Solo calcula. Liquidar, pagar o congelar comisiones no está disponible en esta versión.

**¿Por qué el total cambia si consulto otro día?**
El cálculo usa las reglas vigentes en el momento de la consulta. Si una regla cambió o hubo nuevas facturas o recibos, el resultado cambia.

**¿Por qué una venta aparece con 0 %?**
Ninguna regla vigente aplicó a esa línea en la fecha del documento. Aparece como **Sin regla**.

**¿Qué pasa con las devoluciones?**
Restan: aparecen con base y comisión negativas.

**¿Por qué el recaudo se calcula por edad?**
La comisión de recaudo depende de cuántos días después del vencimiento se pagó la factura. La **edad** es la fecha del recibo menos el vencimiento; si es negativa, el cliente pagó antes.

---

## Relacionado

- [Ficha del vendedor · Comisiones](../vendedores/ficha-comisiones.md)
- [Ficha del vendedor · Ventas](../vendedores/ficha-ventas.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
