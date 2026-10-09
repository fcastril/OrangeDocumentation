[Regresar a Compras](../readme.md)

---

# 🧑‍💼 Compradores

![Static Badge](https://img.shields.io/badge/Tipo-MaestroTipoII-red)
![Static Badge](https://img.shields.io/badge/Module-Compras-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Compradores-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## 📋 Descripción

Los **compradores** son los terceros que realizan las compras de la compañía. Cada comprador tiene su ficha con los datos de identificación, ubicación y tributarios, además de su logo y sus documentos adjuntos.

En esta pantalla puede **consultar, crear, editar y eliminar** compradores, y **exportar** el listado a Excel. Trabaje siempre con la compañía que aparece en el título de la pestaña.

> 📘 La búsqueda, el orden, la paginación y la ayuda funcionan igual en todas las tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Un tercero puede ser **comprador y proveedor** a la vez. Sus datos, su logo y sus adjuntos son los mismos en ambas pantallas; ver [Proveedores](proveedores.md).

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Compras**.
2. En **Maestros**, haga clic en **Compradores**.

Para ver la pantalla necesita el permiso **Consultar** sobre la opción Compradores. Los demás botones dependen de los permisos de su perfil (ver la tabla más abajo).

---

## 🖥️ Pantalla principal

![Listado de compradores](../recursos/img/compradores/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. Ver *Cambios de otros usuarios* más abajo. |
| **Nuevo comprador** | Abre la ficha para crear un comprador. |
| **Buscar por documento o nombre** | Filtra el listado mientras escribe. No distingue mayúsculas ni tildes. |
| **Exportar a Excel** | Descarga los compradores que cumplen la búsqueda actual. Ver la sección *Exportar a Excel* más abajo. |
| **Importar** | Pendiente en esta versión: ver *Importar desde Excel* más abajo. |
| **Lápiz** / **Papelera** | Editar o eliminar el comprador de esa fila. Siempre están en la **primera columna**. Si no tiene permiso para editar, el lápiz dice **Ver** y abre la ficha en solo lectura. |
| **Encabezados** | Un clic ordena de forma ascendente, el segundo descendente y el tercero quita el orden. |
| **Filas por página** y paginación | Cambian cuántos compradores ve por página (10, 20, 50 o 100) y la página. |

Las columnas del listado son: **Nro. documento**, **Nombre completo**, **Nombre comercial**, **Activo** y **Última modificación**.

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil sobre la opción Compradores:

| Permiso | Qué habilita |
|---------|--------------|
| Consultar | Ver el listado, abrir la ficha y ver el logo y los adjuntos. |
| Crear | **Nuevo comprador**, subir el logo y los adjuntos. |
| Actualizar | Editar la ficha, reemplazar o quitar el logo, subir o quitar adjuntos. |
| Eliminar | **Papelera** y eliminar adjuntos. |
| Exportar | **Exportar a Excel**. |

Si solo tiene **Consultar**, la ficha aparece con el aviso *"Solo tienes permiso de consulta: la ficha no se puede modificar."*

---

## ➕ Crear un comprador

1. Haga clic en **Nuevo comprador**.
2. Escriba el **Tipo de documento** y el **Número de documento**. Mientras escribe, el sistema revisa si ese documento ya está registrado en la compañía (ver el paso siguiente).
3. Complete la ficha y haga clic en **Guardar**.

![Crear comprador](../recursos/img/compradores/02-crear.png)

La ficha del comprador tiene **una sola pestaña, Tercero**, con:

- **Identificación**: tipo y número de documento, nombre o razón social, género.
- **Ubicación y contacto**: dirección, ciudad, teléfono, celular, correo y página web.
- **Información tributaria**: régimen, actividad económica, cuenta contable, resolución, gran contribuyente y autorretenedor.
- **Estado y observaciones**: activo y observaciones.
- **Logo** y **Adjuntos**: ver el logo y los adjuntos en [Proveedores](proveedores.md).

Al guardar verá el mensaje **"Comprador … creado."** y el comprador aparece en el listado. Si un campo está incompleto o tiene un valor no válido, la ficha muestra el motivo debajo del campo y no guarda hasta corregirlo.

### Verificar el documento antes de crear

Cuando escribe el número de documento (entre 5 y 20 caracteres) y deja el campo, el sistema verifica si ese documento ya existe en la compañía. Verá uno de estos avisos:

| Aviso | Qué significa | Qué puede hacer |
|-------|---------------|-----------------|
| *"Verificando si el documento ya está registrado…"* | La revisión está en curso. | Espere un momento. |
| *"Este documento ya existe en la compañía como {nombre} ({roles})."* y *"Se cargó la información registrada…"* | El tercero ya existe con otro perfil (cliente, empleado u otro). **No se duplica.** La ficha se llena con sus datos. | Revise los datos precargados y haga clic en **Guardar**: el tercero se agrega como comprador sin crear otro. |
| *"Este documento ya es comprador en la compañía."* y *"{nombre} ya está registrado con este documento."* | Ya tiene este perfil. | Haga clic en **Abrir su edición** para modificarlo. |
| *"No se pudo verificar el documento…"* | La revisión falló por la conexión. | Haga clic en **Reintentar**, o guarde: el sistema lo verifica otra vez al guardar. |

Si cambia el número de documento después de haber cargado un tercero existente, la información precargada se quita y la verificación se repite.

> ⚠️ Si otro usuario crea ese mismo tercero mientras usted llena la ficha, al guardar el sistema vuelve a revisar el documento: carga la información registrada en la ficha y le pide revisarla y guardar otra vez. Si el sistema no puede cargar el tercero registrado con ese documento, verá *"Este documento ya lo usa otro tercero de la compañía."* El sistema nunca crea dos terceros con el mismo documento.

---

## ✏️ Editar un comprador

1. Haga clic en el **lápiz** del comprador (o en **Ver** si solo tiene consulta).
2. Cambie los datos y haga clic en **Guardar**.

Si sale de la ficha con cambios sin guardar, el sistema pregunta **"¿Salir sin guardar?"**: **Seguir editando** lo deja en la ficha; **Salir sin guardar** descarta los cambios.

Si otro usuario modificó el mismo comprador mientras lo edita, vea *Cambios de otros usuarios* más abajo.

---

## 🗑️ Eliminar un comprador

Hay dos formas de empezar: la **papelera** de la fila en el listado, o el botón **Eliminar** al final de la ficha. Antes de borrar, el sistema confirma con **Eliminar comprador** y le muestra el documento.

| Situación | Qué ocurre |
|-----------|------------|
| El tercero **solo es comprador**. | Se elimina el comprador. Mensaje: *"Comprador … eliminado."* |
| El tercero **también es proveedor, cliente, empleado u otro perfil**. | El aviso dice *"Este tercero también es {roles}. Solo se retirará su condición de comprador; el tercero se conserva."* Se retira la condición de comprador y **el tercero se conserva** con sus otros perfiles. Mensaje: *"Se retiró la condición de comprador de …; el tercero se conserva."* |
| El comprador **está referenciado en documentos de compra**. | No se puede eliminar. El diálogo muestra: *"… está referenciado en documentos de compra y no se puede eliminar."* Si la pantalla da un motivo, aparece como **Motivo**. Cierre el diálogo: el comprador no cambia. |

Cuando se elimina el comprador de verdad, también se borran sus adjuntos y su logo. Si solo se retira la condición de comprador, el tercero, su logo y sus adjuntos se conservan.

![Comprador referenciado en documentos de compra](../recursos/img/compradores/03-en-uso.png)

### ¿Qué puede salir mal?

| Mensaje | Qué hacer |
|---------|-----------|
| *"No tienes permiso para realizar esta acción con compradores."* | Pida el permiso de **Eliminar** a su administrador. |
| *"El comprador ya no existe. Se quitó del listado."* | Otro usuario lo eliminó. El listado ya se actualizó. |
| *"No se pudo eliminar. Inténtalo de nuevo."* | Revise la conexión e intente otra vez. |

---

## 📤 Exportar a Excel

Haga clic en **Exportar a Excel**. Se descarga el archivo con los compradores que cumplen la **búsqueda** y el **orden** que tiene en pantalla, de todas las páginas (no solo la visible).

- El archivo puede tener **hasta 10.000 filas**. Si la búsqueda tiene más resultados, verá el aviso *"Hay más de 10.000 resultados: acota la búsqueda para exportar."* Escriba más texto en el buscador (documento o nombre) para reducir la lista y vuelva a exportar.
- Si la exportación falla por la conexión, verá *"No se pudo exportar. Inténtalo de nuevo."*

---

## 📥 Importar desde Excel

> 🚧 **Pendiente.** La importación de compradores desde Excel todavía no está disponible en esta versión. Esta sección se completará cuando la pantalla de importación esté publicada (el permiso necesario es **Exportar**).

---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica o elimina compradores mientras usted tiene abierto el listado, **no tiene que recargar**: el listado se pone al día solo, sin perder lo que buscó, el orden ni la página.

- Las filas nuevas o modificadas se **resaltan** unos segundos.
- Abajo a la derecha aparece un aviso, por ejemplo *"Otro usuario creó el comprador …"*.
- Junto a la descripción verá **En vivo** mientras la conexión esté activa. Si se interrumpe, dice **Reconectando…**; al volver, la pantalla se actualiza sola.

**Si estaba editando ese mismo comprador:**

| Qué hizo el otro usuario | Qué verá | Qué puede hacer |
|--------------------------|----------|-----------------|
| Lo modificó | *"Otro usuario modificó este comprador mientras lo editabas. Si guardas, reemplazarás sus cambios."* | **Ver sus cambios** para cargar lo que él guardó, o **Guardar** para dejar lo suyo. |
| Lo eliminó | *"Otro usuario eliminó este comprador. Ya no se puede guardar."* | **Cancelar**. El botón Guardar queda deshabilitado. |

Si estaba por confirmar la eliminación de un comprador que otro ya eliminó, el diálogo se cierra con el aviso *"Otro usuario ya eliminó el comprador …"*.

> ℹ️ Los cambios que usted hace en esta misma pestaña no generan avisos.

---

## ❓ Preguntas frecuentes

**¿Por qué el sistema dice que el documento ya existe?**
El número de documento es único en la compañía. Si el tercero ya existe (por ejemplo, como proveedor), la ficha carga sus datos y, al guardar, solo se agrega la condición de comprador.

**¿Por qué no veo la sección de proveedor o de contactos en el comprador?**
Un comprador solo tiene los datos del tercero. Las condiciones comerciales y los contactos se administran desde [Proveedores](proveedores.md).

**Quité el comprador y el tercero sigue apareciendo en otra pantalla.**
Si el tercero tenía otro perfil (proveedor, cliente, empleado u otro), solo se retiró su condición de comprador, y eso es lo esperado.

**¿Por qué no veo "En vivo"?**
La conexión en vivo no está disponible en este momento (por ejemplo, por la red de su empresa). La pantalla funciona igual; para ver cambios de otros usuarios, recargue la página.

---

## 📚 Relacionado

- [Proveedores](proveedores.md)
- [Manejo general de la información](../../Generales/manejo-general-informacion.md)
