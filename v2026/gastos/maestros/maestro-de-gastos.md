[Regresar a Gastos](../readme.md)

---

# 🧾 Maestro de Gastos

![Static Badge](https://img.shields.io/badge/Tipo-MaestroTipoII-red)
![Static Badge](https://img.shields.io/badge/Module-Gastos-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-MaestroDeGastos-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261021-yellow)

---

## 📋 Descripción

El **Maestro de Gastos** es la lista de **conceptos de gasto** de la compañía: por ejemplo, arrendamiento de oficina, energía eléctrica o servicios de mensajería. Cada concepto (una **referencia de gasto**) tiene su código, su nombre, su subgrupo, su unidad de medida, sus impuestos (IVA), sus cuentas contables y, si lo necesita, sus proveedores y sus documentos adjuntos.

Las referencias de gasto son las que se eligen al registrar una **solicitud** o una **causación de gasto**. Por eso conviene mantenerlas al día.

En esta pantalla puede **consultar, crear, editar y eliminar** referencias de gasto de la compañía con la que está trabajando.

> 📘 La búsqueda, el orden, la paginación y la ayuda funcionan igual que en el resto de las pantallas. Para la página donde crea o modifica una referencia, vea [Detalle de una referencia de gasto](maestro-de-gastos-detalle.md).

> 💡 Cada pestaña del navegador trabaja con **una compañía**. El nombre de la compañía aparece en el título de la pestaña y en la barra superior.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Gastos**.
2. En **Maestros**, haga clic en **Maestro de Gastos**.

---

## 🖥️ Pantalla principal

![Listado del Maestro de Gastos](../recursos/img/maestro-de-gastos/01-listado.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **En vivo** | La pantalla está conectada: los cambios de otros usuarios aparecen solos. Ver *Cambios de otros usuarios* más abajo. |
| **Nueva referencia** | Abre la página para crear una referencia de gasto. |
| **Estado** | Muestra **Activas** (predeterminado), **Inactivas** o **Todas**. |
| **Subgrupo** | Limita el listado a un subgrupo. Escriba el código o el nombre para buscarlo. |
| **Buscar por código o nombre** | Filtra el listado mientras escribe. Escriba al menos 2 letras. No distingue mayúsculas ni tildes. |
| **Limpiar filtros** | Vuelve a Estado = Activas y quita el subgrupo. Aparece solo cuando hay un filtro distinto del predeterminado. |
| **Lápiz** / **Papelera** | Editar o eliminar la referencia de esa fila. Están en la **primera columna**. |
| **Encabezados** | Un clic ordena de forma ascendente, el segundo descendente y el tercero quita el orden. |
| **Filas por página** y paginación | Cambian cuántas referencias ve por página (10, 20, 50 o 100) y la página. |

Las columnas son **Código**, **Nombre**, **Subgrupo** (con el grupo debajo), **Unidad**, **Estado** (Activa o Inactiva) y **Última modificación** (fecha y hora del último cambio). Al entrar, las referencias aparecen de la más reciente a la más antigua.

Encima de la tabla verá el resumen: **64 referencias activas** sin búsqueda, o **2 resultados para «arr-00»** mientras busca.

> 📱 En el celular cada referencia se muestra como una tarjeta, con las acciones arriba.

**¿No ve algún botón?** Cada acción depende de los permisos de su perfil sobre la opción Maestro de Gastos:

| Permiso | Qué habilita |
|---------|--------------|
| Consultar | Ver la pantalla y las referencias |
| Crear | **Nueva referencia** |
| Actualizar | **Lápiz** (editar). Sin este permiso, el lápiz se convierte en **Ver** y la referencia se abre en solo consulta. |
| Eliminar | **Papelera** (eliminar) |

![Listado con solo permiso de consulta](../recursos/img/maestro-de-gastos/04-solo-consulta.png)

Con solo el permiso de consulta el listado se ve completo, pero no aparecen los botones de crear, editar ni eliminar.

> ℹ️ Los permisos de la opción Maestro de Gastos son independientes de los de **Referencias** de Inventarios. Tener permisos en Referencias no da acceso a esta pantalla, y al revés.

---

## 🔎 Buscar, filtrar y ordenar

- **Buscar:** escriba un código o parte de un nombre. El listado se actualiza solo, unos instantes después de dejar de escribir. Por ejemplo, *ARR* encuentra *ARR-001* y *Arrendamiento oficina*.
- **Estado:** en **Activas** solo ve las referencias que se pueden elegir al registrar un gasto. Elija **Inactivas** o **Todas** para ver también las que dejó de usar.
- **Subgrupo:** elija un subgrupo para ver solo sus referencias.
- **Orden:** haga clic en el encabezado de la columna. El orden se mantiene al cambiar de página.

![Listado con filtros y búsqueda](../recursos/img/maestro-de-gastos/02-filtros.png)

Si la búsqueda o los filtros no encuentran nada, verá **Sin resultados** con el botón **Limpiar búsqueda**. Si busca una referencia que sabe que existe y no aparece, cambie **Estado** a **Todas**: puede estar inactiva.

![Sin resultados](../recursos/img/maestro-de-gastos/03-sin-resultados.png)

Si todavía no hay referencias de gasto en la compañía, verá **Aún no hay referencias de gasto** y, si tiene permiso para crear, el botón **Nueva referencia**.

---

## ➕ Crear una referencia de gasto

1. Haga clic en **Nueva referencia**.
2. Complete los datos en la pestaña **Referencia** y, si lo necesita, en **Configuración contable**.
3. Haga clic en **Guardar referencia**.

Al guardar verá el mensaje **"Referencia {nombre} creada"**. La página queda abierta en la referencia recién creada, lista para agregarle proveedores y documentos.

Para los campos y sus reglas, vea [Detalle de una referencia de gasto](maestro-de-gastos-detalle.md#-crear-una-referencia-de-gasto).

---

## ✏️ Editar una referencia de gasto

1. Haga clic en el **lápiz** de la referencia.
2. Cambie los datos que necesite y haga clic en **Guardar referencia**.

Si no cambió nada, el sistema no guarda nada y le indica **"No había cambios que guardar"**.

Para los detalles de cada campo, vea [Detalle de una referencia de gasto](maestro-de-gastos-detalle.md#-editar-una-referencia-de-gasto).

---

## 🗑️ Eliminar una referencia de gasto

1. Haga clic en la **papelera** de la referencia.
2. Revise el código y el nombre que aparecen en el mensaje y confirme con **Eliminar**.

Al confirmar, la referencia desaparece del listado y verá el mensaje **"Referencia {nombre} eliminada"**. Esta acción no se puede deshacer: con la referencia se borran también sus proveedores y sus documentos adjuntos.

### Referencia que ya se usó

Una referencia **no se puede eliminar** si ya se usó en una solicitud o en una causación de gasto. Esto protege los gastos registrados: si se borrara la referencia, esos documentos quedarían sin concepto.

En ese caso verá el aviso **"No se puede eliminar"**, con el código y el nombre de la referencia y la indicación de inactivarla:

![Referencia en uso: no se puede eliminar](../recursos/img/maestro-de-gastos/05-eliminar-en-uso.png)

El botón **Ir a inactivarla** lleva a la referencia con el campo **Activa** listo para desmarcarlo. Después, haga clic en **Guardar referencia**.

![Ir a inactivarla](../recursos/img/maestro-de-gastos/06-ir-a-inactivar.png)

**Inactivar** no borra nada: la referencia sigue en el listado (con el estado **Inactiva**) y puede verla con el filtro **Inactivas** o **Todas**. Lo que cambia es que deja de ofrecerse al registrar nuevas solicitudes y causaciones de gasto. Si la necesita de nuevo, vuelva a marcar **Activa**.

> ℹ️ Una referencia que nunca se usó en un documento sí se elimina. Solo tiene que confirmar.

---

## 🔄 Cambios de otros usuarios (en vivo)

Si otra persona crea, modifica o elimina referencias de gasto mientras usted tiene abierto el listado, **no tiene que recargar**: el listado se pone al día solo, sin perder lo que buscó, el filtro, el orden ni la página.

- Las filas nuevas o modificadas se **resaltan** unos segundos.
- Abajo a la derecha aparece un aviso, por ejemplo *"Otro usuario creó la referencia ARR-002."*
- Junto a la descripción verá **En vivo** mientras la conexión esté activa. Si se interrumpe, verá **Reconectando…**; al volver, la pantalla se actualiza sola.

![Otro usuario crea una referencia](../recursos/img/maestro-de-gastos/07-tiempo-real.png)

Si estaba editando una referencia que otro usuario cambió o eliminó, vea [Detalle de una referencia de gasto](maestro-de-gastos-detalle.md#-cambios-de-otros-usuarios-en-vivo).

> ℹ️ Los cambios que usted hace en esta misma pestaña no generan avisos.

---

## ❓ Preguntas frecuentes

**¿Por qué no veo una referencia que sé que existe?**
Es probable que esté inactiva. Cambie **Estado** a **Todas**. También revise que esté en la compañía correcta (título de la pestaña) y que no tenga un subgrupo elegido en el filtro.

**¿Qué significa "Inactiva"?**
La referencia no se ofrece al registrar nuevas solicitudes o causaciones de gasto. Los documentos que ya la usaron no cambian.

**¿Por qué no puedo eliminar una referencia?**
Porque ya se usó en una solicitud o en una causación de gasto. Inactívela para que deje de ofrecerse. Vea *Referencia que ya se usó* más arriba.

**¿Por qué no encuentro el botón Nueva referencia, Editar o Eliminar?**
Su perfil no tiene ese permiso sobre la opción Maestro de Gastos. Pida a su administrador que lo revise.

**¿Puedo exportar el listado a Excel o importar referencias desde Excel?**
Por ahora no. Estas opciones no están disponibles en esta pantalla.

**No veo "En vivo".**
La conexión en vivo no está disponible en este momento (por ejemplo, por la red de su empresa). La pantalla funciona igual; para ver los cambios de otros usuarios, recargue la página.

**El listado no carga y aparece "No se pudieron cargar las referencias de gasto".**
Revise su conexión y haga clic en **Reintentar**. Si el problema continúa, avise a su administrador.
