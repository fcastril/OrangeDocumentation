[Regresar a Compras](../readme.md)

---

# 🏭 Proveedores

![Static Badge](https://img.shields.io/badge/Tipo-MaestroTipoII-red)
![Static Badge](https://img.shields.io/badge/Module-Compras-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Proveedores-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## 📋 Descripción

Los **proveedores** son los terceros a quienes la compañía les compra bienes o servicios. Cada proveedor tiene su ficha con los datos de identificación, la información tributaria, las condiciones comerciales (descuento, plazos, cupo de crédito y retenciones), sus contactos, un logo y los documentos adjuntos.

En esta pantalla puede **consultar, crear, editar y eliminar** proveedores, y **exportar** el listado a Excel. Trabaje siempre con la compañía que aparece en el título de la pestaña.

> 📘 La búsqueda, el orden, la paginación y la ayuda funcionan igual en todas las tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Una persona puede ser **proveedor y comprador** a la vez. Los datos del tercero (documento, nombre, logo y adjuntos) son los mismos en ambas pantallas; ver [Compradores](compradores.md).

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Compras**.
2. En **Maestros**, haga clic en **Proveedores**.

Para ver la pantalla necesita el permiso **Consultar** sobre la opción Proveedores. Los demás botones dependen de los permisos que le haya dado el administrador (ver la tabla más abajo).

La pantalla tiene las pestañas **Proveedores** y **Cartera**. La pestaña **Cartera** aparece solo si tiene el permiso **Consultar** sobre la opción *Cartera Terceros*. Su manual está en [Cartera de proveedores](cartera-proveedores.md).

---

## 🖥️ Pantalla principal

![Listado de proveedores](../recursos/img/proveedores/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. Ver *Cambios de otros usuarios* más abajo. |
| **Nuevo proveedor** | Abre la ficha para crear un proveedor. |
| **Buscar por documento o nombre** | Filtra el listado mientras escribe. No distingue mayúsculas ni tildes. |
| **Exportar a Excel** | Descarga los proveedores que cumplen la búsqueda actual. Ver la sección *Exportar a Excel* más abajo. |
| **Importar** | Abre la página para cargar proveedores desde un archivo de Excel. Solo aparece en Proveedores y con el permiso **Exportar**. Ver *Importar desde Excel* más abajo. |
| **Lápiz** / **Papelera** | Editar o eliminar el proveedor de esa fila. Siempre están en la **primera columna**. Si no tiene permiso para editar, el lápiz dice **Ver** y abre la ficha en solo lectura. |
| **Encabezados** | Un clic ordena de forma ascendente, el segundo descendente y el tercero quita el orden. |
| **Filas por página** y paginación | Cambian cuántos proveedores ve por página (10, 20, 50 o 100) y la página. |

Las columnas del listado son: **Nro. documento**, **Nombre completo**, **Nombre comercial**, **Activo** y **Última modificación**.

> 📱 En pantallas pequeñas el listado se ajusta al ancho disponible y las acciones quedan visibles en cada fila.

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil sobre la opción Proveedores:

| Permiso | Qué habilita |
|---------|--------------|
| Consultar | Ver el listado, abrir la ficha y ver el logo y los adjuntos. |
| Crear | **Nuevo proveedor**, agregar contactos, subir el logo y los adjuntos. |
| Actualizar | Editar la ficha, editar contactos, reemplazar o quitar el logo, subir o quitar adjuntos. |
| Eliminar | **Papelera**, quitar contactos y eliminar adjuntos. |
| Exportar | **Exportar a Excel**. |

Si solo tiene **Consultar**, la ficha aparece con el aviso *"Solo tienes permiso de consulta: la ficha no se puede modificar."*

---

## ➕ Crear un proveedor

1. Haga clic en **Nuevo proveedor**.
2. Escriba el **Tipo de documento** y el **Número de documento**. Mientras escribe, el sistema revisa si ese documento ya está registrado en la compañía (ver el paso siguiente).
3. Complete las secciones de la ficha y haga clic en **Guardar**.

![Crear proveedor](../recursos/img/proveedores/02-crear.png)

La ficha tiene tres pestañas:

| Pestaña | Qué incluye |
|---------|-------------|
| **Tercero** | Identificación (tipo y número de documento, nombre o razón social, género), ubicación y contacto (dirección, ciudad, teléfono, celular, correo, página web), información tributaria (régimen, actividad económica, cuenta contable, resolución, gran contribuyente, autorretenedor) y estado (activo, observaciones). También tiene el **logo** y los **adjuntos**. |
| **Proveedor** | Condiciones comerciales (descuento comercial, días de plazo de factura y de orden de compra, tipo de movimiento de compras y de gastos), impuestos y retenciones (realiza IVA, retefuente, reteIVA, ICA u otra retención) y crédito y pagos (cupo de crédito, días de mora, banco, tipo y número de cuenta bancaria, pago electrónico). |
| **Contactos** | Las personas con quienes se trata en el proveedor. Ver la sección *Contactos* más abajo. |

**Fecha de nacimiento** (pestaña Proveedor, en Condiciones comerciales): elíjala en el calendario o escríbala. Debe estar entre **1753-01-01** y hoy; fuera de ese rango, el campo muestra *"La fecha de nacimiento debe estar entre 1753-01-01 y hoy."* y no guarda. Si la deja vacía, se guarda 1753-01-01.

**Número de cuenta bancaria** (pestaña Proveedor, en Crédito y pagos): admite hasta **20 caracteres**; con más, verá *"El número de cuenta admite hasta 20 caracteres."*. Con permiso para **Actualizar** lo ve y lo edita completo. Si solo tiene consulta, el número aparece **enmascarado** con los últimos 4 dígitos (por ejemplo, `****1234`). El número completo nunca se registra en el historial de cambios.

Los campos obligatorios se marcan en la ficha. Si falta algún dato o un valor no es válido, la pestaña aparece con un contador de errores (por ejemplo, **2 errores**) y el campo muestra el motivo, como *"Escribe un valor numérico válido."*, *"Debe estar entre 0 y 100."* o *"Elige el impuesto o desmarca la casilla."*. Corríjalo y guarde de nuevo.

Al guardar verá el mensaje **"Proveedor … creado."** y el proveedor aparece en el listado.

### Verificar el documento antes de crear

Cuando escribe el número de documento (entre 5 y 20 caracteres) y deja el campo, el sistema verifica si ese documento ya existe en la compañía. Verá uno de estos avisos:

| Aviso | Qué significa | Qué puede hacer |
|-------|---------------|-----------------|
| *"Verificando si el documento ya está registrado…"* | La revisión está en curso. | Espere un momento. |
| *"Este documento ya existe en la compañía como {nombre} ({roles})."* y *"Se cargó la información registrada…"* | El tercero ya existe con otro perfil (cliente, empleado u otro). **No se duplica.** La ficha se llena con sus datos. | Revise los datos precargados y haga clic en **Guardar**: el tercero se agrega como proveedor sin crear otro. |
| *"Este documento ya es proveedor en la compañía."* y *"{nombre} ya está registrado con este documento."* | Ya tiene este perfil. | Haga clic en **Abrir su edición** para modificarlo. La ficha se abre directamente, sin preguntar nada: lo que escribió en el documento no cuenta como cambio. |
| *"No se pudo verificar el documento…"* | La revisión falló por la conexión. | Haga clic en **Reintentar**, o guarde: el sistema lo verifica otra vez al guardar. |

![Documento ya registrado con otro perfil](../recursos/img/proveedores/03-reutilizar-tercero.png)

Si cambia el número de documento después de haber cargado un tercero existente, la información precargada se quita y la verificación se repite.

> ⚠️ Si otro usuario crea ese mismo tercero mientras usted llena la ficha, al guardar el sistema vuelve a revisar el documento: carga la información registrada en la ficha y le pide revisarla y guardar otra vez. Si el sistema no puede cargar el tercero registrado con ese documento, verá *"Este documento ya lo usa otro tercero de la compañía."* El sistema nunca crea dos terceros con el mismo documento.

---

## ✏️ Editar un proveedor

1. Haga clic en el **lápiz** del proveedor (o en **Ver** si solo tiene consulta).
2. Cambie los datos y haga clic en **Guardar**.

En un proveedor guardado, la ficha suma pestañas de solo consulta (en ellas no hay **Guardar**):

| Pestaña | Para qué sirve | Vea |
|---------|----------------|-----|
| **Órdenes y compras** | Órdenes de compra y compras del proveedor. | [Órdenes y compras](#-órdenes-y-compras-del-proveedor) |
| **Cumplimiento de OC** | Si las órdenes llegaron a tiempo y completas. | [Cumplimiento de OC](#-cumplimiento-de-oc) |
| **Cartera** | Cartera del proveedor (con permiso sobre *Cartera Terceros*). | [Cartera de proveedores](cartera-proveedores.md) |
| **Indicadores** | Saldos y vencimientos, y la evaluación I1 e I2 del proveedor. | [Indicadores](#-indicadores-del-proveedor) |

Si le falta el permiso de un bloque dentro de **Órdenes y compras** o **Cumplimiento de OC**, ese bloque muestra el aviso *"Sin permiso de …"* con el nombre de la opción que le falta, y el resto de la ficha sigue disponible. Las pestañas **Cartera** e **Indicadores** solo aparecen con su permiso.

Los cambios se guardan cuando hace clic en **Guardar**. Si sale de la ficha con cambios sin guardar, el sistema pregunta **"¿Salir sin guardar?"**: **Seguir editando** lo deja en la ficha; **Salir sin guardar** descarta los cambios.

Si otro usuario modificó el mismo proveedor mientras lo edita, vea *Cambios de otros usuarios* más abajo.

---

## 📇 Contactos

Los contactos se agregan dentro de la pestaña **Contactos** de la ficha del proveedor.

1. Escriba el **nombre del contacto** (obligatorio), el **tipo de contacto**, el teléfono, el celular, el correo y la ciudad.
2. Haga clic en **Agregar contacto**.

![Contactos del proveedor](../recursos/img/proveedores/04-contactos.png)

- **Los contactos se guardan al instante**: no hace falta pulsar **Guardar** en la ficha.
- El nombre y el tipo de contacto se guardan en **MAYÚSCULAS**.
- Para cambiar un contacto, haga clic en su **lápiz**, modifique los datos y pulse **Actualizar contacto**. Para cancelar, **Cancelar edición**.
- Para quitar un contacto, haga clic en la **papelera** de la fila y confirme con **Quitar contacto**. Esta acción no se puede deshacer.

> ℹ️ La pestaña **Contactos** solo se usa cuando el proveedor ya está guardado: si es nuevo, primero guarde la ficha. El aviso dice *"Guarda el proveedor para poder agregar contactos."*

---

## 🖼️ Logo y adjuntos

El **logo** y los **adjuntos** están en la pestaña **Tercero** de la ficha. Son los mismos para el proveedor y el comprador de un mismo tercero. Se suben al instante, así que el proveedor debe estar guardado antes (el aviso dice *"Guarda el tercero para poder subir el logo y los adjuntos."*).

![Logo y adjuntos](../recursos/img/proveedores/05-logo-adjuntos.png)

### Logo

| Regla | Detalle |
|-------|---------|
| Formatos | JPG, JPEG o PNG. |
| Tamaño | Hasta 2 MB. |
| Acciones | **Subir o reemplazar el logo** y **Quitar logo** (con confirmación). |

El logo queda guardado aunque edite otros datos del tercero y no lo vuelva a subir.

### Adjuntos

| Regla | Detalle |
|-------|---------|
| Formatos | JPG, JPEG, PNG, DOC, XLS o PDF. |
| Tamaño por archivo | Hasta **2 MB** por archivo. |
| Cupo por tercero | **10 MB** en total para todos los adjuntos del tercero. La lista muestra *"Cupo de adjuntos usado: X de 10 MB"*. |
| Descripción | Obligatoria, de 1 a 200 caracteres. |

Para agregar un adjunto: escriba la **descripción**, elija el **archivo** y haga clic en **Agregar adjunto**. En la lista puede **Descargar** cada archivo o **Eliminar** el adjunto (con confirmación: *"Se eliminará el adjunto …"*).

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"El logo debe ser JPG, JPEG o PNG."* / *"El adjunto debe ser JPG, JPEG, PNG, DOC, XLS o PDF."* | Use un archivo de un tipo permitido. |
| *"El archivo supera el máximo de 2 MB."* | Reduzca el tamaño del archivo. |
| *"Con este archivo se superaría el cupo de 10 MB por tercero."* | Elimine adjuntos que ya no necesite o reduzca el archivo. |
| *"El archivo está vacío."* | Elija otro archivo. |
| *"Escribe una descripción de 1 a 200 caracteres."* | Escriba la descripción del adjunto. |
| *"El archivo ya no existe."* | Actualice la pantalla: alguien más pudo eliminarlo. |

---

## 🗑️ Eliminar un proveedor

Hay dos formas de empezar: la **papelera** de la fila en el listado, o el botón **Eliminar** al final de la ficha.

Antes de borrar, el sistema confirma con **Eliminar proveedor** y le muestra el documento. Según el caso, verá una de estas situaciones:

| Situación | Qué ocurre |
|-----------|------------|
| El tercero **solo es proveedor**. | Se elimina el proveedor. Mensaje: *"Proveedor … eliminado."* |
| El tercero **también es cliente, empleado u otro perfil**. | El aviso dice *"Este tercero también es {roles}. Solo se retirará su condición de proveedor; el tercero se conserva."* Se retira la condición de proveedor y **el tercero se conserva** con sus otros perfiles. Mensaje: *"Se retiró la condición de proveedor de …; el tercero se conserva."* |
| El proveedor **tiene información relacionada** (compras, referencias asociadas). | No se puede eliminar. El diálogo muestra: *"… tiene información relacionada (compras, referencias asociadas) y no se puede eliminar."* Si la pantalla da un motivo, aparece como **Motivo**. Cierre el diálogo: el proveedor no cambia. |

Cuando se elimina el proveedor de verdad, también se borran sus contactos, su logo y sus adjuntos. Si solo se retira la condición de proveedor, el tercero, su logo y sus adjuntos se conservan.

![Confirmar eliminación](../recursos/img/proveedores/06-confirmar-eliminar.png)

![Proveedor con información relacionada](../recursos/img/proveedores/07-en-uso.png)

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"No tienes permiso para realizar esta acción con proveedores."* | Pida el permiso de **Eliminar** a su administrador. |
| *"El proveedor ya no existe. Se quitó del listado."* | Otro usuario lo eliminó. El listado ya se actualizó. |
| *"No se pudo eliminar. Inténtalo de nuevo."* | Revise la conexión e intente otra vez. |

---

## 📤 Exportar a Excel

Haga clic en **Exportar a Excel**. Se descarga el archivo con los proveedores que cumplen la **búsqueda** y el **orden** que tiene en pantalla, de todas las páginas (no solo la visible).

- El archivo puede tener **hasta 10.000 filas**. Si la búsqueda tiene más resultados, verá el aviso *"Hay más de 10.000 proveedores: acota la búsqueda para exportar."* Escriba más texto en el buscador (documento o nombre) para reducir la lista y vuelva a exportar.
- Si la exportación falla por la conexión, verá *"No se pudo exportar los proveedores. Inténtalo de nuevo."*
- Los avisos de exportar se quitan cuando inicia otro intento, cuando la exportación sale bien o cuando cambia la búsqueda o el orden.

---

## 📥 Importar desde Excel

Use esta función cuando tenga muchos proveedores en una hoja de cálculo y quiera cargarlos de una vez. Antes de guardar, el sistema le muestra qué se va a crear, qué se va a convertir y qué se va a actualizar. **Nada se guarda hasta que haga clic en Aplicar.**

> ℹ️ Esta importación es solo para **proveedores**. Los compradores se importan desde su propia página, con el mismo procedimiento: ver [Compradores](compradores.md#-importar-desde-excel).

Para importar necesita el permiso **Exportar** sobre la opción Proveedores. Si no lo tiene, el botón **Importar** no aparece en el listado.

### Antes de empezar

| Regla | Detalle |
|-------|---------|
| Formato | Archivo de Excel **.xlsx**. Solo se lee la **primera hoja**. |
| Tamaño | Hasta **1 MB** por archivo. |
| Filas | Hasta **1.000** filas con datos. Si tiene más, divídalo en varios archivos. |
| Columnas | Las columnas se reconocen por su **encabezado** (el nombre de la fila 1), no por su posición. Use la plantilla para no equivocarse. |
| Documento | La columna **Documento** es obligatoria: sin ella el archivo no se puede usar. |

### Paso a paso

**Paso 1. Cargar archivo**

1. En el listado de **Proveedores**, haga clic en **Importar**.
2. Haga clic en **Descargar plantilla**. Se descarga un archivo de Excel con las columnas de la importación, una fila de ejemplo en la fila 2 y una nota en cada encabezado.
3. Llene la plantilla: escriba un proveedor por fila, empezando en la fila 2. **Borre la fila de ejemplo** o reemplácela por sus datos. Las filas vacías se omiten.
4. Haga clic en **Seleccionar archivo** (o arrastre el archivo a la zona punteada) y elija su archivo .xlsx.

![Cargar archivo](../recursos/img/proveedores/importar-01-cargar-archivo.png)

El sistema lee el archivo en su equipo y lo revisa. Si no se puede usar, verá uno de estos avisos:

| Aviso | Qué hacer |
|-------|-----------|
| *"El archivo no es un .xlsx válido."* | Guarde el archivo como **Libro de Excel (.xlsx)** y vuelva a cargarlo. |
| *"No se encontró la columna «Documento». Usa la plantilla."* | Copie sus datos en la plantilla descargada, sin cambiar los encabezados. |
| *"El archivo no tiene filas con datos."* | Escriba los proveedores debajo de los encabezados. |
| *"El archivo tiene N filas; el máximo es 1.000."* | Divida el archivo en varias partes de 1.000 filas o menos. |
| *"El archivo pesa más de 1 MB."* | Quite columnas o filas que no use, o divídalo. |

![Archivo no válido](../recursos/img/proveedores/importar-02-archivo-invalido.png)

**Paso 2. Revisar (vista previa)**

Cuando el archivo está bien, el sistema compara cada fila con los terceros de la compañía y le muestra el resultado. **Esta revisión no guarda nada.**

- Los **indicadores** arriba muestran cuántas filas son **Nuevos**, **Se convierten**, **Se actualizan**, **Sin cambios** y **Con error**.
- Los **filtros** (Todas, Nuevo, Se actualiza, Existe como tercero, Sin cambios, Error) muestran solo las filas de ese estado.
- Cada fila muestra su **número de fila** del archivo, el **documento**, el **nombre** y el **estado**. Las filas con error muestran el motivo.
- Con el **buscador** puede buscar por documento o nombre.

![Vista previa](../recursos/img/proveedores/importar-03-vista-previa.png)

**Paso 3. Aplicar**

1. Revise la vista previa. Si hay filas con error, puede corregirlas (ver la sección siguiente) o aplicar las demás.
2. Haga clic en **Aplicar N cambios**. El número cuenta las filas **Nuevos**, **Se convierten** y **Se actualizan**.
3. Espere el indicador **Aplicando…**. Al terminar verá la pantalla **Importación terminada** con el resumen.

En la pantalla de resultado puede **Ver el listado** o **Importar otro archivo**. El listado de proveedores se actualiza con los cambios aplicados.

![Resultado de la importación](../recursos/img/proveedores/importar-06-resultado.png)

Otros botones de la página:

| Botón | Qué hace |
|-------|----------|
| **Cambiar archivo** | Vuelve al paso 1 para cargar otro archivo. Lo que revisó antes se descarta. |
| **Descargar filas con error** | Descarga solo las filas con error, para corregirlas en Excel. |
| **Cancelar** / **Cargar otro archivo** | Sale de la importación sin guardar nada. |

> ℹ️ Si la vista previa dice *"Nada que aplicar: todas las filas están sin cambios o con error."*, el botón **Aplicar** queda deshabilitado: no hay nada que guardar.

### Todo o nada

Al aplicar, el sistema guarda **todas las filas válidas juntas**, en una sola operación:

- Si todo sale bien, se guardan todas las filas **Nuevos**, **Se convierten** y **Se actualizan**.
- Si ocurre un fallo del servidor, **no se guarda ninguna fila**. Verá *"No se pudo completar. No se guardó ningún cambio. Inténtalo de nuevo."* y puede reintentar.
- Las filas con **error** no se guardan, pero **no bloquean** a las demás: las filas válidas sí se aplican. Corrija las filas con error y vuelva a cargar el archivo cuando quiera.
- La importación **nunca borra** proveedores ni datos que no estén en el archivo.

El resultado muestra cuántos fueron **nuevos**, **convertidos**, **actualizados**, **sin cambios** y **con error**.

### Estados de cada fila

| Estado | Qué significa | Qué pasa al aplicar |
|--------|---------------|---------------------|
| **Nuevo** | El documento no está registrado en la compañía. | Se crea el proveedor. |
| **Existe como tercero** (se convierte) | El documento ya está registrado con otro perfil (por ejemplo, cliente o empleado). | Se agrega la condición de **proveedor** al tercero existente. **No se duplica.** Si el nombre del archivo es distinto del registrado, la fila muestra *"Actual: …"* con el nombre actual. |
| **Se actualiza** | Ya es proveedor y el archivo cambia algún dato. | Se actualizan los datos que cambiaron. |
| **Sin cambios** | Ya es proveedor y el archivo no cambia nada. | No se escribe nada. |
| **Error** | La fila tiene un problema que hay que corregir. | No se guarda. Ver *Errores por fila* más abajo. |

### Qué significa una celda vacía

Una celda vacía significa **sin dato**. Lo que pasa depende de si el proveedor es nuevo o ya existe:

| Caso | Qué ocurre con la celda vacía |
|------|-------------------------------|
| **Dato obligatorio** (por ejemplo, Documento, Tipo de documento, Primer nombre, Dirección, Ciudad, Teléfono, Celular, Correo y Régimen tributario) | Si el proveedor es **nuevo**, la fila tiene error. Si el tercero **ya existe**, se conserva el dato registrado. |
| **Dato opcional** y proveedor **nuevo** | Se usa el valor por defecto: por ejemplo, **Dígito de verificación** vacío queda como NA, **Nombre comercial** vacío toma el nombre completo, **Activo** vacío queda en Sí y **Realizar IVA** (u otro impuesto) con su código queda en Sí. |
| **Dato opcional** y tercero **que ya existe** | Se **conserva** lo que ya está registrado. Una celda vacía no borra datos. |

Para **borrar** un dato que ya existe, no use la importación: modifique el proveedor en su ficha.

### Errores por fila y cómo corregirlos

Cada fila con error muestra el motivo en el paso de revisión. Corrija la celda indicada en Excel y vuelva a cargar el archivo.

| Mensaje | Qué significa | Cómo corregirlo |
|---------|---------------|-----------------|
| *"La fila está vacía."* | La fila no tiene datos. | Borre la fila o escriba los datos del proveedor. |
| *"Falta el número de documento."* | La columna **Documento** está vacía. | Escriba el número de documento. |
| *"El documento debe tener entre 5 y 20 caracteres."* | El documento es muy corto o muy largo. | Revise el número, sin espacios ni texto adicional. |
| *"Documento repetido en el archivo (filas N)."* | El mismo documento aparece en dos o más filas del archivo. | Deje una sola fila por documento o corrija el número de la que sobra. |
| *"Falta un dato obligatorio: {campo}."* | Un dato obligatorio está vacío en un proveedor nuevo. | Complete la celda del campo indicado. |
| *"El dato es demasiado largo: {campo}."* | El texto supera el máximo permitido. | Acorte el texto. |
| *"El dato no es válido: {campo}."* | El formato no es correcto (un número, un sí/no, un porcentaje o un correo). | Revise el formato del campo. Ver los valores aceptados abajo. |
| *"El código no existe en la compañía: {campo}."* | El código (ciudad, actividad económica, cuenta contable, banco, tipo de movimiento o impuesto) no está en la compañía. | Use el código tal como aparece en las tablas de la compañía, o consulte con su administrador. |
| *"La fila tiene un error."* | El error no tiene un mensaje específico. | Revise la fila completa y vuelva a validar. |

Formatos aceptados en los campos:

- **Sí/No**: escriba `1`, `0`, `Sí`, `No`, `S`, `N`, `true`, `false`, `verdadero`, `falso` o `x`.
- **Números**: use punto o coma como separador decimal, sin separador de miles.
- **Descuento comercial**: porcentaje de 0 a 100 (por ejemplo, `5` para 5 %).
- **Días**: de 0 a 9999.
- **Correo**: uno o varios correos separados por `;` o `,`.
- **Tipo de cuenta bancaria**: `A` (ahorros), `C` (corriente) o vacío.

Los campos **Otra retención** y **Fecha de nacimiento** no se importan: se conservan como están en el tercero.

### Conflicto: "Volver a validar"

La vista previa es una foto del momento en que la revisó. Si mientras tanto otra persona cambia proveedores o crea el mismo documento, puede pasar lo siguiente:

| Aviso | Qué significa | Qué hacer |
|-------|---------------|-----------|
| *"Otro usuario cambió proveedores mientras revisabas. Vuelve a validar antes de aplicar."* | Hubo cambios en la compañía mientras revisaba. La vista previa ya no es confiable. | Haga clic en **Volver a validar**. El sistema revisa el archivo otra vez. |
| *"Los datos cambiaron. Otro usuario creó el documento o el perfil mientras revisabas, y no se guardó nada. Vuelve a validar antes de aplicar."* | Al aplicar, un documento ya no era el mismo: no se guardó nada. | Haga clic en **Volver a validar** y revise de nuevo la vista previa antes de aplicar. |

Con **Volver a validar** no se pierde el archivo: el sistema vuelve a leer lo que cargó. Si el error no es de datos sino de conexión, use **Reintentar**.

![Conflicto al aplicar](../recursos/img/proveedores/importar-07-conflicto.png)

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"Importar requiere el permiso de exportar."* | Pida el permiso **Exportar** a su administrador. |
| *"No se pudo descargar la plantilla. Inténtalo de nuevo."* | Revise la conexión y pulse **Descargar plantilla** otra vez. |
| *"El servidor no aceptó las filas del archivo (vacío, más de 1.000 filas o numeración repetida). Revisa el archivo."* | Revise el archivo con las reglas de *Antes de empezar*. |
| *"El archivo es demasiado grande para enviarlo (máximo 2 MB de datos). Divídelo en partes."* | Divida el archivo en varias partes. |
| *"No se pudo completar. No se guardó ningún cambio. Inténtalo de nuevo."* | Pulse **Reintentar**. Nada quedó a medias. |


---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica o elimina proveedores mientras usted tiene abierto el listado, **no tiene que recargar**: el listado se pone al día solo, sin perder lo que buscó, el orden ni la página.

- Las filas nuevas o modificadas se **resaltan** unos segundos.
- Abajo a la derecha aparece un aviso, por ejemplo *"Otro usuario creó el proveedor …"*.
- Junto a la descripción verá **En vivo** mientras la conexión esté activa. Si se interrumpe, dice **Reconectando…**; al volver, la pantalla se actualiza sola.

**Si estaba editando ese mismo proveedor:**

| Qué hizo el otro usuario | Qué verá | Qué puede hacer |
|--------------------------|----------|-----------------|
| Lo modificó | *"Otro usuario modificó este proveedor mientras lo editabas. Si guardas, reemplazarás sus cambios."* | **Ver sus cambios** para cargar lo que él guardó, o **Guardar** para dejar lo suyo. |
| Lo eliminó | *"Otro usuario eliminó este proveedor. Ya no se puede guardar."* | **Cancelar**. El botón Guardar queda deshabilitado. |

Si estaba por confirmar la eliminación de un proveedor que otro ya eliminó, el diálogo se cierra con el aviso *"Otro usuario ya eliminó el proveedor …"*.

> ℹ️ Los cambios que usted hace en esta misma pestaña no generan avisos.

**Terceros que son proveedor y comprador.** Si el tercero tiene los dos perfiles, un cambio en su ficha (crear, editar, convertir, eliminar o retirar un perfil, contactos o importar) también aparece en vivo en la pantalla de [Compradores](compradores.md), y viceversa. Si se retira un perfil, el aviso llega a las dos pantallas cuando el tercero tenía ambos perfiles antes del cambio.

---

## 🔖 Identificar los documentos

Las pantallas de Proveedores muestran cada documento con su **identificador**, y debajo, en letra pequeña, su **Doc. Referencia**.

![Documento con su Doc. Referencia](../recursos/img/proveedor-documento-referenciado/01-con-doc-referencia.png)

**Cómo leer el identificador.** Tiene tres partes: el **código del tipo**, el **prefijo** y el **consecutivo**. Por ejemplo, **CMP-1-1025** es un documento del tipo CMP, con prefijo 1 y consecutivo 1025. Si el tipo no usa prefijo, el identificador es solo código y consecutivo, como **OC-0101**.

**Pase el mouse sobre el identificador** para ver el **nombre del tipo de documento** (por ejemplo, *Compra*). En las compras y en las órdenes, el identificador es un enlace: haga clic para abrir el documento.

**Qué es el Doc. Referencia.** Es un texto libre que se escribe al capturar el documento, con **hasta 20 caracteres**. Por ejemplo, el número de la factura o del pedido del proveedor. Puede repetir el consecutivo o ser muy corto; la pantalla lo muestra **tal cual**, sin cambiarlo. **No es un enlace.** Si el documento no tiene Doc. Referencia, verá **—**.

**Dónde aparece:**

| Pantalla | Qué muestra |
|----------|-------------|
| **Órdenes y compras** | Cada orden de compra con su Doc. Referencia debajo del número. En **Compras y devoluciones**, la columna **Órdenes ligadas** muestra las órdenes a las que está ligada cada compra. |
| **Cumplimiento de OC** | Cada recepción de una línea, con su documento (identificador y Doc. Referencia). |
| **Indicadores › Evaluación, I1** | Las líneas de *Líneas que explican el I1*, con el documento de cada recepción. |
| **Indicadores › Evaluación, I2** | Los documentos de *Documentos que explican el I2*, con su identificador y su Doc. Referencia. |

![Órdenes con su Doc. Referencia](../recursos/img/proveedor-ordenes-compras/01-ordenes-y-compras.png)

---

## 🧾 Órdenes y compras del proveedor

En la ficha de un proveedor guardado, la pestaña **Órdenes y compras** muestra, sin salir de la ficha, las órdenes de compra del proveedor y sus compras y devoluciones. Son los mismos listados de **Órdenes de compra** y de **Compras y devoluciones**, filtrados por este proveedor. Es de solo consulta.

| Bloque | Permiso necesario |
|--------|-------------------|
| Pestaña **Órdenes y compras** | Consultar sobre **Proveedores** |
| **Órdenes de compra** | Consultar sobre **Órdenes de compra** |
| **Compras y devoluciones** | Consultar sobre **Compras y devoluciones** |

**Órdenes de compra.** Columnas: orden, valor, fecha, fecha de entrega, estado (abierta, cerrada o anulada) y recepción (sin recibir, recibida parcial o recibida). La **fecha de entrega** es la fecha de la orden más sus días de plazo; si la orden no tiene plazo, dice *Sin plazo pactado*. Filtre por estado, recepción, periodo o texto. **Abrir** lleva a la orden.

**Compras y devoluciones.** Columnas: documento, valor, fecha, naturaleza (compra o devolución), estado y órdenes ligadas. Filtre por naturaleza, por *con* o *sin orden de compra*, por periodo o por texto. **Abrir** lleva al documento.

**Periodo.** Filtra por la fecha del documento. Por defecto son los últimos 365 días terminados ayer; el periodo no puede superar 366 días. Cambie las fechas y pulse **Actualizar**.

![Órdenes y compras del proveedor](../recursos/img/proveedor-ordenes-compras/01-ordenes-y-compras.png)

![Filtro por estado de la orden](../recursos/img/proveedor-ordenes-compras/02-filtro-estado.png)

> ℹ️ Por ahora la ficha **no exporta a Excel** las órdenes ni las compras del proveedor.

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"Sin permiso de Órdenes de compra (48)"* o *"Sin permiso de Compras y devoluciones (57)"* | Ese bloque necesita Consultar sobre la opción indicada. Pida el permiso a su administrador; el resto de la ficha sigue disponible. |
| *"El periodo no puede superar 366 días."* | Acorte las fechas. |
| *"La fecha inicial no puede ser posterior a la final."* | Corrija el orden de las fechas. |
| *"No pudimos cargar esta información"* | Pulse **Reintentar**. Si vuelve a pasar, intente más tarde. |
| *"Este proveedor ya no existe."* | Otro usuario lo eliminó. Vuelva al listado. |

![Bloque sin permiso](../recursos/img/proveedor-ordenes-compras/03-sin-permiso-compras-57.png)

---

## ✅ Cumplimiento de OC

La pestaña **Cumplimiento de OC** responde a una pregunta: ¿las órdenes de compra del proveedor llegaron en la fecha pactada y completas? Compara cada orden y cada línea con lo que realmente se recibió. Es de solo consulta y necesita Consultar sobre **Proveedores**, **Órdenes de compra** y **Compras y devoluciones**.

> ℹ️ **Solo se mide lo que se compró contra una orden de compra.** Las compras sin orden no entran al cumplimiento. La pantalla informa cuántas compras no tienen orden, y las devoluciones sin orden aparecen aparte.

**Cómo se lee la pantalla:**

1. **Periodo de cumplimiento.** Filtra por la fecha pactada de cada línea. Tiene el mismo límite de 366 días.
2. **Resumen.** Órdenes evaluadas, líneas evaluables, a tiempo, tarde, pendientes vencidas y completas.
3. **Más detalle del periodo.** Parciales, sobre-entregadas, entregas anticipadas, sin plazo pactado, en curso (no se evalúan) y las unidades pedidas, recibidas y pendientes.
4. **De dónde salen los datos.** Cuántas líneas de compra tienen orden (por ejemplo, *9 de 214*), cuántas órdenes tienen plazo pactado y cuántas compras no tienen orden.
5. **Órdenes y sus líneas.** Una fila por orden. Las líneas de cada orden se cargan solo al expandirla. Al expandirla verá sus líneas con la fecha pactada, la primera recepción, la fecha en que se completó y las unidades pedidas, recibidas y pendientes. Cada línea muestra también **sus recepciones por fecha y unidades**. Use **Expandir todas** y **Colapsar todas**, o filtre por estado de la orden o marque **Solo incumplidas**.

![Cumplimiento de OC del proveedor](../recursos/img/proveedor-cumplimiento-oc/01-resultado.png)

![Orden expandida con sus líneas y recepciones](../recursos/img/proveedor-cumplimiento-oc/03-expandir-una-orden.png)

### Estado de cada línea

| Estado | Qué significa |
|--------|---------------|
| **A tiempo** | Se recibió dentro de los días de gracia de la fecha pactada. |
| **Tarde** | Se completó después de los días de gracia. |
| **Pendiente vencida** | Ya pasó la fecha pactada y falta recibir. |
| **En curso** | La fecha pactada es futura: todavía no se evalúa. |
| **Sin plazo pactado** | La orden no tiene días de plazo: solo cuenta la cantidad. |

Además, cada línea puede mostrar una nota: **Parcial vencida**, **Completa fuera de plazo**, **Completa**, **Sobre-entrega** (con su porcentaje), **Entrega anticipada** o **Aún dentro del plazo**.

**Reglas que usa el cálculo:**

- **Fecha pactada** = fecha de la orden + días de plazo.
- **Gracia** = 2 días después de la fecha pactada.
- **Completa** = se recibe al menos el 98 % de lo pedido.
- **Sobre-entrega** = se recibe más del 110 % de lo pedido. Se marca, pero no suma más de lo pedido.
- Las devoluciones **ligadas a la orden** restan de lo recibido. Las que no tienen orden no cambian ninguna línea.
- Las **órdenes anuladas** no se evalúan. Una orden **cerrada con faltante** cuenta lo que faltó como incumplimiento.

**Qué puede ver en blanco:**

| Aviso | Qué significa |
|-------|---------------|
| *"Aún no hay entregas que medir"* | Ninguna compra de este proveedor está ligada a una orden en el periodo. Las compras registradas antes de que se guardara la orden no se pueden comparar con lo pedido. El cumplimiento crece con las compras nuevas que se registren contra una orden. |
| *"Datos insuficientes"* | Hay menos de 5 líneas evaluables. Las cifras se muestran, pero tómelas como referencia. |

![Cumplimiento sin compras ligadas a una orden](../recursos/img/proveedor-cumplimiento-oc/06-vacio-sin-cobertura.png)

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"Sin permiso de Órdenes de compra (48)"* o *"Sin permiso de Compras y devoluciones (57)"* | Pida el permiso de consulta de la opción indicada. |
| *"El resultado es demasiado grande"* | Acorte el periodo o aplique un filtro y vuelva a consultar. |
| *"Este proveedor ya no existe."* | Vuelva al listado de proveedores. |
| *"No pudimos cargar esta información"* | Pulse **Reintentar**. |

---

## 📊 Indicadores del proveedor

La pestaña **Indicadores** de la ficha tiene dos sub-pestañas:

- **Saldos y vencimientos**: la cartera del proveedor, con sus documentos vencidos y su historia de pagos. Es la misma cartera de la pestaña **Cartera**; su manual completo está en [Cartera de proveedores](cartera-proveedores.md). Es de solo consulta.
- **Evaluación**: dos indicadores de la relación con el proveedor, **I1** e **I2**, con su detalle; I2 se puede exportar a Excel.

| Qué ve | Permiso necesario |
|--------|-------------------|
| Pestaña **Indicadores** | Consultar sobre **Cartera Terceros (107)**, o bien **Proveedores (46)**, **Órdenes de compra (48)** y **Compras y devoluciones (57)** |
| Sub-pestaña **Saldos y vencimientos** | Consultar sobre **Cartera Terceros (107)** |
| Indicador **I1** | **Proveedores (46)**, **Órdenes de compra (48)** y **Compras y devoluciones (57)** |
| Indicador **I2** | **Proveedores (46)** y **Cartera Terceros (107)** |

Si le falta el permiso de uno de los indicadores, verá la tarjeta con el aviso *"Sin permiso de Cartera Terceros (107)"*; el otro indicador se muestra igual. La sub-pestaña **Evaluación** aparece si tiene permiso para ver al menos uno.

![Indicadores: sub-pestañas Saldos y vencimientos y Evaluación](../recursos/img/proveedor-evaluacion-ficha/03-indicadores-evaluacion.png)

### Evaluación: periodo y cálculo

El **periodo de la evaluación** tiene por defecto los últimos 365 días terminados ayer y no puede superar 366 días. **I1** filtra por la fecha pactada de cada línea; **I2**, por la fecha de vencimiento de cada documento. Si cambia las fechas, pulse **Actualizar**: hasta entonces verá el aviso *"Cambiaste el periodo. Pulse Actualizar para ver el resultado con él."*

Los números se calculan al consultar. Para ver los cambios recientes de otros usuarios, pulse **Actualizar**.

El pie de la sección indica los parámetros usados: gracia de entrega (2 días), tolerancia de faltante (2 %), sobre-entrega (por encima del 10 %) y gracia de pago del contado (5 días, provisional).

### I1 · Cumplimiento en entregas

**Pregunta:** ¿las órdenes llegan en la fecha pactada y completas?

**Cómo se calcula:**

- **Cumplimiento de fecha** (la mitad del indicador): unidades recibidas a tiempo ÷ unidades pedidas, solo de las líneas con plazo pactado.
- **Cantidades y referencias completas** (la otra mitad): el promedio de dos cifras: unidades recibidas ÷ unidades pedidas, y el porcentaje de líneas recibidas completas.
- **I1** = 50 % × cumplimiento de fecha + 50 % × cantidades y referencias completas.
- **A tiempo y completas (OTIF)**: porcentaje de líneas que cumplieron fecha y cantidad a la vez. Es más exigente que I1 y se muestra aparte, sin cambiar I1.

*Ejemplo:* cumplimiento de fecha 80 %, cantidades 90 % y referencias 70 %. Las cantidades y referencias dan 80 %, así que I1 = 0,5 × 80 + 0,5 × 80 = **80,0 %**.

**Semáforo de I1:**

| Color | Texto | Valor |
|-------|-------|-------|
| Verde | **Cumple la meta** | 90 % o más |
| Amarillo | **En seguimiento** | de 75 % a 89,9 % |
| Rojo | **Por debajo de la meta** | menos de 75 % |

El color nunca va solo: siempre aparece el texto. El semáforo compara el valor exacto: 89,95 % es amarillo.

**Qué tener en cuenta:**

- En *Líneas que explican el I1* cada recepción muestra su documento (identificador y Doc. Referencia).
- **Solo cuentan las compras ligadas a una orden de compra.** Una compra sin orden no tiene compromiso con el cual medirla, por eso no entra en I1.
- Las compras se cuentan por su fecha y las órdenes por su fecha pactada. Por eso, en un mismo periodo, la cobertura y el cumplimiento pueden no cuadrar exactamente.
- Si **más de la mitad** de las líneas no tiene plazo pactado, el cumplimiento de fecha sale como *Sin dato* y I1 se calcula solo con cantidades y referencias. El aviso lo dice así. Para medir fechas, revise los días de plazo de orden de compra en la pestaña **Proveedor** de la ficha.
- Con **menos de 5 líneas evaluables**, verá *Datos insuficientes*: la cifra aparece, sin color.
- Sin ninguna compra ligada a una orden, verá *"Aún no hay entregas medibles"* con la cobertura: *"Líneas de compra con orden: N de M · Órdenes con plazo pactado: n de m."*

![I1 con semáforo amarillo](../recursos/img/proveedor-evaluacion/02-semaforo-amarillo.png)

![I1 con datos insuficientes](../recursos/img/proveedor-evaluacion/04-datos-insuficientes.png)

### I2 · Cumplimiento de pago (CxP)

**Pregunta:** ¿cuánto de lo que le debíamos al proveedor se pagó dentro del plazo?

> ℹ️ **I2 mide a la empresa, no al proveedor**: es nuestro cumplimiento al pagarle. Por eso se compara con cuidado entre proveedores.

**Cómo se calcula:**

**I2** = valor pagado a más tardar el día del vencimiento ÷ valor de los documentos vencidos en el periodo.

- Cuentan los documentos que generan deuda con el proveedor (compras, gastos y similares, los mismos de la cartera) y los pagos (egresos) aplicados a ellos.
- Las **notas crédito** reducen el saldo, pero no cuentan como pago a tiempo. Los anticipos y los saldos a favor no entran en el cálculo.
- En los documentos **a crédito** (con plazo), el pago debe entrar el día del vencimiento o antes.
- En los documentos de **contado** (sin plazo), hay una gracia de pago de **5 días** (valor provisional, en revisión con negocio).

**Complementos** (no cambian I2):

- **Documentos pagados a tiempo**: cuántos de los documentos vencidos se pagaron completos a tiempo.
- **Atraso medio ponderado**: días de atraso de los pagos tardíos, promediados por valor.
- **Vencido sin pagar**: saldo de los documentos ya vencidos y sin pagar.
- **Saldo a favor** (informativo).

**Crédito y contado, por separado.** I2 muestra dos bloques: **Crédito (plazo mayor a 0)** y **Contado (gracia N días)**. Cada uno indica sus documentos (a tiempo y tardíos), su valor y su propio I2. Así, los documentos de contado, que vencen el mismo día, no distorsionan la cifra de crédito. La cifra total se muestra arriba.

**Semáforo provisional.** I2 tiene semáforo: **verde** desde 95 %, **amarillo** de 85 % a 94,9 % y **rojo** por debajo de 85 %. Como negocio aún confirma esos umbrales y los días de gracia del contado, el semáforo lleva la insignia **Provisional** y el aviso *"Provisional: umbrales y días de gracia en revisión"*. Tómelo como orientación: la cifra es una referencia, no una calificación final.

**Datos insuficientes.** Con **menos de 3 documentos vencidos** verá la cifra sin color y con *Datos insuficientes*. Si el periodo no tiene documentos vencidos, verá *"No hay documentos vencidos en el periodo"*: no es un error.

![I2 con semáforo provisional](../recursos/img/proveedor-evaluacion/03-i2-semaforo-provisional.png)

![I2 con crédito y contado por separado](../recursos/img/proveedor-evaluacion/13-i2-credito-y-contado.png)

### Exportar a Excel

**I2** tiene **Exportar a Excel**. El archivo incluye el proveedor, la fecha de corte, el periodo, los parámetros usados y los documentos que explican el resultado. No pide el permiso **Exportar** de la opción.

El archivo de I2 tiene **16 columnas**. Las tres nuevas son **Tipo de movimiento**, **Consecutivo** y **Doc. Referencia**, para identificar cada documento sin abrirlo.

Las órdenes de compra y las compras del proveedor no se exportan desde la ficha.

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"Sin permiso de Cartera Terceros (107)"* | Pida el permiso de consulta de Cartera Terceros. Los demás indicadores siguen disponibles. |
| *"Sin permiso de Órdenes de compra (48)"* o *"Sin permiso de Compras y devoluciones (57)"* | Pida el permiso de consulta de la opción indicada. I1 no se muestra sin ellas. |
| *"El periodo no puede superar 366 días."* / *"La fecha inicial no puede ser posterior a la final."* | Corrija las fechas y pulse **Actualizar**. |
| *"No pudimos cargar esta información"* | Pulse **Reintentar**. Si solo falla un indicador, el otro se muestra igual. |
| *"El resultado es demasiado grande"* | Acorte el periodo o aplique un filtro. |
| *"Este proveedor ya no existe."* | Vuelva al listado de proveedores. |

---

## ❓ Preguntas frecuentes

**¿Por qué el sistema dice que el documento ya existe?**
El número de documento es único en la compañía. Si el tercero ya existe (por ejemplo, como cliente), la ficha carga sus datos y, al guardar, solo se agrega la condición de proveedor.

**¿Por qué no puedo guardar el proveedor?**
Revise las pestañas marcadas con el contador de errores. Los campos obligatorios de la pestaña **Proveedor** son necesarios cuando el tercero es proveedor.

**Quité el proveedor y el tercero sigue apareciendo en otra pantalla.**
Si el tercero tenía otro perfil (cliente, empleado u otro), solo se retiró su condición de proveedor, y eso es lo esperado.

**¿Por qué no veo "En vivo"?**
La conexión en vivo no está disponible en este momento (por ejemplo, por la red de su empresa). La pantalla funciona igual; para ver cambios de otros usuarios, recargue la página.

**¿Por qué el archivo de importación dice que no se puede usar?**
Revise el mensaje de la página: el archivo debe ser un .xlsx de hasta 1 MB, con la columna **Documento** y hasta 1.000 filas. Descargue la plantilla y copie sus datos en ella.

**¿Por qué no encuentro un proveedor que sí existe?**
Revise que esté en la compañía correcta (título de la pestaña) y borre el texto del buscador con la **✕**.

**¿Por qué no veo las pestañas Órdenes y compras o Cumplimiento de OC?**
Aparecen solo en un proveedor guardado y con permiso de consulta sobre **Proveedores**. Si la pestaña está pero un bloque dice *"Sin permiso de …"*, pida ese permiso a su administrador.

**Cumplimiento de OC está vacío, aunque el proveedor tiene compras.**
Solo cuentan las compras ligadas a una orden de compra. Las compras que se registraron sin orden, o antes de que se guardara la orden, no entran en el cálculo.

**¿Por qué una orden dice *Sin plazo pactado*?**
La orden tiene 0 días de plazo, así que no hay fecha pactada con la cual comparar la entrega. Revise los días de plazo de orden de compra en la pestaña **Proveedor** de la ficha.

**¿Por qué el semáforo de I2 dice *Provisional*?**
Los umbrales (95 % y 85 %) y los días de gracia del contado los está confirmando negocio. Mientras tanto, el color orienta, pero la cifra no es final.

**¿Qué es el Doc. Referencia y por qué dice —?**
Es el texto que se escribió al capturar el documento (hasta 20 caracteres), por ejemplo, el número de la factura del proveedor. Si el documento no lo tiene, se muestra **—**. La pantalla lo muestra tal cual y no es un enlace.

**¿Por qué dice *Datos insuficientes*?**
Hay pocas líneas (I1, menos de 5) o pocos documentos vencidos (I2, menos de 3) para sacar conclusiones. La cifra se muestra, pero sin color.

---

## 📚 Relacionado

- [Compradores](compradores.md)
- [Cartera de proveedores](cartera-proveedores.md)
- [Manejo general de la información](../../Generales/manejo-general-informacion.md)
