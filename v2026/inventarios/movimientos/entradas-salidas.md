[Regresar a Inventarios](../readme.md)

---

# 🔁 Entradas y salidas

![Static Badge](https://img.shields.io/badge/Tipo-Movimiento-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Entradas%20y%20salidas-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261007-yellow)

---

## 📋 Descripción

Los **movimientos de inventario** son los documentos con los que entra o sale mercancía de las bodegas sin pasar por compras ni ventas: ajustes por conteo, consumos internos, traslados, devoluciones, dotación, etc. Cada documento tiene un **tipo** (por ejemplo *EI - Entrada por ajuste* o *SI - Salida por consumo*), un **encabezado** (fecha, tercero, observaciones) y sus **líneas** (qué referencia, en qué bodega, cuántas unidades y a qué valor).

Lo más importante de esta pantalla: **cada línea se guarda en el momento en que la confirma** y actualiza de inmediato las existencias y la contabilidad. No hay un botón "Guardar documento": lo que ve como *Guardada* ya quedó registrado.

En esta pantalla puede **buscar, filtrar, consultar, crear, duplicar, cerrar, anular, eliminar, imprimir, exportar e importar** los movimientos de la compañía con la que está trabajando.

> 📘 El orden, la paginación y la ayuda funcionan como en las demás tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Cada pestaña del navegador trabaja con **una compañía**. El nombre de la compañía se ve en la barra superior.


---

## 🎯 Acceso

1. En el menú principal, haga clic en **Inventarios**.
2. En **Movimientos**, haga clic en **Entradas y salidas**.

---

## 🖥️ Pantalla principal

![Listado de entradas y salidas](../recursos/img/movimientos/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La pantalla está conectada: los documentos que crean o cambian otros usuarios aparecen solos. Ver *Cambios de otros usuarios*. |
| **Nuevo movimiento** | Abre un documento nuevo. Ver *Crear un movimiento*. |
| **Documentos**, **Entradas**, **Salidas**, **Neto** | Resumen de **todo lo que cumple los filtros** (no solo de la página). Ver *Filtrar el listado y leer el resumen*. |
| **Desde**, **Hasta**, **Tipo de movimiento**, **Bodega**, **Tercero**, **Estado**, **Número** | Filtros del listado. |
| **Documentos eliminados** | Solo para administradores de la compañía (próxima entrega). Ver *Bitácora*. |
| **Buscar por tipo, doc. referencia o tercero** | Busca mientras escribe, a partir de 2 caracteres. |
| **Exportar a Excel** | Descarga los documentos que cumplen la búsqueda y los filtros. |
| **N registros** | Cuántos documentos cumplen la búsqueda y los filtros. |
| **Iconos de la primera columna** | **Lápiz** (editar) u **ojo** (ver), **Duplicar**, **Imprimir**, **Anular** y **Papelera** (eliminar). Solo aparecen las acciones que usted puede hacer sobre **ese** documento. |
| **Columnas** | Tipo, Consecutivo, Fecha, Doc. referencia, Tercero, Cantidad, Valor, Estado y Última modificación. Puede ordenar por cualquiera haciendo clic en el encabezado. Las salidas se muestran con signo **−**. |

Cada documento está en uno de estos **estados**:

| Estado | Qué significa |
|--------|---------------|
| **Abierto** | Se le pueden agregar, cambiar y quitar líneas. |
| **Cerrado** | Ya no se modifica (salvo con el permiso especial *editar documentos cerrados*). |
| **Anulado** | Se conserva como rastro, pero **no afecta** existencias ni costos. |
| **Periodo cerrado** (marca adicional) | La fecha del documento cae en un periodo contable cerrado: solo se puede consultar. |

> 📱 En el celular cada documento se muestra como una tarjeta y los filtros se apilan.

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil sobre la opción *Entradas y salidas* y del estado del documento:

| Permiso | Qué habilita |
|---------|--------------|
| Consultar | Ver el listado, el resumen y abrir los documentos en solo lectura |
| Crear | **Nuevo movimiento** y **Duplicar** |
| Actualizar | Agregar, cambiar y quitar líneas, cambiar el encabezado y **Cerrar transacción** en documentos abiertos |
| Anular | **Anular** |
| Eliminar | **Eliminar** |
| Imprimir | **Imprimir** |
| Exportar | **Exportar a Excel** (listado y líneas del documento) |
| Editar documentos cerrados (permiso especial del usuario) | **Editar cerrado** |
| Administrador de la compañía | Pestaña **Bitácora** y **Documentos eliminados** |

Además, los **tipos de movimiento** que ve y puede usar son los que su usuario tiene autorizados.

---

## 🧰 Filtrar el listado y leer el resumen

| Filtro | Qué hace | Por defecto |
|--------|----------|-------------|
| **Desde** / **Hasta** | Rango de fechas de los documentos. Máximo **92 días**. | El mes en curso |
| **Tipo de movimiento** | Un tipo, elegido en el buscador | Todos los tipos |
| **Bodega** | Documentos con movimiento en esa bodega | Todas las bodegas |
| **Tercero** | Documentos de ese tercero (busque por documento o nombre) | Todos los terceros |
| **Estado** | Abierto, Cerrado y/o Anulado (puede elegir varios) | Todos |
| **Número** | Consecutivo o doc. referencia | — |

- Los filtros se combinan entre sí y con la búsqueda. Al cambiar uno, el listado vuelve a la página 1.
- **Limpiar filtros** los deja como al abrir la pantalla.
- Si **Desde** es posterior a **Hasta**, verá *"La fecha inicial no puede ser posterior a la final"* y no se consulta nada hasta corregirlo.
- Los filtros quedan en la dirección de la página: si la copia y la comparte, la otra persona ve el mismo listado.

El **resumen** (las cuatro tarjetas de arriba) se calcula con **todos** los documentos que cumplen los filtros:

| Tarjeta | Qué muestra |
|---------|-------------|
| **Documentos** | Cuántos hay y, debajo, cuántos están cerrados, abiertos y anulados |
| **Entradas** | Unidades que entraron y, debajo, su valor |
| **Salidas** | Unidades que salieron (con signo −) y su valor |
| **Neto** | Entradas menos salidas, su valor y el número de líneas |

> ℹ️ Los documentos **anulados** se cuentan en *Documentos*, pero **no suman** unidades ni valores.

Si el resumen no se puede calcular, verá *"No se pudo calcular el resumen"* con **Reintentar**; el listado sigue funcionando.

---

## 📤 Exportar a Excel

Haga clic en **Exportar a Excel**. Se descarga `movimientos-inventario_DESDE_HASTA.xlsx` con **todos** los documentos que cumplen la búsqueda y los filtros (no solo la página visible), con las mismas columnas del listado, y verá *"Se descargó … con N documentos."*

> ⚠️ Se exportan hasta **50.000 documentos**. Si el filtro da más, verá *"El filtro tiene más de 50.000 documentos. Acote las fechas u otros filtros para exportar."* y no se descarga nada.

Dentro de un documento cerrado o anulado, la tabla de líneas tiene su propio botón para exportar las líneas de ese documento.

---

## 📥 Importar entradas y salidas desde Excel

Crea **varios documentos nuevos de una sola vez** a partir de una hoja de Excel: cada fila es una línea y las filas con la misma **Clave de documento** forman un documento. Antes de guardar, el sistema le muestra qué documentos va a crear y qué filas tienen errores. **Nada se guarda hasta que usted aplica.**

> 🔐 Necesita los permisos **Crear** y **Exportar** sobre Entradas y salidas, y estar autorizado para los tipos de movimiento que importe. Con ambos permisos verá el botón **Importar**, junto a **Exportar a Excel**; si falta alguno, el botón no aparece. Los **traslados** no se importan aquí.

La importación **solo crea documentos nuevos**: nunca modifica ni borra los existentes.

### Los tres pasos: Cargar archivo → Revisar → Resultado

![Importar: cargar archivo](../recursos/img/movimientos/24-importar-cargar.png)

**1. Cargar archivo.** Descargue la **plantilla vacía** (hoja **Movimientos** con 18 columnas) o **Exportar para reimportar** (sus documentos actuales, sin anulados y con el filtro del listado, en el mismo formato; hasta 200 documentos y 5.000 líneas). Arrastre el archivo `.xlsx` al recuadro o elíjalo. Con **Cancelar** (o **Volver al listado**) regresa sin importar nada.

> 💡 Un archivo exportado para reimportar **crea documentos nuevos** con otro consecutivo; no actualiza los que ya existen.

### La hoja Movimientos: 18 columnas

El orden de las columnas no importa (se leen por su nombre) y las columnas desconocidas se ignoran. Las marcadas con * son obligatorias.

| Parte | Columna | Qué escribir |
|-------|---------|--------------|
| Encabezado (igual en todas las filas del documento) | **Clave de documento*** | Texto de hasta 20 caracteres, sin comas ni punto y coma. Solo agrupa las filas: no se guarda. |
| | **Código tipo de movimiento*** | Por ejemplo `EI` o `SI`. |
| | **Fecha*** | Fecha de Excel o `aaaa-mm-dd`. |
| | **Documento tercero*** | NIT o cédula de un tercero activo. |
| | **Documento referencia** | Hasta 20 caracteres. |
| | **Observaciones** | Hasta 200 caracteres (se quitan comas y punto y coma). |
| Línea | **Código referencia**, **Código atributo principal**, **Código atributo secundario** | La variante por sus códigos (atributos vacíos si la referencia no los usa). |
| | **Código de barras** | La variante por su código de barras (EAN13, EAN8 o código alterno). |
| | **Código bodega*** | Código de la bodega. |
| | **Código ubicación** | Opcional. |
| | **Código centro de costos** | Obligatorio si el tipo lo exige. |
| | **Número OP** | Obligatorio si el tipo exige orden de producción. |
| | **Lote** | Hasta 20 caracteres; obligatorio si la referencia exige lote. |
| | **Detalle** | Hasta 200 caracteres. |
| | **Cantidad*** | Mayor que 0, hasta 4 decimales. |
| | **Valor unitario*** | Mayor que 0. |

**Reglas importantes**

| Regla | Detalle |
|-------|---------|
| **Un archivo, varios documentos** | Cada **Clave de documento** distinta es un documento nuevo. El consecutivo lo asigna el sistema (no hay columna). |
| **Encabezado igual** | Tipo, fecha, tercero, documento de referencia y observaciones deben ser iguales en todas las filas del documento; si una difiere, el documento completo queda con error. |
| **La variante, de una sola forma** | Por referencia + atributos **o** por código de barras; nunca las dos, y al menos una. Solo variantes activas, de referencias con inventario. |
| **Líneas iguales** | Las líneas iguales (variante, bodega, ubicación y lote) se suman en una sola, como en la captura; en la revisión verá *"Se suma a la fila N"*. |
| **Abiertos** | Los documentos se crean **Abiertos**: no se cierran ni se contabilizan solos. Ciérrelos desde el listado cuando corresponda. |
| **No se importan** | Fecha de vencimiento, criterios de aceptación, estado, cierre ni anulación. |

**Límites**

| Límite | Valor |
|--------|-------|
| Archivo | `.xlsx`, hasta **5 MB**, hoja **Movimientos** |
| Para **revisar** (vista previa) | Hasta **200 documentos y 5.000 líneas** |
| Para **aplicar** | Hasta **200 documentos y 5.000 líneas** por archivo, igual que la revisión. La aplicación corre en segundo plano; el tiempo que toma con archivos grandes aún está por medir en el ambiente de pruebas |

Si el archivo no sirve verá **"El archivo no se puede importar"** con el motivo y no se envía nada: no es un `.xlsx`, no tiene la hoja *Movimientos*, falta una columna obligatoria, no tiene filas, pesa más de 5 MB, o trae demasiados documentos o líneas (divídalo).

![Archivo no válido](../recursos/img/movimientos/25-importar-archivo-invalido.png)

### 2. Revisar

El sistema valida cada fila **sin guardar nada**.

![Vista previa de la importación](../recursos/img/movimientos/26-importar-vista-previa.png)

- El resumen muestra **Documentos a crear**, **Documentos con error**, **Líneas**, **Cantidad** y **Valor**, y el detalle **Por tipo**.
- La tabla muestra, por fila: **Fila** (la de su Excel), **Documento**, **Tipo**, **Variante**, **Bodega**, **Cantidad**, **Valor unit.** y **Estado y errores** (*Se creará* o *Con error*). Con **Todas / A crear / Con error** filtra por estado del documento.
- Un error en una fila marca **todo el documento** como *Con error*.
- **Descargar errores** genera un Excel con las filas con error y su motivo. **Cambiar archivo** vuelve al paso 1.

![Filas con error](../recursos/img/movimientos/27-importar-con-errores.png)

**Sin errores para aplicar:** mientras haya **una sola fila con error**, **Aplicar** está deshabilitado y no se crea ningún documento (nunca se omiten solo los documentos con error). Corrija el archivo y vuelva a cargarlo.

![Encabezado distinto](../recursos/img/movimientos/28-importar-encabezado-distinto.png)

![Líneas consolidadas](../recursos/img/movimientos/29-importar-lineas-consolidadas.png)

**Errores frecuentes y qué hacer**

| Mensaje | Qué hacer |
|---------|-----------|
| Falta la clave de documento. / La clave supera 20 caracteres o tiene "," o ";". | Escriba una clave corta, sin comas ni punto y coma. |
| La columna … difiere de la primera fila del documento (filas …). | Deje el encabezado idéntico en todas las filas del documento. |
| El tipo de movimiento … no existe. / No está autorizado para el tipo …. | Use un código de tipo existente y que usted pueda usar. |
| La fecha … no es válida. / El periodo de … está cerrado. | Corrija la fecha o use una de un periodo abierto. |
| El tercero … no existe. / Está inactivo. | Escriba el documento de un tercero activo. |
| Falta la variante. / Informa la variante por referencia o por código de barras, no por ambas. | Use una sola forma, completa. |
| La variante … no existe o no está activa. | Revise los códigos de referencia y atributos. |
| El código de barras … coincide con más de una variante. | Use referencia y atributos. |
| La bodega … no existe. / … no existe (ubicación, centro de costos, orden de producción). | Escriba un código existente. |
| El tipo exige centro de costos / número de orden de producción. / La referencia exige lote. | Complete la celda. |
| La cantidad … no es válida (mayor que 0, hasta 4 decimales). / El valor unitario … no es válido. | Corrija el número. |
| El saldo quedaría en …; el tipo no permite negativos. | Reduzca la salida, o registre antes la entrada que la cubre (se simula en el orden del archivo). |
| El documento supera el máximo de … líneas / el tope de …. | Divida el documento en dos claves. |

**Archivo demasiado grande para aplicar.** Si el archivo pasa de **200 documentos** o de **5.000 líneas**, el sistema no lo acepta (ni para revisar ni para aplicar): divídalo en archivos más pequeños.

![Límite para aplicar](../recursos/img/movimientos/30-importar-limite-aplicar.png)

### 3. Aplicar y resultado

Haga clic en **Aplicar N documentos**. La aplicación **no ocurre al instante**: el sistema la pone en cola como un **proceso en segundo plano** y se aplica **documento por documento**.

![Importación en proceso](../recursos/img/movimientos/32-importar-en-proceso.png)

- Mientras corre verá **Importación en proceso**, con el porcentaje (*"En curso: 33 %"*) y cuántos documentos van aplicados (*"1 de 3 documentos aplicados"*). Cada documento se marca como **Aplicado**, **Falló** o **Pendiente**.
- Puede salir de la pantalla: *"te avisaremos en la campana cuando termine"*. El resultado llega también a la **campana de notificaciones**.

![Aviso en la campana](../recursos/img/movimientos/35-importar-aviso-campana.png)

- Si cierra y vuelve a abrir la importación mientras el proceso sigue vivo (o desde el aviso de la campana), la pantalla retoma el estado del proceso.
- **No envíe dos veces el mismo archivo en 10 minutos.** Si lo hace, el sistema reutiliza el proceso que ya está en curso y no crea otro: no se duplican documentos.

**Una transacción por documento.** Cada documento se guarda completo o no se guarda. Si uno falla, **no se deshacen los documentos que ya se aplicaron**; el resto queda pendiente o con su error.

**Resultado.** Al terminar, cada documento aparece con su estado y, si se aplicó, con un **enlace** a su número (por ejemplo *EI-000231*). Los documentos quedan **Abiertos**.

![Resultado de la importación](../recursos/img/movimientos/33-importar-resultado-final.png)

Use **Ver el listado** o **Importar otro archivo**.

**Resultado parcial.** Si algunos documentos se aplicaron y otros no, verá el aviso *"Importación parcial"* y el conteo (*"2 de 4 documentos aplicados"*). Los aplicados ya están registrados; los que fallaron muestran el motivo.

![Resultado parcial](../recursos/img/movimientos/34-importar-resultado-parcial.png)

- **Reintentar pendientes** reanuda el proceso solo con los documentos que faltan, sin duplicar los ya aplicados. Se puede reintentar una vez.
- **Volver a validar** vuelve a revisar el archivo, por si los datos cambiaron.
- Si vuelve a enviar el mismo archivo cuando ya hubo un resultado parcial, el sistema responde **409 IMPORT_PARCIAL**: no crea otro proceso. Use **Reintentar pendientes**, o corrija el archivo y cárguelo solo con los documentos que faltan.

| Aviso | Qué hacer |
|-------|-----------|
| *Importación parcial: los documentos aplicados ya están registrados.* | Reintente los pendientes, o cargue un archivo solo con ellos. |
| *Otro proceso está usando esa bodega.* | El sistema reintenta solo los pendientes; si persiste, haga clic en **Reintentar**. |
| *Los datos cambiaron: el saldo ya no alcanza* (IMPORT_CONFLICT) | Use **Volver a validar** y ajuste el archivo. |
| *Otro usuario importó movimientos mientras revisabas.* | Use **Volver a validar** antes de aplicar. |
| *La importación falló. No se aplicó ningún documento.* | Corrija la causa que se muestra por documento y reintente. |

Cada documento y línea importados aparece en la [bitácora](#-bitácora-solo-administradores) igual que si los hubiera capturado, y los demás usuarios con el listado abierto reciben el aviso de cambios nuevos.

---

## ➕ Crear un movimiento

Haga clic en **Nuevo movimiento**.

![Movimiento nuevo](../recursos/img/movimientos/02-nuevo.png)

1. Llene el **encabezado**:
   - **Tipo de movimiento** (obligatorio): define si es entrada o salida, el prefijo y qué datos pide cada línea (por ejemplo, centro de costos u orden de producción). Algunos tipos traen **bodega, centro de costos o tercero por defecto**, que se llenan solos si están vacíos.
   - **Fecha**: viene con la fecha de hoy. Si cae en un **periodo cerrado**, lo verá de inmediato y no podrá capturar líneas.
   - **Tercero** (obligatorio). Si el tercero tiene una observación importante (por ejemplo, pagos pendientes), aparece un aviso amarillo *"Observación del tercero"*; es informativo, no le impide seguir.
   - **Doc. referencia** (opcional, máx. 20 caracteres): si lo deja vacío se usa el prefijo más el consecutivo.
   - **Observaciones** (opcional, máx. 200 caracteres, sin comas ni punto y coma).
   - **Consecutivo**: dice *"Se asigna al guardar la primera línea"*.
2. Mientras falte tipo, fecha o tercero, la captura de líneas dice *"Complete tipo, fecha y tercero para capturar líneas."*
3. Capture la **primera línea** (ver *Captura por teclado*). Al guardarse, el documento **se crea**: verá *"Movimiento SI 41 creado"*, aparece el consecutivo y el **tipo queda bloqueado** (*"El tipo no se puede cambiar después de guardar la primera línea."*).
4. Siga agregando líneas. Cuando termine, **cierre la transacción** si su proceso lo exige (ver *Cerrar la transacción*).

> ⚠️ **No hay borrador.** Lo que no se ha guardado (la línea que está escribiendo o las que están *En cola* o con error) se pierde si sale de la pantalla. Si intenta salir con líneas sin guardar verá *"Hay N líneas sin guardar; si sale se perderán. Las líneas ya guardadas no se ven afectadas."* con **Quedarme** y **Salir y perderlas**.

---

## ⌨️ Captura por teclado

La fila de captura está pensada para trabajar **sin ratón**. Los campos se recorren en este orden:

**Código o EAN → Variante → Bodega → Ubicación → C. costos → Lote → Cantidad → Valor unit.**

![Captura de una línea por teclado](../recursos/img/movimientos/03-captura-teclado.png)

1. Escriba el **código** de la referencia o su **código de barras** y presione **Enter**:
   - Si corresponde a **una** variante, la toma y salta a **Cantidad** (o a **Bodega** si aún no la ha elegido).
   - Si corresponde a **varias** variantes (por ejemplo, tallas o colores), se abre *"El código … corresponde a N variantes"*: elija con **↑/↓** y **Enter**.
   - Si no existe, verá *"No se encontró el código …"* y el cursor se queda en el campo.
   - Si prefiere buscar por nombre, use el campo **Variante** (*Referencia / talla / color*).

   ![Elegir entre varias variantes](../recursos/img/movimientos/04-varias-variantes.png)

2. Al tener variante y bodega, debajo de la captura verá la **existencia** en esa bodega (*"Existencia en 02 - Almacén centro: 40"*) y el **valor sugerido** (*"Valor sugerido $ 15.000 (costo promedio)"*).
3. Escriba la **Cantidad** (mayor que cero, hasta 4 decimales) y presione **Enter**.
4. En **Valor unit.**, presione **Enter** para aceptar el sugerido o escriba otro.
5. El Enter del último campo (o el botón **Agregar línea**) **envía** la línea: aparece enseguida en la tabla, la captura se limpia **conservando bodega, ubicación y centro de costos**, y el cursor vuelve a **Código o EAN** para la siguiente. No tiene que esperar a que el servidor responda.

**Campos que dependen del tipo o de la referencia:**

| Campo | Cuándo es obligatorio |
|-------|-----------------------|
| **Bodega** | Siempre |
| **Ubicación** | Nunca (opcional) |
| **C. costos** | Si el tipo de movimiento lo exige |
| **Lote** (máx. 20) | Si la referencia maneja lote |
| **Vence** | Aparece si la referencia maneja fecha de vencimiento |
| **Orden de producción** | Si el tipo de movimiento lo exige |

**Atajos de teclado** (también aparecen debajo de la captura):

| Tecla | Qué hace |
|-------|----------|
| **Enter** | Pasa al siguiente campo; en el último, envía la línea |
| **Esc** | Limpia la captura (o cancela la edición de una línea) |
| **↑ / ↓** | Seleccionan una línea de la tabla |
| **F2** | Edita la línea seleccionada: la carga en la captura (*"Editando la línea 3: Enter guarda el cambio, Esc lo cancela."*) |
| **Supr** | Quita la línea seleccionada (pide confirmación) |
| **Ctrl+D** | Copia la línea seleccionada a la captura, para crear una parecida |
| **Alt+N** | Vuelve a la captura |
| **Alt+R** | Reintenta las líneas que no se guardaron |

**Matriz:** para referencias con tallas y colores, el botón **Matriz** abre una tabla talla × color con la existencia de cada variante en la bodega elegida. Escriba la cantidad en cada celda y haga clic en **Agregar N líneas**: cada celda con cantidad se envía como una línea, con su valor sugerido.

![Matriz de tallas y colores](../recursos/img/movimientos/10-matriz.png)

**Cambiar o quitar una línea ya guardada:** use el **lápiz** (o **F2**) y confirme con **Enter**, o la **papelera** (o **Supr**). Al quitarla verá *"Se quitará … del documento y se actualizarán existencias y contabilidad."* Si quita la última línea, se le pregunta si quiere eliminar también el documento vacío o **Conservarlo**.

---

## 📷 Lector de código de barras

Con un lector de código de barras la captura es todavía más rápida:

1. Deje listos la **bodega** y, si el tipo lo exige, el **centro de costos**. El campo **Código o EAN** lo confirma: *"Lector listo: bodega y centro de costos definidos; cada lectura agrega 1 unidad."*
2. Con el cursor en **Código o EAN**, lea el código: la línea se envía sola con **cantidad 1**, sin tocar más teclas.
3. Si vuelve a leer el mismo producto, **no se crea otra línea**: se suma a la que ya existe (ver *Línea sumada*).

![Lecturas del lector: la segunda se suma a la línea 1](../recursos/img/movimientos/05-lector.png)

- Puede leer tan rápido como quiera: las lecturas se ponen en cola y no se pierde ninguna.
- Si el código corresponde a varias variantes, se abre la ventana para elegir.
- Para una cantidad distinta de 1, corrija la línea con el lápiz o escriba la cantidad a mano en la captura.

> ℹ️ La pantalla reconoce el lector porque los caracteres llegan muy rápido. Si usted escribe el código a mano, se comporta como la captura normal.

---

## 🚦 Estado de cada línea

Cada línea muestra en la columna **Estado** qué pasó con ella. Las líneas guardadas no muestran nada especial: su **N.º** indica que ya están registradas.

| Estado | Qué significa | Qué hacer |
|--------|---------------|-----------|
| **Por guardar** | Línea copiada (al duplicar) que aún no se envía | **Guardar todas** |
| **En cola** | Espera su turno: las líneas se envían **una a la vez, en orden** | Nada, siga capturando |
| **Guardando…** | Se está registrando | Nada |
| **Guardada** | Quedó registrada (el aviso dura unos segundos) | — |
| **Sumada a la línea N** | Era igual a otra línea y se sumó a ella | — |
| **Error** + motivo | El sistema la rechazó por una regla (por ejemplo, *"La existencia quedaría en −1"*) | **Corregir** (la devuelve a la captura) o **Descartar** |
| **No se guardó** | No hubo respuesta del servidor o estaba ocupado | **Reintentar** o **Alt+R**. Reintentar **no la duplica**: antes se comprueba si ya había quedado guardada |
| **En conflicto** | Otro usuario cambió esa misma línea | Ver *Cambios de otros usuarios* |

![Líneas guardándose y en cola](../recursos/img/movimientos/07-linea-guardando.png)

Mientras haya líneas sin guardar:

- Arriba de la tabla verá *"N líneas sin guardar"* y el botón **Reintentar todas** si alguna falló.
- El valor del resumen del documento dice *"Totales sin incluir N líneas sin guardar"*: los totales son siempre los que ya quedaron registrados.
- **Cerrar transacción** está deshabilitado (*"Hay N líneas sin guardar"*).

![Línea con error y línea guardada](../recursos/img/movimientos/08-linea-error.png)

### Línea sumada

Si agrega una línea **igual** a otra que ya existe (misma variante, bodega, centro de costos y valor, sin lote), no se crea una línea nueva: la cantidad **se suma**. Antes de enviarla, la captura lo avisa: *"Se sumará a la línea 1: 5 + 2 = 7"*. Después, la línea destino se resalta con *"Sumada a la línea 1"*.

![Línea sumada a la línea 1](../recursos/img/movimientos/06-linea-consolidada.png)

### Validaciones antes de guardar

| Aviso | Por qué |
|-------|---------|
| *"La existencia quedaría en −N"* | La salida dejaría la bodega en negativo y el tipo no lo permite. Se avisa en la captura y el sistema la rechaza. |
| *"La fecha está en un periodo cerrado: no se pueden guardar líneas."* | El periodo contable de la fecha del documento está cerrado. |
| *"Superaría el tope de …"* | La cantidad supera el tope configurado. |
| *"Alcanzó el máximo de N líneas para este tipo"* | El tipo de movimiento limita el número de líneas. |
| *"La cantidad debe ser mayor que cero (máx. 4 decimales)"*, *"El valor unitario debe ser mayor que cero"* | Datos de la línea inválidos. |
| *"Este tipo exige centro de costos"*, *"Esta referencia exige lote (máx. 20)"*, *"Elija la bodega"*, *"Elija la variante"* | Falta un dato obligatorio. |

![Aviso de existencia negativa](../recursos/img/movimientos/09-saldo-negativo.png)

---

## 📄 El documento

Al abrir un documento (lápiz u ojo en el listado) ve:

![Documento abierto](../recursos/img/movimientos/11-documento.png)

- **Barra superior**: *Volver al listado*, el estado, *En vivo* y las acciones: **Cerrar transacción** (la principal), **Imprimir**, **Duplicar**, **Anular** y **Eliminar**. Si una acción no se puede usar, aparece deshabilitada con el motivo debajo.
- **Encabezado**: editable si el documento está abierto; en un documento cerrado o anulado muestra además quién lo **creó**, quién lo **cerró** y cuántas veces se ha **impreso**.
- **Resumen**: Líneas, Cantidad y Valor; **Por bodega** y **Por referencia** (las 20 de mayor valor).
- **Pestañas**:
  - **Detalle**: la captura y las líneas. En un documento de solo lectura, las líneas se ven en una tabla paginada con búsqueda por referencia, orden y exportación.
  - **Contabilidad**: los registros contables del documento con sus sumas. Si débitos y créditos no cuadran verá *"Documento descuadrado — diferencia …"*: revise la configuración contable del tipo o de las referencias.
  - **Adjuntos**: soportes del movimiento (actas, remisiones, fotos), máximo 10 MB por documento. *Por ahora muestra "Disponible en la próxima entrega".*
  - **Bitácora**: solo administradores. Ver *Bitácora*. *Por ahora muestra "Disponible en la próxima entrega".*

### Cambiar el encabezado

En un documento ya creado, cada cambio del encabezado **se guarda solo**: al elegir la fecha o el tercero, o al salir del campo de texto. Verá *"Guardando encabezado…"* y luego *"Encabezado guardado"*. El tipo no se puede cambiar.

> ⚠️ Cambiar la **fecha** de un documento con líneas **no recalcula** el valor de las líneas ya guardadas ni vuelve a revisar sus existencias; solo valida que la nueva fecha esté en un periodo abierto.

---

## 🔒 Cerrar la transacción

Cuando termine de capturar, haga clic en **Cerrar transacción** y confirme: *"¿Cerrar el movimiento SI 40? Después no podrá modificarse."*

![Confirmar el cierre](../recursos/img/movimientos/12-cerrar.png)

Verá *"Movimiento SI 40 cerrado"* y el documento pasa a solo lectura.

El botón está deshabilitado, con el motivo debajo, si:

- hay líneas sin guardar (*"Hay N líneas sin guardar"*), o
- el documento no tiene líneas (*"Agregue al menos una línea"*).

### Editar un documento cerrado

Si su usuario tiene el permiso especial para editar documentos cerrados, en un documento cerrado verá **Editar cerrado**. Al usarlo aparece el aviso *"Editando un documento cerrado — Sigue cerrado: cada línea se guarda y la contabilidad se vuelve a registrar."* y la captura funciona como en un documento abierto.

![Editando un documento cerrado](../recursos/img/movimientos/13-editar-cerrado.png)

---

## 🚫 Anular o eliminar

| | **Anular** | **Eliminar** |
|---|---|---|
| ¿Qué pasa con el documento? | **Se conserva** como rastro, con el motivo, quién y cuándo | **Desaparece** con sus líneas, su contabilidad y sus adjuntos |
| Existencias y costos | Deja de afectarlos | Deja de afectarlos |
| ¿Se puede deshacer? | No | No |
| Cuándo usarlo | Documentos cerrados, o cuando necesita dejar evidencia | Documentos hechos por error que no tienen nada relacionado |

Ambas acciones exigen que el **periodo** del documento esté **abierto**.

### Anular

Haga clic en **Anular**, escriba el **Motivo de anulación** (obligatorio, máx. 200 caracteres, sin comas ni punto y coma) y confirme. Si el documento estaba abierto, queda también cerrado.

![Anular un documento](../recursos/img/movimientos/14-anular.png)

El documento muestra *"Documento anulado: <motivo>"* con quién y cuándo lo anuló. Un documento anulado **no se puede eliminar** (*"Los documentos anulados se conservan"*) ni imprimir.

![Documento anulado](../recursos/img/movimientos/16-anulado.png)

### Eliminar

Eliminar pide una confirmación reforzada:

1. Haga clic en **Eliminar**. El diálogo dice exactamente qué se borrará: *"Se eliminarán el documento EI-125, sus 3 líneas, sus 2 registros contables y sus 2 adjuntos. No se puede deshacer."*
2. Si el documento está **cerrado**, le recomienda *"Mejor anúlelo: se conserva y deja de afectar existencias."* con el botón **Anular** en el mismo diálogo.
3. Para habilitar **Eliminar**, escriba el **número del documento** tal como se indica (*"Escriba EI-125 para confirmar"*).

![Eliminar con confirmación](../recursos/img/movimientos/15-eliminar.png)

**Eliminar** no aparece, o aparece deshabilitado con el motivo, cuando:

| Motivo que verá | Qué significa |
|-----------------|---------------|
| *"Tiene documentos relacionados; anúlelo en su lugar"* | Otro documento depende de este |
| *"Los documentos anulados se conservan"* | Ya está anulado |
| *"El periodo está cerrado"* | La fecha cae en un periodo cerrado |

> ⚠️ Para evitar borrados masivos por error, hay un límite de eliminaciones seguidas por usuario. Si lo alcanza verá *"Demasiadas eliminaciones seguidas; intente de nuevo en N s"*.

---

## 🖨️ Imprimir

Haga clic en **Imprimir** (en el listado o en el documento). Se abre la vista del formato en tamaño carta; la barra superior indica qué formato se aplicó, por ejemplo *"Formato FRT-INV-001 (tipo EI)"*. Haga clic en **Imprimir** para enviarlo a la impresora o guardarlo en PDF desde el navegador, y en **Volver al documento** para regresar.

![Formato FRT-INV-001](../recursos/img/movimientos/17-imprimir.png)

El formato por defecto **FRT-INV-001** incluye, en este orden: datos de la compañía; tipo, número, doc. referencia y fecha; datos del tercero; líneas (referencia, atributos, lote, bodega, centro de costos, cantidad, valor unitario y subtotal); total de cantidad, total de valor y el valor en letras; el detalle contable con sus sumas; observaciones; firma de recibido; y el pie con quién lo elaboró, **Original** o **Copia**, y la fecha y hora de impresión.

- La **primera** impresión dice **Original**; las siguientes, **Copia**. Cada impresión queda registrada (*"Impresión n.º N registrada"*) y el encabezado del documento muestra cuántas veces se ha impreso.
- **Papel y color:** en la barra superior elija **Carta** o **A4** y, en la hoja, **Color** o **Blanco y negro**.
- **Descargar PDF:** el botón **Descargar PDF** genera el formato en el servidor con el papel y el modo elegidos y lo guarda con el nombre del documento, por ejemplo `EI-125.pdf`. Mientras se descarga, el botón muestra un indicador y no se puede pulsar de nuevo. Descargar no suma una impresión: el contador cuenta las veces que se abre la vista. Si el documento es demasiado grande (más de 4000 líneas) aparece *"El documento es demasiado grande para el PDF; usa Imprimir"*; en ese caso use **Imprimir**.
- **Formato por tipo:** cada tipo de movimiento puede tener su propio formato, configurado en el tipo de movimiento. Un formato puede cambiar el título, los textos fijos, las columnas opcionales, las firmas (por ejemplo *Entregó* y *Recibió*) y ocultar valores, valor en letras o contabilidad. Si el tipo no tiene formato o el configurado no existe, se usa **FRT-INV-001**.

![Formato propio de un tipo de salida](../recursos/img/movimientos/18-imprimir-variante.png)

---

## 📑 Duplicar

**Duplicar** (en el listado o en el documento) abre un documento **nuevo** con el mismo tipo, tercero, observaciones y líneas del original, con la fecha de hoy y el valor unitario **sugerido de nuevo** para esa fecha. No copia el consecutivo, el doc. referencia ni los adjuntos.

Las líneas copiadas aparecen como **Por guardar** y el aviso dice *"Copia de EI 125: revise y pulse Guardar todas"*. Revise, corrija o quite lo que necesite y haga clic en **Guardar todas**: se envían una a una (la primera crea el documento) y cada una muestra su estado. Es útil para devoluciones o movimientos que se repiten.

---

## 📥 Descargar insumos de una OP {#descargar-insumos-de-op}

Cuando el documento tiene un **tipo de salida** que exige **orden de producción** (OP), aparece el botón **Descargar insumos de OP** en la captura. Úselo para agregar líneas de una vez, desde la **hoja de consumos** de la orden.

### Cuándo aparece el botón

**Descargar insumos de OP** se muestra si:

- El tipo de movimiento **exige orden de producción**
- El documento es una **salida** (no entrada)
- El documento está **abierto** y no tiene líneas en conflicto de OP (ver *Limitaciones*)

Si el botón está deshabilitado, verá el motivo debajo. Algunos motivos comunes:

| Motivo | Por qué | Qué hacer |
|--------|--------|----------|
| *Hay N líneas sin guardar* | El documento tiene líneas pendientes | Guarde las líneas primero o descarte los cambios |
| *Complete el encabezado para descargar insumos* | Falta tipo, fecha, tercero o bodega destino | Rellene los campos obligatorios del encabezado |
| *El documento ya tiene líneas de otra OP (OP-121, OP-122)* | Mezclaría órdenes diferentes | Cree otro documento o elimine las líneas de la OP anterior |
| *Editar documentos cerrados* | El documento está cerrado | Si es administrador, haga clic en **Editar cerrado** primero |

### Abrir y navegar el diálogo

Haga clic en **Descargar insumos de OP**. Se abre un diálogo con:

1. **Origen** (obligatorio):
   - **OP**: la orden de producción. Solo ve las órdenes vigentes y elegibles. Si alguna aparece en rojo, no se puede usar (congelada, cancelada o sin hoja de consumos).
   - **Bodega**: dónde salen los insumos. Obligatoria.
   - **Ubicación**: dentro de la bodega (opcional).
   - **Centro de costos**: según lo exija el tipo de movimiento.

2. **Insumos**: la tabla con los artículos de la hoja de consumos. Puede cambiar de bodega en el origen: la tabla se actualiza con la existencia en esa bodega.

3. **Resumen**: abajo, cuántos insumos seleccionó, cuántas líneas resultarán y el valor estimado.

4. **Botones**: 
   - **Seleccionar suficientes**: marca solo los insumos cuya existencia cubre la cantidad que necesita (atolondrado, pero oportuno).
   - **Confirmar**: envía las líneas al documento. Si hay errores no se cierra el diálogo.
   - **Cancelar**: cierra sin guardar. Si tiene cambios, pide confirmar *"¿Descartar la selección?"*.

**Teclas de atajo:**

| Tecla | Qué hace |
|-------|----------|
| **?** | Abre esta ayuda |
| **Esc** | Cierra el diálogo (si no hay cambios, o tras confirmar el descarte) |
| **Ctrl+Enter** | Confirma (igual que el botón) |

### Los insumos de la tabla

Cada fila muestra un artículo de la hoja de consumos:

| Columna | Qué significa |
|---------|--------------|
| **Casilla** | Marca si desea descargar este insumo. Solo activa si el insumo es válido (ver *Insumos no descargables* abajo). |
| **Insumo** | Código, nombre, unidad y variante. Si hay avisos, aparecen en texto pequeño debajo. |
| **Requerido** | Lo que debe surtirse según la OP (cantidad que la OP pide). |
| **Ya descargado** | Lo que ya descargó de esta OP en documentos anteriores. |
| **Pendiente** | Lo que falta por descargar (Requerido − Ya descargado). |
| **Existencia** | Lo que hay en la bodega que eligió. |
| **A descargar** | Lo que va a sacar ahora. **Editable**: solo si la casilla está marcada. El máximo es `min(Pendiente, Existencia)`. Si escribe más, verá *"Máximo N"* en rojo y **Confirmar** queda deshabilitado. Presione **Esc** para volver al valor sugerido; si lo borra o pone 0, se desmarca la casilla. |
| **Lote** | Solo aparece cuando marca un insumo cuya referencia exige lote. Es una casilla (*"Lote de …"*) donde digita el lote: hasta 20 caracteres, se convierte a mayúsculas y es **obligatoria**. Ver *Insumos con lote* abajo. |
| **Estado** | Leyenda (verde, amarilla, etc.) que resume por qué el insumo está en ese estado. Algunos estados llevan insignias adicionales. |

### Insumos no descargables

Si un insumo tiene alguno de estos problemas, aparece deshabilitado (la casilla no se puede marcar) y verá el motivo en texto:

| Motivo | Por qué | Qué hacer |
|--------|--------|----------|
| **Ya descargado por completo** | El pendiente es 0. No hay más que sacar. | Nada, es normal. |
| **Faltan N** | La existencia en bodega es menor que lo pendiente. | Reciba más inventario, elija otra bodega o descargue cantidad parcial; edite la fila a mano (o elija **Seleccionar suficientes**). |
| **Sin costo** | La referencia no tiene costo configurado. | Defina el costo de la referencia en el maestro. |

Los insumos con **duplicados**, **autoconsumo** u **otra variante sospechosa** en la hoja de consumos aparecen con la insignia **Revisar**. No están bloqueados: la descarga funciona, pero vea qué ocurrió.

### Insumos con lote

Si la referencia de un insumo **exige lote**, la fila se puede marcar como cualquier otra. Al marcarla aparece la casilla **"Lote de …"** y el cursor pasa a ella:

- Digite el lote (hasta **20 caracteres**; si escribe en minúsculas se convierte a mayúsculas).
- Mientras la casilla esté vacía verá *"Digite el lote (máx. 20)"* en rojo y **Confirmar** queda deshabilitado, con el motivo a la vista.
- Si el servidor no acepta el lote, la casilla se marca con el error y el diálogo se queda abierto para corregirlo.
- Cada insumo se descarga con **un solo lote** por fila. Para sacar el mismo insumo de dos lotes distintos, haga una descarga con un lote y luego otra con el otro.
- Si la referencia **no** exige lote, no aparece la casilla.

### Resumen y límites

**Resumen**: debajo de la tabla, ve cuántos insumos seleccionó (ej. *"4 de 6"*), cuántas líneas resultarán (si varias descargas se consolidan en una, es menos), y el valor total estimado.

**Límites**: los tipos de movimiento pueden tener un límite de cantidad máxima de líneas o de valor. Si está cerca o lo supera:

- Verá un aviso **naranja** (aviso) o **rojo** (error).
- **Confirmar** queda deshabilitado si supera el límite.
- Puede desmarcar insumos para entrar dentro del límite.
- Si el servidor rechaza (por si el límite cambió), verá el error y el diálogo se queda abierto.

### Errores y reintentos

**Error al cargar la OP**. Si no se puede traer la hoja de consumos, verá *"No se pudieron cargar los insumos"* con **Reintentar**. La OP y bodega se conservan.

**Error de validación al confirmar**. Si algún dato es inválido (período cerrado, centro de costos faltante, etc.), verá un resumen de errores en rojo. El diálogo no se cierra; corrija y vuelva a confirmar.

- Los errores por fila aparecen bajo el insumo (ej. *"Falta centro de costos"* o el error de la casilla de lote).
- Use **Seleccionar suficientes** para limpiar filas problemáticas.

**Error del sistema al confirmar**. Si el servidor falla:

- **Ocupado**: *"El sistema está ocupado. No se guardó nada"* con **Reintentar**. La selección se conserva con la misma clave de idempotencia (no se duplican líneas).
- **Error**: *"No se pudo generar la salida. No se guardó ninguna línea"* con **Reintentar**.
- **Conflicto**: otro usuario cambió el documento mientras lo tenía abierto. Aparece *"El documento cambió mientras elegía los insumos"* con **Actualizar y revisar** (relee sin escribir nada).
- **Cambio de saldo**: otra persona descargó insumos de la misma OP antes que usted. Aparece el aviso y la tabla se actualiza con las existencias nuevas; el insumo que ya no alcanza se marca como *"Faltan …"*.
- **Cambio de pendiente**: el pendiente de un insumo bajó porque otra descarga llegó antes. Aparece el aviso y la tabla se actualiza.

En todos estos casos, el diálogo se queda abierto para revisar.

### Cambios en tiempo real (otro usuario)

Si otro usuario modifica el documento mientras el diálogo está abierto, verá *"El documento cambió; actualice los insumos"* con un botón **Actualizar**. La tabla no se refresca sola; úselo para traer los cambios sin perder su selección.

### Limitaciones

- **Una OP por documento**: el diálogo impide mezclar órdenes en el mismo documento. Si tiene líneas de OP-120 y abre para OP-121, verá *"El documento ya tiene líneas de otra OP"* y no abrirá. Cree otro documento.
- **Máximo 50 insumos por descarga**: si la OP tiene más, solo ve los primeros 50 ordenados por código. Vuelva a abrir para los siguientes.
- **Órdenes sin hoja de consumos**: el diálogo no abre si la OP no tiene consumos. Cargue la hoja en el módulo de Producción primero.

### Después de confirmar

Si la descarga fue correcta:

- El diálogo se cierra.
- Las líneas nuevas aparecen en la tabla del documento, **resaltadas** unos segundos.
- Verá *"Se descargaron N insumos de OP-…"* con el consolidado: si dos descarga de diferentes materiales se sumaron a líneas que ya tenía, aparece *"X líneas se sumaron a líneas existentes"*.
- El foco vuelve al botón que abrió el diálogo.

Si alguna línea **se sumó** a otra existente (misma variante, bodega, lote y valor), solo ve una fila con *"Sumada a la línea N"*.

---

## 🏭 Producción desde una entrada {#produccion-desde-una-entrada}

Cuando una **entrada tiene una orden de producción (OP)**, puede **registrar un movimiento de producción** para toda la entrada de una sola vez, registrando que las cantidades avanzan de una operación a la siguiente en la ruta de fabricación. Un documento de entrada produce para **una única orden de producción**; sus líneas generan un solo movimiento de producción con un detalle por variante. Desde aquí crea, ve y anula esa producción sin salir del documento de inventario.

### Cuándo aparece la acción

En la **barra de acciones del documento** (arriba, junto a **Cerrar transacción** e **Imprimir**), aparecen botones de producción solo si el documento es elegible:

| Acción | Cuándo aparece |
|--------|----------------|
| **Registrar producción** | El documento es una entrada con OP única, tiene líneas elegibles (todas las líneas con OP apuntan a la misma orden), la ruta de la referencia tiene operaciones, ninguna línea tiene producción registrada todavía, y la compañía no requiere sincronización externa. |
| **Completar producción** | El documento ya tiene producción registrada (completa o parcial) y hay líneas pendientes elegibles (nuevas, sin producción). |
| **Ver producción** | El documento tiene movimientos de producción registrados. |
| **Anular producción** | El documento tiene movimientos de producción activos y ninguno tiene movimientos posteriores en la cadena. |

Si ningún botón aparece, el documento no cumple los requisitos (ver motivos en la tabla de *Errores*).

### Propuesta de producción del documento

Al abrir **"Registrar producción"** o **"Completar producción"**, verá un diálogo con:

**Tabla de líneas** (solo lectura):
- Las líneas elegibles del documento con su variante, cantidad y saldo (cuánto hay disponible en la operación de origen, o vacío si es el primer movimiento).
- Si hay líneas sin orden de producción o de una OP distinta, aparecen omitidas en una sección aparte con *"Estas líneas no tienen OP / tienen otra OP y no se incluirán"*.

**Responsable** (obligatorio):
- Viene precompletado con el **tercero del documento**. Si no es un responsable válido, edite el campo o elija otro con la lupa.

**Fechas** (obligatorias):
- **Fecha**: por defecto, la **fecha del documento**. Debe estar en un periodo contable abierto.
- **Fecha de entrega**: por defecto, la **fecha del documento + 1 día**. Debe ser posterior a la fecha del movimiento.
- **Fecha de entrega real** (opcional): cuándo se completó realmente (no puede ser anterior a la fecha del movimiento).

**Operación destino** (una por grupo):
- Si el documento tiene **un grupo de líneas** (todas con la misma cabeza de movimiento), ve un solo selector **Operación destino**: dónde pasan las cantidades (la primera operación si es el primer movimiento, o la siguiente según dependencias).
- Si hay **varios grupos** (variantes con cabezas distintas), ve un título por grupo y un selector de operación para cada uno. Puede elegir una operación distinta por grupo según sus dependencias.
- Si una operación ya está completa o sus dependencias no se cumplen, no aparece como opción.

### Registrar la producción del documento

1. Revise la **propuesta**: líneas incluidas, responsable, fechas, operaciones destino.
2. Corrija responsable, fechas u operaciones si es necesario.
3. Haga clic en **Registrar** o presione **Ctrl+Enter**.

Si todo es válido, verá *"Se registró la producción del documento"* con el resumen (número de líneas, operación destino, responsable). La barra se actualiza: **Registrar producción** desaparece y aparecen **Ver producción** y **Anular producción**. Otros usuarios ven el cambio en vivo.

**Si quedó incompleta** (agregó líneas nuevas después de registrar), la acción pasa a **"Completar producción"**, que crea un movimiento adicional solo con las líneas pendientes (mismas reglas de origen, destino y responsable único).

### Resumen de la producción del documento

La pantalla muestra un resumen con un renglón por par de movimientos (salida y entrada de la producción):

| Columna | Qué significa |
|---------|---------------|
| **Operación** | De dónde a dónde (por ejemplo, *"Corte → Costura"*) |
| **Responsable** | Quién ejecutó la operación |
| **Líneas** | Cuántas líneas del documento se movieron |
| **Estado** | *Activo*, *Parcial* o *Anulado* |

Haga clic en un renglón para **Ver producción** y más detalles.

### Ver el movimiento registrado

Al hacer clic en **Ver producción** (ojo en el resumen) o en la barra del documento, se abre un panel con:

- Operación origen → Operación destino (por ejemplo, vacío → Corte para el primer movimiento)
- Responsable
- Detalles de la producción (variante y cantidad producida, enteras)
- Fechas (movimiento, entrega, entrega real si se completó)
- Quién lo registró y cuándo
- Botón **Anular** (si tiene permiso y el movimiento no tiene dependientes)

### Anular la producción del documento

Si se equivocó o necesita revertir:

1. En el resumen, haga clic en **Ver producción** del movimiento que quiere anular.
2. O haga clic en **Anular producción** en la barra del documento.
3. Escriba el **motivo de anulación** (obligatorio, máx. 200 caracteres).
4. Confirme.

Verá *"Se anuló la producción del documento"*. El resumen desaparece, la barra se actualiza con **Registrar producción** y **Completar producción** (si hay pendientes). **No se puede deshacer**: los avisos de otros usuarios muestran que la operación quedó anulada.

#### Cascada al anular o eliminar el documento

Si **anula o elimina el documento** con **producción registrada**:

- El sistema avisa: *"Se anulará también el movimiento de producción Corte → Costura (3 líneas)"* con cada par que tenga.
- Confirme y se anulan **todos los movimientos de producción** del documento en una sola transacción.
- Si algún movimiento tiene **movimientos posteriores** en la cadena (otra entrada de la misma OP depende de este), verá el error *"Tiene producción con dependientes; anúlela desde el resumen"* y deberá anular primero desde **Anular producción**.

### Cambios en las líneas con producción registrada

**Agregar una línea nueva:**
- Se permite: la línea nueva queda sin producción y la acción en la barra pasa a **"Completar producción"** (para registrar solo las pendientes).

**Cambiar cantidad, variante u orden de producción, o eliminar:**
- Si la línea es parte de un **movimiento compartido** (el movimiento de producción incluye varias líneas), verá *"No se puede cambiar: línea con producción registrada (par compartido)"* con un botón **Anular producción**. Anule primero desde la barra, luego edite.
- **Otros cambios** (valor, lote, detalle, criterios) se permiten sin anular.

### Líneas sin orden de producción

Si el documento tiene líneas sin OP o con una OP distinta a las demás:

- Aparecen omitidas en el diálogo de propuesta (*"Estas líneas no tienen OP / tienen otra OP"*).
- En la tabla de líneas, muestran *"Sin producción (sin OP)"* en lugar de estado.
- No se incluyen en el registro de producción.

**Documento con varias órdenes de producción:**
- Si las líneas con OP apuntan a órdenes distintas, el sistema rechaza el registro: *"El documento tiene líneas de más de una OP; una entrada produce para una sola OP"*. Cree un documento separado por cada OP.

### Errores y validaciones

| Error | Por qué | Qué hacer |
|-------|--------|----------|
| **Saldo insuficiente en: {lista}** | Una línea quiere producir más de lo disponible en la operación origen. Se lista qué variantes y cuánto falta. | Reduzca las cantidades, registre primero producción en otra línea de la misma OP, o verifique las operaciones anteriores. |
| **Cantidad no entera** | La tabla solo muestra las líneas que se registran; si una cantidad tiene decimales, no se puede registrar como entera. | Revise la cantidad de la línea en el inventario. |
| **Dependencia no cumplida** | Una operación depende de saldo suficiente en otra que aún no lo tiene (por ejemplo, "Depende de Costura (producido 4 de 10) para Variante 1"). | Registre primero la operación previa, o elija una operación alternativa sin dependencia. |
| **Periodo cerrado** | La fecha del movimiento o la fecha de entrega cae en un periodo contable cerrado. | Use una fecha de un periodo abierto. |
| **Variante inválida** | La referencia de la línea no está configurada con la ruta de operaciones. | En **Maestro de referencias**, agregue operaciones para esta referencia. |
| **Compañía con sincronización externa no disponible** | La empresa está configurada para sincronizar con un sistema externo y esa sincronización no está disponible. | Consulte al administrador. |
| **Documento ya tiene movimiento de producción** | Todas las líneas elegibles ya tienen producción registrada. | Si necesita registrar más, agregue líneas nuevas y use **Completar producción**. |
| **El documento tiene líneas de más de una OP** | Las líneas con OP apuntan a órdenes distintas. | Cree un documento separado para cada OP. |
| **No hay líneas elegibles** | El documento no tiene líneas con OP, o todas están anuladas. | Agregue líneas con orden de producción válida. |

---

## 💰 Costear la producción {#costear-la-produccion}

Cuando guarda una **entrada de producción** (un documento donde sus líneas tienen la misma orden de producción), el sistema le propone un **valor unitario** basado en **los costos reales que la orden acumuló**: materiales que sacó de inventario, servicios de compras (confección, corte, etc.), e indirectos de fabricación. Antes de aplicar ese valor a las líneas, usted ve el resumen por rubro, lo compara con el precosteo teórico de la referencia, lo ajusta si es necesario, y solo entonces lo aplica al documento.

### Cuándo aparece la acción

En la **barra de acciones del documento** (arriba, junto a **Registrar producción** e **Imprimir**), aparece **Costear producción** solo si:

- El documento es una **entrada** con una **orden de producción única** (todas las líneas de la OP).
- El documento está **abierto** o usted tiene el permiso para editarlo cerrado.
- Su usuario tiene el permiso **Actualizar** sobre *Entradas y salidas*.
- El periodo del documento está abierto.

Si el botón no aparece o está deshabilitado, el documento no cumple los requisitos anteriores.

### Abrir el diálogo de costeo

Haga clic en **Costear producción**. El sistema trae el resumen de costos de la orden, que puede tardar unos segundos (*"Calculando el resumen de costos de la OP…"*). Una vez listo, verá:

1. **Avisos** (naranja y rojo, si aplica): le avisan si falta algo importante (sin materiales, sin servicios de compras, costo cero o negativo, etc.). A pesar de los avisos amarillos, puede seguir; los avisos rojos impiden aplicar.
2. **Resumen de costos por rubro**: la base para calcular el valor unitario.
3. **Comparación con el Teórico**: el precosteo de la referencia, solo de referencia.
4. **Valor unitario propuesto** y cómo se distribuye por línea.
5. **Botones**: Cancelar y Aplicar al documento (o solo Cerrar si no tiene permiso de actualizar).

### Resumen de costos por rubro

Es una tabla que muestra de dónde sale el costo de la orden:

| Rubro | Qué incluye | Quién lo propone |
|-------|------------|-----------------|
| **Materiales** | Las salidas de inventario a la orden menos las devoluciones (el costo registrado de cada salida). | El sistema, de los documentos de salida de la orden. |
| **Cada servicio** (por ej. *Confección*, *Corte*) | Las compras de servicios asignadas a la orden: valor bruto sin IVA ni retenciones, descuento ya restado. Se agrupa por tipo de servicio. | El sistema, de los documentos de Compras con la orden asignada. |
| **Indirectos** | Un porcentaje (por ejemplo, 8 %) multiplicado por la base (Materiales + servicios). Solo incluye los indirectos de fabricación: la utilidad y los indirectos de administración y ventas no entran aquí. | El sistema, del porcentaje configurado en la referencia. |

Cada rubro muestra:

- **Real**: el costo que se ha gastado (materiales salidos, servicios facturados, etc.).
- **Teórico** (para referencia): cuál debería ser según el precosteo de la referencia.
- **Diferencia**: en pesos y porcentaje. Un icono le dice si es mayor, menor o igual al teórico.
- **Efectivo**: lo que entra al cálculo del valor unitario (real más cualquier ajuste que haga).

Debajo, la **fila Total** suma todos los rubros: ese es el **costo acumulado** de la orden.

### Ajustar un rubro

Si el costo de un rubro no es correcto —por ejemplo, hubo retoques no facturados, o un error en el cálculo—, puede **ajustarlo**:

1. Haga clic en **Ajustar** de la fila del rubro.
2. Se abre un pequeño diálogo con:
   - **Monto actual** del rubro (solo lectura).
   - **Ajuste**: escriba el aumento o disminución (puede ser negativo).
   - **Motivo** (obligatorio, máx. 200 caracteres): por qué hace este ajuste. Queda en la bitácora del documento.
3. Presione **Guardar** o **Enter**.

Verá el rubro con un chip *"Ajustado"* y el motivo. El **Efectivo** recalcula al instante, así como el **Indirectos** (si lo ajustó) y el **valor unitario propuesto**.

**Para quitar el ajuste**, vuelva a abrir y escriba 0 en el ajuste, o use **Quitar ajuste**.

> 💡 El ajuste **no cambia** los documentos de origen (las compras, las salidas): solo modifica el cálculo del valor unitario para este documento. La bitácora registra quién, qué, cuándo y por qué.

### Comparación con el Teórico

Debajo del resumen aparecen tres tarjetas que comparan lo que costó en realidad con lo que la receta estimó:

- **Total**: el costo acumulado vs el precosteo total.
- **Mano de obra**: suma de todos los servicios vs la mano de obra de la receta.
- **Materiales**: materiales reales vs materiales de la receta.

El Teórico es **solo referencia**: no afecta el valor propuesto. Sirve para saber si los costos reales están cerca de lo esperado. Si la orden tiene variantes sin receta, verá una nota (*"Teórico incompleto"*).

### Valor unitario propuesto

Es el resultado de dividir:

```
Costo acumulado (Materiales + servicios + Indirectos ajustado) ÷ Cantidad acumulada producida = Valor propuesto
```

Se muestra con:**

- **Costo acumulado**: el total de todos los rubros después de ajustes.
- **Cantidad acumulada producida**: la cantidad total de todas las entradas de producción de esta orden que hay registradas (incluida esta).
- **Absorbido**: lo que ya pagaron documentos anteriores de la misma orden (solo para su información).
- **Por absorber**: lo que queda para próximas entradas de la orden (si las hay).
- **Valor propuesto**: el resultado, redondeado a los decimales del tipo de documento.

Este valor se aplica **de forma uniforme** a todas las líneas elegibles del documento.

### Valor por línea

Una tabla muestra cada línea del documento con:

- **Línea**: número de la línea.
- **Variante**: código y nombre.
- **Cantidad**: unidades de esa línea.
- **Actual**: el valor unitario que tiene ahora.
- **Propuesto**: el nuevo valor que propone el sistema.
- **Cambio**: la diferencia en pesos.

Las líneas sin orden de producción aparecen con la nota *"No se modifican"*.

### Aplicar el costo

Una vez que revise el resumen, compare con el Teórico y haga los ajustes que considere:

1. Haga clic en **Aplicar al documento**. Se abre una confirmación que dice exactamente qué va a pasar: *"Se escribirá $ X.XXX,00 como Valor de Y línea(s). Se registran Z ajuste(s) por rubro en la bitácora."*
2. Revise y haga clic en **Aplicar valor** para confirmar.

Verá *"Valor unitario aplicado"*. El documento se actualiza:

- Las líneas muestran el nuevo valor.
- La barra del documento muestra *"Valor unitario aplicado: $ X.XXX,00 el fecha por usuario"*.
- Los ajustes quedan registrados en la bitácora (solo el administrador los ve).

**El costeo nunca es automático**: hasta que no haga clic en **Aplicar**, nada cambia.

### Casos especiales

#### Entradas parciales de la misma orden

Si la orden tiene **varias entradas de producción** en documentos distintos, el cálculo es acumulativo:

- **Cantidad acumulada** incluye todas las cantidades que ya entró, más la de este documento.
- **Absorbido** es lo que ya se asignó en entradas anteriores (solo información).
- **Por absorber** es lo que queda si hay más entradas pendientes.

El valor propuesto es diferente en cada entrada (se recalcula con la cantidad acumulada hasta ese momento) y se registra en la bitácora con fecha y usuario.

#### Propuesta provisional

Si a la orden le **falta costo de compras** o le **faltan materiales**:

- Verá un aviso naranja: *"Provisional: falta el costo de servicios/materiales"*.
- El valor propuesto está marcado como **Provisional** (no definitivo).
- **Aplicar** le pide que confirme explícitamente que está seguro (*"Confirmo que el valor es provisional"*).
- La bitácora lo registra como provisional.

Cuando registre la compra o la salida que faltaba, puede volver a abrir **Costear producción** y proponer de nuevo.

#### Sin base o costo cero

Si la orden **no tiene ningún costo** (sin materiales, sin servicios, sin receta), o si los ajustes la dejan en cero o negativo:

- Verá un aviso rojo: *"No hay base para costear"* o *"El costo quedó cero o negativo"*.
- **Aplicar** queda deshabilitado.
- Revise: agregue ajustes positivos con motivo, o registre los costos que faltan en compras o inventario.

#### Desfase (cambió algo después de proponer)

Si después de que propuso el costo, **cambió una salida de materiales o una compra de servicios** de la orden:

- Verá un aviso naranja: *"El costo de la OP cambió después de asignar el valor"*.
- La propuesta anterior aparece grisada.
- Los botones permiten **Recalcular** para traer los cambios y hacer una nueva propuesta, sin perder los ajustes que ya hizo.

#### Líneas excluidas (reclasificaciones y traslados)

Algunas líneas de movimiento (reclasificaciones, traslados internos) **no cuentan** en el costeo porque no son costo real de la orden:

- Aparecen omitidas del resumen con una nota: *"Líneas excluidas: X reclasificación/traslado"*.
- No impiden aplicar ni afectan el valor propuesto.

### Errores y avisos

| Aviso / Error | Qué significa | Qué hacer |
|---|---|---|
| **Documento no elegible (periodo cerrado, OP sin líneas, etc.)** | El documento no cumple los requisitos. | Vea el motivo específico. Algunos no se pueden corregir; otros requieren cambiar el documento. |
| **Sin permiso** | No tiene el permiso **Actualizar** sobre Entradas y salidas. | El diálogo se abre en **solo lectura**: puede ver pero no aplicar. Consulte al administrador. |
| **El sistema está ocupado** o **No se pudo cargar el resumen** | Error de conexión o del servidor. | Haga clic en **Reintentar**. |
| **El costo cambió; actualice** | Otro usuario modificó una compra o salida de la orden mientras el diálogo estaba abierto. | Haga clic en **Actualizar** para traer los cambios. Su propuesta y ajustes se conservan. |
| **No se pudo aplicar** | Error al guardar. | Haga clic en **Reintentar** (usa la misma clave de idempotencia, no se duplica). |
| **Tipo sin configuración de costos** | El tipo de documento no está configurado para costear. | Consulte al administrador. |

### Sugerencia: recalcular costos posteriores

Cuando aplica el valor unitario a una entrada de producción, **solo cambia ese documento**. Si más adelante la orden tiene **otras entradas posteriores**, esas también necesitan costeo propio (con la cantidad acumulada que incluya esta entrada).

Además, si después de costear cambian materiales o servicios de la orden, el módulo de **Inventario › Recálculo de costos** permite recalcular todas las salidas e identificar diferencias acumuladas. Ver esa pantalla para ajustes a escala.

### Cambios en tiempo real

Si otro usuario modifica el documento (agrega o cambia líneas) mientras el diálogo está abierto, verá un aviso: *"El documento cambió; actualice"*. Haga clic en **Actualizar** para traer los cambios sin perder los ajustes que ya hizo. El resumen se recalcula al instante.

---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica o elimina movimientos mientras usted trabaja, **no tiene que recargar**:

**En el listado**

- El listado y el resumen se actualizan solos, sin perder filtros, orden ni página; las filas nuevas o modificadas se **resaltan** unos segundos.
- Aparece un aviso como *"Otro usuario creó un movimiento"*, *"… modificó un movimiento"* o *"… eliminó un movimiento"*.

![Aviso de un movimiento creado por otro usuario](../recursos/img/movimientos/19-otro-crea.png)

**En un documento abierto**

- Si otro usuario lo modifica, verá *"Otro usuario modificó este documento"* con **Ver sus cambios**. Al usarlo, la pantalla se actualiza **sin tocar** lo que usted está capturando ni sus líneas en cola.
- Si otro usuario lo elimina, verá *"Este documento fue eliminado por otro usuario"*: ya no se puede guardar. Sus líneas sin guardar se pueden llevar a un documento nuevo con **Duplicar**.
- Si otro usuario lo cierra o anula mientras usted captura, las líneas pendientes muestran *"El documento ya no se puede modificar (lo cerró, anuló o eliminó otro usuario)."*

**Conflictos.** Si usted cambia una línea que otro usuario acaba de cambiar, la línea queda **En conflicto** con el valor actual (*"Otro usuario cambió esta línea (ahora 8 un)"*) y dos opciones: **Usar la actual** (descarta su cambio) o **Aplicar mi cambio sobre la actual**. Si la línea fue quitada, verá *"Otro usuario quitó esta línea"*.

![Línea en conflicto](../recursos/img/movimientos/20-conflicto.png)

Si el conflicto es en el **encabezado**, verá *"Otro usuario cambió el encabezado"* con quién y a qué hora, y las opciones **Recargar encabezado** o **Aplicar mis cambios** (lo que usted escribió se conserva para volver a aplicarlo).

> ℹ️ Junto al estado verá **En vivo** mientras la conexión esté activa y **Reconectando…** si se interrumpe. Sin conexión en vivo la pantalla funciona igual; los cambios de otros se ven al recargar. Los cambios que usted hace en esta misma pestaña no generan avisos.

---

## 🕵️ Bitácora (solo administradores)

> 🚧 La pestaña **Bitácora** se habilita en una próxima entrega y mientras tanto muestra *"Disponible en la próxima entrega"*. El interruptor **Documentos eliminados** del listado todavía no aparece. Esta sección describe cómo van a funcionar.

Los **administradores de la compañía** ven la pestaña **Bitácora** en cada documento: quién creó, cambió, cerró, anuló, imprimió o eliminó el movimiento y sus líneas, y cuándo.

![Bitácora de un movimiento](../recursos/img/movimientos/21-bitacora.png)

- **Filtros**: **Periodo** (Último mes, Últimos 3 meses, Todo), **Acción** (Creó, Modificó, Eliminó), **Qué** (Encabezado, Línea, Cierre, Impresión, Anulación, Eliminación del documento), **Usuario** y **Línea**.
- **Ver el detalle** (ojo) muestra cada campo **Antes** y **Después**; **Mostrar todos los campos** incluye los que no cambiaron.
- Los registros marcados **Versión anterior** los guardó la versión anterior de OrangeERP: se muestra lo que guardó, sin comparar campos.
- Si alguien cambia el documento mientras usted mira la bitácora, verá *"Hay cambios nuevos en este movimiento."* con **Actualizar**.
- Debajo de los filtros se indica desde qué fecha conserva cambios la bitácora.

![Detalle de un cambio](../recursos/img/movimientos/22-bitacora-detalle.png)

**Documentos eliminados.** En el listado, el interruptor **Documentos eliminados** muestra los documentos eliminados en el rango de fechas, con quién y cuándo los eliminó. **Ver bitácora** abre la bitácora de ese documento en solo lectura.

![Bitácora de un documento eliminado](../recursos/img/movimientos/23-documentos-eliminados.png)

Si su usuario no es administrador, no verá la pestaña ni el interruptor.

---

## ❓ Preguntas frecuentes

**No veo el botón Importar.**
Necesita los permisos **Crear** y **Exportar** sobre Entradas y salidas. Consulte a su administrador.

**Mi archivo tiene un error en una fila: ¿se crean los demás documentos?**
No. Con una fila con error no se puede aplicar: corrija el archivo y vuelva a cargarlo. Ver [Importar](#-importar-entradas-y-salidas-desde-excel).

**Apliqué y la pantalla dice "En proceso". ¿Tengo que esperar?**
No. Puede salir: el resultado llega a la campana y puede volver a abrir la importación.

**Fallaron algunos documentos, ¿se pierden los que sí se aplicaron?**
No. Cada documento es una transacción propia. Use **Reintentar pendientes**: solo se procesan los que faltan, sin duplicar.

**Envié el archivo otra vez y no se creó otro proceso.**
Es lo esperado: dentro de 10 minutos el mismo archivo reutiliza el proceso en curso. Si ya hubo un resultado parcial verá el aviso 409 IMPORT_PARCIAL.

**¿Cuántos documentos puedo aplicar por archivo?**
Hasta 200 documentos y 5.000 líneas. Los archivos grandes pueden tardar; por eso la aplicación es en segundo plano.

**¿Los documentos importados quedan cerrados?**
No. Quedan **Abiertos**; ciérrelos desde el listado.

**¿Tengo que guardar el documento al final?**
No. Cada línea se guarda al confirmarla. Lo único que puede hacer al final es **Cerrar transacción**, para que nadie lo modifique.

**Cerré la pestaña con líneas "En cola" o con error. ¿Se guardaron?**
No. Solo quedan registradas las líneas con número (**N.º**). Abra el documento desde el listado, revise qué líneas tiene y vuelva a capturar las que falten.

**Leí dos veces el mismo producto y solo veo una línea.**
Es lo esperado: las lecturas iguales se **suman** a la misma línea (*"Sumada a la línea N"*). Revise la cantidad de esa línea.

**Una línea dice "No se guardó". ¿Si reintento se duplica?**
No. Antes de reenviarla, el sistema comprueba si ya había quedado guardada (*"La línea ya estaba guardada; no se reenvió."*).

**Me dice "La existencia quedaría en −1", pero en la versión anterior sí me dejaba.**
En esta versión las existencias negativas y el periodo cerrado se validan **siempre en el servidor**, línea por línea, salvo que el tipo de movimiento permita negativos. Revise la existencia de la bodega (se ve en la captura) o registre primero la entrada.

**Las cantidades con decimales se redondeaban antes.**
Ahora se aceptan hasta **4 decimales** y se respetan en la existencia, en la contabilidad y en el formato impreso.

**No puedo cambiar el tipo de movimiento.**
El tipo se bloquea al guardar la primera línea. Si se equivocó de tipo, elimine el documento (o anúlelo si ya está cerrado) y créelo de nuevo; **Duplicar** le ahorra volver a capturar las líneas.

**Cambié la fecha del documento y el valor de las líneas no cambió.**
Es lo esperado: cambiar la fecha no recalcula el valor de las líneas ya guardadas. Si necesita el costo de la nueva fecha, cambie el valor de cada línea o duplique el documento.

**¿Anulo o elimino?**
Anule si el documento está cerrado o si necesita dejar evidencia; elimine solo documentos hechos por error que no tengan nada relacionado. Ver la tabla de *Anular o eliminar*.

**El formato impreso no es el que espero.**
Revise qué formato tiene configurado el tipo de movimiento (la barra de impresión lo indica). Si el tipo no tiene uno válido, se usa FRT-INV-001.

**Veo "Disponible en la próxima entrega" en Adjuntos o en Bitácora.**
Esas dos pestañas se habilitan en una próxima entrega. Todo lo demás (capturar y guardar líneas, cambiar el encabezado, cerrar, anular, eliminar, duplicar e imprimir) ya funciona. Mientras tanto, para adjuntar soportes o revisar quién cambió un documento, use la versión anterior de OrangeERP.

**No veo "En vivo".**
La conexión en vivo no está disponible en este momento (por ejemplo, por la red de su empresa). La pantalla funciona igual; para ver cambios de otros usuarios, recargue la página.
