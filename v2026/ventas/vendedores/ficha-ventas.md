[Regresar a Ventas](../readme.md)

---

# Ficha del vendedor · Ventas

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Vendedores-blue)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## Descripción

La pestaña **Ventas** muestra cómo ha vendido un vendedor en un periodo: cuánto vendió neto, cuántos documentos emitió, a qué clientes y con qué referencias, y cómo compara con periodos anteriores.

Es una pantalla de **consulta**: no crea, cambia ni elimina nada. Las cifras son las de la última vez que pulsó **Consultar**.

> Para el uso general de las tablas (orden, paginación y ayuda) vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Maestros de Ventas**, haga clic en **Vendedores**.
3. Busque el vendedor y haga clic en el lápiz (**Editar**) de su fila.
4. Haga clic en la pestaña **Ventas**.

Las pestañas de consulta solo aparecen en un vendedor **guardado**. En un vendedor nuevo no las verá.

---

## Pantalla principal

![Ventas del vendedor](../recursos/img/vendedores-ficha/01-ventas.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la ficha. |
| **Desde** y **Hasta** | Periodo de la consulta. Por defecto es el último mes. El periodo no puede superar 366 días, no puede tener fechas futuras y **Desde** no puede ser posterior a **Hasta**. |
| **Consultar** | Aplica el periodo elegido. Cambiar las fechas no consulta hasta que pulse el botón. |
| **Tarjetas de indicadores** | Ventas netas, Devoluciones, Documentos de venta, Ticket promedio y Clientes atendidos del periodo. |
| **Evolución de los últimos 12 meses** | Ventas netas mes a mes. No depende del periodo elegido: siempre muestra 12 meses hasta el mes de **Hasta**. |
| **Top 10 clientes** | Los diez clientes con más ventas netas del periodo. |
| **Top 10 referencias** | Las diez referencias con más ventas netas del periodo. |
| **Comparativo** | Compara el periodo elegido con el periodo anterior (de igual duración) y con el mismo periodo del año anterior. |

### Qué significa cada indicador

| Indicador | Cómo se calcula |
|-----------|-----------------|
| **Ventas netas** | Facturas menos devoluciones, sin IVA y después de descuento. |
| **Devoluciones** | Valor devuelto en el periodo. |
| **Documentos de venta** | Número de facturas del periodo (las devoluciones no cuentan como documento). |
| **Ticket promedio** | Ventas netas dividido entre documentos de venta. |
| **Clientes atendidos** | Clientes distintos con al menos una factura en el periodo. |

Las facturas anuladas no se cuentan.

### Comparativo

| Fila | Qué muestra |
|------|-------------|
| **Periodo elegido** | Ventas netas del periodo que eligió. |
| **Periodo anterior (misma duración)** | Ventas netas de los mismos días inmediatamente antes de **Desde**. |
| **Mismo periodo del año anterior** | Ventas netas de las mismas fechas, un año antes. |

Cada fila muestra la **Variación** en valor y en **Variación %**. Si el periodo de comparación no tuvo ventas, la variación en porcentaje muestra **n/a**.

Debajo del comparativo aparece la **participación**: el porcentaje que representan las ventas del vendedor frente a las ventas de toda la compañía en el mismo periodo.

> La pestaña no muestra ventas de otros vendedores ni un ranking entre vendedores. Solo muestra la participación del vendedor sobre la compañía.

---

## Mensajes

| Mensaje | Qué hacer |
|---------|-----------|
| **Sin ventas en el periodo** | El vendedor no tiene facturas ni devoluciones entre esas fechas. Cambie el periodo y pulse **Consultar**. |
| **Sin ventas en los últimos 12 meses.** | No hay ventas en la evolución. |
| **Escriba la fecha.** | Falta **Desde** o **Hasta**. |
| **La fecha no puede ser futura.** | Elija hoy o una fecha anterior. |
| **«Desde» no puede ser posterior a «Hasta».** | Corrija las dos fechas. |
| **El periodo no puede superar 366 días.** | Acorte el periodo. |
| **No se pudo cargar la información** | Sus filtros se conservaron. Pulse **Reintentar**. |
| **No tiene permiso para ver esta información** | Su perfil no puede consultar esta pestaña. Pida el acceso a su administrador. |
| **Vendedor no disponible** | El vendedor ya no existe en esta compañía. Vuelva a **Vendedores**. |

---

## Qué ve cada permiso

| Permiso | Qué ve |
|---------|--------|
| Consultar **Vendedores** y **Ventas por clientes y referencias** | La pestaña **Ventas** completa. |
| Solo Consultar **Vendedores** | La pestaña no aparece. |

Esta pestaña **no exporta a Excel**.

---

## Cambios de otros usuarios

Esta pantalla **no se actualiza sola**. Si otra persona registra ventas mientras la mira, pulse **Consultar** para ver las cifras al día.

---

## Preguntas frecuentes

**¿Por qué la venta del vendedor no coincide con lo que veo en un cliente?**
La pestaña suma las facturas y devoluciones **registradas con este vendedor** en el documento. Si un cliente tiene facturas de varios vendedores, cada una cuenta para el vendedor que aparece en ella.

**¿Por qué la evolución no cambia cuando cambio el periodo?**
La evolución siempre muestra los últimos 12 meses hasta el mes de **Hasta**, sin importar el periodo elegido.

**¿Para qué sirve la ayuda de la pestaña?**
Pulse **?** junto al título para leer este manual sin salir de la ficha.

![Botón de ayuda de la ficha del vendedor](../recursos/img/vendedores-ficha/08-ayuda.png)

---

## Relacionado

- [Ficha del vendedor · Cartera](ficha-cartera.md)
- [Ficha del vendedor · Clientes asignados](ficha-clientes-asignados.md)
- [Ficha del vendedor · Clientes no asignados](ficha-clientes-no-asignados.md)
- [Ficha del vendedor · Comisiones](ficha-comisiones.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
