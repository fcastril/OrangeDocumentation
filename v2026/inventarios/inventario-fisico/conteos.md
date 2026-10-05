[Regresar a Inventarios](../readme.md)

---

# 📋 Inventario físico — Conteos

![Static Badge](https://img.shields.io/badge/Tipo-CRUDMaestro-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-InventarioFisico-blue)
![Static Badge](https://img.shields.io/badge/Opcion-313-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261005-yellow)

---

## 📋 Descripción

Un **conteo** es una toma de inventario físico: una lista de referencias y variantes que cuenta el equipo en una bodega en una fecha. Cada conteo tiene un **estado** (Abierto, Cerrado, Ajustado o Anulado) que marca su ciclo de vida. En esta pantalla puede **listar conteos, crearlos, capturar lecturas, cerrarlos, reabrirlos, anularlos y consultar su detalle**.

El conteo puede ser **completo** (se cuenta toda la bodega) o **aleatorio** (solo algunas referencias), como el usuario declare al crearlo. Las lecturas se registran con un escáner tipo teclado o manualmente, desde el celular o la computadora.

En esta pantalla el jefe de inventarios ve todos los conteos abiertos, cerrados o ajustados de la compañía, con sus totales: cuántas lecturas, variantes y unidades tiene cada uno.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Inventarios**.
2. En **Maestros**, haga clic en **Inventario físico**.

---

## 🖥️ Pantalla principal

<!-- CAPTURA PENDIENTE: story Pantallas/Inventario/Inventario físico/Conteos/Listado -->

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. Ver *Cambios de otros usuarios* más abajo. |
| **Nuevo conteo** | Abre el diálogo para crear un conteo. Ver *Crear un conteo*. |
| **Estado**, **Bodega**, **Desde**, **Hasta** | Filtros del listado. Ver *Filtrar el listado*. |
| **Limpiar filtros** | Restablece todos los filtros a su valor inicial. |
| **Fecha**, **Bodega**, **Tipo**, **Estado**, **Lecturas**, **Unidades**, **Responsable** | Columnas del listado. Ver la tabla de abajo. |
| Acciones en la primera columna | Según el estado y su permiso: **Capturar**, **Ver**, **Cerrar**, **Reabrir** y **Anular**. Ver *Acciones según el estado*. |

### Columnas

| Columna | Qué ve |
|---------|--------|
| **Fecha** | Fecha del conteo (fecha del calendario, sin hora). Si muestra la marca **Fecha no válida**, es un histórico con fecha fuera de rango (2000-01-01 a hoy): puede verlo y anularlo, pero no cerrarlo. |
| **Bodega** | La bodega donde se cuenta. |
| **Tipo** | **Completo**: se cuenta toda la bodega. **Aleatorio**: se cuentan solo algunas referencias. |
| **Estado** | El estado actual del conteo, con icono y color. Ver *Estados* abajo. Si muestra **(histórico)**, es un conteo anterior que el sistema derivó del estado anterior; no es un error. |
| **Lecturas** | Número de lecturas registradas en el conteo (si registró 10 veces el mismo código, suma 10). |
| **Unidades** | Suma de las cantidades de todas las lecturas. |
| **Responsable** | Quién creó el conteo (el usuario del token en ese momento). |

### Estados

| Estado | Significado |
|--------|------------|
| **Abierto** 🟢 | El conteo está en captura: puede registrar y eliminar lecturas, cerrar el conteo o anularlo. |
| **Cerrado** 🟡 | El conteo ya no acepta lecturas nuevas. Puede reabrirlo (si no está Ajustado) o anularlo. |
| **Ajustado** 🟣 | El comparativo se ejecutó y generó los movimientos de sobrantes y faltantes. No se puede reabrir ni anular. |
| **Anulado** 🔴 | El conteo se descartó con trazabilidad. Las lecturas se conservan. No se puede reabrir. |

---

## 🔍 Buscar y filtrar

### Filtros

Los filtros se aplican en memoria sin recargar la página. Combínese para acotar el listado:

| Filtro | Opciones | Efecto |
|--------|----------|--------|
| **Estado** | Abierto · Cerrado · Ajustado · Anulado · Todos | Muestra solo conteos en ese estado. Por defecto, todos. |
| **Bodega** | Busque el nombre o código. Un buscador con las bodegas de la compañía. | Filtra por bodega. Sin filtro, todas las bodegas. |
| **Desde** | Fecha de calendario | Muestra conteos desde esa fecha en adelante (inclusive). |
| **Hasta** | Fecha de calendario | Muestra conteos hasta esa fecha hacia atrás (inclusive). |

- Al cambiar un filtro, el listado se actualiza al instante.
- **Limpiar filtros** restablece todo al estado inicial.
- Si **Desde** es posterior a **Hasta**, verá un aviso *La fecha inicial no puede ser posterior a la final*.

---

## ➕ Crear un conteo

1. Haga clic en **Nuevo conteo**. Se abre un diálogo.
2. **Tipo de conteo**: Seleccione **Completo** o **Aleatorio**.
   - **Completo**: se cuenta toda la bodega. Las referencias que no se escaneen y tengan saldo en el sistema se marcan como cero al generar el ajuste.
   - **Aleatorio**: se cuentan solo algunas referencias. Al ajustar, el sistema solo verifica las referencias que usted escaneó, con todas sus variantes.
3. **Bodega**: Seleccione la bodega donde se contará. Busque por código o nombre.
4. **Fecha del conteo**: Elija una fecha entre 01/01/2000 y hoy. Una fecha válida es obligatoria para poder cerrar el conteo después.
5. **Observaciones** (opcional): Hasta 500 caracteres. Por ejemplo, *Cierre anual*, *Conteo de sobrantes*, etc. Queda registrada.
6. Haga clic en **Crear conteo**.

### Validaciones

- **Bodega**: Es obligatoria. Debe ser una bodega de su compañía.
- **Fecha**: Es obligatoria y debe estar entre 01/01/2000 y hoy.
- **Observaciones**: Máximo 500 caracteres.

Si falla algún campo, el diálogo lo marca con rojo y el foco va al primero inválido.

### Regla de unicidad (Conteos completos)

Si ya existe un conteo **completo** abierto en la misma bodega y fecha, el servidor responde con el aviso:

> *Para esta bodega y fecha ya hay un conteo completo abierto.*

El diálogo le ofrece **Continuar el conteo existente**, que lo cierra y lo lleva a capturar en ese conteo.

> ℹ️ Los conteos **aleatorios** no tienen esta restricción: puede haber varios abiertos en la misma bodega y fecha.

---

## 👁️ Ver el listado según su permiso

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil sobre la opción Inventario físico (313):

| Permiso | Qué habilita |
|---------|--------------|
| **Consultar** | Ver el listado, abrir conteos en consulta (solo lectura), ver detalles y lecturas |
| **Crear** | **Nuevo conteo**, registrar y eliminar lecturas |
| **Actualizar** | **Cerrar** y **Reabrir** conteos |
| **Eliminar** | **Anular** conteos |

---

## ⚙️ Acciones según el estado

Las acciones están en la **primera columna** de cada fila, con objetivos táctiles de 44×44 píxeles. El nombre accesible incluye la bodega y fecha para saber de cuál conteo es cada botón.

| Estado | Acciones |
|--------|----------|
| **Abierto** | **Capturar** (registrar lecturas), **Ver** (consultar sin editar), **Cerrar**, **Anular** |
| **Cerrado** | **Ver**, **Reabrir** (si no está Ajustado), **Anular** |
| **Ajustado** | **Ver** solamente |
| **Anulado** | **Ver** solamente |

> ℹ️ Si le falta el permiso de Actualizar, el botón **Cerrar** y **Reabrir** no aparecen (en su lugar no ve nada, no un botón deshabilitado). Si le falta Eliminar, no ve **Anular**.

---

## 📌 Cerrar un conteo

Cuando termina de capturar, cierre el conteo:

1. Haga clic en **Cerrar** en la fila del conteo.
2. Se abre un diálogo que resume: *El conteo tiene **N lecturas**, **M variantes** y **X unidades**.*
3. El diálogo explica: *Al cerrarlo ya no se podrán registrar ni eliminar lecturas. Podrás reabrirlo mientras no se haya ajustado.*
4. Haga clic en **Cerrar conteo**.

El botón muestra *Procesando…* mientras espera respuesta. Si hay un error del servidor, verá el mensaje dentro del diálogo.

Al cerrar exitosamente, el estado cambia a **Cerrado** y aparece el aviso *Conteo de [Bodega] del [Fecha] cerrado.*

### Validación al cerrar

- El conteo debe tener **al menos una lectura**.
- La fecha debe ser válida (entre 2000-01-01 y hoy). Los históricos con fecha inválida no se pueden cerrar, pero sí anular.

---

## 🔄 Reabrir un conteo

Si cerró por error o necesita agregar más lecturas:

1. Haga clic en **Reabrir** en la fila del conteo (solo aparece en conteos **Cerrados** no ajustados).
2. Se abre un diálogo: *El conteo volverá a estar abierto para registrar y eliminar lecturas.*
3. El diálogo advierte: *Si ya hay otro conteo completo abierto de la misma bodega y fecha, no se podrá reabrir.*
4. Haga clic en **Reabrir conteo**.

El estado vuelve a **Abierto** y puede seguir capturando.

---

## 🔴 Anular un conteo

Para descartar un conteo de forma definitiva con trazabilidad (en lugar de borrarlo):

1. Haga clic en **Anular** en la fila del conteo.
2. Se abre un diálogo: *El conteo quedará anulado y no se tendrá en cuenta para el ajuste. Las lecturas se conservan, pero un conteo anulado no se puede reabrir.*
3. **Motivo** (opcional): Hasta 500 caracteres. Por ejemplo, *Conteo equivocado*, *Interrupción*, etc. Queda registrado en la bitácora.
4. Haga clic en **Anular conteo**.

El estado cambia a **Anulado** (🔴) y aparece el aviso *Conteo de [Bodega] del [Fecha] anulado.*

---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica o anula conteos mientras usted tiene abierta esta pantalla, **no tiene que recargar**: el listado se actualiza solo.

- Las filas nuevas o modificadas se **resaltan** unos segundos.
- Abajo a la derecha aparece un aviso, por ejemplo *"Otro usuario creó un conteo…"* o *"Otro usuario cerró el conteo de Bodega Principal del 2026-10-05."*
- Junto a la descripción verá **En vivo** mientras la conexión esté activa. Si se interrumpe, dice **Reconectando…**; al volver, la pantalla se actualiza sola.

> ℹ️ Los cambios que usted hace en esta misma pestaña no generan avisos.

---

## ❓ Preguntas frecuentes

**¿Cuál es la diferencia entre completo y aleatorio?**

Un conteo **completo** cuenta toda la bodega: lo que no se escanee y tenga existencia en el sistema se marca como cero al generar el ajuste. Sirve para limpiezas de bodega o auditorías.

Un conteo **aleatorio** cuenta solo lo que usted escanea. Sirve para verificar referencia por referencia sin tener que recorrer toda la bodega.

**¿Por qué no puedo crear otro conteo completo de la misma bodega y fecha?**

El sistema no permite dos conteos completos abiertos de la misma bodega en la misma fecha, para evitar duplicados. Si necesita otro, cierre o anule el primero, o cree un aleatorio en paralelo.

**¿Qué significa "Fecha no válida"?**

Es un conteo histórico cuya fecha está fuera del rango permitido (antes de 01/01/2000 o en el futuro). Puede verlo y anularlo, pero no cerrarlo. El sistema nunca corrige esa fecha.

**¿Qué significa el estado "(histórico)"?**

Los conteos anteriores a esta versión de OrangeERP están marcados como históricos si el estado se derivó de los datos guardados (p. ej., `Activo=0` se interpreta como "Ajustado" en el sistema anterior). No es un error; solo indica que viene de una versión anterior.

**¿Puedo eliminar un conteo?**

No hay un botón "Eliminar". Para descartar un conteo use **Anular**, que lo marca como inactivo y conserva su historia para auditoría.

**¿Qué pasa si cierro un conteo sin haber registrado lecturas?**

El servidor rechaza el cierre con el mensaje *"No se puede cerrar un conteo sin lecturas."* Registre al menos una lectura antes de cerrar.

**¿Se puede reabrir un conteo que ya se ajustó?**

No. Una vez que el conteo está en estado **Ajustado**, ya se generaron los movimientos de sobrantes y faltantes. No se puede reabrir ni anular.

---

## 📍 Siguiente paso

- Cree un conteo y vaya a **[Captura de conteo](captura.md)** para registrar lecturas.
- Consulte **[Detalle del conteo](detalle.md)** para ver el resumen y las acciones por estado.
