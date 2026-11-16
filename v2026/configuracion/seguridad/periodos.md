[Regresar a Configuración](../readme.md)

---

# 🗓️ Períodos

![Static Badge](https://img.shields.io/badge/Module-Configuracion-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Seguridad-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Periodos-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261116-yellow)

---

## 📋 Descripción

Los **períodos** definen **qué fechas admiten registrar documentos** en su compañía y **cierran la contabilidad de cada mes**.

Desde aquí usted puede:

- Crear, editar y eliminar períodos (estos últimos, solo si están abiertos y no tienen saldos).
- **Abrir o cerrar cada opción** del sistema (ventas, compras, recibos, notas, etc.) para cada período.
- **Cerrar un período**: OrangeERP calcula y guarda los saldos del mes y cierra sus opciones.
- **Reabrir un período**: OrangeERP elimina los saldos del mes para poder corregirlo.
- Ver el **historial** de cambios de cada período.

> ⚠️ Cerrar y reabrir afectan los saldos de su compañía. Lea la confirmación antes de aceptar: le dice qué saldos se calculan o se eliminan y qué opciones quedan cerradas.

> 📘 La búsqueda y el orden de la lista funcionan como en el resto de pantallas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 🕒 Si su compañía usa **cierre diario**, las opciones de los períodos **no restringen los documentos**. Ver [Compañías con cierre diario](#-compañías-con-cierre-diario).

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Configuración**.
2. En **Seguridad**, haga clic en **Períodos**.

Para ver la pantalla necesita el permiso **Consultar** de esta opción. Si su perfil no lo tiene, verá el mensaje **"No tienes permiso para ver los períodos"** y la pantalla no mostrará datos.

### Permisos

| Permiso | Qué le permite |
|---------|----------------|
| **Consultar** | Ver la lista, los avisos, la ficha de cada período y su historial. Los botones de cambio no aparecen; en la fila verá **Ver** en lugar de **Editar**. |
| **Crear** | Crear períodos con **Nuevo período**. |
| **Actualizar** | Editar fechas y descripción, abrir y cerrar opciones, **cerrar** y **reabrir** un período. |
| **Eliminar** | Eliminar períodos abiertos que no tengan saldos. |
| **Exportar** | Descargar la lista con el botón **Exportar a Excel**. |

> 💡 Cada acción exige su propio permiso. Si un botón no aparece, su perfil no tiene ese permiso; pida al administrador de la compañía que se lo asigne.

---

## 🖥️ Pantalla principal

![Lista de períodos con avisos](../recursos/img/periodos/01-listado.png)

En la parte superior verá:

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La lista se actualiza sola cuando otro usuario crea, cambia o cierra un período. Ver [Cambios en vivo](#-cambios-en-vivo). |
| **Ver cierres de saldos** | Lleva a la pantalla de [Cierres de saldos](cierres-saldos.md). |
| **Nuevo período** | Crea un período (requiere **Crear**). |

Debajo aparece un **resumen de la compañía**: **Períodos**, **Abiertos**, **Cerrados**, **Último cierre hasta** (la fecha final del último período cerrado) y **Avisos**.

### Avisos

Si hay algo que revisar, aparece un panel amarillo **"N avisos en los períodos de la compañía"**. Pulse **Ver detalle** para desplegar la lista; cada aviso tiene un enlace **Abrir** con el código del período.

| Aviso | Qué significa |
|-------|---------------|
| **Hueco** | Hay días sin ningún período entre dos períodos. Un documento con fecha en ese rango **se rechaza**. |
| **Solape** | Dos períodos comparten fechas. Con solape, el sistema puede tomar cualquiera de los dos para validar una fecha. |
| **Abierto antes de un cierre** | Un período abierto termina antes del último período cerrado. |
| **Cerrado con opciones abiertas** | Un período está cerrado pero todavía tiene opciones abiertas. Es una situación inconsistente. |
| **Mismo mes** | Dos períodos terminan en el mismo mes. Cerrar uno recalcula los saldos del mes completo y puede pisar los saldos del otro. |

Los avisos son informativos: **no bloquean ninguna acción**. Sirven para corregir la configuración antes de que afecte a los documentos o a los cierres.

### La lista

Cada fila es **un período** de la compañía en la que está trabajando.

| Columna | Qué muestra |
|---------|-------------|
| **Acciones** | Los botones de la fila (ver [Acciones de cada fila](#acciones-de-cada-fila)). |
| **Código** | Identificador corto del período, por ejemplo `JUL-26`. |
| **Descripción** | Texto que describe el período. |
| **Fecha inicial** y **Fecha final** | Rango de fechas del período (se muestran como día/mes/año). |
| **Estado** | **Abierto**, **Cerrado** o **Cerrado con opciones abiertas (inconsistente)**. |
| **Opciones abiertas** | Cuántas de las 13 opciones aceptan documentos, por ejemplo **4 de 13**. Los puntos debajo muestran el mismo dato de forma visual. |
| **Avisos** | Los avisos que afectan a esa fila, por ejemplo **Hueco antes** o **Solapa con NOV-26**. |
| **Última modificación** | Cuándo y quién lo cambió por última vez, en la zona horaria de la compañía. |

Para ordenar, pulse el encabezado de la columna. En la búsqueda puede escribir un código, una descripción o un estado; no importan las tildes ni las mayúsculas.

Si no hay períodos, verá **"Aún no hay períodos"**. Sin períodos no se pueden registrar documentos con fecha; cree el primero con **Nuevo período**.

### Acciones de cada fila

| Botón | Para qué sirve | Permiso |
|-------|----------------|---------|
| **Editar** (lápiz) | Abre la ficha para cambiar datos. Si solo tiene **Consultar**, el botón se llama **Ver**. | Actualizar |
| **Opciones** (engranaje) | Abre la ficha en la pestaña **Opciones**. | Actualizar |
| **Cerrar el período** (candado) | Aparece en los períodos abiertos. | Actualizar |
| **Reabrir el período** (candado abierto) | Aparece en los períodos cerrados. | Actualizar |
| **Eliminar** (papelera) | Aparece solo en períodos abiertos sin saldos. | Eliminar |

---

## ➕ Crear un período

1. Pulse **Nuevo período**.
2. Complete los datos:
   - **Código**: hasta 8 caracteres. Se guarda en mayúsculas.
   - **Descripción**: hasta 50 caracteres.
   - **Fecha inicial** y **Fecha final**: la final no puede ser anterior a la inicial.
3. Opcional: marque **Abrir todas las opciones al crear**.
4. Pulse **Guardar**.

![Crear un período](../recursos/img/periodos/03-crear.png)

Por defecto, el período **nace con todas las opciones cerradas**: no se podrá registrar ningún documento con fecha en él hasta que las abra. Si marca **Abrir todas las opciones al crear**, nace con todas abiertas (las opciones que correspondan).

Al guardar aparece **"Período JUL-26 creado."** y la fila nueva queda resaltada.

### Si el período se solapa con otro

Si las fechas se cruzan con un período existente, el sistema no lo guarda y le indica con cuál: **"Las fechas se cruzan con el período NOV-26. Ajusta el rango para que no se solapen."**

![Fechas que se solapan](../recursos/img/periodos/04-solape.png)

---

## ✏️ Editar un período

1. En la fila, pulse **Editar** (o **Opciones** para ir directamente a las opciones).
2. Cambie lo que necesite y pulse **Guardar**.

La ficha tiene tres pestañas:

| Pestaña | Contenido |
|---------|-----------|
| **Datos** | Código, descripción, fechas y la última modificación. |
| **Opciones** | Las 13 opciones con su estado. Ver [Abrir y cerrar opciones](#-abrir-y-cerrar-opciones). |
| **Historial** | Quién creó, modificó, abrió, cerró o reabrió el período y cuándo. Ver [Historial](#-historial). |

### Período cerrado

Un período cerrado **solo permite cambiar el código y la descripción**. Las fechas y las opciones aparecen deshabilitadas con la nota:

> **"El período está cerrado: solo puedes cambiar el código y la descripción. Reabre el período para cambiar las fechas y las opciones."**

![Editar un período cerrado](../recursos/img/periodos/05-editar-cerrado.png)

Para cambiar las fechas o las opciones de un período cerrado, primero **reábralo** (ver [Reabrir un período](#-reabrir-un-período)).

---

## 🔘 Abrir y cerrar opciones

En la pestaña **Opciones** de la ficha verá cada una de las 13 opciones con su estado **Abierta** o **Cerrada**. Cada opción muestra la opción de menú que gobierna (por ejemplo, **Venta**), para que sepa dónde se usa.

![Opciones de un período](../recursos/img/periodos/06-opciones.png)

| Opción | Qué documentos regula |
|--------|-----------------------|
| Entrada/Salida | Movimientos de inventario de entrada y salida. |
| Orden de compra | Órdenes de compra. |
| Compra/Devolución | Compras y devoluciones de compra. |
| Pedido | Pedidos de venta. |
| Venta | Ventas. |
| Recibo de caja/Egreso | Recibos de caja y de egreso. |
| Nota débito/crédito | Notas débito y crédito. |
| Solicitud de gasto | Solicitudes de gasto. |
| Causación de gasto | Causaciones de gasto. |
| Nota bancaria | Notas bancarias. |
| Asientos contables | Asientos contables. |
| Traslado | Traslados. |
| Punto de venta | Documentos del punto de venta. |

- **Cada interruptor aplica de inmediato**. No hay botón **Guardar** para las opciones.
- **Abrir todas** y **Cerrar todas** cambian las 13 de una vez.
- Si la opción no se puede cambiar, el interruptor vuelve a su valor anterior y aparece **"No se pudo cambiar la opción. Se restauró el valor anterior."**

Con el período abierto, puede abrir o cerrar opciones sin cerrar el período. Para **cerrar el período** no hace falta apagar antes las opciones: al cerrar, se cierran solas.

### Cerrado con opciones abiertas

Un período cerrado no debería tener opciones abiertas. Si lo tiene, la fila y la ficha lo marcan como **Cerrado con opciones abiertas (inconsistente)** y lo listan.

![Período cerrado con opciones abiertas](../recursos/img/periodos/07-cerrado-con-opciones-abiertas.png)

Para corregirlo, pulse **Cerrar las opciones abiertas**. Esta es la única acción permitida en un período cerrado: solo apaga opciones. Si prefiere, también puede reabrir el período y volver a cerrarlo.

---

## 🔒 Cerrar un período

Cerrar un período hace dos cosas:

1. **Calcula y guarda los saldos** del mes: de terceros, de cuentas contables y de centros de costo, acumulados hasta la fecha final del período.
2. **Cierra todas las opciones** que estaban abiertas.

Para cerrarlo:

1. En la fila del período abierto, pulse **Cerrar el período** o use **Cerrar período…** en la ficha.
2. Lea la confirmación.
3. Pulse **Cerrar período**.

![Confirmar el cierre](../recursos/img/periodos/08-confirmar-cerrar.png)

La confirmación le muestra:

- El **mes** cuyos saldos se calcularán y hasta qué fecha.
- Los tipos de saldos que se calcularán.
- Las **opciones que se cerrarán** (o "Ninguna opción está abierta").
- Que, después del cierre, **no se podrá registrar ninguna transacción con fecha dentro del período**.

Mientras el sistema calcula, el botón queda deshabilitado y aparece **"Calculando los saldos del mes. Puede tardar; no cierres esta ventana."**. Al terminar, verá **"Período JUL-26 cerrado: saldos calculados."**.

Si el cierre no se completa, **no se guarda ningún cambio** y el período sigue abierto. Verá **"El cierre no se completó y no se guardó ningún cambio. Inténtalo de nuevo; si persiste, avisa al administrador."**

### Mes compartido

Si otro período de la compañía termina en el mismo mes, la confirmación lo avisa:

![Cierre con mes compartido](../recursos/img/periodos/09-confirmar-cerrar-mes-compartido.png)

> **"Cerrar este recalcula los saldos del mes completo; si cierras también el otro, el último cierre pisa los saldos del anterior."**

Revise los períodos antes de cerrarlos. Si el otro período ya está cerrado, el sistema no permitirá el cierre (ver [Mensajes de error](#-mensajes-de-error-frecuentes)).

---

## 🔓 Reabrir un período

Reabrir sirve para corregir un período ya cerrado. Al reabrirlo:

- Se **eliminan los saldos del mes** (terceros, cuentas contables, centros de costo y saldos contables del período).
- **Las opciones quedan cerradas**. Usted las abre después, una por una o todas juntas.
- Los **saldos acumulados de los períodos posteriores no se recalculan**. Cuando termine, vuelva a cerrar el período.

Para reabrirlo:

1. En la fila del período cerrado, pulse **Reabrir el período** o use **Reabrir período…** en la ficha.
2. Lea la confirmación.
3. Pulse **Reabrir período** (botón rojo).

![Confirmar la reapertura](../recursos/img/periodos/10-confirmar-reabrir.png)

Al terminar verá **"Período JUL-26 reabierto: saldos eliminados. Sus opciones quedaron cerradas."**

> ⚠️ Reabra un período solo cuando sea necesario. Mientras esté reabierto, sus saldos no existen hasta que vuelva a cerrarlo.

---

## 🗑️ Eliminar un período

Solo se pueden eliminar períodos **abiertos y sin saldos asociados**.

1. En la fila, pulse **Eliminar** (papelera).
2. Lea la confirmación: muestra la descripción del período y que la eliminación es definitiva.
3. Pulse **Eliminar**.

Verá **"Período JUL-26 eliminado."**.

### Si no se puede eliminar

| Mensaje | Qué hacer |
|---------|-----------|
| **No se puede eliminar: el período tiene saldos contables asociados. Reábrelo si está cerrado para quitar sus saldos.** | Si está cerrado, reábralo; luego podrá eliminarlo. |
| **Un período cerrado no se puede eliminar.** | Reábralo primero y después elimínelo. |

---

## 📤 Exportar

Con el permiso **Exportar** aparece el botón **Exportar a Excel**. Descarga un archivo de Excel con las filas que ve en la lista, en el mismo orden y con el estado y las 13 opciones de cada período.

Si no ve el botón, su perfil no tiene el permiso **Exportar**.

---

## 📜 Historial

En la pestaña **Historial** de la ficha verá, de más reciente a más antigua:

| Columna | Qué muestra |
|---------|-------------|
| **Fecha y hora** | Cuándo ocurrió, en la zona horaria de la compañía. |
| **Usuario** | Quién lo hizo. |
| **Acción** | **Creó el período**, **Modificó el período**, **Abrió opciones**, **Cerró opciones**, **Cerró el período** o **Reabrió el período**. |
| **Detalle** | Información adicional de la acción. |
| **Resultado** | **Completado** o **Con error**. |

![Historial de un período](../recursos/img/periodos/11-historial.png)

Si el período nunca ha cambiado, verá **"Sin movimientos registrados"**.

### Historial pendiente de activar

Mientras el administrador de la base de datos no active el índice de historial, la pestaña muestra **"Historial detallado pendiente de activar"**. Los cambios se registran igual; lo que no aparece es la lista detallada. Mientras tanto, verá la **última modificación** (usuario, fecha y hora).

---

## 🔄 Cambios en vivo

Mientras la pantalla está abierta y el indicador dice **En vivo**, la lista se actualiza sola cuando otro usuario:

- crea un período (**"Otro usuario creó el período JUL-26."**),
- cierra un período (**"Otro usuario cerró el período JUL-26."**),
- reabre un período (**"Otro usuario reabrió el período JUL-26."**).

La fila cambiada se resalta unos segundos y su búsqueda y su orden se conservan.

### Si tiene una ficha o una confirmación abiertas

Si tiene abierta la ficha o la confirmación de un período que otro usuario cambió, **la pantalla no se cierra sola**. Verá un aviso:

> **"Otro usuario cambió este período mientras lo tenías abierto. Si guardas sin recargar, el servidor lo rechazará."**

Pulse **Ver sus cambios** para recargar. En una confirmación de cerrar o reabrir, el botón queda deshabilitado hasta que recargue.

![Conflicto por cambios de otro usuario](../recursos/img/periodos/12-conflicto-modificado.png)

Si el otro usuario elimina el período, el aviso lo indica y el botón **Guardar** se deshabilita.

Si el indicador dice **Reconectando…**, la conexión se interrumpió; al recuperarse, la lista se recarga sola.

---

## ❗ Mensajes de error frecuentes

| Mensaje | Qué hacer |
|---------|-----------|
| **Otro usuario modificó este período. Recarga para ver su estado actual antes de continuar.** | Pulse **Ver sus cambios**, revise el período y repita la acción si todavía corresponde. |
| **El período ya estaba cerrado (otro usuario lo cerró). Recarga para ver su estado actual.** | No es necesario cerrarlo otra vez. Recargue la lista. |
| **El período ya estaba abierto (otro usuario lo reabrió). Recarga para ver su estado actual.** | No es necesario reabrirlo. Recargue la lista. |
| **Ya existe un período con el código JUL-26.** | Use otro código. No distingue mayúsculas de minúsculas. |
| **Las fechas se cruzan con el período NOV-26.** | Ajuste el rango para que no se solape con otro período. |
| **La fecha final no puede ser anterior a la inicial.** | Corrija las fechas. |
| **El código admite hasta 8 caracteres.** / **La descripción admite hasta 50 caracteres.** | Acorte el texto. |
| **No se puede cerrar: NOV-26 ya está cerrado y comparte el mes 2026-11; cerrar este pisaría sus saldos. Reabre NOV-26 primero.** | Reabra primero el otro período que comparte el mes. |
| **El período está cerrado: reábrelo para cambiar sus fechas, sus opciones o eliminarlo.** | Reabra el período para hacer el cambio. |
| **No se pudo completar la acción. No se guardó ningún cambio; inténtalo de nuevo.** | Vuelva a intentarlo. Si persiste, avise al administrador. |
| **El cierre tardó más de lo permitido. Revisa el estado del período antes de reintentar.** | Revise si el período quedó cerrado antes de volver a intentarlo. |
| **No tienes permiso para ver los períodos.** | Pida al administrador de la compañía el permiso **Consultar** de la opción. |

---

## 🏢 Compañías con cierre diario

Si su compañía usa **cierre diario**, verá el aviso **"Esta compañía usa cierre diario"**. En ese caso:

- Las opciones de los períodos **no restringen los documentos**; se guardan igual, pero no bloquean nada.
- Puede seguir creando, editando, cerrando y reabriendo períodos, y revisando los avisos.

![Compañía con cierre diario](../recursos/img/periodos/02-cierre-diario.png)

---

## ❓ Preguntas frecuentes

**¿Por qué un documento con fecha de un período me lo rechaza?**
La fecha cae en un hueco (sin período) o en un período cerrado, o la opción correspondiente está cerrada. Revise la lista: el aviso **Hueco** indica el rango afectado.

**¿Qué es "Cerrado con opciones abiertas"?**
Es una situación inconsistente: el período está cerrado, pero algunas opciones siguen abiertas. Pulse **Cerrar las opciones abiertas** en la pestaña **Opciones**.

**¿Puedo cerrar un período cuya fecha final todavía no ha llegado?**
Sí, por defecto el sistema lo permite. Tenga en cuenta que los documentos posteriores a la fecha final seguirán sin período hasta que lo cree.

**¿Cerrar un período es reversible?**
Sí. Al reabrirlo se eliminan los saldos del mes y se cierran sus opciones. Luego puede volver a cerrarlo. Los saldos acumulados de los períodos posteriores no se recalculan automáticamente.

**¿Por qué el cierre tarda?**
Calcular los saldos de toda la compañía puede tardar unos minutos. No cierre la ventana mientras aparece **"Calculando los saldos del mes"**.

**¿Por qué no puedo editar las fechas de un período?**
Porque está cerrado. Reábralo para cambiar las fechas y las opciones.

**¿Qué pasa si dos usuarios cierran el mismo período a la vez?**
Solo uno lo consigue. El otro recibe **"El período ya estaba cerrado (otro usuario lo cerró)"** y la lista se actualiza.

**¿Por qué no veo los botones de cambio?**
Su perfil tiene solo el permiso **Consultar**. Para crear, editar, cerrar o reabrir necesita los permisos correspondientes (ver [Permisos](#permisos)).

**¿Dónde veo los cierres de saldos?**
Desde el botón **Ver cierres de saldos** de esta pantalla. Ahí verá el estado de los saldos que se guardan al cerrar cada período: ver [Cierres de saldos](cierres-saldos.md).

**¿Qué diferencia hay con [Usuarios conectados](usuarios-conectados.md)?**
Esa pantalla muestra quién está conectado. Esta muestra los períodos contables de la compañía.
