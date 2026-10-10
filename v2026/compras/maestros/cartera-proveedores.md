[Regresar a Compras](../readme.md)

---

# 💰 Cartera de Proveedores

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Compras-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Cartera%20Terceros%20(107)-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## 📋 Descripción

La **cartera de proveedores** muestra cuánto le debe la compañía a cada proveedor a una **fecha de corte**, con sus documentos (facturas, devoluciones y anticipos) y la **historia** de cómo se han ido pagando.

Es una pantalla **solo de consulta**: desde aquí no se crea, no se edita y no se elimina nada. Los pagos, las notas y las facturas se registran en sus pantallas de origen, y la cartera los toma de ahí.

La cartera está en la pestaña **Cartera** de la pantalla de [Proveedores](proveedores.md). Dentro de ella hay dos vistas: **Saldos** (el listado de la cartera) y **Dashboard** (el resumen de la cartera a una fecha de corte). Ver [Dashboard](#-dashboard).

> 📘 La búsqueda, el orden, la paginación y la ayuda funcionan igual en todas las tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Compras**.
2. En **Maestros**, haga clic en **Proveedores**.
3. Haga clic en la pestaña **Cartera**, junto a **Proveedores**, en la parte de arriba de la pantalla.

![Pestaña Cartera junto a Proveedores](../recursos/img/cartera-proveedores/00-pestana-cartera.png)

También puede llegar desde la ficha de un proveedor: en la pantalla de [Proveedores](proveedores.md), abra la ficha y use el botón **Cartera**. Se abre la cartera con los documentos de ese proveedor ya abiertos.

La pestaña **Cartera** aparece solo si tiene el permiso **Consultar** sobre la opción *Cartera Terceros* (menú Cartera › Consultas/Reportes). Si no lo tiene, no verá la pestaña; y si escribe la dirección de la cartera, vuelve a la pantalla de Proveedores con un aviso. Para ver el botón **Exportar a Excel** necesita además el permiso **Exportar** sobre esa misma opción (ver la tabla de permisos más abajo).

---

## 🖥️ Pantalla principal

![Listado de la cartera de proveedores](../recursos/img/cartera-proveedores/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **Fecha de corte** | Fecha hasta la que se cuentan los pagos y las notas. Por defecto es hoy. No se puede elegir una fecha futura. |
| **Rango de vencimiento** | Reparte el saldo de cada proveedor en tramos de días. Ver *Rangos de vencimiento* más abajo. |
| **Incluir proveedores en saldo cero** | Muestra también los proveedores que ya no deben nada. Ver *Saldo cero* más abajo. |
| **Más filtros** | Permite filtrar por **Tipo de movimiento** y por **Centro de costos**. |
| **Consultar** | Aplica la fecha de corte, el rango y los filtros que haya elegido. |
| **Actualizar** | Vuelve a calcular la cartera con los mismos filtros, para ver los saldos al día. |
| **Exportar a Excel** | Descarga todo el listado filtrado. Ver *Exportar a Excel* más abajo. |
| **Buscar por documento o nombre** | Filtra por NIT o por nombre del proveedor. Escriba al menos dos caracteres. |
| **Encabezados** | Un clic en el nombre de una columna ordena el listado por esa columna. Otro clic invierte el orden. Por defecto, el listado va del mayor saldo al menor. |
| **Filas por página** y paginación | Cambian cuántos proveedores ve por página (10, 25, 50 o 100). |

Las tarjetas de arriba suman el **filtro completo**, no solo la página que está viendo:

| Tarjeta | Qué suma |
|---------|----------|
| **Saldo por pagar** | Lo que la compañía debe a todos los proveedores del filtro. |
| **Vencido** | El saldo de los documentos que ya tienen atraso. |
| **Saldo a favor** | Anticipos, sobrepagos y notas sin aplicar. Se muestra en valor positivo, rotulado **Saldo a favor**, y ya está descontado del saldo por pagar. |
| **Proveedores** | Cuántos proveedores cumplen el filtro actual. |

Debajo de las tarjetas aparece la línea **Saldos con corte al** (la fecha de corte) **· calculado a las** (la hora en que se calculó). Si hay proveedores en saldo cero ocultos, la línea indica cuántos son y tiene el enlace **mostrarlos**.

### Columnas del listado

| Columna | Qué muestra |
|---------|-------------|
| **NIT** | Documento del proveedor, con su dígito de verificación. |
| **Proveedor** | Nombre del proveedor. Haga clic en el nombre para ver sus documentos. |
| **Comprador** | El comprador asignado al proveedor. |
| **Docs.** | Cuántos documentos con saldo tiene el proveedor. |
| **Valor total** | Suma del valor de sus documentos. |
| **Notas** | Notas débito y crédito aplicadas a sus documentos. |
| **Pagos** | Egresos aplicados a sus documentos. |
| **Saldo** | Lo que se le debe (valor total − notas − pagos). |
| **Vencido** | La parte del saldo que ya está vencida. |
| **Mayor atraso** | Los días de atraso del documento más atrasado. Dice **Al día** si no tiene nada vencido, o **Vence en** y los días que faltan. |

Cuando elige un **rango de vencimiento**, aparecen además las columnas de tramos (ver más abajo).

Los saldos a favor se marcan con la etiqueta **A favor**. Los proveedores que están en cero y se muestran con la opción de saldo cero llevan la etiqueta **Saldo 0**.

> 📱 En pantallas pequeñas, cada proveedor se muestra como una tarjeta con sus datos principales.

### Si la consulta falla

Si la cartera no carga, la pantalla muestra el aviso *"No se pudo consultar la cartera"* con el botón **Reintentar**. Haga clic en **Reintentar** para volver a consultar: los filtros, la fecha de corte y el rango se conservan.

![Error al consultar la cartera, con Reintentar](../recursos/img/cartera-proveedores/22-error-reintentar.png)

![Cartera en pantalla pequeña](../recursos/img/cartera-proveedores/17-movil.png)

![Búsqueda por nombre o documento](../recursos/img/cartera-proveedores/02-buscar.png)

### Rangos de vencimiento

Elija un rango en **Rango de vencimiento** y haga clic en **Consultar**:

| Opción | Tramos de |
|--------|-----------|
| Sin rangos (valores) | No reparte el saldo; solo muestra el total. |
| Semanal (7 días) | 7 días. |
| Catorcenal (14 días) | 14 días. |
| Quincenal (15 días) | 15 días. |
| Mensual (30 días) | 30 días. |

Con un rango, cada proveedor muestra su saldo en tramos: los que **todavía no vencen** (*Vence en…*) y los **vencidos** (*Vencido…*). Con el rango mensual, los tramos son 1–30, 31–60, 61–90, 91–120 y más de 120 días; con los demás rangos, los tramos crecen con el mismo tamaño. La suma de los tramos siempre es igual al saldo del proveedor.

El tramo más cercano al vencimiento se rotula **Vence en** seguido de sus días (por ejemplo, **Vence en 1–30** con el rango mensual). Ese tramo incluye también los documentos que **vencen hoy**.

![Listado con rango mensual](../recursos/img/cartera-proveedores/04-rangos-vencimiento.png)

### Más filtros

Haga clic en **Más filtros** para ver:

- **Tipo de movimiento**: solo cuentan los documentos de ese tipo (por ejemplo, facturas de compra o gastos).
- **Centro de costos**: solo cuentan los documentos cuyo tipo tiene ese centro por defecto.

Elija el filtro y haga clic en **Consultar**. Con **Todos** (la opción por defecto en ambos campos), no se filtra.

![Más filtros](../recursos/img/cartera-proveedores/05-mas-filtros.png)

### Saldo cero

Por defecto, la lista solo muestra los proveedores que **deben algo** (saldo distinto de cero) a la fecha de corte.

- Active **Incluir proveedores en saldo cero** para ver también los proveedores que están en cero. Se marcan con **Saldo 0**.
- Con el selector **Qué mostrar** puede elegir **Con y sin saldo** o **Solo saldo cero**.

Un proveedor que nunca tuvo documentos de cartera no aparece en ningún caso.

![Proveedores con saldo cero](../recursos/img/cartera-proveedores/03-saldo-cero.png)

### Cuando no hay proveedores

Si a la fecha de corte no hay proveedores con saldo, verá el mensaje **No hay proveedores con saldo a esta fecha**. Cambie la fecha de corte o active **Incluir proveedores en saldo cero**.

![Sin proveedores con saldo](../recursos/img/cartera-proveedores/13-vacio.png)

---

## 📊 Dashboard

El **Dashboard** es la segunda vista de la pestaña **Cartera**, junto a **Saldos** (el listado), en la parte de arriba de la pantalla de Proveedores. Resume la cartera a una fecha de corte: cuánto se debe, cuánto está vencido, cómo envejece la deuda, qué proveedores concentran el saldo, qué vence pronto y qué se pagó en los últimos días.

Las cifras son las mismas de la lista para el mismo corte, rango y filtros. Como la lista, es una pantalla de solo consulta.

Para abrirlo, en la pestaña **Cartera** haga clic en **Dashboard**. También puede abrirlo con la dirección de la cartera seguida de `?vista=dashboard`.

![Dashboard de la cartera de proveedores](../recursos/img/cartera-proveedores/18-dashboard.png)

### Filtros del dashboard

Los filtros se aplican al hacer clic en **Consultar**. Cambiar un filtro no recalcula la cartera por sí solo.

| Filtro | Opciones | Por defecto |
|--------|----------|-------------|
| **Fecha de corte** | Hasta hoy. No se puede elegir una fecha futura. | Hoy |
| **Tamaño de los tramos** | 7, 14, 15 o 30 días | 30 días |
| **Proveedores en el top** | Top 5 o Top 10 | Top 10 |
| **Ventana de pagos recientes** | Últimos 7, 15, 30, 60 o 90 días | 30 días |
| **Más filtros** | **Tipo de movimiento** y **Centro de costos**, igual que en el listado | Todos |

A diferencia del listado, el dashboard no tiene la opción **Sin rangos**: el envejecimiento siempre se reparte en tramos.

### Tarjetas

| Tarjeta | Qué muestra |
|---------|-------------|
| **Total por pagar** | Suma de los saldos con deuda a la fecha de corte. |
| **Vencido** | Parte del total que ya está vencida, con su porcentaje del total. |
| **Por vencer** | Parte del total que todavía no vence, con su porcentaje. Vencido y por vencer suman el total. |
| **Saldo a favor** | Anticipos, devoluciones y notas sin aplicar. Se muestra en valor positivo y rotulado como **Saldo a favor**. Ese valor ya está descontado del total por pagar. |
| **Proveedores con saldo** | Cuántos proveedores deben algo. Debajo indica cuántos están en saldo cero y cuántos tienen saldo a favor. |

Debajo de las tarjetas aparece la línea **Cifras con corte al** (la fecha de corte) **· calculadas a las** (la hora del cálculo) **· tramos de** (los días del rango elegido).

### Composición

Una barra divide el total entre **Vencido** y **Por vencer**, con su valor y su porcentaje en la leyenda. El botón **Ver proveedores con saldo vencido** abre la lista ordenada por lo vencido (ver *Desglose* más abajo).

### Antigüedad del saldo

Son diez tramos. Los cinco primeros son **por vencer** (*Vence en…*), del más lejano al más cercano. Los cinco últimos son **vencidos** (*Vencido…*), del más cercano al más antiguo. Cada tramo muestra su saldo y su porcentaje del total.

- El tramo más cercano al vencimiento, rotulado **Vence en** con los días del tamaño elegido (por ejemplo, **Vence en 1–30** con tramos de 30 días), incluye también los documentos que vencen **hoy**.
- La suma de los diez tramos es igual al total por pagar.

### Concentración

Muestra los proveedores con más saldo, según el **Top 5** o el **Top 10** elegido, con su saldo y su porcentaje del total.

- La fila **Otros** agrupa al resto de los proveedores. El top más **Otros** da siempre el total por pagar.
- **Otros** puede ser **negativo**: incluye el saldo a favor de los proveedores con anticipos o devoluciones, que se resta de la deuda. Aparece con signo «−», en color de alerta, con la nota que lo explica.

![Concentración con «Otros» negativo](../recursos/img/cartera-proveedores/20-dashboard-otros-negativo.png)

### Vencimientos próximos

Muestra el saldo y el número de documentos que vencen en los próximos **7, 15 y 30 días** desde la fecha de corte. Son acumulados: el de 30 días incluye lo de 7 y de 15. Solo cuentan los saldos de deuda, no los saldos a favor.

Estas barras no abren nada: la lista todavía no filtra por fecha de vencimiento.

### Pagos recientes

Arriba aparece el resumen: cuánto se pagó, en cuántos egresos y entre qué fechas. Abajo están los últimos 10 pagos, con fecha, egreso, proveedor y valor pagado.

Haga clic en el nombre del proveedor para abrir sus documentos. Si no hubo pagos en el periodo, verá el mensaje **No hubo pagos en este periodo**.

### Ver como tablas

El botón **Ver como tablas** cambia la antigüedad, la concentración y los vencimientos por tablas con los mismos números. La composición se mantiene como barra. Use **Gráficos** para volver a verlos.

![Dashboard como tablas](../recursos/img/cartera-proveedores/19-dashboard-tablas.png)

### Desglose

Algunas partes del dashboard llevan a otra vista:

| Haga clic en | Qué se abre |
|--------------|-------------|
| El nombre de un proveedor del **top** o de **pagos recientes** | Sus documentos, con la misma fecha de corte y los mismos tramos. Use **Volver al dashboard** para regresar. |
| Un tramo de **antigüedad** | La vista **Saldos**, con la misma fecha de corte, tipo de movimiento, centro de costos y tamaño de tramos. La lista va ordenada por saldo vencido (tramos vencidos) o por saldo (tramos por vencer). |
| **Ver proveedores con saldo vencido** | La misma lista, ordenada por saldo vencido. |
| **Vencimientos próximos** | Nada: no abren la lista. |

Cuando llega desde un tramo o desde **Vencido**, la lista muestra un aviso: *la lista aún no filtra por tramo*. Los tramos aparecen como columnas, pero la lista no muestra solo los proveedores de ese tramo.

![Lista abierta desde un tramo de antigüedad](../recursos/img/cartera-proveedores/21-dashboard-tramo-lista.png)

Si no hay cartera por pagar a la fecha de corte, el dashboard muestra **No hay cartera por pagar a esta fecha** con el botón **Ver proveedores en saldo cero**.

### Tiempo de carga

Cada consulta del dashboard tarda cerca de **2 segundos**. Mientras tanto verá el aviso *"Calculando el dashboard…"*. Si tarda más, aparece *"Calculando la cartera a la fecha de corte. Puede tardar unos segundos."* No es necesario recargar la página.

Si la consulta falla, verá *"No se pudo calcular el dashboard"*. Haga clic en **Reintentar**; los filtros se conservan.

### Qué no incluye el dashboard

Por ahora el dashboard **no** muestra:

- La tendencia mensual del saldo.
- El plazo medio de pago.
- La calificación del proveedor. Está aplazada: no aparece ni se simula.
- Los descuentos por pronto pago.

### Permisos del dashboard

El dashboard usa el mismo permiso que el listado: **Consultar** sobre *Cartera Terceros*. No necesita ningún permiso adicional. Sin **Consultar** no verá la pestaña **Cartera** ni sus vistas.

---

## 📄 Documentos de un proveedor

Haga clic en el nombre de un proveedor en el listado. Se abre la página de sus documentos, con el mismo nombre y la misma fecha de corte.

![Documentos del proveedor](../recursos/img/cartera-proveedores/06-documentos.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **Volver a proveedores** | Regresa al listado con los filtros que tenía. |
| **Ver ficha del proveedor** | Abre la ficha del proveedor en la pantalla de Proveedores. |
| **Incluir documentos en saldo cero** | Muestra también los documentos ya saldados. Mientras estén ocultos, la línea de la derecha dice cuántos hay, por ejemplo *1 documento saldado está oculto*. |
| **Buscar documento** (el campo dice *Buscar por movimiento o referencia*) | Filtra por el código del documento o por su documento de referencia. |
| **Movimiento** (código subrayado) | Abre la historia del documento. Ver *Historia del movimiento*. |

Las columnas son: **Movimiento**, **Doc. referencia**, **Fecha**, **Plazo (d)**, **Vence**, **Atraso**, **Valor total**, **Notas**, **Pagos** y **Saldo**.

- El **vencimiento** es la fecha del documento más sus días de plazo.
- El **atraso** es la diferencia entre la fecha de corte y el vencimiento. Un atraso positivo aparece en rojo como *días de atraso*; si todavía no vence, aparece *Vence en* y los días que faltan.
- Un **anticipo** aparece con su saldo a favor y la etiqueta **A favor**. Una **devolución** aparece con valor negativo.

Si eligió un rango de vencimiento en el listado, la página muestra además el **saldo por vencimiento** del proveedor en barras.

![Saldo por tramos de vencimiento](../recursos/img/cartera-proveedores/08-documentos-tramos.png)

### Anticipos y saldo a favor

Un proveedor puede tener un anticipo o una nota sin aplicar. Ese documento aparece con su saldo a favor y reduce el saldo total del proveedor.

![Documento con saldo a favor](../recursos/img/cartera-proveedores/07-saldo-a-favor.png)

---

## 🔎 Historia del movimiento

La historia explica **cómo llegó un documento a su saldo**: desde que se generó, cada pago, nota o cruce que lo afectó, y cuánto queda.

Para abrirla, haga clic en el código del documento (por ejemplo, **FC-1201**) en la página de documentos. Se abre un panel a la derecha.

![Historia de una factura con cruces](../recursos/img/cartera-proveedores/09-historia-cruces.png)

### Cómo leer la historia

La parte de arriba muestra los datos del documento: **Tipo**, **Número**, **Fecha**, **Vence**, **Valor total**, **Doc. referencia**, **Proveedor** y **Observaciones**.

Debajo está la **Línea de tiempo**:

| Línea | Qué significa |
|-------|---------------|
| **Generado** | El valor con el que se creó el documento, en su fecha. Es el punto de partida. |
| **Pagado con** (un egreso) | Un pago que cruzó contra este documento, con la fecha del pago y el valor aplicado. También cuenta como pago un egreso contable que cruzó contra la factura. |
| **Nota aplicada** (una nota débito o crédito) | Una nota que cruzó contra este documento. |
| **Aplicado por** | Otro documento que cruzó contra este, como una devolución (categoría *Otro*); no cambia el saldo. |
| **Aplicado a** | Este documento cruzó contra otros (por ejemplo, un egreso o un anticipo que pagó facturas). Aparece en la historia del documento que aplicó. |
| **Sin aplicar** | El valor que queda sin cruzar en un egreso o un anticipo. |

En cada línea verá:

- **Valor aplicado**: cuánto se cruzó en esa operación.
- **Saldo después**: cuánto queda por pagar del documento después de esa línea.
- **Componentes del cruce**: descuento, IVA, retenciones, seguros y fletes, intereses u otros, cuando la operación los tiene. Solo aparecen los que tienen valor.

La última línea, **Saldo actual**, es el mismo saldo que ve en el listado. Si la fecha de corte es anterior a hoy, la historia solo muestra los cruces hasta esa fecha, igual que la lista.

### Reversos y saldo a favor

Un reverso es un cruce guardado en negativo. El sistema lo cuenta por su valor absoluto, igual que un cruce positivo del mismo monto. Se marca con la etiqueta **Reverso**; si pasa el cursor sobre la etiqueta, la pantalla explica lo mismo en un aviso.

Los documentos con saldo a favor se marcan con la etiqueta **A favor** junto a su saldo.

![Historia con reversos y saldo a favor](../recursos/img/cartera-proveedores/11-historia-reversos.png)

### Egreso con valor sin aplicar

Si abre un **egreso** (un pago) o un **anticipo**, la historia muestra las facturas que ese documento cruzó y cuánto aplicó a cada una. Lo que no se aplicó aparece al final como **Sin aplicar**, con el valor que queda.

![Egreso con valor sin aplicar](../recursos/img/cartera-proveedores/10-historia-sin-aplicar.png)

### Ir a otro documento y volver

En una línea de la historia, haga clic en el nombre del documento cruzado (por ejemplo, **Egreso EG-0412**). La historia cambia a ese documento. Para volver, use el botón **Atrás** del panel o el botón Atrás del navegador.

Use **Cerrar** para salir de la historia.

### Documentos sin cruces

Si el documento todavía no tiene pagos ni notas, la historia muestra solo **Generado** y el mensaje **Sin cruces todavía**.

![Documento sin cruces](../recursos/img/cartera-proveedores/12-historia-sin-cruces.png)

### Qué no aparece en la historia

Los documentos **anulados** no se muestran y no suman al saldo, ni como documento ni como cruce.

---

## 📤 Exportar a Excel

Haga clic en **Exportar a Excel** (necesita el permiso **Exportar**). Se descarga un archivo llamado `CarteraProveedores_` seguido de la fecha de corte, por ejemplo `CarteraProveedores_2026-10-09.xlsx`.

![Exportar a Excel](../recursos/img/cartera-proveedores/15-exportar.png)

- El archivo tiene **todo el filtro**, no solo la página que está viendo.
- Trae el encabezado de la compañía, la fecha de corte, el rango, los filtros usados, la fecha y el usuario que lo generó.
- Una fila por proveedor, con su NIT, nombre, nombre comercial, teléfono, ciudad, zona, dirección, comprador, documentos, valor total, notas, pagos, saldo, vencido, saldo a favor y mayor atraso. Si eligió un rango, también trae los tramos.
- Al final, una fila **TOTAL**.

**Límite:** el archivo puede tener hasta **50.000 proveedores**. Si el filtro trae más, no se genera el archivo y verá el aviso *"Hay demasiadas filas para exportar (máximo 50.000). Acota el filtro e inténtalo de nuevo."* Escriba más texto en el buscador, elija una fecha de corte o un filtro más específico y vuelva a exportar.

Por ahora la exportación es **solo a Excel**. No hay exportación a PDF.

---

## 🔐 Permisos

| Permiso | Qué habilita |
|---------|--------------|
| Consultar (opción *Cartera Terceros*) | Ver la pestaña **Cartera**, el listado, el Dashboard, abrir los documentos de un proveedor y ver la historia de cada documento. |
| Exportar | El botón **Exportar a Excel**. |

Si solo tiene **Consultar**, la pantalla funciona igual, pero no verá el botón **Exportar a Excel**.

![Solo consulta, sin Exportar a Excel](../recursos/img/cartera-proveedores/16-solo-consulta.png)

---

## ⏱️ Tiempos de carga

La cartera se calcula en el momento, a la fecha de corte que eligió. La **primera consulta puede tardar entre 2 y 3 segundos**. Mientras tanto verá el aviso *"Consultando la cartera…"* y, si tarda más, *"Calculando la cartera a la fecha de corte. La primera consulta puede tardar unos segundos."*

No es necesario recargar la página: espere a que aparezca el resultado.

---

## ⚠️ ¿Qué puede salir mal?

| Aviso | Qué significa y qué hacer |
|-------|---------------------------|
| *"No se pudo consultar la cartera"* | Hubo un problema de conexión o del servidor. Revise su conexión y haga clic en **Reintentar**. Sus filtros se conservan. |
| *"La fuente de datos no respondió a tiempo. Inténtelo de nuevo en unos minutos."* | El servidor tardó demasiado. Espere unos minutos y vuelva a consultar. |
| *"La fecha de corte no es válida. Elija una fecha que no sea futura."* | La fecha de corte está en el futuro. Elija hoy o una fecha anterior. |
| *"Un filtro ya no existe en esta compañía. Quite el filtro e inténtelo de nuevo."* | El tipo de movimiento o el centro de costos que eligió ya no existe. Quite el filtro y consulte otra vez. |
| *"El resultado es demasiado grande para consultarlo. Acote el filtro."* | Hay demasiados documentos para la consulta. Elija una fecha de corte o un filtro más específico. |
| *"No se encontró"* | El proveedor o el documento no existe en esta compañía, o ya fue anulado. Vuelva a la lista. |
| *"No se pudieron cargar los documentos"* | Los documentos del proveedor no llegaron. Haga clic en **Reintentar**. |
| *"No se pudo cargar la historia"* | La historia no llegó, pero los documentos siguen disponibles. Haga clic en **Reintentar**. |
| *"Esta historia tiene demasiados cruces para mostrarla."* | El documento tiene demasiados cruces (más de 1.000) y la historia no se puede mostrar. Elija una fecha de corte anterior o consulte el documento con contabilidad. |
| *"No se pudo generar el archivo. Inténtelo de nuevo."* | La exportación falló. Vuelva a intentarlo. |

---

## ❓ Preguntas frecuentes

**¿Por qué un proveedor aparece con saldo a favor?**
Porque tiene anticipos, sobrepagos o notas sin aplicar. Ese valor ya está descontado del saldo del proveedor y se marca con **A favor**.

**¿Por qué cambia el saldo si cambio la fecha de corte?**
La cartera solo cuenta los pagos y las notas con fecha hasta el corte. Con una fecha anterior, los pagos hechos después no se descuentan.

**¿Por qué no aparece un proveedor que sí existe en Proveedores?**
Solo aparecen los proveedores que tienen documentos de cartera (compras, gastos, comprobantes o anticipos) a la fecha de corte. Un proveedor sin documentos no aparece, aunque active el saldo cero. Los documentos anulados no cuentan.

**¿Por qué el vencimiento no coincide con el plazo que tiene hoy el proveedor?**
La cartera usa el **plazo del documento**: la fecha del documento más sus días de plazo. Si después cambió el plazo del proveedor, los documentos anteriores conservan el suyo.

**¿Por qué el total no cambia cuando paso de página?**
Los totales de las tarjetas y el conteo de proveedores son del filtro completo, no de la página.

**¿Por qué no veo un documento saldado?**
Los documentos en saldo cero están ocultos. Active **Incluir documentos en saldo cero** en la página del proveedor.

**¿Por qué un documento tiene una línea marcada como Reverso?**
Es un cruce guardado en negativo. El sistema lo cuenta por su valor absoluto, igual que un cruce positivo del mismo monto. Pase el cursor sobre la etiqueta para leer la explicación. Ver *Reversos y saldo a favor*.

**¿Por qué una factura aparece pagada con un egreso contable?**
Un egreso contable que cruzó contra la factura cuenta como pago de esa factura: resta del saldo y aparece en la historia como **Pagado con**. Si la factura debería seguir pendiente, revise el cruce con contabilidad.

**¿Por qué no veo la pestaña Cartera?**
Su perfil no tiene el permiso **Consultar** sobre la opción *Cartera Terceros*. Consulte con el administrador.

**¿Por qué no veo el botón Exportar a Excel?**
Su perfil no tiene el permiso **Exportar** sobre esta opción. Consulte con el administrador.

**¿Se queda registro de las exportaciones?**
Sí. Se registra cuándo se exportó, con la fecha de corte y los filtros usados. No se registra el contenido del archivo.

---

## 📚 Relacionado

- [Proveedores](proveedores.md) (la cartera es su pestaña **Cartera**)
- [Compradores](compradores.md)
- [Manejo general de la información](../../Generales/manejo-general-informacion.md)
