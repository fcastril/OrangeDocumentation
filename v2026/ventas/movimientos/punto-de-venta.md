[Regresar a la documentación de Ventas](../readme.md)

---

# 🛒 Punto de venta

![Static Badge](https://img.shields.io/badge/Tipo-Movimiento-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-PuntoDeVenta-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261106-yellow)

---

## 📋 Descripción

El **punto de venta** es la pantalla para vender en el mostrador de forma rápida. Usted escanea o toca los productos, ajusta cantidades y descuentos, y cobra en **un solo paso**: al cobrar se cierra la venta y se crea el **recibo de caja** automáticamente.

La pantalla usa la **caja** que tiene asignada su usuario en [Cajeros](../maestros/cajeros.md). La caja le dice con qué tipo de movimiento de venta vende, a qué cliente y bodega, y qué forma de pago aparece por defecto. Los tipos que se asignan a una caja son los del **punto de venta**, no los de [Ventas y devoluciones](ventas-devoluciones.md).

Las ventas cobradas aquí aparecen también en [Ventas y devoluciones](ventas-devoluciones.md), pero **solo para consulta**: con el origen *Punto de venta*, no se pueden editar allí. Gestiónelas desde el punto de venta.

> 📘 Cada pestaña del navegador trabaja con **una compañía**. El nombre y el color de la compañía se ven en la barra superior.

> 💡 La venta se guarda al agregar cada producto. Si se cierra la pestaña o se recarga la página, al volver puede **continuar la venta abierta**, desde la caja o desde el listado con **Editar**.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Movimientos**, haga clic en **Punto de venta**.

Se abre el **listado de ventas del punto de venta** (ver [Listado de ventas del punto de venta](#-listado-de-ventas-del-punto-de-venta)). Para vender, pulse **Nueva venta (F2)**.

---

## 📋 Listado de ventas del punto de venta

![Listado de ventas del punto de venta](../recursos/img/punto-venta/23-listado-ventas.png)

Al entrar a **Punto de venta** ve las ventas hechas en el punto de venta. Por defecto muestra las de **hoy**. Cambie **Desde** y **Hasta** para ver otro rango.

El listado usa la misma tabla que [Ventas y devoluciones](ventas-devoluciones.md), sin la columna ni el filtro **Origen**, porque todas sus filas son del punto de venta.

**Nueva venta (F2)**: abre la caja con una venta nueva. La tecla **F2** también funciona desde el listado.

| Venta | Qué hacer |
|-------|-----------|
| **Abierta** (en curso) | Pulse **Editar**. La venta vuelve a la caja con sus líneas, cliente y datos, para seguir o cobrar. |
| **Cerrada** (cobrada) | Pulse **Ver** para abrir el detalle (solo consulta). Desde la fila también puede imprimir, anular o crear una devolución. |

Los botones de cada fila son íconos. Al pasar el cursor aparece su nombre:

- **Ver**: abre el detalle de la venta.
- **Editar**: solo en una venta abierta. La vuelve a la caja.
- **Imprimir**: abre el PDF de la venta en una pestaña nueva.
- **Crear nota crédito o devolución**: abre el detalle para hacer la devolución.
- **Anular**: pide un motivo (de 1 a 200 caracteres, sin comas ni punto y coma). Si la venta no se puede anular, la pantalla dice por qué.
- **Eliminar**: pide confirmación antes de borrar la venta.

Si un botón aparece deshabilitado, su perfil no tiene el permiso correspondiente (ver *¿No ve algún botón?* en la pantalla principal).

---

## 🚦 Antes de vender: estados de entrada

Al entrar, la pantalla revisa su caja. Si algo no está listo, **no muestra el buscador**: le dice qué pasa y qué hacer.

| Lo que ve | Qué significa | Qué hacer |
|-----------|---------------|-----------|
| **Cargando** | La pantalla está revisando su caja. | Espere unos segundos. |
| **Este usuario no está configurado como cajero** | Su usuario no tiene caja asignada. | Si tiene acceso a Cajeros, haga clic en **Ir a Cajeros** y cree su caja. Si no, pida a un administrador con acceso a Ventas › Maestros › Cajeros que lo configure. |
| **La caja no está lista para vender** | La caja existe, pero le falta algo. La lista indica qué (por ejemplo, el tipo de movimiento de venta, la forma de pago, o que el tipo no tiene recibo de caja automático, cliente por defecto, sucursal o bodega). | Pida a un administrador de Ventas que complete la caja o el tipo de movimiento. |
| **No tiene permiso para vender** | Su perfil puede abrir el punto de venta, pero no crear ventas. | Pida a un administrador que le asigne el permiso (ver la tabla *¿No ve algún botón?* en la pantalla principal). |
| **No se pudo cargar la caja** | Hubo un problema de conexión. | Haga clic en **Reintentar**. Lo que escribió no se pierde. |

![Sin cajero](../recursos/img/punto-venta/01-sin-cajero.png)

![Sin cajero y sin acceso a Cajeros](../recursos/img/punto-venta/02-sin-cajero-sin-acceso.png)

![Caja incompleta](../recursos/img/punto-venta/03-incompleto.png)

![Sin permiso para vender](../recursos/img/punto-venta/04-sin-permiso.png)

> ℹ️ Si su usuario tiene más de una caja, la pantalla usa la que se registró primero. Un administrador puede revisarlo en [Cajeros](../maestros/cajeros.md).

---

## 🖥️ Pantalla principal

![Punto de venta con favoritos](../recursos/img/punto-venta/05-favoritos.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **Caja**, **Cajera** y **Tipo** | Caja, usuario y tipo de movimiento de venta con el que vende. |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. |
| **Cliente** | El cliente y la sucursal de la venta. Un clic (o **F4**) lo cambia. |
| **Vendedor**, **Lista** y **Observaciones** | Datos opcionales de la venta. No son obligatorios para vender. |
| **Atajos** | Abre el panel de teclas rápidas. |
| **Ventas** | Abre el listado de ventas del punto de venta. La venta en curso queda abierta. |
| **Código, EAN o nombre** | El buscador. Siempre queda enfocado. |
| **Favoritos** y **Catálogo** | Las pestañas con los productos para tocar. |
| **Venta actual** | Las líneas de la venta, con los totales y el botón **Cobrar**. |
| **Modo táctil** | Agranda botones y tarjetas. Ver [Modo táctil](#-modo-tactil). |

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil:

| Permiso | Qué habilita |
|---------|--------------|
| Consultar **Punto de venta** | Entrar a la pantalla y ver el listado de ventas. |
| Crear y Actualizar en **Punto de venta** | Agregar, cambiar y cobrar ventas. |
| Crear en **Recibos de Caja y Egresos** | Que el cobro cree el recibo de caja automáticamente. |
| Eliminar en **Punto de venta** | Cancelar la venta y borrarla. Sin este permiso, la venta queda guardada como abierta. |
| Imprimir en **Punto de venta** | El botón **Imprimir tirilla** y la impresión desde el listado. |
| Crear en **Punto de venta** | Crear un cliente nuevo desde la pantalla. |
| Consultar e Imprimir en **Ventas y devoluciones** | Ver e imprimir, desde esa pantalla, las ventas del punto de venta (solo lectura). No hace falta para vender. |
| **Cambiar precio POS** | El botón **Cambiar precio** y el cambio de precio de una línea a cualquier valor. Es el único permiso para cambiar precios; ser administrador no basta (ver más abajo). |

---

## 🔍 Buscar y agregar productos

### Escribir o escanear un código

1. Con el buscador enfocado, escanee el código de barras (EAN) o escriba el código, el código alterno o el nombre.
2. Pulse **Enter**.

- Si el código coincide con **un solo producto**, se agrega **una unidad**.
- Si tiene **varias variantes**, se abre la ventana para elegir (ver *Variantes*).
- Si **no existe**, aparece el aviso *Código no encontrado* y el buscador queda listo para seguir. No bloquea la venta.

Si escribe un nombre **sin pulsar Enter**, aparece una lista de coincidencias con el formato *Código - Nombre*. Elija el producto con un clic.

> 💡 Si escanea el **mismo código otra vez**, no se crea otra línea: se **suma una unidad** a la línea que ya está en la venta.

### Favoritos y catálogo

- **Favoritos** muestra los productos marcados como favoritos para el punto de venta.
- **Catálogo** muestra todos los productos que se pueden vender en el punto de venta.
- Use el filtro de **grupo** y **subgrupo** para encontrar productos del catálogo.
- Un clic en la tarjeta agrega el producto. Si el producto tiene foto, la verá; si no, verá un ícono.
- Un producto sin existencia en la bodega de la caja lleva la etiqueta **Agotada**. La etiqueta **no aparece al mismo tiempo que las fichas**: se consulta aparte, así que se pone un instante después de que se pintan los productos. Si un cambio de existencia hecho en otro lugar tarda en reflejarse, la etiqueta puede demorar **hasta 60 segundos**. Si una ficha no tiene la etiqueta, el producto puede estar agotado igual: al intentar venderlo sin existencia, la pantalla muestra *Sin existencia en la bodega.* y no lo agrega.

> 📸 Los favoritos, el catálogo del punto de venta y la foto se administran en el maestro de [Referencias](../../inventarios/maestros/referencias.md). Un producto sin foto **sigue apareciendo**: se muestra con un ícono.

Para cambiar de pestaña sin tocar la pantalla, use **F7**.

![Catálogo](../recursos/img/punto-venta/06-catalogo.png)

### Búsqueda relacionada

Mientras escribe, la pantalla le muestra las coincidencias. Las listas se cargan por páginas: la pantalla nunca trae todos los productos de una vez.

![Búsqueda relacionada](../recursos/img/punto-venta/07-buscar-relacionada.png)

### Código no encontrado

![Código no encontrado](../recursos/img/punto-venta/08-ean-no-encontrado.png)

### Variantes

Si el producto tiene tallas, colores u otros atributos, la pantalla le pide elegir:

1. Toque el **atributo principal** (por ejemplo, la talla).
2. Toque el **atributo secundario** (por ejemplo, el color).
3. Revise la **existencia** de cada opción y pulse **Agregar**.

Las opciones que están **agotadas en la bodega** aparecen marcadas y no se pueden elegir, salvo que el tipo de movimiento de venta permita vender sin existencia.

Si el producto tiene **una sola variante**, se agrega directamente, sin preguntar.

![Elegir variante](../recursos/img/punto-venta/09-selector-variantes.png)

### Fecha de vencimiento y lote

Algunos productos exigen **fecha de vencimiento** o **lote**. Si es así, la pantalla se lo pide **antes** de agregar el producto:

1. **Fecha de vencimiento** (primero). Aparece cuando el producto exige fecha de vencimiento. Escríbala en el calendario y pulse **Agregar**.
   - Es **obligatoria**: no puede agregar el producto sin ella.
   - No puede ser **anterior a hoy**. La pantalla lo avisa: *La fecha de vencimiento no puede ser anterior a hoy.*
2. **Lote** (después). Aparece cuando el producto exige lote. Escriba el lote (máximo 20 caracteres) y pulse **Agregar**. Enter agrega, Esc cancela.

**Esc** o **Cancelar** en cualquiera de las dos ventanas **cancela la acción**: el producto no se agrega a la venta.

> ℹ️ Si el producto exige fecha y lote, primero le pide la fecha y luego el lote.

![Ventana de fecha de vencimiento](../recursos/img/punto-venta/20-fecha-vencimiento.png)

![Ventana con la fecha indicada](../recursos/img/punto-venta/21-fecha-vencimiento-con-fecha.png)

![Aviso cuando la fecha ya pasó](../recursos/img/punto-venta/22-fecha-vencimiento-pasada.png)

---

## 🧾 La venta actual (carrito)

Cada línea muestra el producto, la variante, la **cantidad**, el valor unitario y el **descuento**.

| Acción | Cómo |
|--------|------|
| **Cambiar cantidad** | Use **+** y **−**, o escriba el número. También **+** y **−** del teclado sobre la línea seleccionada. |
| **Descuento** | Escriba el porcentaje en **Dto. %** (de 0 a 100). Solo se puede si el tipo de venta permite descuentos; si no, el campo aparece deshabilitado. |
| **Quitar una línea** | Toque la **papelera** y confirme con **Quitar**. Con la línea seleccionada, también **Supr**. |
| **Cambiar precio** | Solo aparece con el permiso **Cambiar precio POS**. Ver *Cambio de precio* más abajo. |

Los **totales** (artículos, subtotal, descuento, IVA y total) los calcula el sistema. Siempre se ven en la parte inferior de la venta.

![Editar una línea](../recursos/img/punto-venta/10-carrito-editar-linea.png)

### Cambio de precio

El precio de cada línea es el de la **lista de precios** elegida. Para cambiarlo, su usuario necesita el permiso **Cambiar precio POS**. Ser administrador no basta si ese permiso no está asignado.

**Con el permiso Cambiar precio POS:**

1. Seleccione la línea y haga clic en **Cambiar precio**.
2. Escriba el **Nuevo valor unitario** (cualquier valor) y pulse **Aplicar**. El precio cambia directamente, sin pedir autorización.

**Sin el permiso** no aparece el botón **Cambiar precio**. Si la venta necesita un precio distinto del de la lista, otro usuario que sí tenga el permiso puede autorizarlo: en la ventana **Autorización de precio**, escribe su **Usuario autorizador** y su **Clave del autorizador**. La autorización vale solo para ese cambio: no inicia sesión en la pantalla y la clave no se guarda en la pantalla ni en la venta. Si la autorización se vence, vuelva a pedirla.

### Cancelar, nueva venta y retomar

- **Cancelar venta (Esc)** descarta todas las líneas. Se pide confirmación.
  - Si su perfil tiene el permiso de **Eliminar** en Punto de venta, la venta se borra.
  - Si **no** lo tiene, la venta queda guardada como **abierta** y la pantalla se lo avisa: un supervisor puede eliminarla.
- **Nueva venta (F2)** empieza una venta limpia. Si hay líneas, pide confirmación.
- **Retomar**: si al entrar hay una venta abierta, la pantalla pregunta **Continuar** o **Descartar**. Con **Continuar** recupera las líneas, el cliente y los datos de la venta.

![Venta abierta para retomar](../recursos/img/punto-venta/16-venta-abierta-retomar.png)

---

## 👤 Cliente

El cliente de la venta viene de la caja (el cliente por defecto del tipo de movimiento). Se muestra en la cabecera con su **sucursal**.

### Cambiar el cliente

1. Haga clic en el cliente o pulse **F4**.
2. Escriba el **documento** y pulse **Enter**, o busque por nombre.
3. Elija la **sucursal** del cliente. Solo aparecen las sucursales de ese cliente.
4. Pulse **Usar este cliente**.

**Cambiar el cliente no borra la venta**: las líneas, las cantidades y los descuentos se conservan.

Si el cliente tiene **mora** o supera su **cupo**, la pantalla lo muestra con el motivo y no deja cerrar la venta hasta corregirlo.

![Cliente por defecto](../recursos/img/punto-venta/11-cliente-por-defecto.png)

### Crear un cliente nuevo

Si el cliente no existe, cree uno sin salir de la pantalla y sin perder la venta:

1. En la ventana de cliente, pulse **Nuevo cliente**.
2. Complete los campos mínimos:
   - **Tipo y número de documento** (con el dígito de verificación si es NIT).
   - **Tipo de persona**: *Natural* (nombres y apellidos) o *Jurídica* (razón social).
   - **Teléfono**, **Correo**, **Dirección** y **Ciudad** (viene preseleccionada la ciudad de la compañía).
3. Pulse **Crear y usar**.

Al crear el cliente, el sistema también crea su **sucursal 0000** (la sucursal por defecto) con los datos que escribió, la lista de precios de la compañía y el vendedor y la zona por defecto. Esa sucursal queda seleccionada para la venta.

**Qué puede salir mal:**

| Mensaje | Qué hacer |
|---------|-----------|
| Escriba el número de documento / el primer nombre / el primer apellido / elija la ciudad | Complete el campo señalado. |
| El correo no es válido. | Corríjalo. |
| *Ya existe un cliente con ese documento: [nombre]. ¿Quiere usarlo en esta venta?* | Pulse **Usar este cliente**. No se crea uno repetido. |
| *La compañía no tiene vendedor o zona por defecto para crear la sucursal 0000.* | Pida a un administrador que configure esos datos de la compañía. |
| *No se pudo registrar el cliente porque el intento anterior quedó en conflicto. Revise los datos y pulse Guardar de nuevo.* | Revise los datos y pulse **Crear y usar** otra vez. La pantalla prepara un intento nuevo: el cliente no se duplica. |

![Nuevo cliente](../recursos/img/punto-venta/12-cliente-nuevo.png)

---

## 🧑‍💼 Vendedor, lista de precios y observaciones

En la cabecera hay tres datos opcionales. **No son obligatorios para vender.**

| Dato | Qué hace |
|------|----------|
| **Vendedor** | Viene el vendedor de la sucursal del cliente. Puede cambiarlo buscando otro vendedor. |
| **Lista de precios** | Viene la lista de la sucursal del cliente (de 1 a 5). Cambiarla afecta a las **líneas que agregue después**; las líneas ya agregadas conservan su precio. |
| **Observaciones** | Texto libre de hasta 200 caracteres. No admite comas ni punto y coma. |

---

## 💵 Cobrar la venta

Cobrar es un solo paso: al confirmar, el sistema **cierra la venta** y **crea el recibo de caja automáticamente**. O se hacen las dos cosas, o no se hace ninguna.

1. Pulse **Cobrar (F9)**. Se abre la ventana con el **total a cobrar**.
2. Revise la **forma de pago**. Viene la **forma de pago por defecto** de su caja, marcada. Para usar otra, toque la tarjeta.
3. Si la forma de pago es **efectivo**, escriba el **valor recibido**, o pulse **Exacto**. La pantalla muestra el **cambio** o, si falta dinero, cuánto falta.
4. Si la forma de pago pide un **banco** o un **documento de referencia**, escríbalos en esa misma ventana.
5. Pulse **Confirmar cobro (Enter)**.

Con el teclado: **F9** abre el cobro y **Enter** lo confirma. **Esc** vuelve a la venta sin cobrar.

![Cobro](../recursos/img/punto-venta/13-cobro.png)

![Cobro con cambio](../recursos/img/punto-venta/14-cobro-con-cambio.png)

### Venta cerrada

Al cobrar, la pantalla muestra **Venta cerrada** con el número de venta, el **recibo de caja** que se creó, el total cobrado y el cambio.

- **Imprimir tirilla (F8)**: solo aparece si tiene el permiso de imprimir.
- **Nueva venta (F2)**: empieza la siguiente venta.
- **Ver ventas**: abre el listado de ventas del punto de venta.

![Venta cerrada](../recursos/img/punto-venta/15-venta-cerrada.png)

**Qué puede salir mal al cobrar:**

| Mensaje | Qué hacer |
|---------|-----------|
| *No se pudo cobrar: no se cerró la venta ni se creó el recibo. Puede reintentar con los mismos datos.* | Pulse **Reintentar cobro**. No se cobró nada: lo que escribió se conserva. |
| *El periodo del recibo de caja está cerrado. No se cobró nada.* | Pida a un administrador que revise el periodo de recibos de caja. |
| *Faltan $ …* | El valor recibido es menor que el total. Escriba el valor completo. |

---

## ⌨️ Atajos de teclado

Los atajos funcionan con el buscador enfocado. Puede ver esta lista en la pantalla con el botón **Atajos**.

| Tecla | Acción |
|-------|--------|
| **F2** | Nueva venta |
| **F3** o **/** | Enfocar la búsqueda |
| **F4** | Cambiar cliente |
| **F6** | Descuento de la línea seleccionada |
| **F7** | Alternar Favoritos y Catálogo |
| **F8** | Imprimir tirilla (tras cobrar) |
| **F9** | Cobrar y confirmar |
| **Esc** | Cancelar o cerrar el panel |
| **Supr** | Quitar la línea seleccionada |
| **↑** / **↓** | Mover entre líneas |
| **+** / **−** | Cantidad de la línea |

> ℹ️ F1, F5, F10, F11 y F12 los reserva el navegador y no se usan en esta pantalla.

![Panel de atajos](../recursos/img/punto-venta/17-panel-atajos.png)

---

## 📱 Modo táctil

El punto de venta está pensado para usarse con pantalla táctil.

- En el encabezado está el botón **Modo táctil**. En un equipo con pantalla táctil se activa solo; puede encenderlo o apagarlo cuando quiera.
- Con el modo táctil activo, las tarjetas de productos, las líneas y los botones son **más grandes**, para tocarlos sin error.
- En **pantallas pequeñas** (por ejemplo, un celular), la pantalla se divide en dos pestañas: **Productos** y **Carrito (n)**. Abajo queda una barra con el **total** y el botón **Cobrar**.

| Productos | Carrito |
|-----------|---------|
| ![Móvil: productos](../recursos/img/punto-venta/18-movil-productos.png) | ![Móvil: carrito](../recursos/img/punto-venta/19-movil-carrito.png) |

---

## 🔄 Cambios de otros usuarios (en vivo)

La pantalla se mantiene conectada: no tiene que recargar para ver cambios importantes.

- Si **otra persona modifica la venta abierta** que usted tiene en pantalla, la pantalla se lo avisa: *Otra persona modificó la venta abierta.* Se recarga la venta con lo que quedó guardado.
- Si **cambia la configuración de su caja** (por ejemplo, el tipo de movimiento o la forma de pago), aparece el aviso: *Su configuración de caja cambió. Pulse Reintentar para recargarla.*
- Junto a la descripción verá **En vivo** mientras la conexión esté activa. Si se interrumpe, la pantalla intenta reconectarse sola.

> ℹ️ Lo que usted hace en esta misma pestaña no genera avisos.

---

## ❓ Preguntas frecuentes

**¿Por qué no aparece el buscador?**
Porque la caja no está lista para vender (no está configurada, está incompleta o su perfil no tiene permiso). Vea *Antes de vender* arriba.

**¿Por qué la venta quedó como abierta y no se eliminó?**
Porque su perfil no tiene el permiso de **Eliminar** en Punto de venta. Pida a un supervisor que la elimine.

**¿Por qué no puedo cambiar el descuento de una línea?**
Porque el tipo de movimiento de venta de su caja no permite descuentos.

**¿Por qué no puedo cambiar el precio?**
Porque su usuario no tiene el permiso **Cambiar precio POS**. Ser administrador no lo reemplaza. Sin ese permiso, otro usuario que lo tenga puede autorizar ese cambio puntual con su usuario y clave (ventana **Autorización de precio**).

**¿Por qué sale marcada esa forma de pago?**
Es la forma de pago por defecto de su caja. Puede elegir otra en la ventana de cobro, pero la que sale por defecto la define la caja en [Cajeros](../maestros/cajeros.md).

**¿Un producto sin foto aparece en la pantalla?**
Sí. Se muestra con un ícono. La foto se agrega en el maestro de Referencias.

**¿Puedo vender sin cliente?**
La venta siempre tiene el cliente de la caja o el que usted elija. Si no tiene uno, cree un cliente nuevo desde la pantalla.

**¿Dónde veo las ventas que cobré?**
En el **listado de ventas** de este punto de venta (hoy por defecto). Las mismas ventas aparecen en [Ventas y devoluciones](ventas-devoluciones.md) con el origen *Punto de venta*, solo para consulta.

---

## 🧭 Errores frecuentes

| Mensaje | Solución |
|---------|----------|
| *Código no encontrado* | Revise el código o el EAN, o busque por nombre. |
| *Agotada en la bodega* | No hay existencia de esa variante en la bodega de la caja. |
| *Sin existencia en la bodega.* | No hay existencia en la bodega de la caja para esa cantidad. Revise la existencia o use otra cantidad. |
| *No tiene autorizada la bodega de esta venta. Pida a un administrador que se la asigne o use otra caja.* | La bodega de la caja no está entre las bodegas autorizadas a su usuario. Pida que se la asignen, o use otra caja. No se agrega la línea. |
| *La fecha de vencimiento no puede ser anterior a hoy.* | Escriba una fecha de hoy en adelante. |
| *La referencia exige una fecha de vencimiento válida. Agréguela de nuevo indicando la fecha.* | Vuelva a agregar el producto e indique la fecha de vencimiento. |
| *Ya existe un cliente con ese documento* | Pulse **Usar este cliente**. |
| *No se pudo cargar la caja* | Pulse **Reintentar**. Si sigue igual, revise su conexión. |
| *No se pudieron cargar los productos.* | Pulse **Reintentar** o cambie de pestaña. |
