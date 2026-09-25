[Regresar a Bodegas](bodegas.md)

---

# 📥 Importar bodegas desde Excel

![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Bodegas-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20260925-yellow)

---

## 📋 Descripción

Crea bodegas nuevas o **actualiza el nombre** de las existentes a partir de un archivo de Excel. Antes de guardar, el sistema le muestra qué va a crear, qué va a actualizar y qué filas tienen errores. **Nunca elimina bodegas.**

> 🔐 Necesita el permiso **Exportar** sobre la opción Bodegas (es el mismo permiso de Exportar a Excel).

---

## 🎯 Acceso

En [Bodegas](bodegas.md), haga clic en **Importar** (junto a **Exportar a Excel**).

La importación tiene tres pasos: **Cargar archivo → Revisar → Resultado**.

---

## 1️⃣ Cargar archivo

![Cargar archivo](../recursos/img/bodegas/05-importar-cargar.png)

1. Haga clic en **Descargar plantilla**. Se descarga `bodegas-plantilla.xlsx` con las columnas **Código** y **Nombre**.
2. Llene **una fila por bodega**:
   - Si el **código ya existe**, se actualiza su **nombre**.
   - Si el **código no existe**, se **crea** la bodega.
3. Guarde el archivo y arrástrelo al recuadro, o haga clic en **Seleccionar archivos**.

| Regla | Detalle |
|-------|---------|
| Formato | Excel `.xlsx`. Solo se lee la **primera hoja**. |
| Encabezado | La primera fila debe tener **Código** y **Nombre** (con o sin tilde, en mayúsculas o minúsculas). El orden de las columnas no importa. |
| Tamaño | Hasta **1.000 filas** y **1 MB**. Si tiene más, divida el archivo. |
| Filas vacías | Se ignoran. |
| Código | Hasta 10 caracteres: letras, números y guion. Se guarda en mayúsculas. |
| Nombre | Hasta 50 caracteres, sin comas ni punto y coma. |

Si el archivo no sirve (no es Excel, le faltan las columnas, está vacío o es muy grande), verá el motivo y no se envía nada.

---

## 2️⃣ Revisar

El sistema valida cada fila **sin guardar nada** y le muestra un resumen:

![Revisar la importación](../recursos/img/bodegas/06-importar-revisar.png)

| Indicador | Significado |
|-----------|-------------|
| **Nuevas** | Códigos que no existen: se crearán. |
| **Se actualizan** | Códigos que ya existen con otro nombre: se cambiará el nombre (debajo verá **Antes: …**). |
| **Sin cambios** | Códigos que ya existen con el mismo nombre: no se toca nada. |
| **Con error** | Filas que **no se importarán**. Debajo del estado verá el motivo. |

Use las pestañas **Todas / Nuevas / Se actualizan / Sin cambios / Con error** para filtrar la tabla, y el buscador para ubicar una fila.

### Errores por fila

| Mensaje | Cómo corregirlo |
|---------|-----------------|
| Falta el código. / Falta el nombre. | Complete la celda. |
| El código tiene más de 10 caracteres. | Acorte el código. |
| El código solo puede tener letras, números y guion. | Quite espacios, tildes o símbolos. |
| El código / El nombre no puede tener comas ni punto y coma. | Quite `,` y `;`. |
| El nombre tiene más de 50 caracteres. | Acorte el nombre. |
| El código se repite en el archivo (filas …). | Deje una sola fila por código. Todas las filas repetidas quedan con error. |

> 💡 **Descargar filas con error** genera un Excel solo con esas filas y su motivo, para corregirlas y volver a cargarlas.

---

## 3️⃣ Aplicar y resultado

Haga clic en **Aplicar N cambios** (N = nuevas + se actualizan). Las filas con error se omiten.

- Todo se guarda **junto**: si algo falla, **no se guarda ningún cambio** y puede reintentar.
- Si otro usuario cambió bodegas mientras usted revisaba, verá **"Otro usuario cambió bodegas mientras revisabas"**: haga clic en **Volver a validar** y revise de nuevo.

![Resultado de la importación](../recursos/img/bodegas/07-importar-resultado.png)

Al terminar verá el resumen (creadas, actualizadas, sin cambios y con error). Use **Ver bodegas** para volver al listado, que ya muestra los cambios, o **Importar otro archivo**.

---

## ❓ Preguntas frecuentes

**¿Puedo cambiar el código de una bodega con la importación?**
No. El código es lo que identifica la bodega: si pone un código distinto, se crea una bodega nueva. Para cambiar un código use **Editar** en [Bodegas](bodegas.md).

**¿La importación borra las bodegas que no están en el archivo?**
No. Nunca elimina bodegas.

**No veo el botón Importar.**
Su perfil necesita el permiso **Exportar** sobre Bodegas. Consulte a su administrador.
