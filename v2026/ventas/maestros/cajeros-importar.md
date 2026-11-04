[Regresar a Cajeros](cajeros.md)

---

# 📥 Importar cajeros desde Excel

![Static Badge](https://img.shields.io/badge/Tipo-MaestroTipoI-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Cajeros-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261104-yellow)

---

## 📋 Descripción

Crea cajeros nuevos o actualiza los existentes a partir de un archivo de Excel. Antes de guardar, el sistema le muestra qué va a crear, qué va a actualizar y qué filas tienen errores. **Nunca elimina cajeros.**

El archivo tiene **5 columnas**: Caja, Usuario, Tipo de movimiento de venta, Forma de pago y Base. El cliente, la sucursal, la bodega, el centro de costos, el recibo de caja y el descuento **ya no se piden**: se toman del tipo de movimiento de venta.

> 🔐 Necesita el permiso **Exportar** sobre la opción Cajeros (es el mismo permiso de **Exportar a Excel**).

---

## 🎯 Acceso

En [Cajeros](cajeros.md), haga clic en **Importar** (junto a **Exportar a Excel**). La importación tiene tres pasos: **Cargar archivo → Revisar → Resultado**.

---

## 1️⃣ Cargar archivo

![Cargar archivo](../recursos/img/cajeros-importar/01-cargar-archivo.png)

1. Haga clic en **Descargar plantilla**. Se descarga `cajeros-plantilla.xlsx` con las columnas: **Caja, Usuario, Tipo de movimiento de venta, Forma de pago** y **Base**.
2. Llene **una fila por cajero**. Las referencias van por su código o documento: usuario (Login), tipo de movimiento de venta y forma de pago.
3. Guarde el archivo y arrástrelo al recuadro, o haga clic en **Seleccionar archivos**.

La **llave** de cada fila es **Caja + Usuario**: si ya existe un cajero con esa caja y ese usuario, se **actualiza**; si no, se **crea**. Al actualizar, la caja conserva los datos que vienen del tipo de movimiento.

| Regla | Detalle |
|-------|---------|
| Formato | Excel `.xlsx`. Solo se lee la **primera hoja**. |
| Encabezado | La primera fila debe tener los encabezados de la plantilla (con o sin tilde, en mayúsculas o minúsculas). El orden no importa. |
| Tamaño | Hasta **1.000 filas** y **1 MB**. Si tiene más, divida el archivo. |
| Filas vacías | Se ignoran; en **Revisar** se indica cuántas se omitieron. |
| Caja | Obligatoria, hasta 50 caracteres, sin comas ni punto y coma. |
| Usuario | Obligatorio. Debe ser un usuario activo de la compañía. |
| Tipo de movimiento de venta | Obligatorio. Solo los tipos de venta que usted tiene autorizados, y que tengan recibo de caja automático, cliente por defecto con sucursal y bodega. |
| Forma de pago | Obligatoria. |
| Base | Número mayor o igual a 0. |

### Archivos del formato anterior (11 columnas)

Si tiene un archivo con el formato anterior, **también se acepta**. Las columnas **Cliente, Sucursal, Bodega, Centro de costos, Tipo de recibo de caja y Descuento** se **ignoran**: la vista previa muestra un aviso por cada una (*"columna ignorada: se toma del tipo de movimiento"*). Las cinco columnas de la plantilla se procesan como siempre.

Si el archivo no sirve, verá el motivo y no se envía nada: no es un `.xlsx`, faltan columnas, no tiene filas, tiene más de 1.000 filas o pesa más de 1 MB.

![Archivo no válido](../recursos/img/cajeros-importar/02-archivo-invalido.png)

---

## 2️⃣ Revisar

El sistema valida cada fila **sin guardar nada**:

![Revisar la importación](../recursos/img/cajeros-importar/03-vista-previa.png)

| Indicador | Significado |
|-----------|-------------|
| **Nuevos** | Caja + Usuario que no existen: se crearán. |
| **Se actualizan** | Ya existen y algún dato cambia: se actualizan. |
| **Sin cambios** | Ya existen con los mismos datos: no se toca nada. |
| **Con error** | Filas que **no se importarán**. En **Estado** verá el motivo. |

Use las pestañas **Todas / Nuevos / Se actualizan / Sin cambios / Con error** para filtrar la tabla.

### Errores frecuentes

| Mensaje | Cómo corregirlo |
|---------|-----------------|
| *Falta la caja / el usuario / el tipo de venta / la forma de pago / la base.* | Complete la celda. |
| *El usuario no existe o no está activo en esta compañía.* | Revise el Login. |
| *El tipo de venta no existe o no está autorizado para usted.* | Use un tipo de venta al que tenga acceso. |
| *El usuario del cajero no está autorizado a este tipo de venta.* | Use un tipo al que ese usuario tenga acceso, o cambie el usuario de la fila. |
| *El tipo de venta no sirve para el POS: …* | El tipo no tiene recibo de caja automático, cliente con sucursal o bodega. Complételo en Tipos de movimiento, o use otro tipo. |
| *La base debe ser mayor o igual a 0.* | Corrija el número. |
| *La fila se repite en el archivo.* | Deje una sola fila por Caja + Usuario. |
| **Conflicto: ya hay una caja con ese nombre de otro usuario** | Dos cajeros no deberían compartir nombre de caja. El sistema **no lo resuelve solo**: cambie el nombre de la caja o el usuario. |

> 💡 **Descargar filas con error** genera un Excel solo con esas filas, para corregirlas y volver a cargarlas.

Si no hay nada para aplicar, verá *"No hay nada que aplicar"* y el botón queda deshabilitado.

![Vista previa sin errores](../recursos/img/cajeros-importar/04-vista-previa-sin-errores.png)

![Nada que aplicar](../recursos/img/cajeros-importar/05-nada-que-aplicar.png)

---

## 3️⃣ Aplicar y resultado

Haga clic en **Aplicar N cambios** (nuevos + se actualizan). Las filas con error se omiten. Todo se guarda **junto**: si algo falla, **no se guarda ningún cambio**.

Al terminar verá el resumen de cuántos se crearon, cuántos se actualizaron, cuántos no tenían cambios y cuántas filas no se aplicaron por errores. **Ver cajeros** vuelve al listado, que ya muestra los cambios.

![Resultado de la importación](../recursos/img/cajeros-importar/06-resultado.png)

### ¿Qué puede salir mal al aplicar?

| Mensaje | Qué hacer |
|---------|-----------|
| **No se pudo completar la importación.** | Haga clic en **Reintentar**. No se guardó nada. |
| **Los datos cambiaron mientras importaba.** | Otro usuario cambió cajeros; no se guardó nada. Haga clic en **Volver a validar**. |

![Error al aplicar](../recursos/img/cajeros-importar/07-error-servidor.png)

![Conflicto al aplicar](../recursos/img/cajeros-importar/08-conflicto.png)

Si otra persona cambia cajeros mientras usted revisa, verá un aviso para **Volver a validar** antes de aplicar.

---

## ❓ Preguntas frecuentes

**¿Puedo cambiar el nombre de una caja con la importación?**
No: Caja + Usuario es la llave, así que otro nombre crea un cajero nuevo. Para renombrar use **Editar** en [Cajeros](cajeros.md).

**¿Qué pasa con el cliente, la sucursal o la bodega de mi archivo anterior?**
Se ignoran y se toman del tipo de movimiento de venta. La vista previa le avisa de cada columna ignorada.

**¿La importación borra los cajeros que no están en el archivo?**
No. Nunca elimina cajeros.

**No veo el botón Importar.**
Su perfil necesita el permiso **Exportar** sobre Cajeros. Consulte a su administrador.

**Una fila marca "Conflicto" con el nombre de la caja.**
Ya hay una caja con ese nombre asignada a otro usuario. Cambie el nombre o el usuario de la fila; el sistema no elige por usted.
