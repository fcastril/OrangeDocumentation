[Regresar a Contabilidad](readme.md)

---

# ASIENTOS CONTABLES

> **Estado de esta pantalla.** Esta opción todavía no está activa en el menú. Mientras no se habilite, el guardado de asientos está deshabilitado: si intenta guardar, la pantalla muestra **Servicio no disponible ahora** y le dice que **no se guardó nada**. Cuando el administrador la habilite, podrá crear, editar y cerrar asientos como se describe aquí. Los **documentos adjuntos** todavía no están disponibles en esta pantalla.

## Qué es

Los **asientos contables** son los comprobantes manuales de la compañía. Cada asiento tiene un encabezado (tipo de movimiento, consecutivo, fecha, documento de referencia y observaciones) y varias **líneas** de débito o crédito, cada una con su cuenta contable.

Desde aquí consulta el listado de asientos, ve el detalle de cada uno, crea y edita asientos, los cierra cuando cuadran, los elimina si todavía están abiertos e imprime el comprobante.

## Cómo llegar

- Abra **Contabilidad** en el menú principal y luego **Movimientos > Asientos contables**.
- Necesita permiso de **Consultar** sobre Asientos contables. Si no ve la opción, pida a su administrador que se lo asigne.

Si abre la dirección de una pantalla de asiento sin permiso de consulta, la pantalla lo lleva de vuelta al inicio del módulo.

## Pantalla principal (listado)

![Listado de asientos contables](recursos/img/asientos/01-listado.png)

El listado muestra una fila por asiento, con estas columnas:

