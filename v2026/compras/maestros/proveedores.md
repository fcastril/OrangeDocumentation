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
| **Importar** | Pendiente en esta versión: ver *Importar desde Excel* más abajo. |
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

Los campos obligatorios se marcan en la ficha. Si falta algún dato o un valor no es válido, la pestaña aparece con un contador de errores (por ejemplo, **2 errores**) y el campo muestra el motivo, como *"Escribe un valor numérico válido."*, *"Debe estar entre 0 y 100."* o *"Elige el impuesto o desmarca la casilla."*. Corríjalo y guarde de nuevo.

Al guardar verá el mensaje **"Proveedor … creado."** y el proveedor aparece en el listado.

### Verificar el documento antes de crear

Cuando escribe el número de documento (entre 5 y 20 caracteres) y deja el campo, el sistema verifica si ese documento ya existe en la compañía. Verá uno de estos avisos:

| Aviso | Qué significa | Qué puede hacer |
|-------|---------------|-----------------|
| *"Verificando si el documento ya está registrado…"* | La revisión está en curso. | Espere un momento. |
| *"Este documento ya existe en la compañía como {nombre} ({roles})."* y *"Se cargó la información registrada…"* | El tercero ya existe con otro perfil (cliente, empleado u otro). **No se duplica.** La ficha se llena con sus datos. | Revise los datos precargados y haga clic en **Guardar**: el tercero se agrega como proveedor sin crear otro. |
| *"Este documento ya es proveedor en la compañía."* y *"{nombre} ya está registrado con este documento."* | Ya tiene este perfil. | Haga clic en **Abrir su edición** para modificarlo. |
| *"No se pudo verificar el documento…"* | La revisión falló por la conexión. | Haga clic en **Reintentar**, o guarde: el sistema lo verifica otra vez al guardar. |

![Documento ya registrado con otro perfil](../recursos/img/proveedores/03-reutilizar-tercero.png)

Si cambia el número de documento después de haber cargado un tercero existente, la información precargada se quita y la verificación se repite.

> ⚠️ Si otro usuario crea ese mismo tercero mientras usted llena la ficha, al guardar el sistema vuelve a revisar el documento: carga la información registrada en la ficha y le pide revisarla y guardar otra vez. Si el sistema no puede cargar el tercero registrado con ese documento, verá *"Este documento ya lo usa otro tercero de la compañía."* El sistema nunca crea dos terceros con el mismo documento.

---

## ✏️ Editar un proveedor

1. Haga clic en el **lápiz** del proveedor (o en **Ver** si solo tiene consulta).
2. Cambie los datos y haga clic en **Guardar**.

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

- El archivo puede tener **hasta 10.000 filas**. Si la búsqueda tiene más resultados, verá el aviso *"Hay más de 10.000 resultados: acota la búsqueda para exportar."* Escriba más texto en el buscador (documento o nombre) para reducir la lista y vuelva a exportar.
- Si la exportación falla por la conexión, verá *"No se pudo exportar. Inténtalo de nuevo."*

---

## 📥 Importar desde Excel

> 🚧 **Pendiente.** La importación de proveedores desde Excel todavía no está disponible en esta versión. Esta sección se completará cuando la pantalla de importación esté publicada (pasos: cargar archivo, revisar y resultado; el permiso necesario es **Exportar**).

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

**¿Por qué no encuentro un proveedor que sí existe?**
Revise que esté en la compañía correcta (título de la pestaña) y borre el texto del buscador con la **✕**.

---

## 📚 Relacionado

- [Compradores](compradores.md)
- [Manejo general de la información](../../Generales/manejo-general-informacion.md)
