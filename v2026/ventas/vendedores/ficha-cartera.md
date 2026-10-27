[Regresar a Ventas](../readme.md)

---

# Ficha del vendedor · Cartera

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Vendedores-blue)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## Descripción

La pestaña **Cartera** muestra cuánto deben los clientes de **lo que vendió este vendedor**, a una fecha de corte. Los saldos se agrupan por cliente y por edad del documento, para saber qué está vencido y qué está por vencer.

Solo muestra cartera **por cobrar** de clientes. No muestra proveedores ni lo que la compañía debe a terceros.

Es una pantalla de **consulta**: no registra cobros ni cruces. Para la gestión de cobro de un cliente use la ficha del cliente.

> Para el uso general de las tablas (orden, paginación y ayuda) vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Maestros de Ventas**, haga clic en **Vendedores**.
3. Busque el vendedor y haga clic en el lápiz (**Editar**) de su fila.
4. Haga clic en la pestaña **Cartera**.

---

## Pantalla principal

![Cartera del vendedor](../recursos/img/vendedores-ficha/02-cartera.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la ficha. |
| **Fecha de corte** | Día con el que se calculan los saldos. Por defecto es hoy. No puede ser una fecha futura. |
| **Rango de vencimiento** | Cambia los tramos de edad de las columnas. Ver [Rango de vencimiento](#rango-de-vencimiento). |
| **Saldo cero** | Muestra también los clientes cuyo saldo ya es cero. Se aplica al instante. |
| **Consultar** | Aplica la fecha de corte y el rango de vencimiento. La pantalla no se actualiza sola. |
| **Buscar cliente** | Filtra la lista por nombre o código del cliente. Escriba al menos 2 letras. Para quitar el texto, use **Quitar la búsqueda**. |
| **Exportar Excel** | Descarga la lista filtrada. Ver [Exportar a Excel](#exportar-a-excel). |
| **Tarjetas de totales** | **Saldo total**, **Vencido** y **Por vencer**, del conjunto filtrado (no solo de la página). |
| **Tabla de clientes** | Un cliente por fila, con su saldo total, lo vencido y su número de documentos. Los saldos por edad aparecen como columnas. |

### Columnas de la tabla

| Columna | Qué muestra |
|---------|-------------|
| **Cliente** | Nombre del cliente. |
| **Saldo total** | Suma de los saldos pendientes de todos sus documentos. |
| **Vencido** | Saldo de los documentos que ya superaron su vencimiento. |
| **Documentos** | Cuántos documentos con saldo tiene el cliente. |
| Columnas de edad | Saldo por tramo de días de atraso. El primer tramo es **Por vencer**; los demás muestran el rango de días, por ejemplo **1–30 días**, o **Más de 90 días**. |

Para ver los documentos de un cliente, use el botón **Ver los documentos de [cliente]** de su fila.

### Documentos de un cliente

Al abrir un cliente se muestra la lista de sus documentos con saldo, con estas columnas:

- **Documento**, **Fecha** y **Vencimiento**.
- **Días de mora**: días de atraso del documento.
- **Valor** y **Saldo** del documento.

Esta lista también se pagina y se ordena en el servidor.

![Documentos de un cliente en la cartera del vendedor](../recursos/img/vendedores-ficha/04-cartera-documentos.png)

### Rango de vencimiento

El rango define cada cuántos días se agrupan las edades de la cartera.

| Opción | Efecto |
|--------|--------|
| **Por defecto** | Usa la agrupación inicial de la pantalla. |
| **Cada 7 días**, **Cada 14 días**, **Cada 15 días**, **Cada 30 días** | Cambia los tramos de las columnas de edad al rango elegido. |

Cambie el rango y pulse **Consultar** para aplicarlo.

![Cartera del vendedor con otro rango de vencimiento](../recursos/img/vendedores-ficha/03-cartera-rango.png)

### Totales

| Tarjeta | Qué significa |
|---------|---------------|
| **Saldo total** | Suma de todos los saldos de los clientes del filtro. |
| **Vencido** | Saldo con días de mora. |
| **Por vencer** | Saldo que todavía no ha vencido. |

Debajo de la tabla, el resumen indica cuántos clientes se muestran y su saldo. Si hay clientes con saldo cero ocultos, el texto le indica cuántos son.

---

## Mensajes

| Mensaje | Qué hacer |
|---------|-----------|
| **Sin cartera por cobrar al [fecha]** | Los clientes de este vendedor no tienen saldo pendiente a esa fecha. Pulse **Ver clientes con saldo cero** o cambie la fecha de corte. |
| **Ningún cliente coincide con la búsqueda** | Pruebe con otro nombre o pulse **Quitar la búsqueda**. |
| **La fecha no puede ser futura.** | Elija hoy o una fecha anterior. |
| **Cifras con corte al [fecha].** | Indica la fecha de corte con la que se calcularon las cifras. |
| **No se pudo cargar la información** | Sus filtros se conservaron. Pulse **Reintentar**. |
| **No se pudo exportar. Intente de nuevo.** | Pulse **Exportar Excel** otra vez. |
| **Hay más de 50.000 filas con este filtro.** | Acote la búsqueda y exporte de nuevo. |
| **No tiene permiso para ver esta información** | Su perfil no puede consultar la cartera del vendedor. Pida el acceso a su administrador. |

---

## Exportar a Excel

1. Aplique la búsqueda, la fecha de corte y el rango que necesite.
2. Pulse **Exportar Excel**.
3. El archivo tiene los mismos filtros de la pantalla, con el encabezado de la compañía, los filtros usados, su usuario y la fecha.

Si el resultado supera **50.000 filas**, el sistema no exporta. Acote la búsqueda y vuelva a intentar.

El botón solo aparece si su perfil tiene permiso para exportar la cartera por vendedor.

---

## Qué ve cada permiso

| Permiso | Qué ve |
|---------|--------|
| Consultar **Vendedores** y **Cartera por Vendedores** | La pestaña **Cartera** completa, con sus totales y los documentos de cada cliente. |
| Consultar **Vendedores** sin **Cartera por Vendedores** | La pestaña no aparece. |
| Consultar **Cartera por Vendedores** sin **Exportar** | Todo menos el botón **Exportar Excel**. |

---

## Cambios de otros usuarios

Esta pantalla **no se actualiza sola**. Las cifras son las de la última consulta. Si otra persona registra pagos o facturas mientras la mira, pulse **Consultar** para ver el saldo al día.

---

## Preguntas frecuentes

**¿Por qué un cliente aparece en la cartera del vendedor y no en la de otro?**
La cartera se atribuye al vendedor de cada **factura**. Si un cliente tiene facturas de dos vendedores, cada vendedor ve solo el saldo de sus propias facturas.

**¿Por qué no veo los proveedores?**
Esta pestaña es solo de clientes. Muestra únicamente lo que los clientes deben por lo vendido por este vendedor.

**¿Por qué no coincide con el reporte de cartera por vendedor del sistema anterior?**
La pestaña usa las mismas reglas de saldo y edad de ese reporte. Si nota una diferencia, avise a su administrador con la fecha de corte y el vendedor.

**¿Qué hago si el saldo de un cliente se ve raro?**
Pulse **Ver los documentos de [cliente]** para revisar qué documentos lo componen y sus días de mora.

---

## Relacionado

- [Ficha del vendedor · Ventas](ficha-ventas.md)
- [Ficha del vendedor · Clientes asignados](ficha-clientes-asignados.md)
- [Ficha del vendedor · Clientes no asignados](ficha-clientes-no-asignados.md)
- [Ficha del vendedor · Comisiones](ficha-comisiones.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
