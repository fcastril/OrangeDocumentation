[Regresar a Inventarios](../readme.md)

---

# 🔍 Inventario físico — Detalle del conteo

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-InventarioFisico-blue)
![Static Badge](https://img.shields.io/badge/Opcion-313-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261005-yellow)

---

## 📋 Descripción

En esta pantalla ve el **resumen del conteo** (bodega, fecha, estado, responsable, observaciones) y el **detalle de todas las lecturas agrupadas por variante** (referencia, atributos, cantidad y número de lecturas). También accede a las **acciones del ciclo de vida**: cerrar, reabrir y anular.

Es el lugar para revisar el conteo antes de cerrarlo, después de cerrado para ver si es correcto, o después de ajustado para consultar qué sobrantes y faltantes se generaron.

---

## 🎯 Acceso

Desde **[Conteos](conteos.md)**:

1. Haga clic en **Ver** en la fila del conteo.

O desde **[Captura](captura.md)**:

1. Haga clic en **Ver detalle** en la cabecera.

---

## 🖥️ Pantalla principal

![Pantalla de detalle del conteo mostrando el resumen (bodega, fecha, estado, responsable), totales (Lecturas, Variantes, Unidades), y tabla de variantes contadas con códigos, referencias, atributos, lecturas y cantidades. Botones de acciones (Capturar, Cerrar, Anular) en la cabecera.](../recursos/img/inventario-fisico/05-detalle-abierto.png)

### Cabecera

| Elemento | Para qué sirve |
|----------|----------------|
| **Volver a conteos** | Regresa al listado de [Conteos](conteos.md). |
| **Bodega, Fecha, Tipo, Estado** | Resumen del conteo. Solo lectura. |
| **En vivo** | La pantalla está conectada. Ver *Cambios en vivo*. |
| **Capturar** | Botón disponible si el conteo está Abierto y usted tiene permiso de Crear. Abre la pantalla de [Captura](captura.md). |
| **Cerrar**, **Reabrir**, **Anular** | Acciones del ciclo de vida. Disponibles según el estado y su permiso. Ver *Acciones*. |

### Sección de resumen

Muestra en una lista de definición (en celular una columna, en escritorio tres):

| Campo | Qué ve |
|-------|--------|
| **Bodega** | La bodega donde se contó. |
| **Fecha del conteo** | Fecha en formato local (p. ej., *10/05/2026*). Si muestra la marca **Fecha no válida**, es un histórico que no se puede cerrar. |
| **Tipo** | **Completo** o **Aleatorio** (según lo que declaró al crear). |
| **Estado** | El estado actual: Abierto (🟢), Cerrado (🟡), Ajustado (🟣) o Anulado (🔴). |
| **Responsable** | Quién creó el conteo. |
| **Creado** | Fecha y hora de creación en zona local. |
| **Cierre** | Si está Cerrado o Ajustado, fecha y hora del cierre. Si está Abierto, dice *"Sin cerrar"*. |
| **Observaciones** | Las observaciones ingresadas al crear (opcional). Si no hay, dice *"Sin observaciones"*. |
| **Movimientos de ajuste** | Si el conteo está Ajustado, muestran los ids de los movimientos de sobrantes y faltantes generados. Si fue ajustado antes de que el sistema guardara los ids, dice *"Ajustado antes de que el sistema guardara los movimientos de ajuste."* |

### Avisos

Si hay datos históricos problemáticos, aparecen avisos:

| Aviso | Qué significa |
|-------|--------------|
| 📍 **Fecha no válida** | El conteo es histórico y su fecha está fuera del rango permitido (antes de 01/01/2000 o en el futuro). No se puede cerrar, pero sí anular. |
| 📍 **Cantidad no positiva** | El conteo histórico tiene líneas con cantidad ≤ 0. Se muestran marcadas y no se modifican. |

### Sección de detalle — Resumen por variante

| Columna | Qué ve |
|---------|--------|
| **Código** | Código de referencia (p. ej., `CAM-001`). |
| **Referencia** | Nombre de la referencia. |
| **Atributo principal** (si aplica) | Talla, color o el primer atributo (p. ej., *M*, *Azul*). |
| **Atributo secundario** (si aplica) | El segundo atributo (p. ej., *Corte clásico*). |
| **Lecturas** | Número de líneas registradas de esta variante (si escanea la misma variante 3 veces, suma 3). |
| **Cantidad** | Suma de las cantidades. Si la marca dice **Cantidad no positiva**, es un histórico que el sistema no toca. |

### Paginación y búsqueda

- **Paginación en servidor**: 25 variantes por página. Use los botones de página.
- **Búsqueda**: Escriba por referencia o atributos. Exige **2 o más caracteres**. No distingue mayúsculas ni tildes. Se filtra al instante.
- **Orden**: Puede ordenar por referencia, lecturas o cantidad (haga clic en el encabezado de la columna).

### Estado de carga

- Si está cargando el conteo, aparece un esqueleto.
- Si el conteo no existe (fue eliminado o pertenece a otra compañía), ve *"El conteo ya no existe"*.
- Si hay un error al cargar, ve un aviso con **Reintentar**.

---

## ⚙️ Acciones según el estado

### Abierto (🟢)

**Disponibles:**
- **Capturar**: Abre la pantalla de [Captura](captura.md) para registrar más lecturas.
- **Cerrar**: Fija el conteo como listo para ajuste (ver *Cerrar un conteo*).
- **Anular**: Descarta el conteo con trazabilidad.

**No disponibles:**
- Reabrir (no tiene sentido, ya está abierto).

### Cerrado (🟡)

**Disponibles:**
- **Reabrir**: Vuelve a Abierto para registrar más lecturas (si no está Ajustado). Ver *Reabrir un conteo*.
- **Anular**: Descarta el conteo.

**No disponibles:**
- Capturar (está cerrado, pero puede reabrirlo para capturar).
- Cerrar (ya está cerrado).

### Ajustado (🟣)

**Disponibles:**
- Solo **Ver** (consulta).

**No disponibles:**
- Capturar, Cerrar, Reabrir, Anular. El estado Ajustado es irreversible: el comparativo generó los movimientos de sobrantes y faltantes.

### Anulado (🔴)

**Disponibles:**
- Solo **Ver** (consulta).

**No disponibles:**
- Capturar, Cerrar, Reabrir, Anular (ya está anulado y no se puede reabrir).

---

## 🔴 Cerrar el conteo

Desde esta pantalla puede cerrar un conteo Abierto:

1. Haga clic en **Cerrar**.
2. Se abre un diálogo con el resumen: *"El conteo tiene {{lecturas}} lecturas, {{variantes}} variantes y {{unidades}} unidades."*
3. Explica: *"Al cerrarlo ya no se podrán registrar ni eliminar lecturas. Podrás reabrirlo mientras no se haya ajustado."*
4. Haga clic en **Cerrar conteo**.

El botón muestra *Procesando…* mientras espera respuesta. Si hay error, verá el mensaje dentro del diálogo.

### Validaciones

- El conteo debe tener **al menos una lectura**.
- La **fecha debe ser válida** (entre 01/01/2000 y hoy). Los históricos con fecha inválida no se pueden cerrar, pero sí anular.

Al cerrar exitosamente, el estado cambia a **Cerrado** (🟡) y aparece el aviso *"Conteo de [Bodega] del [Fecha] cerrado."*

---

## 🔄 Reabrir el conteo

Si cerró por error o necesita agregar más lecturas:

1. Haga clic en **Reabrir** (disponible solo en conteos Cerrados no ajustados).
2. Se abre un diálogo: *"El conteo volverá a estar abierto para registrar y eliminar lecturas."*
3. Advierte: *"Si ya hay otro conteo completo abierto de la misma bodega y fecha, no se podrá reabrir."*
4. Haga clic en **Reabrir conteo**.

El estado vuelve a **Abierto** (🟢) y puede seguir capturando desde [Captura](captura.md).

### Validación

Si intenta reabrir un conteo completo y ya existe otro conteo completo abierto de la misma bodega y fecha, el servidor lo rechaza.

---

## ❌ Anular el conteo

Para descartar el conteo de forma definitiva con trazabilidad:

1. Haga clic en **Anular**.
2. Se abre un diálogo: *"El conteo quedará anulado y no se tendrá en cuenta para el ajuste. Las lecturas se conservan, pero un conteo anulado no se puede reabrir."*
3. **Motivo** (opcional): Hasta 500 caracteres. Queda registrado en la bitácora.
4. Haga clic en **Anular conteo**.

El estado cambia a **Anulado** (🔴) y aparece el aviso *"Conteo de [Bodega] del [Fecha] anulado."*

### Validaciones

- No se puede anular un conteo **Ajustado** (estado irreversible).
- Un conteo **Anulado** no se puede reabrir.

---

## 🔄 Cambios en vivo

Si otro usuario cierra, reabre o anula el conteo mientras usted lo consulta:

1. El estado se actualiza al instante.
2. Aparece el aviso: *"Este conteo cambió a «{{Estado}}» por otro usuario."*
3. Si el cambio afecta las acciones disponibles (p. ej., otro lo cerró y usted no puede reabrirlo), los botones se actualizan.

Puede hacer clic en **Actualizar** si necesita refrescar toda la información.

---

## 🔐 Permisos y visibilidad

### Con Consultar

- Ve el resumen y el detalle.
- No ve los botones de acción (Cerrar, Reabrir, Anular, Capturar).
- Solo lectura.

### Sin Actualizar

- No ve **Cerrar** ni **Reabrir**.

### Sin Eliminar

- No ve **Anular**.

### Sin Crear

- No ve **Capturar** (no puede registrar lecturas).

---

## ❓ Preguntas frecuentes

**¿Qué es la marca "Fecha no válida"?**

Es un conteo histórico cuya fecha está fuera del rango permitido (antes de 01/01/2000 o en el futuro). Puede consultar sus datos, pero no cerrarlo. Use **Anular** para descartarlo.

**¿Qué significa "Cantidad no positiva"?**

Una línea histórica con cantidad ≤ 0. El sistema las muestra sin modificarlas (es dato del pasado). Si crea una lectura nueva con cantidad 0 o negativa, el servidor la rechaza.

**¿Qué significa "Ajustado antes de que el sistema guardara los movimientos"?**

Es un conteo ajustado antes de esta versión de OrangeERP, cuando el sistema no guardaba los ids de los movimientos generados. Los datos están; solo falta la referencia.

**¿Puedo reabrir un conteo ajustado?**

No. **Ajustado** es irreversible: el comparativo generó los movimientos de sobrantes y faltantes y ajustó el inventario del sistema. Para contar de nuevo esa bodega, cree un nuevo conteo.

**¿Qué diferencia hay entre Cerrado y Ajustado?**

- **Cerrado**: El conteo está listo para que alguien genere el comparativo y el ajuste. Puede reabrirlo si cambió de idea.
- **Ajustado**: Ya se ejecutó el comparativo. Se generaron movimientos de sobrantes y faltantes, y se actualizó el inventario. No se puede reabrir.

**¿Cuándo aparecen los "Movimientos de ajuste"?**

Cuando el conteo está en estado **Ajustado** (🟣). Muestra los ids de los movimientos de entrada por sobrantes y salida por faltantes. Si el conteo fue ajustado en versión anterior y esos ids no se grabaron, dice *"Ajustado antes de que el sistema guardara los movimientos."*

**¿Cómo busco una variante en el detalle?**

Escriba 2 o más caracteres en el campo de búsqueda. Puede buscar por código o nombre de referencia, o por atributos (p. ej., *azul*, *M*). Sin mayúsculas ni tildes.

---

## 📍 Siguiente paso

- Vuelva a **[Conteos](conteos.md)** para cerrar el conteo o continuar capturando.
- Si el conteo está en estado **Cerrado**, comunique al jefe de inventarios para que genere el **[Comparativo y ajuste](ajuste.md)** (opción 316).
