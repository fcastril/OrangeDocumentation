[Regresar a Grupos](grupos.md)

---

# 📥 Importar grupos desde Excel

![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Grupos-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20260925-yellow)

---

## 📋 Descripción

Crea grupos nuevos o **actualiza el nombre y la configuración contable** (cuentas y naturalezas) de los existentes a partir de un archivo de Excel. Es la forma más rápida de cargar los grupos de una compañía nueva o de **cambiar las cuentas de muchos grupos** de una vez. Antes de guardar, el sistema le muestra qué va a crear, qué va a actualizar y qué filas tienen errores. **Nunca elimina grupos ni cambia códigos.**

> 🔐 Necesita el permiso **Exportar** sobre la opción Grupos (es el mismo permiso de Exportar a Excel).

---

## 🎯 Acceso

En [Grupos](grupos.md), haga clic en **Importar** (junto a **Exportar a Excel**).

La importación tiene tres pasos: **Cargar archivo → Revisar → Resultado**.

---

## 1️⃣ Cargar archivo

![Cargar archivo](../recursos/img/grupos/06-importar-cargar.png)

1. Haga clic en **Descargar plantilla**. Se descarga `grupos-plantilla.xlsx` con 18 columnas:
   - **Código** y **Nombre**.
   - **Cuenta valor bruto**, **Naturaleza valor bruto**, **Cuenta IVA**, **Naturaleza IVA**, **Cuenta descuento**, **Naturaleza descuento**, **Cuenta costos**, **Naturaleza costos**, **Cuenta inventario**, **Naturaleza inventario**, **Cuenta devolución valor bruto**, **Naturaleza devolución valor bruto**, **Cuenta devolución descuento**, **Naturaleza devolución descuento**, **Cuenta devolución IVA** y **Naturaleza devolución IVA**.
2. Llene **una fila por grupo**:
   - Si el **código ya existe**, se actualizan su **nombre** y las **cuentas y naturalezas** que escriba.
   - Si el **código no existe**, se **crea** el grupo.
3. Guarde el archivo y arrástrelo al recuadro, o haga clic en **Seleccionar archivos**.

> 💡 También puede partir de **Exportar a Excel** en el listado: el archivo exportado tiene las mismas columnas (la columna *Última modificación* se ignora).

| Regla | Detalle |
|-------|---------|
| Formato | Excel `.xlsx`. Solo se lee la **primera hoja**. |
| Encabezado | La primera fila debe tener las 18 columnas de la plantilla (con o sin tilde, en mayúsculas o minúsculas). El orden de las columnas no importa. |
| Tamaño | Hasta **1.000 filas** y **1 MB**. Si tiene más, divida el archivo. |
| Filas vacías | Se ignoran; en **Revisar** se indica cuántas se omitieron ("Filas vacías omitidas"). |
| Código | Hasta 5 caracteres: letras, números y guion. Se guarda en mayúsculas. |
| Nombre | Hasta 50 caracteres, sin comas ni punto y coma. |
| Cuentas | Escriba el **código de la cuenta** (por ejemplo `41350501`), no el nombre. Debe ser una cuenta **de movimiento** de la compañía. **Al crear**, las 8 cuentas son obligatorias. **Al actualizar**, una celda de cuenta **vacía conserva** la cuenta actual. |
| Naturalezas | `C` (Crédito), `D` (Débito) o vacía. También acepta `Crédito` y `Débito` escritos completos. Al crear, vacía = sin naturaleza; al actualizar, vacía = **conserva** la actual. |

> ⚠️ Excel puede quitar los ceros a la izquierda o convertir códigos largos en números. Las columnas de **cuenta** de la plantilla ya vienen en formato **Texto** para evitarlo; si usa otro archivo, ponga esas columnas en formato Texto antes de escribir los códigos.

Si el archivo no sirve (no es Excel, le falta alguna columna, está vacío o es muy grande), verá el motivo y no se envía nada.

---

## 2️⃣ Revisar

El sistema valida cada fila **sin guardar nada** y le muestra un resumen:

![Revisar la importación](../recursos/img/grupos/07-importar-revisar.png)

