[Regresar a Ventas](../readme.md)

---

# 🧾 Ventas y devoluciones

![Static Badge](https://img.shields.io/badge/Tipo-Movimiento-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-VentasDevoluciones-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261103-yellow)

---

## 📋 Descripción

Esta pantalla sirve para **vender**, **devolver** y **emitir notas crédito** a los clientes de la compañía. Una sola pantalla maneja los tres casos: lo que determina si el documento es una venta, una devolución o una nota crédito es el **tipo de documento** que elija.

Quién la usa:

- **Facturador o cajero**: captura la venta con el teclado o con el lector de código de barras, la cierra e imprime.
- **Jefe de ventas o de cartera**: filtra el listado, revisa el resumen, reenvía a la DIAN las facturas pendientes o con error y anula lo que corresponda.
- **Contabilidad**: confía en que una factura transmitida a la DIAN no se altera. Lo que se corrige se corrige con una nota crédito o una devolución.

En esta pantalla puede **consultar, crear, editar, cerrar, anular, eliminar, imprimir y exportar** documentos, y **seguir la factura electrónica** de cada venta. Trabaje siempre con la compañía que aparece en la barra superior.

> 📘 La búsqueda, el orden y la paginación de las tablas funcionan igual que en el resto de la aplicación: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> ⚠️ **Una factura transmitida a la DIAN no se edita, no se anula y no se elimina.** Para corregirla, cree una **nota crédito** o una **devolución** (ver [Devoluciones y notas crédito](#devoluciones)).

---

<a id="acceso"></a>
## 🎯 Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Movimientos**, haga clic en **Ventas y devoluciones**.

Si no ve la opción en el menú, su usuario no tiene permiso para consultar esta pantalla. Pida acceso a un administrador de la compañía.

---

<a id="permisos"></a>
## 🔐 Permisos por acción

Los botones que ve dependen de los permisos de su usuario y del estado del documento. La pantalla solo muestra lo que puede hacer; el servidor vuelve a revisar cada acción antes de guardarla.

| Permiso | Qué le permite |
|---------|----------------|
| **Consultar** | Ver el listado, abrir un documento, ver su estado de factura electrónica y ver su pestaña **Recibo de caja** (ver [Ver el recibo de caja de una venta](#recibo-caja)). |
| **Crear** | Crear una venta, una devolución o una nota crédito, y facturar desde un pedido o desde remisiones. |
| **Actualizar** | Capturar y cambiar líneas de un documento abierto, cerrarlo y reenviar a la DIAN una factura pendiente o con error. |
| **Editar documento cerrado** | Cambiar una línea existente de un documento cerrado (ver [Editar un documento cerrado](#editar-cerrado)). |
| **Anular** | Anular un documento que aún puede anularse. |
| **Eliminar** | Eliminar un documento que no tiene documentos dependientes. |
| **Imprimir** | Imprimir y ver la vista previa de un documento. |
| **Administrador de la compañía** | Verificar en el proveedor tecnológico y, si hace falta, restablecer o reenviar una factura que ya está transmitida a la DIAN (ver [Facturación electrónica](#fe)). |

> 💡 Para cerrar una venta con recibo de caja automático también necesita el permiso **Crear** en **Recibos de caja y egresos**. Vea [Cerrar y cobrar](#cerrar-y-cobrar).

> 💡 Si su usuario solo tiene **Consultar**, el listado y los documentos aparecen, pero no verá botones como **Nueva venta**, **Editar**, **Anular** o **Eliminar**.

![Usuario que solo puede consultar](../recursos/img/ventas-devoluciones/09-solo-consulta.png)

![Usuario sin permiso de consulta](../recursos/img/ventas-devoluciones/08-sin-permiso.png)

---

<a id="listado"></a>
## 🖥️ Pantalla principal: el listado

![Listado de ventas y devoluciones](../recursos/img/ventas-devoluciones/00-listado.png)

Si todavía no hay documentos en el rango elegido, la tabla aparece vacía. Cambie las fechas para buscar en otro periodo.

![Listado sin documentos en el rango](../recursos/img/ventas-devoluciones/07-vacio.png)

El listado muestra las ventas, devoluciones y notas crédito de la compañía, con el **Resumen del filtro** arriba:

| Tarjeta | Qué muestra |
|---------|-------------|
| **Ventas netas** | Lo vendido menos las devoluciones del filtro. El texto debajo muestra las ventas brutas y las devoluciones. |
| **Contado y crédito** | Cuánto se vendió de contado y cuánto a crédito. |
| **Factura electrónica** | Cuántas facturas están transmitidas a la DIAN, y cuántas están pendientes, en cola o con error. |
| **Por reenviar a la DIAN** | Facturas pendientes de enviar y con error. |

Si el resumen no se puede calcular, la tabla sigue funcionando y el resumen muestra **Reintentar**.

### Filtros

Los filtros están arriba de la tabla y quedan en la dirección de la página, para que pueda compartir la vista:

- **Desde** y **Hasta**: fechas del documento. Por defecto es el mes en curso.
- **Naturaleza**: *Venta*, *Devolución* o *Nota crédito*.
- **Estado**: *Abierta*, *Cerrada* o *Anulada*.
- **Factura electrónica**: *Pendiente de enviar*, *En cola*, *Transmitida a la DIAN* o *Error al enviar*. Para filtrar por factura electrónica debe indicar **Desde** y **Hasta**, con un rango de no más de 366 días.
- **Cliente**: por documento o nombre.
- **Buscar**: por número, documento de referencia o cliente. Escriba al menos 2 caracteres.

Si el rango de fechas está mal (por ejemplo, **Desde** es posterior a **Hasta**), la pantalla lo marca en rojo y no busca.

![Rango de fechas inválido](../recursos/img/ventas-devoluciones/05-rango-invalido.png)

Para quitar todos los filtros, use **Limpiar filtros**.

![Filtro por factura electrónica con error](../recursos/img/ventas-devoluciones/02-filtro-factura-electronica-con-error.png)

### Columnas

Cada fila muestra el **documento** (por ejemplo, *FV-1205* para una factura o *DV-1204* para una devolución), la **naturaleza**, la **fecha**, el **documento de referencia**, el **cliente**, la **cantidad**, el **valor total**, el **estado** y el **estado de la factura electrónica**. El estado siempre lleva texto además del color.

### Estados del documento

| Estado | Qué significa |
|--------|---------------|
| **Abierta** | Se puede seguir capturando. |
| **Cerrada** | Quedó de solo lectura (ver [Cerrar el documento](#cerrar)). |
| **Anulada** | Se anuló y no afecta inventario, cartera ni contabilidad. Se conserva para consulta. |

![Documento anulado](../recursos/img/ventas-devoluciones/28-anulada.png)

### Estados de la factura electrónica

| Estado | Qué significa |
|--------|---------------|
| **No aplica** | El tipo de documento no es de factura electrónica, o la compañía no tiene proveedor tecnológico configurado. |
| **Pendiente de enviar** | El documento está cerrado, pero la factura todavía no se envió a la DIAN. |
| **En cola** | El envío está en curso, en segundo plano. |
| **Transmitida a la DIAN** | La factura ya se envió. Ya no se puede editar, anular ni eliminar. |
| **Error al enviar** | El último intento falló. Vea el motivo y reenvíe la factura. |

### ¿Qué puedo hacer desde una fila?

Cada fila tiene botones con nombre, por ejemplo **Anular FV-1205**. Aparecen solo si su usuario tiene el permiso y el documento lo permite:

| Botón | Cuándo aparece |
|-------|----------------|
| **Ver** | Siempre que tenga permiso para consultar. |
| **Imprimir** | Con el permiso de imprimir. También para documentos abiertos, como vista previa. |
| **Editar** | Documentos abiertos, con el periodo abierto y sin documentos dependientes. |
| **Reenviar a la DIAN** | Facturas pendientes de enviar o con error. |
| **Crear nota crédito o devolución** | Facturas transmitidas a la DIAN. |
| **Anular** | Documentos que todavía se pueden anular, es decir, que no estén transmitidos ni con el envío en cola. |
| **Eliminar** | Documentos sin documentos dependientes, sin factura transmitida y sin envío en cola. |

Para ver el detalle de un documento, haga clic en su número o en **Ver**.

![Documento transmitido: sin editar, anular ni eliminar](../recursos/img/ventas-devoluciones/23-transmitida-bloqueada.png)

Para exportar el listado a Excel, use **Exportar a Excel**. Se exporta lo que ve con los mismos filtros.

---

<a id="crear"></a>
## ➕ Crear una venta

1. En el listado, haga clic en **Nueva venta**.
2. Elija el **Tipo de documento**. Solo aparecen los tipos que su usuario puede usar. Sin tipo no se pueden capturar líneas.
3. Escriba el **Cliente** por documento y pulse **Enter** o **Tab**, o búsquelo por documento o nombre. Solo puede elegir clientes activos. Si el cliente no existe, créelo primero en el maestro de [Clientes](../maestros/clientes.md).
4. Revise la **Sucursal**. Si el cliente tiene una sola, se elige sola. Si tiene varias, elija la que corresponde.
5. Revise el **Vendedor**. Es obligatorio para capturar líneas, y se precarga desde la sucursal.
6. Revise la **Fecha** y los **Días de plazo**. La fecha es la de hoy de la compañía, según el servidor. **Vence** es la fecha más los días de plazo.
7. Complete lo que necesite: **Documento de referencia** (hasta 20 caracteres) y **Observaciones** (hasta 200 caracteres, sin comas ni punto y coma).
8. Capture las líneas (ver [Captura de líneas](#captura)).

> 💡 El número del documento aparece como *tentativo* hasta que se guarda la primera línea. Si el tipo permite cambiar el consecutivo, puede escribirlo; si lo deja vacío, se usa el siguiente.

![Venta nueva, antes de elegir cliente](../recursos/img/ventas-devoluciones/10-nueva-venta.png)

### Valores por defecto y de dónde vienen

Al elegir el tipo, el cliente y la sucursal, la pantalla llena los valores por defecto: **Días de plazo**, **Vendedor**, **Lista de precios**, **% descuento por defecto** y las retenciones del cliente. **Cada valor muestra su origen** debajo del campo:

| Origen | Qué significa |
|--------|---------------|
| **Compañía** | Valor general de la compañía. Es el que queda cuando todavía no hay cliente. |
| **Tipo de documento** | Valor que trae el tipo que eligió. |
| **Cliente** | Valor que trae la ficha del cliente. |
| **Sucursal** | Valor que trae la sucursal del cliente, como el vendedor o la lista de precios. |
| **Lo escribiste tú** | Valor que usted cambió a mano. |

![Valores por defecto del cliente con su origen](../recursos/img/ventas-devoluciones/11-valores-por-defecto.png)

- **Lo que usted escribe nunca se pisa.** Si cambia de cliente, la pantalla actualiza solo los valores que no escribió usted, y un aviso dice qué cambió y qué se conservó.
- **Restablecer a los del cliente** devuelve todos los valores por defecto a los de su origen.
- **Lista de precios**: de la 1 a la 5, o *Costo*. Es la lista que sugiere el valor de cada línea.
- **Retenciones del cliente**: se muestran con su base y su porcentaje, que son de solo lectura. Si el cliente no realiza retenciones, la pantalla lo dice.

![Cambio de cliente: se conserva lo que usted escribió](../recursos/img/ventas-devoluciones/12-cambio-de-cliente.png)

---

<a id="captura"></a>
## ⌨️ Captura de líneas

![Detalle con modo lector y líneas guardadas](../recursos/img/ventas-devoluciones/14-lector-rapido.png)

En una venta no hay botón *Guardar documento*. **Cada línea se guarda cuando la confirma.** Así, si la red falla, solo se pierde la línea que estaba escribiendo.

La fila de captura tiene estos campos, en este orden (con **Enter** pasa al siguiente; en el último, guarda la línea):

| Campo | Regla |
|-------|-------|
| **Código de barras o referencia** | Lea el código con el lector o escríbalo y pulse Enter. |
| **Cantidad** | Mayor que 0, con hasta 4 decimales. |
| **Valor unitario** | Mayor que 0. Se sugiere con la lista de precios elegida. |
| **% Dto.** | De 0 a 100. Se precarga con el descuento por defecto. |
| **Agregar línea** | Guarda la línea. |

Para guardar una línea necesita elegir la **bodega** (la pantalla dice *Elige la bodega para agregar la línea*). Si el tipo exige **centro de costos**, también debe elegirlo.

El **IVA** sale de la referencia. El **Total** de la línea se calcula solo.

Debajo del valor unitario, la pantalla le ayuda:

- **Valor sugerido (Lista 2): 22.000 (puedes cambiarlo).** Puedes cambiar el valor sin problema.
- **Sin precio en la lista elegida: escriba el valor.** La referencia no tiene precio en esa lista.
- **Existencia en la bodega: n.** Si no hay existencia, la pantalla avisa, pero el servidor es quien decide.

### Atajos de teclado

| Tecla | Qué hace |
|-------|----------|
| **Enter** | Pasa al siguiente campo; en el último, guarda la línea. |
| **Esc** | Limpia la fila de captura. |
| **↑ / ↓** | Elige una línea de la lista. |
| **F2** | Edita la línea elegida. |
| **Supr** | Quita la línea elegida. |
| **Ctrl+D** | Copia la línea elegida a la fila de captura. |
| **Alt+N** | Va a la fila de captura. |
| **Alt+R** | Reintenta las líneas que no se guardaron. |

### Estados de cada línea

Cada línea muestra su estado con texto e ícono:

| Estado | Qué significa | Qué puede hacer |
|--------|---------------|-----------------|
| **En cola** | Se va a guardar. | Espere. |
| **Guardando…** | Se está guardando. | Espere. |
| **Guardada** | Quedó guardada. | Editarla o quitarla. |
| **Guardada · Se sumó a la línea N** | Una lectura o una línea igual a otra que ya estaba se sumó a esa línea. | Nada, salvo revisar la cantidad. |
| **Error** | El servidor no la aceptó y dice por qué. | **Corregir** o **Descartar**. |
| **No se guardó** | Se perdió la conexión. | **Reintentar**, **Descartar** o **Reintentar todas**. |

![Líneas que no se guardaron](../recursos/img/ventas-devoluciones/18-cola-con-errores.png)

Mientras haya líneas por guardar, la pantalla dice **N líneas por guardar**. **Cerrar documento** no se puede usar hasta que todas estén guardadas o descartadas.

### Lector de código de barras

Con el lector, lea el código del producto y la línea se agrega sola:

1. Active **Modo lector de código de barras**. La pantalla avisa: *Modo lector activo: lee un código para agregar la línea*.
2. Elija la bodega (y el centro de costos, si el tipo lo exige).
3. Lea el código. La lectura válida agrega la línea con cantidad 1, y el cursor vuelve al campo de código para la siguiente lectura.
4. Si lee el mismo producto otra vez, la pantalla **suma 1** a la línea que ya existe y dice *Se sumó a la línea N*.
5. El contador **Lecturas** y **Líneas** le muestra cuántas lecturas hizo y cuántas líneas hay.

Si el código no existe, la pantalla muestra **Código no encontrado** y deja el foco en el campo para que lo corrija.

![Código no encontrado](../recursos/img/ventas-devoluciones/15-codigo-no-encontrado.png)

Si el código corresponde a **varias variantes** (por ejemplo, talla o color), la pantalla muestra todas para que elija la que leyó.

### Qué puede salir mal al capturar

| Mensaje | Qué hacer |
|---------|-----------|
| **No hay existencia suficiente en la bodega.** | Corrija la cantidad o descarte la línea. |
| **Elige la bodega para agregar la línea.** | Elija la bodega del documento. |
| **Cantidad mayor que 0 y hasta 4 decimales.** | Corrija la cantidad. |
| **El documento admite N líneas como máximo.** | El tipo tiene un límite de líneas. Use otro documento. |
| **Otra persona modificó esta línea.** | Use la **versión actual** o descarte su cambio. |

---

<a id="totales"></a>
## 🧮 Totales y retenciones

En la parte de abajo del documento están los **totales**: Cantidad, Bruto, Descuento, Subtotal, IVA, ReteFuente, ReteIVA, ReteICA y Total.

- Los totales se calculan con una sola fórmula, así que la pantalla, la impresión y la factura electrónica dan el mismo valor.
- **ReteIVA se calcula sobre el IVA.** La pantalla lo dice en el rótulo.
- Las retenciones se aplican solo cuando el subtotal llega a la **base** de cada impuesto.
- Los totales **no incluyen las líneas que todavía no se guardaron**, y la pantalla lo dice.

Los campos **Seguro y flete** y **Otros valores** se suman al total. En un tipo de **factura electrónica** no existen: no se pueden usar, quedan en 0 y la pantalla lo avisa con *Este tipo es de facturación electrónica: fletes y otros valores no se permiten y se pusieron en 0.*

---

<a id="cliente"></a>
## 👤 Cliente, cupo, mora y cartera

### Cupo y mora

Cuando un cliente de crédito supera su cupo o tiene vencidos, la pantalla muestra el aviso **Cupo de crédito y mora** con el cupo, la cartera y lo disponible:

![Aviso de cupo excedido](../recursos/img/ventas-devoluciones/13-cupo-excedido.png)

- Si el indicador de la compañía **bloquea por cupo** o **por mora**, el cierre no se puede hacer y el servidor lo dice.
- Si el indicador está apagado, el aviso es solo una advertencia, y el documento se puede guardar.

> 💡 **Cliente de contado.** Un cliente de contado no tiene cupo ni mora, así que la pantalla no los revisa. Tampoco revisa la cartera de las ventas de contado.

### Cartera del documento

En el documento, la pestaña **Cartera** muestra el total del documento, su saldo, la fecha de vencimiento y los recibos aplicados. Si la venta es de contado, la pestaña dice:

> **No aplica: venta de contado**

Esto solo cambia lo que la pantalla muestra y revisa en la venta. El documento sigue registrado en la cartera de la compañía y en los informes de cartera, como antes.

---

<a id="pedido"></a>
## 📦 Facturar desde un pedido

Use esta opción para facturar lo que el cliente ya pidió.

1. En el documento, haga clic en **Facturar desde pedido**.
2. Busque el **Pedido** en *Busca un pedido con saldo*. Solo aparecen pedidos de la misma sucursal del documento, con saldo.
3. Revise las líneas del pedido. Cada una muestra su **Saldo**.
4. Marque las líneas que quiere facturar y ajuste la **Cantidad** (no puede superar el saldo), el **Lote** y el **Detalle**, si lo necesita.
5. Haga clic en **Agregar líneas**.

Las líneas se guardan **todas o ninguna**. Si una de ellas no se puede guardar, la pantalla dice cuál fue y no guarda nada. Cada línea queda ligada a su pedido, y el saldo del pedido baja en la cantidad facturada.

Si el pedido ya no está disponible (es de otra sucursal, está anulado o no tiene saldo), la pantalla lo dice y no lo deja elegir.

---

<a id="remisiones"></a>
## 🚚 Facturar desde remisiones

Use esta opción para facturar una o varias remisiones en un solo documento.

1. Complete el **Tipo de documento**, la **Fecha**, el **Cliente** y la **Sucursal**. Sin ellos, el botón **Seleccionar remisiones** no se activa, y la pantalla dice *Completa tipo, fecha, cliente y sucursal para seleccionar remisiones.*
2. Haga clic en **Seleccionar remisiones**.
3. Busque por consecutivo o por documento de referencia, y marque las remisiones que quiere facturar.
4. Haga clic en **Agregar remisiones**.

Reglas:

- Se factura **cada remisión completa**. No hay facturación parcial de una remisión.
- Se pueden elegir **hasta 50 remisiones** por operación. La pantalla cuenta las que marca.
- Todas las líneas se guardan **todas o ninguna**. Si una remisión ya está facturada, anulada o es de otra sucursal, no se guarda nada.
- Cada línea muestra la remisión de la que viene.

Si el documento todavía no existe, la operación lo crea con su consecutivo y agrega las líneas de todas las remisiones.

---

<a id="cerrar"></a>
## 🔒 Cerrar el documento

![Documento cerrado, con la factura en cola](../recursos/img/ventas-devoluciones/20-cerrado-en-cola.png)

1. Revise el documento y, cuando esté listo, haga clic en **Cerrar documento**.
2. En el diálogo, revise el total: *Vas a cerrar FV-1205 por el total. Quedará de solo lectura.*
3. Confirme con **Cerrar documento**.

El botón **Cerrar documento** solo se activa con al menos una línea y sin líneas pendientes por guardar.

Al cerrar, el servidor revisa:

- que la fecha esté en un **periodo abierto** (si no, dice *La fecha pertenece a un periodo cerrado. Elige otra fecha.*);
- que la **resolución DIAN** del tipo esté vigente y que el consecutivo esté dentro de su rango (si no, dice *La resolución DIAN aún no está vigente* o *está vencida*);
- el **cupo** y la **mora**, según el indicador de la compañía.

Si todo está bien, el documento queda **cerrado** y de solo lectura. Si el tipo es de **factura electrónica**, la pantalla muestra el aviso *Documento FV-1205 cerrado. La factura electrónica se envía en segundo plano.* y el estado pasa a **En cola**.

> 💡 **Cerrar no espera a la DIAN.** Si el proveedor tecnológico no está disponible, el documento se cierra igual. La factura se envía en segundo plano, y cuando termina le avisamos a quien cerró el documento. Si no se envió, puede reenviarla (ver [Facturación electrónica](#fe)).

<a id="cerrar-y-cobrar"></a>
### Cerrar y cobrar: venta con recibo de caja automático

Algunos tipos de venta generan su **recibo de caja** al cerrarse. Si el tipo de su documento lo hace, **Cerrar documento** no cierra la venta de inmediato: abre el diálogo **Cerrar y cobrar**. Los demás tipos de venta se cierran como se explicó arriba, sin diálogo.

![Diálogo Cerrar y cobrar con las formas de pago](../recursos/img/ventas-devoluciones/40-cerrar-y-cobrar.png)

**Qué pasa al cerrar**

Al confirmar, la pantalla cierra la venta y crea el recibo de caja en un solo paso:

- El documento queda **cerrado** y de solo lectura.
- Se crea un **recibo de caja** por el total de la venta, con la forma de pago que eligió. Si escribió el **valor recibido**, también se guarda con el recibo.
- Los asientos contables del recibo quedan registrados, y el cierre queda en la bitácora de la venta y del recibo.
- Si la venta es factura electrónica, la factura se envía en segundo plano, como siempre. Si ese envío falla, el recibo no se revierte.

Si algo falla antes de terminar, **no queda nada a medias**: la venta sigue abierta, no se crea recibo y el diálogo muestra el error para que pueda reintentar. Si cancela o pulsa **Escape**, no pasa nada.

**Elegir la forma de pago**

1. Revise el **Documento** y el **Total a cobrar**. El total es el de la venta y no se cambia en este diálogo.
2. Toque la tarjeta de la forma de pago: **Efectivo**, **Banco**, **Tarjeta de crédito** u otra. Cada una muestra su icono o, si la compañía la tiene, su imagen.
3. Confirme con **Cerrar y generar recibo**.

![Forma de pago que llega marcada desde su cajero](../recursos/img/ventas-devoluciones/41-forma-del-cajero.png)

Si su usuario tiene una forma de pago por defecto (la de su cajero), la pantalla la marca al abrir el diálogo. Si no tiene ninguna, la pantalla dice *Elija una forma de pago para continuar.* y **Cerrar y generar recibo** queda deshabilitado hasta que elija una.

El recibo cubre el total de la venta con **una sola forma de pago**.

**Banco y documento de referencia**

Algunas formas de pago piden datos extra. Si la forma seleccionada los pide, aparecen dos campos **opcionales**:

- **Banco**: busque y elija el banco. Si no aplica, déjelo vacío.
- **Documento de referencia**: por ejemplo, el número de la transacción. Máximo 20 caracteres, sin comas ni punto y coma.

![Banco y documento de referencia](../recursos/img/ventas-devoluciones/42-banco-y-documento.png)

Si cambia a una forma que no los pide, los campos desaparecen y sus valores se descartan.

![Documento de referencia con caracteres no permitidos](../recursos/img/ventas-devoluciones/43-documento-invalido.png)

**Valor recibido y cambio (solo formas sin banco ni documento)**

Con las formas de pago que no piden banco ni documento de referencia (por ejemplo, **Efectivo**), el diálogo muestra el campo **Valor recibido**. Sirve para ver cuánto debe devolver al cliente.

1. Escriba el valor que le entregó el cliente.
2. Si el valor es igual o mayor al total, aparece la banda verde **Cambio: $X**. Es lo que debe devolver.
3. Si el valor es menor al total, aparece **Faltan $X** en rojo y **Cerrar y generar recibo** queda deshabilitado. Corrija el valor, pulse **Exacto** o deje el campo vacío.

![Valor recibido con cambio](../recursos/img/ventas-devoluciones/49-valor-recibido-cambio.png)

![Valor recibido insuficiente: faltan dinero](../recursos/img/ventas-devoluciones/50-valor-recibido-faltan.png)

- **Exacto** escribe el total en el campo. El cambio queda en $0.
- Si deja el campo **vacío**, el cobro es exacto: no hay cambio y no bloquea el cierre.
- Si escribe algo que no es un número, la pantalla dice *Escriba un valor numérico válido.* y tampoco deja cerrar.
- Si cambia la forma de pago, el valor recibido se borra.
- El **valor recibido se guarda** con el recibo y se imprime en el bloque **Pago** (ver [El bloque Pago](#bloque-pago)). El **cambio** no se guarda como dato: es el valor recibido menos el total.
- El recibo siempre es por el total de la venta. El valor recibido no cambia el total.

**Sin formas de pago**

![Sin formas de pago vigentes](../recursos/img/ventas-devoluciones/44-sin-formas-de-pago.png)

Si la compañía no tiene formas de pago vigentes, la pantalla dice *No hay formas de pago vigentes.* y no se puede cerrar con recibo. Pida al administrador que cree una forma de pago.

**Sin permiso para generar el recibo**

Para cerrar con recibo necesita el permiso **Crear** en **Recibos de caja y egresos**, además de **Actualizar** en esta opción. Si no lo tiene, el diálogo se abre con el aviso *No tiene permiso para generar el recibo de caja.* y sin formas de pago. Puede:

- **Cancelar**: el documento sigue abierto y no cambia nada.
- **Cerrar sin recibo**: el documento se cierra, pero **sin recibo de caja**. La pantalla muestra *Documento cerrado sin recibo de caja: no tiene permiso para generarlo.* Use esta opción con cuidado: la venta de contado quedará sin su recibo.

![Diálogo sin permiso para generar el recibo](../recursos/img/ventas-devoluciones/46-sin-permiso.png)

**Errores al cerrar**

| Mensaje | Qué hacer |
|---------|-----------|
| **No pudimos cargar las formas de pago.** | Pulse **Reintentar**. La venta no cambia. |
| **No se pudo generar el recibo. La venta sigue abierta; puede reintentar.** | Pulse **Reintentar**. Su selección se conserva. |
| **Máximo 20 caracteres, sin comas ni punto y coma.** | Corrija el **Documento de referencia**. |
| **Faltan $X** | El valor recibido es menor al total. Corrija el valor, pulse **Exacto** o deje el campo vacío. |
| **Escriba un valor numérico válido.** | Corrija el **Valor recibido**. |
| **La venta cambió mientras cobraba; recargue para ver los cambios.** | Pulse **Recargar**, revise el documento y vuelva a cerrar. |
| **El tipo de este documento tiene mal configurado su recibo de caja; avise al administrador.** | El administrador debe corregir el tipo. Mientras tanto, la venta no se cierra. |
| **El periodo contable de recibos de caja está cerrado para la fecha del documento.** | Elija otra fecha del documento. |

![Error al cargar las formas de pago](../recursos/img/ventas-devoluciones/45-error-al-cargar.png)

![Error al generar el recibo, con Reintentar](../recursos/img/ventas-devoluciones/47-error-al-guardar.png)

**Cómo se ve en el teléfono**

En pantallas pequeñas las tarjetas se muestran en dos columnas. Si no ve todas, desplácese dentro del diálogo.

![Diálogo en teléfono](../recursos/img/ventas-devoluciones/48-movil.png)

> 💡 Si pulsa dos veces **Cerrar y generar recibo**, se crea un solo recibo.

---

<a id="editar-cerrado"></a>
## ✏️ Editar un documento cerrado

Un documento cerrado se puede corregir en una cosa: **el valor o la cantidad de una línea que ya existe**. Para hacerlo, su usuario necesita el permiso de editar documentos cerrados.

- No puede **agregar** ni **quitar** líneas, ni cambiar el encabezado. La pantalla lo dice: *Documento cerrado: solo puedes editar una línea existente.*
- Al guardar, la contabilidad del documento se recalcula, y el cambio queda en la bitácora.
- No se puede editar un documento **anulado**, uno **transmitido a la DIAN**, uno con **periodo cerrado** ni uno con **documentos dependientes** (recibos o pagos sin anular, notas crédito o devoluciones que lo referencian).

### Venta con recibo de caja automático

Si la venta generó un recibo de caja automático, **no se puede modificar nada** de ella: ni el total, el cliente, la fecha, el vendedor, las observaciones ni las líneas. La pantalla muestra el número del recibo. Para corregir, anule la venta (si el recibo lo permite) y vuelva a crearla.

### Si alguien más cambió el documento

Dos personas pueden tener el mismo documento abierto. Si otra persona lo cambia mientras usted lo edita, la pantalla le avisa:

- **Otra persona modificó este documento mientras lo editabas.** Use **Ver los cambios** o **Recargar** para ver la versión actual. Lo que escribió se muestra para que lo copie si lo necesita.
- **Otra persona modificó esta línea.** Use **Usar la versión actual** o **Descartar** su cambio.
- **Otra persona eliminó este documento.** Ya no se puede seguir editando.

---

<a id="anular"></a>
## 🚫 Anular, eliminar o crear una nota crédito

Estas tres acciones tienen efectos distintos. Elija según el caso:

| Acción | Cuándo se usa | Qué pasa |
|--------|---------------|----------|
| **Anular** | El documento se emitió por error y todavía no fue transmitido a la DIAN ni tiene el envío en cola. | El documento queda **anulado**, con su motivo, su usuario y la fecha. Deja de afectar inventario, cartera y contabilidad. Se conserva para consulta. |
| **Eliminar** | El documento no debe existir y no tiene documentos dependientes. | Se borra de forma definitiva, con sus líneas, sus registros contables y sus adjuntos. **No se puede deshacer.** |
| **Crear nota crédito o devolución** | La factura ya fue transmitida a la DIAN. | Se crea un documento nuevo que corrige o devuelve la venta. La factura original no cambia. |

### Anular

> ⚠️ **Factura electrónica en cola.** Mientras la factura está **en cola**, no se puede anular ni eliminar: la pantalla oculta esos botones y muestra *El envío de la factura electrónica está en curso; espere a que termine o falle para anular.* Cuando el envío termina o falla, los botones reaparecen según el estado del documento.

1. Haga clic en **Anular** (en el documento o en la fila).
2. Escriba el **Motivo de la anulación** (de 1 a 200 caracteres, sin comas ni punto y coma).
3. Haga clic en **Anular documento**.

![Anular con motivo](../recursos/img/ventas-devoluciones/21-anular-con-motivo.png)

Antes de anular, la pantalla revisa si el documento puede anularse. Si no puede, dice por qué. Por ejemplo, con recibos de caja o pagos sin anular, con notas crédito o devoluciones que lo referencian, o con la fecha en un periodo cerrado.

**Venta con recibo de caja automático.** Al anular la venta, también se anula su recibo de caja automático, en el mismo paso. Esto solo se permite si el recibo es **anulable**: tiene un solo pago y una sola línea, no se modificó después de crearse, no tiene otros documentos y el periodo de recibos de caja sigue abierto. Si no lo es, la pantalla dice el número del recibo y el motivo, y no cambia nada. Los recibos de caja que se crearon a mano siguen bloqueando la anulación, como antes.

### Eliminar

1. Haga clic en **Eliminar**.
2. El diálogo dice cuántas líneas, registros contables y adjuntos se borrarán.
3. Escriba el número del documento para confirmar. El botón **Eliminar documento** solo se activa si el número coincide.

![Eliminar con confirmación](../recursos/img/ventas-devoluciones/22-eliminar.png)

Si el documento ya tiene movimiento contable, la pantalla le recomienda **anularlo** en lugar de eliminarlo.

Si la venta tiene un recibo de caja automático, primero **anule** la venta: la eliminación no se permite hasta entonces.

> ⚠️ **Factura electrónica en cola.** Mientras la factura está **en cola**, no se puede anular ni eliminar: la pantalla oculta esos botones y muestra *El envío de la factura electrónica está en curso; espere a que termine o falle para eliminar.* Cuando el envío termina o falla, los botones reaparecen según el estado del documento.

### Crear nota crédito o devolución

Cuando la factura ya fue transmitida, no se anula ni se edita. Haga clic en **Crear nota crédito o devolución** y elija lo que corresponde (ver [Devoluciones y notas crédito](#devoluciones)).

---

<a id="devoluciones"></a>
## ↩️ Devoluciones y notas crédito

![Crear nota crédito o devolución](../recursos/img/ventas-devoluciones/24-nota-credito.png)

### Devolución

Una **devolución** es cuando el cliente regresa mercancía. Se crea un documento de devolución ligado a la venta original, que **queda abierto** para que lo complete y lo cierre.

![Devolución, con su número DV](../recursos/img/ventas-devoluciones/29-devolucion.png)

1. Haga clic en **Crear nota crédito o devolución** y elija **Devolver**.
2. Elija el **Tipo de devolución**, la **Fecha** y, si lo necesita, el **Documento de referencia** y las **Observaciones**.
3. En **Líneas a devolver**, elija **Devolver todo lo pendiente** o **Elegir líneas y cantidades**.
4. Para cada línea, revise lo **Vendido**, lo **Ya devuelto** y lo **Pendiente**, y escriba la **Cantidad** que devuelve (mayor que 0, hasta 4 decimales).
5. Haga clic en **Crear devolución**.

Reglas:

- La cantidad no puede superar lo pendiente. En una devolución **no electrónica** la pantalla solo avisa. En una **nota crédito electrónica** el servidor la rechaza.
- Si el precio es distinto del de la venta, la pantalla lo marca con *El precio difiere del de la venta.*

### Nota crédito electrónica

Una **nota crédito** corrige una factura electrónica ya transmitida a la DIAN.

> 💡 Por ahora la nota crédito se crea desde una factura transmitida. Crear una nota crédito desde cero llegará después.

1. Haga clic en **Crear nota crédito o devolución** y elija **Crear nota crédito**.
2. Elija el **Motivo (DIAN)**. Es obligatorio. Los motivos son:
   - Devolución parcial de los bienes
   - Anulación de factura electrónica
   - Rebaja o descuento parcial
   - Ajuste de precio
   - Descuento por pronto pago
   - Descuento por volumen
3. Haga clic en **Crear nota crédito**.

La nota crédito toma el cliente, la sucursal, el vendedor y las líneas de la factura de origen. La **Factura de origen** queda registrada en la nota.

---

<a id="fe"></a>
## 🧾 Facturación electrónica

La factura electrónica se envía a la DIAN a través del **proveedor tecnológico** de la compañía. Cuando el tipo de documento es de factura electrónica y la compañía tiene su proveedor configurado, **al cerrar el documento el envío queda en cola**. El envío se hace **en segundo plano**: ni cerrar, ni imprimir, ni consultar esperan a la DIAN.

### Seguir el estado

En el documento, el bloque **Factura electrónica** muestra:

- el **Estado** (ver la tabla de [estados de la factura electrónica](#listado));
- los **Intentos** y la fecha del **Último intento**;
- el **Motivo**, cuando el envío falló;
- el **CUFE** (código único de la factura), cuando ya está transmitida.

![Factura con error al enviar](../recursos/img/ventas-devoluciones/26-error-reenviar.png)

### Reenviar a la DIAN

Use **Reenviar a la DIAN** cuando la factura esté **pendiente de enviar** o **con error**. El diálogo le dice que el envío se hace en segundo plano y que le avisará cuando responda.

Si la factura ya está **transmitida a la DIAN**, solo un **administrador de la compañía** puede verificarla en el proveedor y reenviarla (ver [Verificar en el proveedor](#fe)).

Si el sistema reenvía muchas veces seguidas, la pantalla le pide esperar unos segundos.

### Verificar en el proveedor

**Verificar en el proveedor** consulta si la factura ya existe en el proveedor tecnológico. El resultado puede ser:

| Resultado | Qué hacer |
|-----------|-----------|
| **Existe** | La factura ya está en el proveedor. No hace falta reenviarla. |
| **No existe** | Un administrador de la compañía puede reenviarla o restablecerla. |
| **No se pudo comprobar** | Espere un momento y vuelva a verificar. No se puede reenviar por ahora. |

### Factura transmitida: solo lectura

Una factura **transmitida a la DIAN** es de solo lectura. La pantalla lo muestra con el aviso **Documento enviado a la DIAN: no se puede modificar. Para corregirlo cree una nota crédito o una devolución.**

![Factura transmitida, solo lectura](../recursos/img/ventas-devoluciones/23-transmitida-bloqueada.png)

Sobre una factura transmitida puede:

- ver el documento,
- imprimirla,
- crear una nota crédito o una devolución,
- y, si es administrador de la compañía, verificarla en el proveedor y reenviarla o restablecerla, si ya no existe allá.

No puede editarla, cambiar su encabezado, quitar o agregar líneas, anularla ni eliminarla.

### Restablecer (solo administrador)

**Restablecer facturación electrónica** limpia el identificador y el estado de la factura, y la deja **pendiente de enviar**. Solo lo puede hacer un **administrador de la compañía**, y solo si la factura no existe en el proveedor.

> ⚠️ **Riesgo fiscal.** Si la factura **sí** fue aceptada por la DIAN, restablecerla puede producir una **doble emisión**. Hágalo solo si el documento no existe realmente ante la DIAN. Verifique antes en el proveedor.

Para restablecer:

1. Verifique primero en el proveedor. Si la factura **existe**, la pantalla muestra una advertencia.
2. Escriba el **motivo** (de 1 a 200 caracteres, sin comas ni punto y coma).
3. Escriba el número del documento para confirmar.
4. Confirme con **Restablecer**.

Después, la factura queda pendiente y se puede reenviar normalmente.

### CUFE y PDF oficial

- **Ver CUFE** muestra el código de la factura, que puede copiar con **Copiar CUFE**. Si el proveedor no responde a tiempo, la pantalla dice **CUFE no disponible por ahora** y puede reintentar.
- El **PDF oficial de la factura electrónica** solo existe cuando la factura está transmitida. Mientras no lo esté, la pantalla dice *La factura aún no se ha emitido* y le ofrece usar un formato local (ver [Imprimir](#imprimir)).

---

<a id="recibo-caja"></a>
## 💵 Ver el recibo de caja de una venta

Una venta con recibo de caja automático tiene su recibo a la vista, sin salir del documento.

1. En el listado, pulse **Ver** en la fila de la venta (o su número).
2. Pulse la pestaña **Recibo de caja**. Está después de **Contabilidad**.

- La pestaña aparece solo cuando el documento está **cerrado** o **anulado**. Un documento abierto todavía no tiene recibo.
- Es solo de consulta: no tiene botones para cambiar, anular ni imprimir el recibo.
- Necesita el permiso **Consultar** de esta opción.
- Si el recibo cambia (por ejemplo, se anula), la pestaña se actualiza sola.

Lo que ve:

- El **número** del recibo, su **tipo**, la **fecha**, el **estado** (**Vigente** o **Anulado**) y el **valor total**.
- La tabla de pagos: **forma de pago**, **banco**, **documento de referencia** y **valor**.
- **Valor recibido** y **Cambio**, solo si se registraron al cobrar. El cambio sale destacado.

![Recibo de caja vigente con valor recibido y cambio](../recursos/img/ventas-devoluciones/51-pestana-con-recibido.png)

Si la venta no tiene recibo, la pestaña dice *Esta venta no tiene recibo de caja automático.*

![Venta sin recibo de caja automático](../recursos/img/ventas-devoluciones/52-pestana-sin-recibo.png)

Si la pestaña no pudo cargar el recibo, muestra el aviso y el botón **Reintentar**.

![Error al cargar el recibo de caja](../recursos/img/ventas-devoluciones/53-pestana-error.png)

---

<a id="imprimir"></a>
## 🖨️ Imprimir

Haga clic en **Imprimir** en el documento o en la fila del listado.

![Imprimir con formato carta estándar](../recursos/img/ventas-devoluciones/31-carta-estandar.png)

### Formatos

| Formato | Para qué |
|---------|----------|
| **Carta estándar** | Factura o documento completo en hoja carta. |
| **Carta compacta** | Hoja carta con menos espacio. |
| **Tirilla con logo · 80 mm** | Tirilla de 80 mm con el logo de la compañía. |
| **Tirilla de texto · 80 mm** | Tirilla de 80 mm, solo texto. |
| **PDF oficial de la factura electrónica · Carta** | El PDF que entrega el proveedor tecnológico. Solo con la factura transmitida. |

La pantalla **sugiere** un formato según el tipo de documento, y dice cuál es. Puede elegir otro. Si el tipo no tiene un formato propio, la pantalla sugiere **Carta estándar**.

Según el formato, aparecen opciones:

- **Rótulo de sucursal**: el texto que sale como sucursal. Por defecto es *Sucursal*.
- **Mostrar CUFE**: incluye el CUFE en la impresión.
- **Mostrar fecha y hora de creación**: incluye cuándo se creó el documento.
- **Imprimir en Color** o **Blanco y negro**.

![Carta compacta](../recursos/img/ventas-devoluciones/32-carta-compacta.png)

![Tirilla con logo de 80 mm](../recursos/img/ventas-devoluciones/33-tirilla-con-logo.png)

![Tirilla de texto con opciones](../recursos/img/ventas-devoluciones/34-tirilla-de-texto.png)

Para ver el resultado sin imprimir, use la **Vista previa (PDF)**. Para guardar el archivo, use **Descargar PDF**. Para imprimir, use **Imprimir**.

<a id="bloque-pago"></a>
### El bloque Pago

Si la venta tiene recibo de caja, la impresión incluye el bloque **Pago**, después de los totales, con:

- **Forma de pago** de cada pago.
- **Banco** y **Documento**, solo si la forma de pago los tiene.
- **Valor pagado**.
- **Recibido** y **Cambio**, solo si al cobrar se registró el valor recibido y cubre el valor pagado.

El bloque sale en las impresiones en carta y en las tirillas. Si la venta no tiene recibo, no sale. Al reimprimir, sale igual.

### Original y copia

La primera impresión sale como **Original**. Las siguientes salen como **Copia**.

![Impresión como copia](../recursos/img/ventas-devoluciones/35-copia.png)

Cada impresión queda registrada con su número, su usuario y la fecha, y la pantalla lo confirma: *Impresión registrada: n.º N (tipo).*

### Documento abierto

Un documento **abierto** solo tiene **vista previa**. La vista sale marcada como **Sin cerrar** y no cuenta como impresión.

![Vista previa de un documento sin cerrar](../recursos/img/ventas-devoluciones/36-vista-previa-sin-cerrar.png)

### La factura electrónica y la impresión

**La impresión nunca se frena por la factura electrónica.**

- Si el CUFE no llega en unos 3 segundos, se imprime igual y la pantalla dice **CUFE no disponible por ahora**.
- Si la factura todavía no está transmitida, la impresión sale con un formato local y el aviso **Factura electrónica no disponible: está en proceso de envío.** Si el envío falló, el aviso dice **Factura electrónica sin enviar: se reintentará o puede reenviarse.**
- El **PDF oficial** solo sale con la factura transmitida. Si no, la pantalla dice *Factura electrónica no disponible: está en proceso de envío.*

![PDF oficial sin emitir](../recursos/img/ventas-devoluciones/38-pdf-oficial-sin-emitir.png)

![PDF oficial de la factura](../recursos/img/ventas-devoluciones/37-pdf-oficial.png)

> 💡 Si el navegador bloquea la ventana de la vista previa, la pantalla lo dice: *Permite las ventanas emergentes e intenta de nuevo.*

---

<a id="adjuntos"></a>
## 📎 Adjuntos

El bloque **Adjuntos** guarda archivos de soporte del documento (PDF, imágenes, Word o Excel). Cada documento tiene un cupo de **10 MB** en total; la pantalla muestra cuánto lleva usado (*n de 10 MB usados*).

### Agregar y quitar

Solo puede **agregar** y **quitar** adjuntos mientras el documento está **abierto**.

1. En la pestaña **Adjuntos** del documento, o en el bloque **Adjuntos** de la captura, elija el archivo.
2. Escriba la **Descripción** (obligatoria, hasta 200 caracteres).
3. Haga clic en **Agregar a la lista** (en la captura) o en **Adjuntar** (en la pestaña).

En la captura, los archivos quedan en la lista **Se subirán al guardar el documento** y se suben al guardar. Lo mismo pasa si el documento se crea con **Seleccionar remisiones**. Mientras espera, el archivo aparece como *Pendiente de subir*.

Para quitar un adjunto, haga clic en **Quitar** junto al archivo. La pantalla pide confirmación: *Vas a quitar «nombre» del documento. No se puede deshacer.* Confirme con **Quitar adjunto**.

Para **ver** o **descargar** un adjunto, use **Ver** junto al archivo. Esto se puede hacer en cualquier estado del documento.

### Solo lectura

Los adjuntos quedan en solo lectura, aunque pueda verlos, cuando el documento está:

- **cerrado**: *Documento cerrado: los adjuntos se pueden ver, pero no agregar ni quitar.*
- **anulado**: *Documento anulado: los adjuntos se pueden ver, pero no agregar ni quitar.*
- **enviado a la DIAN**: *Documento enviado a la DIAN: no se puede modificar. Los adjuntos solo se pueden ver.*

Si su usuario no tiene permiso para cambiar los adjuntos, la pantalla lo dice: *No tienes permiso para cambiar los adjuntos de este documento.*

### Si una subida falla

Si un adjunto no se sube, **el documento no se deshace**: queda guardado. La pantalla avisa *El documento se guardó, pero N adjuntos no se pudieron subir* y ofrece **Reintentar** para cada archivo, o **Descartar** si ya no lo necesita. También puede reintentarlos desde la pestaña **Adjuntos**.

Un archivo que supera el cupo, de un tipo no permitido o con una descripción no válida no se sube, y la pantalla le dice por qué.

### Al eliminar el documento

Si elimina el documento, también se borran sus adjuntos. El diálogo de eliminar le dice cuántos adjuntos se borrarán (ver [Eliminar](#anular)).

<!-- CAPTURA PENDIENTE: adjuntos -->

---

<a id="proximamente"></a>
## 🔜 Próximamente

- **Documentos abiertos y varios documentos a la vez**: un menú de documentos abiertos y pestañas para trabajar varias ventas al tiempo. **Todavía no está aprobado.** No lo tome como referencia para trabajar hoy.

Mientras tanto, para retomar un documento abierto, búsquelo en el listado con el filtro **Estado** en *Abierta* y ábralo.

---

<a id="en-vivo"></a>
## 🔄 Cambios de otros usuarios (en vivo)

La pantalla se actualiza sola cuando otra persona de la compañía crea, cambia o elimina documentos. Lo ve con el indicador **En vivo**, debajo del título.

Si usted está editando un documento que otra persona cambió, la pantalla se lo dice (ver [Si alguien más cambió el documento](#editar-cerrado)).

---

<a id="faq"></a>
## ❓ Preguntas frecuentes

**¿Por qué al cerrar aparece «Cerrar y cobrar» y no se cierra directo?**
Ese tipo de venta genera un recibo de caja automático al cerrarse. Elija la forma de pago y confirme con **Cerrar y generar recibo**. Los demás tipos de venta se cierran directo, como antes.

**¿Puedo cambiar el total desde el diálogo Cerrar y cobrar?**
No. El diálogo muestra el total de la venta. Si el total no es el que espera, cancele, revise las líneas del documento y vuelva a cerrar.

**¿Se guarda el valor recibido?**
Sí, con el recibo. Sale en el bloque **Pago** de la impresión y en la pestaña **Recibo de caja**. El recibo siempre es por el total de la venta.

**¿Por qué no veo el campo Valor recibido?**
Solo aparece con las formas de pago que no piden banco ni documento de referencia, como **Efectivo**. Con las formas que sí los piden, el diálogo no lo muestra.

**¿Por qué un cliente de contado no muestra cartera?**
La venta de contado no tiene saldo por cobrar. La pantalla muestra **No aplica: venta de contado** y no revisa cupo ni mora. El documento sigue en la cartera de la compañía y en los informes, como siempre.

**¿Por qué no puedo editar un documento?**
Revise el estado del documento y sus permisos. Un documento no se puede editar si:

- ya fue **transmitido a la DIAN** (use una nota crédito o una devolución);
- está **anulado**;
- su fecha está en un **periodo cerrado**;
- tiene **documentos dependientes** sin anular;
- el documento está cerrado y su usuario no tiene el permiso de **editar documentos cerrados**.

**¿Qué hago si la factura electrónica falla?**
Abra el documento y lea el **Motivo** del bloque **Factura electrónica**. Si dice que el proveedor no está disponible, espere un poco y use **Reenviar a la DIAN**. Si dice que el proveedor rechazó datos del documento, revíselo antes de reenviar. Si la pantalla dice **Existe** al verificar, no la reenvíe.

**¿Por qué la tirilla sale sin CUFE?**
Porque el CUFE se consulta al proveedor tecnológico, y la impresión no espera. Si el proveedor no respondió a tiempo, o la factura todavía no está transmitida, la tirilla sale igual. Cuando el proveedor responda, use **Ver CUFE** en el documento.

**¿Por qué no aparece el botón Anular o Eliminar?**
Si la factura electrónica está **en cola**, el envío está en curso y no se puede anular ni eliminar: espere a que termine o falle. Cuando el envío termina o falla, los botones reaparecen según el estado del documento. Si la factura está **transmitida a la DIAN**, use una nota crédito o una devolución.

**¿Cuál es la diferencia entre anular y nota crédito?**
- **Anular** deja sin efecto un documento que todavía no fue transmitido a la DIAN. Queda anulado, con su motivo.
- **Nota crédito** es un documento nuevo que corrige una factura ya transmitida. La factura original no cambia, y la nota se envía a la DIAN.

**¿Puedo cambiar fletes o otros valores en una factura electrónica?**
No. En un tipo de factura electrónica estos valores no existen y quedan en 0.

**¿Por qué no aparece el botón Seleccionar remisiones?**
Falta completar el tipo, la fecha, el cliente o la sucursal.

**¿De dónde sale el valor que trae la línea?**
De la lista de precios de la sucursal del cliente. Si el valor dice **Lo escribiste tú**, usted lo cambió y no se va a pisar.

**¿Por qué la pantalla dice que se sumó a una línea?**
Porque leyó o escribió un producto igual (misma referencia, descuento, IVA y bodega) a una línea que ya estaba. La cantidad se suma y no se crea otra línea.

---

<a id="errores"></a>
## 🛠️ Errores comunes

| Mensaje | Qué hacer |
|---------|-----------|
| **El documento no se puede editar en su estado actual.** | Revise si está transmitido, anulado o en un periodo cerrado. |
| **La factura ya se transmitió a la DIAN: no se puede cambiar.** | Use una nota crédito o una devolución. |
| **La fecha pertenece a un periodo cerrado.** | Elija otra fecha. |
| **El cliente está inactivo.** / **No hay un cliente activo con ese documento.** | Elija un cliente activo. |
| **El vendedor no existe o está inactivo.** | Elija otro vendedor. |
| **Ese consecutivo ya está en uso.** | Elija otro consecutivo, o déjelo vacío. |
| **El servidor está ocupado. Intenta de nuevo en unos segundos.** | Espere unos segundos e intente de nuevo. |
| **No tiene permiso para generar el recibo de caja.** | Cancele, o use **Cerrar sin recibo** si así lo decide. Para tener el permiso, pida al administrador. |
| **No hay formas de pago vigentes.** | Pida al administrador que cree una forma de pago. |
| **Sin conexión con el servidor. Revise su red e intente de nuevo.** | Las líneas quedan en **No se guardó**: use **Reintentar**. |

---

<a id="relacionado"></a>
## 🧷 Relacionado

- [Ventas](../readme.md): índice del módulo.
- [Pedidos](pedidos.md): los pedidos desde los que se factura.
- [Remisiones](remisiones.md): las remisiones que se pueden facturar.
- [Clientes](../maestros/clientes.md): condiciones, sucursales y lista de precios de cada cliente.
- [Vendedores](../maestros/vendedores.md): quién aparece como vendedor del documento.
- [Ficha del cliente · Facturas de Venta y sus Recibos de Caja](../clientes/ficha-facturas.md): las facturas y devoluciones de un cliente.
- [Ficha del cliente · Cartera](../clientes/ficha-cartera.md): lo que debe el cliente, con su saldo.
- [Manejo general de la información](../../Generales/manejo-general-informacion.md): búsqueda, orden, paginación y ayuda.

---

[← Volver al índice de ventas](../readme.md)
