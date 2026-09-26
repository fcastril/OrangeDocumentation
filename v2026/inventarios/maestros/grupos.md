[Regresar a Inventarios](../readme.md)

---

# 🗂️ Grupos

![Static Badge](https://img.shields.io/badge/Tipo-MaestroTipoI-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Grupos-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20260925-yellow)

---

## 📋 Descripción

Los **grupos** clasifican las referencias de inventario en familias amplias, por ejemplo `ALI` Alimentos, `ASE` Aseo o `PAP` Papelería. Cada grupo se divide en **[subgrupos](subgrupos.md)**, y las referencias pertenecen a un subgrupo.

Además de clasificar, cada grupo tiene su **configuración contable**: las cuentas en las que se contabilizan las ventas, el IVA, los descuentos, los costos, el inventario y las devoluciones de las referencias del grupo. Por eso un grupo **no se puede guardar sin sus 8 cuentas**.

En esta pantalla puede **consultar, crear, editar, eliminar, exportar e importar** los grupos de la compañía con la que está trabajando.

> 📘 La búsqueda, el orden, la paginación, la exportación y la ayuda funcionan igual en todas las tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Cada pestaña del navegador trabaja con **una compañía**. El nombre y el color de la compañía se ven en el título de la pestaña y en la barra superior.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Inventarios**.
2. En **Maestros**, haga clic en **Grupos**.

---

## 🖥️ Pantalla principal

![Listado de grupos](../recursos/img/grupos/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. Ver *Cambios de otros usuarios* más abajo. |
| **Nuevo grupo** | Crea un grupo. |
| **Buscar por código o nombre** | Filtra el listado mientras escribe. No distingue mayúsculas ni tildes. |
| **Importar** | Crea o actualiza grupos desde un archivo de Excel. Ver [Importar grupos](grupos-importar.md). |
| **Exportar a Excel** | Descarga los grupos (con el filtro y el orden que tenga en pantalla) **con sus cuentas y naturalezas**. |
| **Lápiz** / **Papelera** | Editar o eliminar el grupo de esa fila. Siempre están en la **primera columna**, visibles aunque la tabla tenga que desplazarse. |
| **Código**, **Nombre**, **Última modificación** | Columnas del listado. Al abrir la pantalla, la tabla viene ordenada por **código**. |
| **Encabezados** | Un clic ordena de forma ascendente, el segundo descendente y el tercero vuelve al orden inicial. |
| **Filas por página** y paginación | Cambian cuántos grupos ve y la página. |

> 📱 En el celular cada grupo se muestra como una tarjeta, con las acciones arriba.

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil sobre la opción Grupos:

| Permiso | Qué habilita |
|---------|--------------|
| Consultar | Ver la pantalla |
| Crear | **Nuevo grupo** |
| Actualizar | **Lápiz** (editar) |
| Eliminar | **Papelera** (eliminar) |
| Exportar | **Exportar a Excel** e **Importar** |

---

## ➕ Crear un grupo

1. Haga clic en **Nuevo grupo**.
2. En la pestaña **General**, escriba el código y el nombre.
3. En la pestaña **Contabilidad**, elija las 8 cuentas (y, si aplica, su naturaleza).
4. Haga clic en **Guardar** (o presione **Enter**).

### Pestaña General

![Crear grupo: pestaña General](../recursos/img/grupos/02-crear-general.png)

| Campo | Obligatorio | Reglas | Ejemplo |
|-------|:-----------:|--------|---------|
| **Código** | ✅ | Hasta 5 caracteres: letras, números y guion. Se guarda **siempre en MAYÚSCULAS** (lo convierte mientras escribe). No se puede repetir en la compañía. | `ALI`, `J-1` |
| **Nombre** | ✅ | Hasta 50 caracteres, sin comas ni punto y coma. | `Alimentos` |

### Pestaña Contabilidad

![Crear grupo: pestaña Contabilidad](../recursos/img/grupos/03-crear-contabilidad.png)

Las cuentas se agrupan en dos secciones. En cada fila elija la **cuenta** (obligatoria) y, si quiere, la **naturaleza**.

| Sección | Concepto | Para qué se usa |
|---------|----------|-----------------|
| **Ventas** | Valor bruto | Ingreso por la venta de las referencias del grupo. |
| | IVA | IVA generado en la venta. |
| | Descuento | Descuentos concedidos en la venta. |
| | Costos | Costo de ventas. |
| | Inventario | Cuenta del inventario de las referencias. |
| **Devoluciones** | Valor bruto | Devoluciones en ventas. |
| | Descuento | Descuento de la devolución. |
| | IVA | IVA de la devolución. |

- **Cuenta**: haga clic en el campo y **escriba parte del código o del nombre** de la cuenta para buscarla (no distingue mayúsculas ni tildes); elija con el mouse o con las flechas y **Enter**. Solo aparecen las cuentas **de movimiento** de la compañía, como `Código · Nombre`.
- **Naturaleza**: **Crédito**, **Débito** o **Sin naturaleza**. Si la deja vacía y elige una cuenta, el sistema **propone la naturaleza de la cuenta** (verá *"Propuesta según la cuenta."*); puede cambiarla. Si ya tenía una naturaleza, elegir otra cuenta no la cambia.

> 💻 En pantallas angostas (celular) la cuenta y la naturaleza se muestran una debajo de la otra.

Al guardar verá el mensaje **"Grupo … creado."** y el grupo aparece en el listado.

### ¿Qué puede salir mal?

Si falta algo, el sistema **abre la pestaña del primer error** y pone el cursor en ese campo. Cada pestaña muestra un **número rojo** con cuántos errores tiene.

| Mensaje | Qué hacer |
|---------|-----------|
| Escribe el código del grupo. / Escribe el nombre del grupo. | Complete el campo en **General**. |
| Usa solo letras, números y guion (máximo 5). | Quite espacios, tildes u otros símbolos del código, o acórtelo. |
| El nombre no puede tener comas ni punto y coma (máximo 50). | Corrija el nombre. |
| Ya existe un grupo con el código … | Use otro código. |
| Elige la cuenta de *concepto* (p. ej. "Elige la cuenta de IVA."). | Elija la cuenta de ese concepto en **Contabilidad** (las 8 son obligatorias). |
| La cuenta ya no existe o no es de movimiento. Elige otra. | Alguien cambió el plan de cuentas mientras usted editaba: elija otra cuenta. |

---

## ✏️ Editar un grupo

1. Haga clic en el **lápiz** del grupo.
2. Cambie el código, el nombre (pestaña **General**) o las cuentas y naturalezas (pestaña **Contabilidad**) y haga clic en **Guardar**.

![Editar grupo cambiando el código](../recursos/img/grupos/04-editar-cambio-codigo.png)

> ⚠️ **Cambiar el código** está permitido y no afecta los subgrupos, las referencias ni los clientes que ya usan el grupo. Verá un aviso porque los **informes, las exportaciones y los archivos externos** mostrarán el código nuevo, y una plantilla de importación con el código anterior crearía otro grupo.

> 💡 Los cambios de cuentas aplican a los documentos que se contabilicen **desde ese momento**; los documentos ya contabilizados no cambian.

Si otro usuario eliminó el grupo mientras lo editaba, al guardar el diálogo se cierra, el grupo desaparece del listado y un aviso le indica **"Este grupo ya no existe"**.

---

## 🗑️ Eliminar un grupo

1. Haga clic en la **papelera** del grupo.
2. Confirme con **Eliminar grupo**.

![Confirmar eliminación](../recursos/img/grupos/05-confirmar-eliminar.png)

Un grupo **no se puede eliminar** si tiene información relacionada: si tiene **subgrupos** (y por lo tanto referencias) o si algún **cliente o sucursal** lo usa. En ese caso verá:

> No se puede eliminar … : tiene información relacionada en otros módulos.

---

## 📤 Exportar a Excel

Haga clic en **Exportar a Excel**. Se descarga `grupos_AAAA-MM-DD.xlsx` con **todos** los grupos del filtro actual (no solo la página visible), con el encabezado fijo y filtros de Excel. Columnas:

- **Código** y **Nombre**.
- Para cada concepto (valor bruto, IVA, descuento, costos, inventario, devolución valor bruto, devolución descuento y devolución IVA): **Cuenta …** con el **código de la cuenta** y **Naturaleza …** con `C`, `D` o vacía.
- **Última modificación**, como fecha de Excel.

Son las **mismas columnas de la plantilla de importación**: puede exportar, corregir en Excel e importar el archivo.

---

## 📥 Importar desde Excel

Para crear muchos grupos o cambiar sus cuentas de una vez, use **Importar**. Vea el paso a paso en [Importar grupos desde Excel](grupos-importar.md).

---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica, elimina o importa grupos mientras usted tiene abierta esta pantalla, **no tiene que recargar**: el listado se pone al día solo, sin perder lo que buscó, el orden ni la página.

- Las filas nuevas o modificadas se **resaltan** unos segundos.
- Abajo a la derecha aparece un aviso, por ejemplo *"Otro usuario creó el grupo Novedades."*
- Junto a la descripción verá **En vivo** mientras la conexión esté activa. Si se interrumpe, dice **Reconectando…**; al volver, la pantalla se actualiza sola.

**Si estaba editando ese mismo grupo:**

| Qué hizo el otro usuario | Qué verá | Qué puede hacer |
|--------------------------|----------|-----------------|
| Lo modificó | *"Otro usuario modificó este grupo mientras lo editabas. Si guardas, reemplazarás sus cambios."* | **Ver sus cambios** para cargar lo que él guardó, o **Guardar** para dejar lo suyo. |
| Lo eliminó | *"Otro usuario eliminó este grupo. Ya no se puede guardar."* | **Cancelar**. El botón Guardar queda deshabilitado. |

Si estaba por confirmar la eliminación de un grupo que otro ya eliminó, el diálogo se cierra con el aviso *"Otro usuario ya eliminó el grupo…"*.

> ℹ️ Los cambios que usted hace en esta misma pestaña no generan avisos. Los cambios hechos desde la versión anterior de OrangeERP no se avisan al instante: se reflejan al volver a esta pestaña después de un rato o al recargar.

---

## ❓ Preguntas frecuentes

**¿Por qué no puedo guardar un grupo sin cuentas?**
Las 8 cuentas son obligatorias: los documentos de venta, devolución e inventario las usan para contabilizar las referencias del grupo. Es la misma regla de la versión anterior.

**¿Por qué no aparece la cuenta que busco?**
Solo se pueden elegir cuentas **de movimiento** (las que reciben asientos, no las cuentas mayores o de agrupación) de la compañía actual. Si la cuenta no aparece, revise en el plan de cuentas que exista en esta compañía y que esté marcada como de movimiento.

**¿Qué pasa si dejo la naturaleza vacía?**
Se guarda vacía, como en la versión anterior. Al elegir una cuenta con la naturaleza vacía, el sistema le propone la naturaleza de la cuenta para que no la olvide; puede cambiarla o volver a **Sin naturaleza**.

**¿Dónde está la imagen del grupo?**
En esta versión la imagen del grupo **no se edita**: la pantalla nueva no muestra ni cambia la imagen, y al editar un grupo **se conserva** la que ya tenía (la usa el Punto de venta). La carga de imágenes llegará cuando se defina el almacenamiento de archivos de la nueva versión; mientras tanto, si necesita cambiarla, use la versión anterior de OrangeERP.

**¿Por qué el código quedó en mayúsculas?**
Los códigos siempre se guardan en mayúsculas para que no haya dos grupos "iguales" escritos distinto.

**¿Por qué no encuentro un grupo que sí existe?**
Revise que esté en la compañía correcta (título de la pestaña) y borre el texto del buscador con la **✕**.

**No veo "En vivo".**
La conexión en vivo no está disponible en este momento (por ejemplo, por la red de su empresa). La pantalla funciona igual; para ver cambios de otros usuarios, recargue la página.

**La "Última modificación" de algunos grupos muestra una hora distinta.**
Las fechas se guardan en hora universal y se muestran en la hora de su equipo; algunos grupos modificados en la versión anterior pueden verse desplazados hasta que se ajusten sus fechas.
