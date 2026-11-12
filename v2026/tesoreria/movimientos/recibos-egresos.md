[Regresar a Tesorería](../readme.md)

---

# 🧾 Recibos de caja

![Static Badge](https://img.shields.io/badge/Tipo-Movimiento-red)
![Static Badge](https://img.shields.io/badge/Module-Tesorer%C3%ADa-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-RecibosDeCaja-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261111-yellow)

---

## 📋 Descripción

Un **recibo de caja** registra el dinero que **entra** a la compañía por un cobro a un cliente: a qué **facturas** se aplica y con qué **formas de pago** (efectivo, transferencia, cheque, tarjeta u otra que tenga configurada).

Cada recibo tiene una **fecha**, un **cliente**, las **facturas que cruza** (una línea por factura, con sus valores) y uno o varios **pagos**. El total de los pagos debe ser igual al total de las líneas. Al **cerrarlo**, OrangeERP registra los asientos contables del cobro y el recibo ya no se edita.

Use esta pantalla cuando un cliente le pagó. Si lo que hace es pagar a un proveedor, use la opción de egresos de esta misma pantalla, cuando esté disponible en su compañía; el banco que se mueve por su cuenta se registra en [Notas bancarias](notas-bancarias.md).

> 📘 La búsqueda, el orden, la paginación y la ayuda funcionan igual en todas las tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Cada pestaña del navegador trabaja con **una compañía**. El nombre de la compañía se ve en el título de la pestaña y en la barra superior.

> ℹ️ Un recibo **no se elimina** desde esta pantalla. Si está mal, **anúlelo** con un motivo: queda en el listado con su historia.

Antes de empezar, revise que el cliente, las formas de pago y los bancos existan. Las formas de pago se mantienen en [Formas de pago](../maestros/formas-pago.md) y los bancos en [Bancos](../maestros/bancos.md).

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Tesorería**.
2. En **Movimientos**, haga clic en **Recibos de caja y egresos**.

---

## 🔐 Permisos

Cada acción depende de los permisos de su perfil sobre la opción **Recibos de caja y egresos**. Además, el **tipo de movimiento** del recibo debe estar autorizado para su usuario.

| Permiso | Qué habilita |
|---------|--------------|
| Consultar | Ver el listado, abrir los recibos, descargar sus adjuntos y ver la bitácora. |
| Crear | **Nuevo documento**, **Guardar** de un recibo nuevo y subir adjuntos a un recibo guardado. |
| Actualizar | **Guardar** de un recibo abierto y **Cerrar transacción**. |
| Anular | **Anular documento**. |
| Imprimir | **Imprimir**, en el recibo y en la fila del listado. |

> ℹ️ Si su perfil no tiene **Consultar**, la pantalla le avisa: *No tienes acceso a esta pantalla.* Pida a su administrador el permiso que necesite.

---

## 🖥️ Pantalla principal

![Listado de recibos de caja y egresos](../recursos/img/recibos-egresos/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. Ver [Ayuda en pantalla](#-ayuda-en-pantalla). |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. Ver [Cambios de otros usuarios](#-cambios-de-otros-usuarios-en-vivo). |
| **Nuevo documento** | Crea un recibo. |
| **Filtros** | Reducen el listado por fecha, tipo de movimiento y estado. Ver *Filtros*. |
| **Buscar** | Busca por tipo, número, documento de referencia o tercero. |
| **Encabezados** | Un clic ordena de forma ascendente, el segundo descendente y el tercero quita el orden. Por defecto, el listado va de la fecha más reciente a la más antigua. |
| **Filas por página** y paginación | Cambian cuántos recibos ve y la página. |

Las columnas son:

| Columna | Qué muestra |
|---------|-------------|
| **Acciones** | Los botones del recibo (ver, imprimir, editar, anular, según el caso). Siempre están en la **primera columna**. |
| **Tipo** | El tipo de movimiento del recibo. |
| **Número** | El número del recibo. |
| **Fecha** | La fecha del recibo. |
| **Fecha efectiva** | La fecha con la que queda registrado. Normalmente es igual a la fecha. |
| **Doc. referencia** | El documento de referencia que escribió al crear el recibo. |
| **Tercero** | El cliente del recibo. |
| **Valor** | El total del recibo. |
| **Estado** | **Abierto**, **Cerrado** o **Anulado**, con su icono. |

Los estados se distinguen por icono y texto:

- **Abierto** (lápiz): se puede editar. Todavía no está cerrado.
- **Cerrado** (candado): registró sus asientos contables y ya no se edita.
- **Anulado** (prohibido): no se borró; quedó con su motivo, su usuario y su hora.

![Filtro por estado: abiertos](../recursos/img/recibos-egresos/02-filtro-estado-abiertos.png)

![Acciones de cada fila según el estado y el permiso](../recursos/img/recibos-egresos/03-acciones-por-fila.png)

### 🔎 Filtros

Los filtros están sobre la tabla y se pueden combinar:

- **Fecha desde** y **Fecha hasta**. Si la fecha inicial es posterior a la final, verá: *La fecha desde no puede ser posterior a la fecha hasta.* y el listado no muestra recibos hasta corregirla.
- **Tipo de movimiento**: solo los recibos de ese tipo. Por defecto, *Todos los tipos*.
- **Estado**: *Todos*, o uno de los estados (Abierto, Cerrado, Anulado).
- **Limpiar filtros**: quita todos los filtros.

**Exportar a Excel** no está disponible en esta pantalla.

### Estados vacíos y errores del listado

| Mensaje | Qué significa | Qué hacer |
|---------|---------------|-----------|
| *Aún no hay recibos ni egresos.* | La compañía no tiene documentos todavía. | Haga clic en **Nuevo documento** (si tiene el permiso de crear). |
| *Sin resultados.* | Ningún recibo coincide con la búsqueda o los filtros. | Cambie o limpie los filtros, o borre el texto del buscador. |
| *No se pudo cargar.* | Falló la consulta. | Revise su conexión y haga clic en **Reintentar**. |
| *No tienes acceso a esta pantalla.* | Su perfil no tiene **Consultar**. | Pida el permiso a su administrador. |

![Listado vacío](../recursos/img/recibos-egresos/04-listado-vacio.png)

![Listado sin resultados](../recursos/img/recibos-egresos/05-listado-sin-resultados.png)

![Rango de fechas inválido](../recursos/img/recibos-egresos/06-rango-invalido.png)

![Error al cargar el listado](../recursos/img/recibos-egresos/07-error-de-carga.png)

![Sin permiso de consulta](../recursos/img/recibos-egresos/08-sin-permiso.png)

> 📱 En el celular, o en una ventana angosta, cada recibo se muestra como una tarjeta, con sus acciones visibles.

---

## ➕ Crear un recibo

1. En el listado, haga clic en **Nuevo documento**.
2. Elija el **Tipo de movimiento**. Solo verá los tipos autorizados para su usuario.
3. Complete el **encabezado** (ver la tabla siguiente).
4. En **Facturas que se cruzan**, haga clic en **Seleccionar facturas** y marque las que cubre el cobro.
5. Revise las **Formas de pago** y el **total**.
6. Haga clic en **Guardar**.

![Nuevo recibo de caja](../recursos/img/recibos-egresos/09-nuevo-recibo.png)

### Encabezado

| Campo | Qué debe tener |
|-------|----------------|
| **Tipo de movimiento** | El tipo del recibo. Define la cartera (clientes) y si el consecutivo se puede escribir. |
| **Consecutivo** | Se asigna al guardar. Si el tipo permite escribirlo, puede digitar un número; si lo deja vacío, se usa el siguiente libre. Si el número ya está usado, verá: *Ese consecutivo ya está usado. Elige otro o déjalo vacío.* |
| **Fecha** | La fecha del recibo. Por defecto es hoy; si ya pasó la hora de cierre de la compañía, es mañana. |
| **Fecha efectiva** | Igual a la fecha por defecto. No puede ser posterior a la fecha: *La fecha efectiva no puede ser posterior a la fecha.* |
| **Documento de referencia** | Hasta 20 caracteres, sin «,» ni «;». Si lo deja vacío, se usa el código del tipo y el consecutivo. |
| **Centro de costos** | Obligatorio solo si el tipo lo exige: *Este tipo exige centro de costos.* |
| **Cliente (tercero)** | Busque por documento o por nombre. Un cliente inactivo no se puede usar: *Tercero inactivo.* |
| **Observaciones** | Hasta 200 caracteres, sin «,» ni «;». |

Si el cliente tiene una alerta en sus observaciones, la verá en el recuadro **Alerta del tercero**, con su texto. Puede continuar con el recibo; la alerta solo informa.

> ℹ️ La fecha define el periodo. Si el periodo de la fecha está cerrado para recibos y egresos, verá: *El periodo de la fecha está cerrado para recibos y egresos.* y no se puede guardar. Pida a Contabilidad que abra el periodo o cambie la fecha.

### Facturas que se cruzan

Este bloque dice a qué facturas del cliente aplica el cobro.

1. Elija primero el **Cliente** y la **Fecha**. Sin ellos, **Seleccionar facturas** está deshabilitado.
2. Haga clic en **Seleccionar facturas**. Verá las facturas del cliente con saldo a esa fecha, ordenadas por fecha. Si quiere ver también las que tienen saldo cero, marque **Mostrar facturas sin saldo**.
3. Marque las facturas que cubre el cobro y haga clic en **Agregar … al documento**. Cada factura queda como una **línea**, con el valor propuesto igual a su saldo.

![Seleccionar facturas del cliente](../recursos/img/recibos-egresos/10-cruce-seleccionar-facturas.png)

![Facturas marcadas para abonar](../recursos/img/recibos-egresos/11-cruce-abonar.png)

Cada línea muestra el **documento afectado**, el **saldo vigente** y una rejilla de valores:

| Valor | Para qué sirve |
|-------|----------------|
| **Valor** | Lo que se abona de la factura. |
| **Descuento**, **IVA**, **Retefuente**, **ReteIVA**, **ReteICA**, **Segufletes**, **Intereses** | Los valores que acompañan el cobro, según corresponda. |
| **Otros valores** | Otros conceptos. Es el único campo que admite negativos (por ejemplo, -5000). |

Al pie de cada línea verá el **Neto de la línea** y el botón **Quitar la línea n**. El neto se actualiza mientras escribe.

![Editar los valores de una línea](../recursos/img/recibos-egresos/12-cruce-editar-linea.png)

> ⚠️ Si abona más que el saldo de la factura, verá: *Abonas más que el saldo (…). Se permite y quedará un saldo a favor.* Puede guardar; el sistema deja el saldo a favor del cliente.

![Abono mayor al saldo](../recursos/img/recibos-egresos/13-cruce-exceso-abono.png)

Si una factura tiene saldo negativo, aparece marcada como **Saldo a favor**. Sus valores se restan del total.

### Formas de pago

En **Formas de pago** registre cómo entró el dinero.

1. Haga clic en **Agregar forma de pago**.
2. Elija la **Forma de pago** (obligatoria).
3. Si la forma de pago pide banco o referencia, complete **Banco** y **Documento de referencia** (hasta 20 caracteres, sin «,» ni «;»). Si no los pide, verá: *Esta forma de pago no pide banco ni referencia.* y esos campos quedan vacíos.
4. Escriba el **Valor** del pago.
5. Para quitar un pago, haga clic en **Quitar el pago n**.

No puede repetir la misma combinación de forma de pago, banco y referencia: *Ya hay un pago con la misma forma, banco y referencia.*

Debajo de los pagos está la línea de cuadre:

- *Los pagos cuadran con el total.*
- *Los pagos no suman el total: faltan …* o *Los pagos superan el total en …*

![Recibo con dos facturas y sus pagos](../recursos/img/recibos-egresos/14-recibo-con-cruce.png)

### El total: Total a pagar

En la parte inferior, el **Total a pagar** se ve siempre. Con **Ver desglose** puede ver los totales por concepto (valores, descuentos, IVA, retefuente, reteIVA, reteICA, segufletes, intereses y otros valores), la **Suma de pagos** y la **Diferencia**.

> ℹ️ Si el total sale negativo (saldo a favor), los pagos se registran por el valor absoluto.

### Guardar

**Guardar** guarda el recibo completo: encabezado, facturas, pagos y adjuntos. Todo se guarda junto o no se guarda nada. Si hace doble clic en **Guardar**, el recibo se guarda una sola vez.

Si los pagos no suman el total, el sistema no guarda y muestra: *Los pagos no suman el total; no se guardó nada.* También verá *Revisa los campos marcados: hay datos por corregir.* y los campos con error quedan señalados.

![Pagos que no cuadran](../recursos/img/recibos-egresos/15-pagos-no-cuadran.png)

![Validación de campos y resumen](../recursos/img/recibos-egresos/16-validacion.png)

Un recibo guardado queda **Abierto**. Puede volver a editarlo, o cerrarlo cuando esté listo.

---

## ✏️ Editar un recibo abierto

1. En el listado, haga clic en **Editar el documento** de la fila, o abra el recibo con **Ver**.
2. Cambie lo que necesite y haga clic en **Guardar**.

Después de guardar, el encabezado no cambia. Se pueden cambiar las **observaciones**, el **centro de costos**, las **líneas** y los **pagos**. Al guardar, los asientos contables se recalculan; si quita una línea o un pago, sus asientos se quitan con él.

![Recibo abierto: se edita y se puede cerrar, anular o imprimir](../recursos/img/recibos-egresos/17-recibo-abierto.png)

Si otro usuario cambió el recibo mientras lo edita, no se pierde su trabajo, pero no se guarda sobre el cambio ajeno. Vea [Cambios de otros usuarios](#-cambios-de-otros-usuarios-en-vivo).

> ℹ️ Un recibo **cerrado**, **anulado** o de un **periodo cerrado** no se edita. Lo verá con su aviso: *Este documento está cerrado: ya no se edita. Puedes imprimirlo o anularlo.*

![Recibo cerrado: solo lectura](../recursos/img/recibos-egresos/19-cerrado.png)

---

## ✅ Cerrar un recibo

Cerrar es el paso que registra los asientos contables del cobro. Es una acción aparte de guardar.

1. Abra el recibo abierto y guarde sus últimos cambios. Si tiene cambios sin guardar, verá: *Guarda los cambios antes de cerrar.*
2. Haga clic en **Cerrar transacción**.
3. Lea el diálogo y haga clic en **Cerrar transacción** para confirmar.

El diálogo dice: *Al cerrar, el documento ya no se podrá editar ni adjuntarle archivos. Solo se puede imprimir o anular. Se revisa otra vez que los pagos sumen el total.*

![Confirmar el cierre](../recursos/img/recibos-egresos/18-cerrar-confirmacion.png)

Al cerrar, el recibo queda **Cerrado** con su usuario y su hora, y el sistema le pregunta: *Documento cerrado. ¿Quieres imprimirlo?*

Si el cierre no se puede hacer, verá el motivo y el recibo sigue abierto:

| Mensaje | Qué hacer |
|---------|-----------|
| *Los pagos no suman el total; no se guardó nada.* | Revise los pagos y guarde de nuevo. |
| *El periodo de la fecha está cerrado para recibos y egresos.* | Pida a Contabilidad que abra el periodo. |
| *El documento ya está cerrado.* | Recargue el recibo para ver su estado. |

---

## ⛔ Anular un recibo

Anular es **invalidar** un recibo que no debió registrarse. No se borra nada: el recibo queda en el listado como **Anulado**, con el motivo, su usuario y la hora. Los saldos de las facturas afectadas vuelven a su valor.

Puede anular un recibo abierto o cerrado si tiene el permiso **Anular**.

1. Haga clic en **Anular documento** (en el recibo o en la fila del listado).
2. Escriba el **Motivo de la anulación**: entre 5 y 200 caracteres.
3. Confirme con **Anular documento**.

![Anular: motivo](../recursos/img/recibos-egresos/20-anular-motivo.png)

El diálogo dice: *No se borra nada: el documento queda anulado con su motivo, usuario y hora, y los saldos de las facturas afectadas vuelven a su valor.*

Un recibo anulado se muestra con este aviso: *Anulado por … el … Motivo: …* Sus adjuntos solo se pueden descargar y ya no se puede imprimir.

### Aviso de certificado de retención

Si el recibo usó cuentas con **certificado de retención**, el diálogo de anulación muestra este aviso, que también queda visible en el recibo:

> Aviso: este documento usó cuentas con certificado de retención. El certificado de retefuente del sistema anterior lo seguirá sumando aunque esté anulado; revísalo antes de emitir certificados.

Revise el certificado antes de emitirlo: el sistema anterior puede seguir sumando el recibo.

![Anular con aviso de certificado de retención](../recursos/img/recibos-egresos/21-anular-aviso-certificado.png)

### Aviso de facturas ya cruzadas

Si el recibo ya fue cruzado por otros recibos, el diálogo lo advierte: *Este documento ya fue cruzado por otros recibos. Se puede anular, pero sus saldos cambiarán.* Puede anularlo, pero revise antes los saldos de esas facturas.

![Recibo anulado](../recursos/img/recibos-egresos/22-anulado.png)

### No se puede anular

| Mensaje | Qué hacer |
|---------|-----------|
| *El periodo de la fecha está cerrado para recibos y egresos.* | Contabilidad debe abrir el periodo, o el recibo queda como está. |
| *El documento ya está anulado.* | Revise el listado: ya no hay nada que anular. |
| *No tienes permiso para esta acción.* | Pida el permiso de **Anular** a su administrador. |

---

## 🖨️ Imprimir

**Imprimir** genera el documento en PDF tamaño carta. Lo puede usar en un recibo abierto o cerrado, y también desde la fila del listado, con la acción **Imprimir el documento** de esa fila.

El documento trae la empresa, el cliente, su saldo a la fecha, las facturas cruzadas (o el anticipo), los totales con el valor en letras, las formas de pago, el detalle contable con débitos y créditos, y quién lo elaboró e imprimió.

Cada impresión suma uno al contador **Impresiones** del recibo, con su usuario y su hora. Un recibo anulado no se imprime.

---

## 📎 Adjuntos

En la pestaña **Adjuntos** puede guardar el soporte del cobro (por ejemplo, la consignación o la certificación del pago).

- **Espacio en uso**: cada recibo puede tener hasta **10 MB** de adjuntos en total.
- Formatos: **PDF**, **PNG** y **JPG**.
- **Descripción** obligatoria, de hasta 200 caracteres.
- Haga clic en **Subir adjunto**. Para bajar un archivo, use **Descargar**; para quitarlo, **Quitar**.

![Adjuntos de un recibo](../recursos/img/recibos-egresos/23-adjuntos.png)

Reglas:

- Si el recibo todavía no está guardado, verá: *Guarda el documento para poder adjuntar soportes.*
- Si el recibo está **cerrado** o **anulado**, no se pueden cambiar sus adjuntos. Puede descargarlos.
- Si el archivo haría pasar el recibo de 10 MB, o si ya llegó al cupo, quite un adjunto antes de subir otro.

---

## 📜 Bitácora

En la pestaña **Bitácora** queda el historial del recibo, de solo lectura, con lo más reciente primero: creación, cambios, cierre, anulación, impresión y adjuntos, con el usuario y la hora de cada evento.

![Bitácora del recibo](../recursos/img/recibos-egresos/24-bitacora.png)

---

## ⚠️ Mensajes de error frecuentes

| Mensaje | Qué significa | Qué hacer |
|---------|---------------|-----------|
| *Los pagos no suman el total; no se guardó nada.* | Los pagos no igualan el total de las líneas. | Revise los pagos y las facturas. Guarde de nuevo. |
| *Tercero inactivo.* | El cliente fue desactivado. | Elija otro cliente. |
| *Ese tipo de movimiento no está autorizado para tu usuario.* | Su usuario no puede usar ese tipo. | Elija otro tipo o pida el permiso a su administrador. |
| *Una de las facturas ya no es válida para este tercero (anulada, de otro tercero o de otra cartera).* | Una factura cambió después de elegirla. | Quite la línea, seleccione las facturas de nuevo y guarde. |
| *Ya hay un pago con la misma forma, banco y referencia.* | Hay dos pagos iguales. | Cambie la referencia o quite uno de los pagos. |
| *No se pudo asignar el número. Intenta de nuevo; si se repite, avisa al administrador.* | Falló la asignación del número. | Intente de nuevo. Si se repite, avise al administrador. |
| *Otro usuario modificó este documento. Revisa sus cambios antes de guardar.* | Otra persona cambió el recibo mientras usted lo editaba. | Haga clic en **Ver sus cambios**, revise, y vuelva a guardar sus cambios. |
| *El documento ya no se puede editar (cerrado, anulado o periodo cerrado).* | El recibo ya no es editable. | Recargue el recibo para ver su estado actual. |
| *Este documento no existe.* | El recibo ya no está disponible o no pertenece a esta compañía. | Vuelva al listado. |
| *No se pudo completar la acción. Reintenta.* | Error del servidor. No se guardó nada. | Haga clic en **Reintentar**. Si se repite, avise al administrador. |

![Descuadre al guardar](../recursos/img/recibos-egresos/25-error-descuadre.png)

![Periodo cerrado](../recursos/img/recibos-egresos/26-error-periodo-cerrado.png)

![Otro usuario modificó el recibo](../recursos/img/recibos-egresos/27-error-conflicto.png)

![Cliente con alerta de observaciones](../recursos/img/recibos-egresos/28-tercero-con-alerta.png)

---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica, cierra o anula recibos mientras usted tiene abierta esta pantalla, **no tiene que recargar**: el listado se pone al día solo, sin perder lo que buscó, el orden ni la página.

- Las filas nuevas o modificadas se **resaltan** unos segundos.
- Abajo a la derecha aparece un aviso con el nombre de quien hizo el cambio, por ejemplo *[nombre] creó el documento RC000000015.*
- Junto al título verá **En vivo** mientras la conexión esté activa. Si se interrumpe, dice **Reconectando…**; al volver, la pantalla se actualiza sola.

![Otro usuario crea un recibo](../recursos/img/recibos-egresos/29-tiempo-real-otro-crea.png)

**Si tiene abierto un recibo que otro usuario cambia:**

| Qué hizo el otro usuario | Qué verá | Qué puede hacer |
|--------------------------|----------|-----------------|
| Lo modificó | *Otro usuario modificó este documento. Revisa sus cambios antes de guardar.* | **Ver sus cambios** para cargar lo que guardó. Revise sus cambios antes de guardar los suyos. |
| Lo cerró | *Otro usuario cerró este documento mientras lo editabas.* | Revise el recibo: ya está cerrado y no se edita. |

![Otro usuario modificó el recibo abierto](../recursos/img/recibos-egresos/30-tiempo-real-otro-modifica.png)

> ℹ️ Los cambios que usted hace en esta misma pestaña no generan avisos.

---

## ❔ Ayuda en pantalla

El botón **?** abre este manual en un panel a la derecha. Puede dejarlo abierto mientras trabaja en el listado o en el recibo.

![Botón de ayuda junto al título](../recursos/img/recibos-egresos/31-ayuda-boton.png)

En un celular, la ayuda ocupa toda la pantalla y se cierra con la **✕**.

---

## ❓ Preguntas frecuentes

**¿Puedo eliminar un recibo?**
No. Anúlelo con un motivo: queda en el listado como **Anulado**, con su historia.

**¿Qué diferencia hay entre abierto y cerrado?**
El recibo abierto se puede editar y todavía no registró sus asientos contables. El recibo cerrado ya los registró y no se edita.

**¿Por qué no aparece el botón Cerrar transacción?**
Porque el recibo debe estar guardado, sin cambios pendientes, y su perfil necesita el permiso **Actualizar**. Guarde primero el recibo.

**¿Por qué no aparece Seleccionar facturas?**
Porque falta el **Cliente** o la **Fecha**. Elíjalos primero.

**¿Por qué el total sale negativo?**
Porque el cliente tiene saldo a favor y sus valores se restan del total. Los pagos se registran por el valor absoluto.

**¿Por qué no veo Nuevo documento, Imprimir o Anular?**
Su perfil no tiene ese permiso sobre la opción Recibos de caja y egresos. Consulte con el administrador de OrangeERP.

**¿Por qué no encuentro un recibo que sí existe?**
Revise que esté en la compañía correcta (título de la pestaña), que los filtros de fecha, tipo y estado no lo oculten, y borre el texto del buscador.

**¿Qué pasa si el número del recibo ya está usado?**
Si el tipo permite escribir el consecutivo, déjelo vacío para que se use el siguiente libre, o elija otro número.

**No veo "En vivo".**
La conexión en vivo no está disponible en este momento (por ejemplo, por la red de su empresa). La pantalla funciona igual; para ver cambios de otros usuarios, recargue la página.
