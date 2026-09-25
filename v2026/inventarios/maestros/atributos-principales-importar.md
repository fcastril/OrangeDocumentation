[Regresar a Atributos principales](atributos-principales.md)

---

# 📥 Importar atributos principales desde Excel

![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-AtributosPrincipales-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20260925-yellow)

---

## 📋 Descripción

Crea atributos principales nuevos o **actualiza el nombre y el orden** de los existentes a partir de un archivo de Excel. Es la forma más rápida de cargar las tallas de una colección o de **reordenarlas** todas de una vez. Antes de guardar, el sistema le muestra qué va a crear, qué va a actualizar y qué filas tienen errores. **Nunca elimina atributos.**

> 🔐 Necesita el permiso **Exportar** sobre la opción Atributos principales (es el mismo permiso de Exportar a Excel).

---

## 🎯 Acceso

En [Atributos principales](atributos-principales.md), haga clic en **Importar** (junto a **Exportar a Excel**).

La importación tiene tres pasos: **Cargar archivo → Revisar → Resultado**.

---

## 1️⃣ Cargar archivo

![Cargar archivo](../recursos/img/atributos-principales/05-importar-cargar.png)

1. Haga clic en **Descargar plantilla**. Se descarga `atributos-principales-plantilla.xlsx` con las columnas **Código**, **Nombre** y **Orden**.
2. Llene **una fila por atributo**:
   - Si el **código ya existe**, se actualizan su **nombre** y su **orden**.
   - Si el **código no existe**, se **crea** el atributo.
3. Guarde el archivo y arrástrelo al recuadro, o haga clic en **Seleccionar archivos**.

| Regla | Detalle |
|-------|---------|
| Formato | Excel `.xlsx`. Solo se lee la **primera hoja**. |
| Encabezado | La primera fila debe tener **Código**, **Nombre** y **Orden** (con o sin tilde, en mayúsculas o minúsculas). El orden de las columnas no importa. |
| Tamaño | Hasta **1.000 filas** y **1 MB**. Si tiene más, divida el archivo. |
| Filas vacías | Se ignoran. |
| Código | Hasta 5 caracteres: letras, números, guion y barra (`/`). Se guarda en mayúsculas. |
| Nombre | Hasta 100 caracteres, sin comas ni punto y coma. |
| Orden | **Obligatorio** en cada fila. Número entero de 0 a 9999; puede repetirse. Es la posición de la talla en informes y matrices. |

> ⚠️ Excel puede cambiar algunos códigos al escribirlos: `06/08` lo convierte en una **fecha** y `01` en el número `1`. La columna **Código** de la plantilla ya viene en formato **Texto** para evitarlo; si usa otro archivo, ponga esa columna en formato Texto antes de escribir los códigos.

Si el archivo no sirve (no es Excel, le falta alguna columna, está vacío o es muy grande), verá el motivo y no se envía nada.

---

## 2️⃣ Revisar

El sistema valida cada fila **sin guardar nada** y le muestra un resumen:

![Revisar la importación](../recursos/img/atributos-principales/06-importar-revisar.png)

| Indicador | Significado |
|-----------|-------------|
| **Nuevos** | Códigos que no existen: se crearán. |
| **Se actualizan** | Códigos que ya existen con otro nombre u otro orden: se cambiarán (debajo verá **Antes: …** con el valor actual). |
| **Sin cambios** | Códigos que ya existen con el mismo nombre y el mismo orden: no se toca nada. |
| **Con error** | Filas que **no se importarán**. Debajo del estado verá el motivo. |

Use las pestañas **Todas / Nuevos / Se actualizan / Sin cambios / Con error** para filtrar la tabla, y el buscador para ubicar una fila.

### Errores por fila

| Mensaje | Cómo corregirlo |
|---------|-----------------|
| Falta el código. / Falta el nombre. / Falta el orden. | Complete la celda. |
| El código tiene más de 5 caracteres. | Acorte el código. |
| El código solo puede tener letras, números, guion y barra. | Quite espacios, tildes u otros símbolos. |
| El código / El nombre no puede tener comas ni punto y coma. | Quite `,` y `;`. |
| El nombre tiene más de 100 caracteres. | Acorte el nombre. |
| El orden debe ser un número entero entre 0 y 9999. | Quite decimales, signos, puntos de miles o texto. |
| El código se repite en el archivo (filas …). | Deje una sola fila por código. Todas las filas repetidas quedan con error. |

> 💡 **Descargar filas con error** genera un Excel solo con esas filas y su motivo, para corregirlas y volver a cargarlas.

> 🔄 Si mientras revisa otro usuario cambia atributos principales, verá *"Otro usuario cambió atributos principales mientras revisabas. Vuelve a validar antes de aplicar."* Haga clic en **Volver a validar** para que la revisión tenga en cuenta esos cambios.

---

## 3️⃣ Aplicar y resultado

Haga clic en **Aplicar N cambios** (N = nuevos + se actualizan). Las filas con error se omiten.

- Todo se guarda **junto**: si algo falla, **no se guarda ningún cambio** y puede reintentar.
- Si otro usuario cambió atributos mientras usted revisaba, verá el aviso de cambios: haga clic en **Volver a validar** y revise de nuevo.

![Resultado de la importación](../recursos/img/atributos-principales/07-importar-resultado.png)

Al terminar verá el resumen (creados, actualizados, sin cambios y con error). Use **Ver atributos principales** para volver al listado, que ya muestra los cambios, o **Importar otro archivo**.

---

## ❓ Preguntas frecuentes

**¿Cómo reordeno todas las tallas de una vez?**
Use **Exportar a Excel** en el listado, cambie la columna **Orden** en el archivo (puede borrar la columna *Última modificación*) e impórtelo. Solo cambiarán las tallas cuyo orden sea distinto.

**¿Puedo cambiar el código de un atributo con la importación?**
No. El código es lo que identifica el atributo: si pone un código distinto, se crea uno nuevo. Para cambiar un código use **Editar** en [Atributos principales](atributos-principales.md).

**¿La importación borra los atributos que no están en el archivo?**
No. Nunca elimina atributos.

**No veo el botón Importar.**
Su perfil necesita el permiso **Exportar** sobre Atributos principales. Consulte a su administrador.
