[Regresar a Unidades de medida](unidades-medida.md)

---

# 📥 Importar unidades de medida desde Excel

![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-UnidadesDeMedida-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20260925-yellow)

---

## 📋 Descripción

Crea unidades de medida nuevas o **actualiza el nombre** de las existentes a partir de un archivo de Excel. Antes de guardar, el sistema le muestra qué va a crear, qué va a actualizar y qué filas tienen errores. **Nunca elimina unidades.**

> 🔐 Necesita el permiso **Exportar** sobre la opción Unidades de medida (es el mismo permiso de Exportar a Excel).

---

## 🎯 Acceso

En [Unidades de medida](unidades-medida.md), haga clic en **Importar** (junto a **Exportar a Excel**).

La importación tiene tres pasos: **Cargar archivo → Revisar → Resultado**.

---

## 1️⃣ Cargar archivo

![Cargar archivo](../recursos/img/unidades-medida/05-importar-cargar.png)

1. Haga clic en **Descargar plantilla**. Se descarga `unidades-medida-plantilla.xlsx` con las columnas **Código** y **Nombre**.
2. Llene **una fila por unidad**:
   - Si el **código ya existe**, se actualiza su **nombre**.
   - Si el **código no existe**, se **crea** la unidad.
3. Guarde el archivo y arrástrelo al recuadro, o haga clic en **Seleccionar archivos**.

| Regla | Detalle |
|-------|---------|
| Formato | Excel `.xlsx`. Solo se lee la **primera hoja**. |
| Encabezado | La primera fila debe tener **Código** y **Nombre** (con o sin tilde, en mayúsculas o minúsculas). El orden de las columnas no importa. |
| Tamaño | Hasta **1.000 filas** y **1 MB**. Si tiene más, divida el archivo. |
| Filas vacías | Se ignoran; en **Revisar** se indica cuántas se omitieron ("Filas vacías omitidas"). |
| Código | Hasta 5 caracteres: letras, números y guion. Se guarda en mayúsculas. Los códigos de la versión anterior con símbolos (como `$`) se aceptan porque ya existen. |
| Nombre | Hasta 30 caracteres, sin comas ni punto y coma. |

Si el archivo no sirve (no es Excel, le falta alguna columna, está vacío o es muy grande), verá el motivo y no se envía nada.

---

## 2️⃣ Revisar

El sistema valida cada fila **sin guardar nada** y le muestra un resumen:

![Revisar la importación](../recursos/img/unidades-medida/06-importar-revisar.png)

| Indicador | Significado |
|-----------|-------------|
| **Nuevas** | Códigos que no existen: se crearán. |
| **Se actualizan** | Códigos que ya existen con otro nombre: se cambiarán (debajo verá **Antes: …** con el nombre actual). |
| **Sin cambios** | Códigos que ya existen con el mismo nombre: no se toca nada. |
| **Con error** | Filas que **no se importarán**. Debajo del estado verá el motivo. |

Use las pestañas **Todas / Nuevas / Se actualizan / Sin cambios / Con error** para filtrar la tabla, y el buscador para ubicar una fila.

### Errores por fila

| Mensaje | Cómo corregirlo |
|---------|-----------------|
| Falta el código. / Falta el nombre. | Complete la celda. |
| El código tiene más de 5 caracteres. | Acorte el código. |
| El código solo puede tener letras, números y guion. | Quite espacios, tildes, barras u otros símbolos. |
| El código / El nombre no puede tener comas ni punto y coma. | Quite `,` y `;`. |
| El nombre tiene más de 30 caracteres. | Acorte el nombre. |
| El código se repite en el archivo (filas …). | Deje una sola fila por código. Todas las filas repetidas quedan con error. |

> 💡 **Descargar filas con error** genera un Excel solo con esas filas y su motivo, para corregirlas y volver a cargarlas.

> 🔄 Si mientras revisa otro usuario cambia unidades de medida, verá *"Otro usuario cambió unidades de medida mientras revisabas. Vuelve a validar antes de aplicar."* Haga clic en **Volver a validar** para que la revisión tenga en cuenta esos cambios.

---

## 3️⃣ Aplicar y resultado

Haga clic en **Aplicar N cambios** (N = nuevas + se actualizan). Las filas con error se omiten.

- Todo se guarda **junto**: si algo falla, **no se guarda ningún cambio** y puede reintentar.
- Si otro usuario cambió unidades mientras usted revisaba, verá el aviso de cambios: haga clic en **Volver a validar** y revise de nuevo.

![Resultado de la importación](../recursos/img/unidades-medida/07-importar-resultado.png)

Al terminar verá el resumen (creadas, actualizadas, sin cambios y con error). Use **Ver unidades de medida** para volver al listado, que ya muestra los cambios, o **Importar otro archivo**.

---

## ❓ Preguntas frecuentes

**¿Puedo cambiar el código de una unidad con la importación?**
No. El código es lo que identifica la unidad: si pone un código distinto, se crea una nueva. Para cambiar un código use **Editar** en [Unidades de medida](unidades-medida.md).

**¿La importación borra las unidades que no están en el archivo?**
No. Nunca elimina unidades.

**No veo el botón Importar.**
Su perfil necesita el permiso **Exportar** sobre Unidades de medida. Consulte a su administrador.