- **Tipo de Movimiento**: el código del tipo. Al pasar el cursor se ve el código y el nombre.
- **Consecutivo** y **Prefijo**.
- **Fecha**.
- **Ref. doc.**: el documento de referencia del asiento.
- **Débitos** y **Créditos**: el total de cada lado.
- **Estado**: **Abierta**, **Cerrada** o **Anulada**.
- **Acciones**: los botones de cada fila (ver [Permisos](#lo-que-ve-segun-sus-permisos)).

Lo que ve depende de sus permisos:

- **Consultar**: ve el listado y el detalle. No ve los botones de crear, editar ni eliminar.
- **Crear**: ve el botón **Crear asiento contable**.
- **Actualizar**: puede abrir un asiento abierto y cambiarlo. Para un asiento cerrado necesita, además, el permiso de editar documentos cerrados.
- **Eliminar**: puede eliminar asientos abiertos.
- **Imprimir**: ve el botón **Imprimir** en las filas que pueden imprimirse.

Si no hay asientos, la pantalla muestra **Aún no hay asientos contables**. Si la búsqueda no encuentra nada, muestra **Sin resultados**. Si el listado no carga, aparece **No se pudo cargar el listado** con **Reintentar**; su búsqueda se conserva.

### Lo que ve según sus permisos

| Botón de la fila | Cuándo aparece |
|---|---|
| **Ver detalle del asiento** | Siempre. |
| **Imprimir el asiento** | Con permiso de imprimir, en los asientos que no están anulados. |
| **Editar el asiento** | Con permiso de actualizar, en un asiento abierto cuyo período está abierto. |
| **Editar el asiento cerrado** | Igual que el anterior, y además con el permiso de editar documentos cerrados. |
| **Eliminar el asiento** | Con permiso de eliminar, en un asiento abierto cuyo período está abierto, y que no sea de cierre anual. |

Un asiento **Anulado** solo permite ver el detalle.

## Buscar

- Escriba en el buscador por tipo, consecutivo, prefijo o documento, y pulse **Enter**. La búsqueda se hace en el servidor.
- Escriba **descuadrados** para ver solo los asientos abiertos que tienen diferencia entre débitos y créditos.
- Los asientos aparecen del más reciente al más antiguo.

## Indicadores

Junto al estado de cada asiento puede aparecer:

- **Descuadrado** (rojo): la suma de los débitos no es igual a la suma de los créditos. Es común en asientos antiguos que se cargaron sin cuadrar. Puede verlos tal como están.
- **Sin líneas**: el asiento no tiene líneas. Un asiento cerrado sin líneas solo se puede consultar.
- **Cierre anual**: el asiento lo genera el cierre del año. No se puede crear, editar, eliminar ni importar desde esta pantalla; solo se consulta.

## Ver el detalle de un asiento

1. Pulse **Ver detalle del asiento** en la fila.
2. Se abre **Detalles Asientos Contables**, con el tipo, el consecutivo y la fecha en el título.
3. La tabla **Líneas del asiento** muestra, por cada línea, el **Cod. Plan Cta.**, el **Plan de Cuenta**, los **Débitos**, los **Créditos** y la **Base tributaria** (vacía cuando es cero).
4. El bloque **Resumen Totales** muestra la suma de débitos y de créditos. Si hay diferencia, aparece **Documento Descuadrado - Diferencia** con el valor.

Si el asiento ya no existe o no es de su compañía, la pantalla dice **El asiento ya no existe o no es de esta compañía.**

## Crear un asiento

1. Pulse **Crear asiento contable**.
2. Complete el encabezado:
   - **Tipo de movimiento**: solo aparecen los tipos de asiento autorizados para su usuario. Los tipos de cierre anual no se ofrecen.
   - **Prefijo**: lo fija el tipo. No se puede cambiar.
   - **Consecutivo**: se asigna solo al guardar. La pantalla muestra un número esperado, pero es informativo. Solo puede escribirlo si el tipo lo permite; si no, la pantalla le pide dejarlo vacío.
   - **Documento Referencia**: si lo deja vacío, se guarda el código del tipo y el consecutivo.
   - **Fecha**: debe caer en un período abierto (ver [Período](#periodo-informativo)).
   - **Observaciones**: hasta 200 caracteres. Las comas y los punto y coma se quitan al guardar.
3. Agregue las líneas (ver la siguiente sección).
4. Pulse **Guardar**.

Al guardar, la pantalla muestra **Asiento guardado. Consecutivo {número} · Documento de referencia {documento}.** El asiento queda **Abierta**.

El guardado es **todo o nada**: si una línea falla, no queda ninguna fila nueva, ni encabezado, ni líneas, y el consecutivo no se gasta. La pantalla le indica la línea y el campo que debe corregir.

Un asiento necesita al menos una línea. Si guarda sin líneas, la pantalla le pide agregar una.

### Las líneas

Para cada línea, complete:

- **Cuenta Contable**: solo cuentas de movimiento de su compañía. Las cuentas de mayor no reciben registros; si elige una, la pantalla lo indica.
- **Tercero**: escriba el documento del tercero (NIT o cédula). Debe existir y estar activo. Si el tercero tiene una observación de alerta, la pantalla la muestra.
- **Centro de Costos**: centro de costos de su compañía.
- **Documento Referencia**: hasta 20 caracteres.
- **Detalle**: hasta 100 caracteres. Las comas y los punto y coma se quitan al guardar.
- **Débitos** o **Créditos**: escriba un valor en uno solo de los dos. No pueden ser los dos mayores que cero, ni los dos cero, ni negativos.
- **Base Tributaria**: solo si la cuenta la maneja. Puede escribir la base a mano (cero es válido) o pulsar **Calcular base tributaria**.

Los campos que la cuenta no maneja aparecen deshabilitados, con el texto que lo explica: **La cuenta no maneja tercero.**, **La cuenta no maneja centro de costos.**, **La cuenta no maneja documento de referencia.** o **La cuenta no maneja base tributaria.**

Lo que exige cada cuenta:

- **Tercero**: si la cuenta lo pide, debe elegir el tercero. La pantalla dice **Elige el tercero que pide la cuenta.**
- **Centro de Costos**: si la cuenta lo pide, debe elegir el centro. La pantalla dice **Elige el centro de costos que pide la cuenta.**
- **Documento de referencia**: si la cuenta lo pide, debe escribirlo. La pantalla dice **Escribe el documento de referencia que pide la cuenta.**
- **Base tributaria**: si la cuenta la maneja, debe escribirla (0 es válido).

**Calcular base tributaria** propone la base como el valor absoluto de **débito menos crédito**, multiplicado por el porcentaje de la cuenta y redondeado a los decimales del tipo. La base propuesta puede editarla. Si la línea no tiene débito ni crédito, la pantalla pide escribir uno de los dos.

Para agregar la línea, pulse **Agregar Detalle**. Las líneas se guardan junto con el asiento al pulsar **Guardar**.

- Para cambiar una línea agregada, pulse **Modificar la línea {n}**, cambie los datos y pulse **Actualizar línea**. Para salir sin cambios, pulse **Cancelar edición**.
- Para quitar una línea, pulse **Quitar la línea {n}**. La pantalla dice **Línea {n} quitada. Se aplicará al guardar.** Hasta que guarde, la línea sigue en el asiento.
- **Limpiar Detalle** vacía los campos de la línea que está escribiendo.

Un asiento tiene un máximo de líneas. Si llega al máximo, la pantalla lo indica y no permite agregar más. Un documento con más líneas que el máximo solo se puede consultar.

### Cuadre

La franja **Totales del asiento** muestra **Total débitos**, **Total créditos** y **Total diferencia**. Cuando débitos y créditos son iguales, dice **Cuadrado**; si no, **Descuadrado**.

- Un asiento **abierto** se puede guardar descuadrado, para seguir trabajándolo después.
- Para **cerrar** el asiento, débitos y créditos deben ser iguales. Si no lo son, no se cierra (ver [Cerrar un asiento](#cerrar-un-asiento)).

## Editar un asiento

1. En el listado, pulse **Editar el asiento {número}**.
2. Cambie el encabezado o las líneas y pulse **Guardar**.

Reglas:

- **Asiento abierto**: se puede editar mientras el período esté abierto.
- **Asiento cerrado**: solo se edita con el permiso de **editar documentos cerrados**. La pantalla lo indica con **Este asiento está cerrado. Solo puede corregirse con el permiso de edición de documentos cerrados y debe terminar cuadrado.** El asiento sigue cerrado después de editarlo, y debe quedar cuadrado. Si no tiene ese permiso, la pantalla dice **Este asiento está cerrado: no se puede modificar.**
- **Período cerrado**: el asiento solo se consulta. La pantalla dice **El período de este asiento está cerrado: no se puede editar ni eliminar.**
- **Asiento anulado**: solo se consulta.
- **Asiento de cierre anual**: solo se consulta.

Si no tiene permiso para editar, la pantalla dice **No tienes permiso para editar asientos: se muestra solo para consulta.**

Para eliminar una línea suelta no hay una acción aparte: quítela y guarde el asiento.

## Cerrar un asiento

Cerrar un asiento significa darlo por terminado. Un asiento cerrado **no admite más modificaciones** (salvo con el permiso de documentos cerrados).

1. Guarde los cambios pendientes. La pantalla pide **Guarde los cambios antes de cerrar.** si hay cambios sin guardar.
2. Pulse **Cerrar Transacción**.
3. Confirme en el cuadro **Cerrar Transacción**: "¿Confirma que desea cerrar la transacción? No podrá hacer más modificaciones."

Para cerrar necesita el permiso de **Crear** o de **Actualizar**.

Reglas al cerrar:

- El asiento debe tener al menos una línea. Si no tiene, la pantalla dice **Agregue al menos una línea antes de cerrar.**
- Débitos y créditos deben ser iguales. Si no, aparece **Error al cerrar Transacción** con el mensaje: *La sumatoria de "Débitos" y "Créditos" debe ser igual a 0 para poder realizar la operación*. El asiento no se cierra.
- Si el asiento ya está cerrado, la pantalla lo indica.

Cuando el cierre funciona, la pantalla dice **Transacción cerrada. Ya no admite modificaciones.** Ya no puede agregar ni quitar líneas, y los campos quedan deshabilitados. Desde allí puede **Imprimir**, **Regresar** o pulsar **Siguiente** para crear otro asiento.

## Eliminar un asiento

Solo se puede eliminar un asiento **abierto**. Desde el listado, pulse **Eliminar el asiento {número}** y confirme en **Eliminar registro**: "¿Está seguro de eliminar este registro? No podrá recuperarlo. Se eliminan el encabezado, las líneas y los adjuntos del asiento {número}."

Para eliminar, deben cumplirse todas estas condiciones:

- Tiene permiso de **Eliminar**.
- El asiento está **abierto** (no cerrado ni anulado).
- El período de la fecha está abierto.
- No es de cierre anual.
- No tiene otros registros que dependan de él.

Si el sistema no lo permite, la pantalla dice **No se eliminó el asiento** y el motivo:

- **Este asiento no se puede eliminar (anulado, en período cerrado o no modificable).**
- **Otros registros dependen de este asiento. Motivo: {motivo}. No se eliminó nada.**

Si se elimina, la pantalla dice **Registro eliminado correctamente.** Se borran el encabezado, las líneas y los adjuntos. No hay forma de recuperarlo.

## Imprimir

- Pulse **Imprimir** en la fila del listado, o en la ficha de un asiento cerrado.
- Se abre el **Comprobante contable** en PDF, tamaño carta. Incluye los datos de la compañía, el tipo, el prefijo, el consecutivo, la referencia, la fecha, las observaciones, las líneas con sus totales, y quién elaboró y quién imprime.
- Un asiento **anulado** no se imprime. La pantalla dice **Un asiento anulado no se imprime.**
- Si el PDF no se puede generar, la pantalla dice **No se pudo generar el PDF. Inténtalo de nuevo.**

Cada impresión queda registrada: el sistema guarda quién imprimió y cuántas veces.

## Período informativo

Al elegir la fecha, la pantalla consulta el período de esa fecha:

- **Período abierto para asientos contables.**: puede guardar.
- **No existe ningún Periodo abierto para la fecha indicada.** o **No se ha creado ningún Periodo para la fecha indicada.**: no puede guardar con esa fecha.

Este aviso es solo informativo. Al guardar, el sistema revisa el período otra vez.

## Cambios de otros usuarios

Esta pantalla **no se actualiza sola**. Si otro usuario cambia un asiento mientras usted lo tiene abierto, no lo verá hasta recargar la pantalla.

Cuando intenta guardar, puede aparecer:

- **Otro usuario modificó este asiento después de que lo abriste. Recarga para ver los cambios.** Nada se guardó. Pulse **Recargar el asiento**: la pantalla vuelve a leerlo y descarta lo que digitó. Revise los cambios y vuelva a hacerlos si todavía aplican.
- **Otro usuario tomó ese consecutivo. No se guardó nada: vuelva a guardar para recibir el siguiente.** Pulse **Reintentar el guardado** o vuelva a guardar. El sistema asigna el siguiente número.
- **Otro usuario está guardando asientos de este tipo. Espera unos segundos y reintenta.** Nada se guardó. Espere unos segundos y pulse **Reintentar el guardado**.

## Qué hacer si el resultado no está claro

- **Sin respuesta del servidor** (*No hubo respuesta del servidor. No sabemos si se guardó*): pulse **Reintentar el guardado**. Es seguro: si el asiento ya se había guardado, el sistema devuelve el mismo asiento y no duplica las líneas.
- **Resultado incierto** (*No se sabe si el asiento quedó escrito. No reintentes*): **no vuelva a guardar**. Revise el listado y busque el tipo y el consecutivo que indica la pantalla. Si el asiento aparece, ya está guardado. Si tiene dudas, consulte con el administrador antes de volver a guardar.
- **No se guardó el asiento** con el mensaje **Se deshizo todo: no quedó ninguna fila ni se gastó consecutivo**: el asiento no existe. Corrija lo que indica la pantalla y guarde otra vez. El código de seguimiento que aparece sirve para que soporte lo revise.
- **Servicio no disponible ahora** (escritura desactivada): nada se guardó. Espere a que el administrador habilite la escritura o avise a soporte.

Si la pantalla no carga, pulse **Reintentar**. Su búsqueda se conserva.

## Preguntas frecuentes

**¿Por qué no me deja guardar un asiento?**
Revise el mensaje. Lo más común es que el período de la fecha esté cerrado, que las líneas no cuadren (cuando quiera cerrar), o que la cuenta exija un tercero, un centro de costos, un documento de referencia o una base.

**¿Puedo guardar un asiento descuadrado?**
Sí, mientras esté abierto. Para cerrarlo tiene que cuadrar.

**¿Por qué no veo el botón Eliminar?**
Porque el asiento está cerrado, anulado, en un período cerrado, es de cierre anual, o su usuario no tiene el permiso de eliminar.

**¿Puedo cambiar el consecutivo?**
Solo si el tipo de movimiento lo permite. Si no, déjelo vacío y el sistema lo asigna al guardar.

**¿Qué significa "Descuadrado" en el listado?**
Que la suma de los débitos no es igual a la suma de los créditos de las líneas. Puede verlo en el detalle, con la diferencia.

**¿Por qué un asiento aparece como "Cierre anual"?**
Lo genera el cierre del año. Solo puede consultarlo.

**¿Cómo subo un archivo al asiento?**
Los documentos adjuntos todavía no están disponibles en esta pantalla.

**¿Cómo cargo muchos asientos a la vez?**
Use la importación desde Excel: [Importar asientos contables](asientos-importar.md).