| Indicador | Significado |
|-----------|-------------|
| **Nuevos** | Códigos que no existen: se crearán con sus 8 cuentas. |
| **Se actualizan** | Códigos que ya existen con otro nombre u otras cuentas o naturalezas. Debajo del nombre verá **Antes: …** y en la columna **Cambios**, qué cuentas o naturalezas cambian (por ejemplo *Cambia: Cuenta IVA*). |
| **Sin cambios** | Códigos que ya existen con el mismo nombre y la misma configuración contable: no se toca nada. |
| **Con error** | Filas que **no se importarán**. Debajo del estado verá el motivo. |

Use las pestañas **Todas / Nuevos / Se actualizan / Sin cambios / Con error** para filtrar la tabla, y el buscador para ubicar una fila.

### Errores por fila

| Mensaje | Cómo corregirlo |
|---------|-----------------|
| Falta el código. / Falta el nombre. | Complete la celda. |
| El código tiene más de 5 caracteres. | Acorte el código. |
| El código solo puede tener letras, números y guion. | Quite espacios, tildes u otros símbolos. |
| El código / El nombre no puede tener comas ni punto y coma. | Quite `,` y `;`. |
| El nombre tiene más de 50 caracteres. | Acorte el nombre. |
| Falta la cuenta en «Cuenta …» (obligatoria al crear). | Un grupo nuevo necesita las 8 cuentas: escriba el código de la cuenta en esa columna. |
| La cuenta … de «Cuenta …» no existe en la compañía. | Revise el código de la cuenta (sin puntos ni espacios) y que exista en el plan de cuentas de esta compañía. |
| La cuenta … de «Cuenta …» no es de movimiento. | Use una cuenta auxiliar (de movimiento), no una cuenta mayor. |
| «Naturaleza …» debe ser C (Crédito), D (Débito) o estar vacía. | Escriba `C`, `D` o deje la celda vacía. |
| El código se repite en el archivo (filas …). | Deje una sola fila por código. Todas las filas repetidas quedan con error. |

> 💡 **Descargar filas con error** genera un Excel solo con esas filas y su motivo, para corregirlas y volver a cargarlas.

> 🔄 Si mientras revisa otro usuario cambia grupos, verá *"Otro usuario cambió grupos mientras revisabas. Vuelve a validar antes de aplicar."* Haga clic en **Volver a validar** para que la revisión tenga en cuenta esos cambios.

---

## 3️⃣ Aplicar y resultado

Haga clic en **Aplicar N cambios** (N = nuevos + se actualizan). Las filas con error se omiten.

- Todo se guarda **junto**: si algo falla, **no se guarda ningún cambio** y puede reintentar.
- Si otro usuario cambió grupos mientras usted revisaba, verá el aviso de cambios: haga clic en **Volver a validar** y revise de nuevo.

![Resultado de la importación](../recursos/img/grupos/08-importar-resultado.png)

Al terminar verá el resumen (creados, actualizados, sin cambios y con error). Use **Ver grupos** para volver al listado, que ya muestra los cambios, o **Importar otro archivo**.

---

## ❓ Preguntas frecuentes

**¿Cómo cambio la cuenta de IVA de todos los grupos de una vez?**
Use **Exportar a Excel** en el listado, cambie la columna **Cuenta IVA** en el archivo e impórtelo. Solo cambiarán los grupos cuya cuenta sea distinta. También puede dejar vacías las demás columnas de cuenta: al actualizar, una cuenta vacía conserva la actual.

**¿Por qué me pide cuentas de movimiento?**
Los documentos solo pueden contabilizar en cuentas de movimiento. Es la misma lista que ve en el selector de la pestaña **Contabilidad**.

**¿Puedo cambiar el código de un grupo con la importación?**
No. El código es lo que identifica el grupo: si pone un código distinto, se crea uno nuevo. Para cambiar un código use **Editar** en [Grupos](grupos.md).

**¿La importación carga la imagen del grupo?**
No. La imagen del grupo no se edita en esta versión; la importación conserva la que tenga cada grupo.

**¿La importación borra los grupos que no están en el archivo?**
No. Nunca elimina grupos.

**No veo el botón Importar.**
Su perfil necesita el permiso **Exportar** sobre Grupos. Consulte a su administrador.
