[Regresar a Ventas](../readme.md)

---

# Ficha del vendedor · Clientes no asignados

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Vendedores-blue)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## Descripción

La pestaña **Clientes no asignados** muestra las **sucursales de la compañía que atiende otro vendedor**, con el **vendedor actual** de cada una. Sirve para saber quién atiende a quién y para detectar huecos de cobertura.

También permite ver los **clientes sin sucursal**: clientes que todavía no tienen ninguna sucursal registrada.

Desde aquí también puede **asignar sucursales a este vendedor**, si su perfil tiene permiso para actualizar **Vendedores** y **Clientes**. Ver [Asignar a este vendedor](#asignar-a-este-vendedor). Sin ese permiso, la pantalla es solo de consulta.

> Para el uso general de las tablas (orden, paginación y ayuda) vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Maestros de Ventas**, haga clic en **Vendedores**.
3. Busque el vendedor y haga clic en el lápiz (**Editar**) de su fila.
4. Haga clic en la pestaña **Clientes no asignados**.

---

## Pantalla principal

![Clientes no asignados del vendedor](../recursos/img/vendedores-ficha/06-clientes-no-asignados.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la ficha. |
| **Buscar cliente, sucursal o ciudad** | Filtra la lista. Escriba al menos 2 letras; la búsqueda se aplica sola mientras escribe. Para quitar el texto, use **Quitar la búsqueda**. |
| **Clientes sin sucursal** | Casilla que muestra solo los clientes que todavía no tienen ninguna sucursal. Se aplica al instante. Ver [Clientes sin sucursal](#clientes-sin-sucursal). |
| **Exportar Excel** | Descarga la lista filtrada. Ver [Exportar a Excel](#exportar-a-excel). |
| **Asignar a este vendedor** | Asigna a este vendedor las sucursales que marcó. Solo con permiso para actualizar. Ver [Asignar a este vendedor](#asignar-a-este-vendedor). |
| **Sucursales** y **Clientes distintos** | Cuántas sucursales aparecen en la lista y cuántos clientes diferentes son. |
| **Tabla de sucursales** | Una sucursal por fila, con el vendedor que la atiende hoy. |

### Columnas de la tabla

| Columna | Qué muestra |
|---------|-------------|
| **Elegir** | Casilla para marcar la sucursal que quiere asignar. Solo aparece con permiso para actualizar. |
| **Cliente** | Nombre del cliente. |
| **Código** | Código de la sucursal. |
| **Sucursal** | Nombre de la sucursal. |
| **Ciudad** | Ciudad de la sucursal. |
| **Zona** | Zona de la sucursal. |
| **Lista de precios** | Lista de precios de la sucursal. |
| **Vendedor actual** | Vendedor que atiende hoy la sucursal. Si no tiene vendedor, dice **Sin vendedor**. |

Por defecto la lista va por **Cliente** y **Código**, de la A a la Z.

### Clientes sin sucursal

Al marcar **Clientes sin sucursal**, la lista muestra solo los clientes que no tienen ninguna sucursal registrada. Son clientes que, por ahora, no tienen un vendedor asignado en ninguna sucursal.

Si no hay clientes en esa situación, la pantalla muestra **Todos los clientes tienen al menos una sucursal**.

Para volver a la lista completa, desmarque la casilla.

![Clientes sin sucursal en la ficha del vendedor](../recursos/img/vendedores-ficha/07-clientes-sin-sucursal.png)

---

## Asignar a este vendedor

Puede asignar a este vendedor las sucursales de la lista. La asignación se hace **por sucursal**, no por cliente.

**Permiso:** necesita **Actualizar** en **Vendedores** y en **Clientes**. Sin ese permiso, el botón **Asignar a este vendedor** no aparece.

### Paso a paso

1. Marque la casilla **Elegir** de cada sucursal que quiera asignar. Puede marcar **hasta 200 sucursales** por vez. La selección se conserva al pasar de página.
2. Para marcar toda la página, use **Seleccionar esta página**. Para quitar todo, use **Quitar la selección**. El contador muestra cuántas sucursales lleva marcadas (por ejemplo, **3 sucursales seleccionadas**).
3. Pulse **Asignar a este vendedor**. Se abre el diálogo **Asignar sucursales a este vendedor**.
4. Lea el resumen: **Se asignarán [n] sucursales de [m] clientes a este vendedor.** Debajo aparece lo que cambia: las ventas y comisiones **futuras** de esas sucursales se atribuirán a este vendedor.
5. Opcional: escriba un **Motivo** (hasta 200 caracteres). Queda en la bitácora.
6. Pulse **Asignar**.

*(captura pendiente: selección de sucursales con casillas, y el diálogo de confirmación)*

### Si una sucursal ya tiene otro vendedor

Si alguna sucursal marcada ya la atiende otro vendedor, el diálogo muestra el aviso **Hay sucursales que ya tienen otro vendedor**, con el texto **Dejarán de ser atendidas por: [vendedores]**. Esa asignación **reasigna** la sucursal.

Para continuar, marque la casilla **Confirmo que quiero reasignar estas sucursales**. Sin esa casilla no se puede asignar.

*(captura pendiente: aviso de reasignación en el diálogo)*

### Reglas de la asignación

- **Todo o nada**: se asignan todas las sucursales marcadas o ninguna. Si algo falla, no cambia ninguna sucursal y aparece **No se pudo asignar. No se cambió nada; intente de nuevo.**
- **No es retroactivo**: las facturas ya emitidas **conservan su vendedor**. Solo cambian las ventas y comisiones que se emitan después.
- **Clientes sin sucursal**: un cliente que no tiene ninguna sucursal no se puede marcar. Créela desde la ficha del cliente y vuelva a intentar.
- **Bitácora**: cada asignación queda en la bitácora de la compañía, con el motivo si lo escribió.

Cuando se asigna bien, aparece **[n] sucursales asignadas** (o **1 sucursal asignada**) y la lista se actualiza.

### Si otra persona cambió la sucursal antes

Si otra persona cambió el vendedor de alguna de las sucursales que usted marcó antes de que usted asigne, aparece el aviso **Otra persona cambió estas sucursales**, con el texto **No se asignó nada. La lista se actualizó; revise y vuelva a seleccionar.** La lista se recarga, las marcas se quitan y no se escribe nada. Revise la lista nueva y vuelva a marcar lo que necesite.

---

## Mensajes

| Mensaje | Qué hacer |
|---------|-----------|
| **Este vendedor atiende todas las sucursales de la compañía** | No hay sucursales atendidas por otro vendedor. La lista está vacía a propósito. |
| **No hay sucursales atendidas por otro vendedor.** | Es el detalle del mensaje anterior. |
| **Todos los clientes tienen al menos una sucursal** | Con la casilla **Clientes sin sucursal** marcada no hay clientes sin sucursal en la compañía. |
| **Ninguna sucursal coincide con la búsqueda** | Pruebe con otro texto o pulse **Quitar la búsqueda**. |
| **No se pudo cargar la información** | Sus filtros se conservaron. Pulse **Reintentar**. |
| **No se pudo exportar. Intente de nuevo.** | Pulse **Exportar Excel** otra vez. |
| **Hay más de 50.000 filas con este filtro.** | Acote la búsqueda y exporte de nuevo. |
| **No tiene permiso para ver esta información** | Su perfil no puede consultar los clientes del vendedor. Pida el acceso a su administrador. |
| **Solo se pueden asignar 200 sucursales por vez. Asigne este lote y repita con las demás.** | Asigne el lote y, después, marque el resto. |
| **Hay sucursales con otro vendedor: marque la confirmación de reasignación para continuar.** | Marque **Confirmo que quiero reasignar estas sucursales** y pulse **Asignar**. |
| **Este cliente no tiene sucursal: créela desde su ficha para poder asignarla.** | Cree la sucursal en la ficha del cliente y vuelva a intentar. |
| **La selección no es válida (lote vacío, de más de 200 sucursales o de otra compañía). Revísela.** | Revise la selección y vuelva a marcar las sucursales. |
| **Otra persona cambió estas sucursales** | No se asignó nada. Revise la lista que se recargó y vuelva a seleccionar. |
| **No se pudo asignar. No se cambió nada; intente de nuevo.** | Pulse **Asignar a este vendedor** otra vez. |
| **No tiene permiso para asignar sucursales (se requiere Actualizar en Vendedores y en Clientes).** | Pida el permiso a su administrador. |

Si el vendedor de la ficha no es vendedor de esta compañía, la pantalla muestra **Vendedor no disponible**.

---

## Exportar a Excel

1. Aplique la búsqueda y la casilla **Clientes sin sucursal** que necesite.
2. Pulse **Exportar Excel**.
3. El archivo trae las filas filtradas, con el encabezado de la compañía, los filtros usados, su usuario y la fecha.

Si el resultado supera **50.000 filas**, el sistema no exporta. Acote la búsqueda y vuelva a intentar.

---

## Qué ve cada permiso

| Permiso | Qué ve |
|---------|--------|
| Consultar **Vendedores** y **Clientes** | La pestaña **Clientes no asignados** completa. |
| Consultar **Vendedores** sin **Clientes** | La pestaña no aparece. |
| Exportar **Vendedores** | El botón **Exportar Excel**. |
| Actualizar en **Vendedores** y en **Clientes** | Además, las casillas **Elegir** y el botón **Asignar a este vendedor**. |

---

## Cambios de otros usuarios

Esta pantalla **no se actualiza sola**. Si otra persona cambia el vendedor de una sucursal mientras la mira, recargue la ficha para ver la lista al día.

Si otra persona cambió una de las sucursales que usted marcó, al pulsar **Asignar** verá el aviso **Otra persona cambió estas sucursales**. No se asigna nada y la lista se recarga. Ver [Si otra persona cambió la sucursal antes](#si-otra-persona-cambió-la-sucursal-antes).

---

## Preguntas frecuentes

**¿Por qué la lista cambia según el vendedor que abro?**
Porque muestra las sucursales que atiende **otro** vendedor. Cada vendedor tiene su propia lista.

**¿Qué significa Sin vendedor en la columna Vendedor actual?**
La sucursal no tiene vendedor registrado. Revise la sucursal en la ficha del cliente.

**¿Esta pestaña cambia el vendedor de un cliente?**
Solo si usted lo confirma. Sin permiso para actualizar, es de consulta. Con el permiso, cambia el vendedor de las sucursales que marque y confirme en **Asignar a este vendedor**.

**¿Las facturas ya emitidas cambian de vendedor si asigno la sucursal?**
No. La asignación **no es retroactiva**: las facturas ya emitidas conservan su vendedor. Solo cambian las ventas y comisiones futuras.

**¿Por qué no puedo asignar más de 200 sucursales de una vez?**
Es el límite por lote. Asigne 200 y repita con las demás.

---

## Relacionado

- [Ficha del vendedor · Clientes asignados](ficha-clientes-asignados.md)
- [Ficha del vendedor · Ventas](ficha-ventas.md)
- [Ficha del vendedor · Cartera](ficha-cartera.md)
- [Ficha del vendedor · Comisiones](ficha-comisiones.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
