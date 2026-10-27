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

Es una pantalla de **consulta**. No cambia el vendedor de ninguna sucursal.

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
| **Sucursales** y **Clientes distintos** | Cuántas sucursales aparecen en la lista y cuántos clientes diferentes son. |
| **Tabla de sucursales** | Una sucursal por fila, con el vendedor que la atiende hoy. |

### Columnas de la tabla

| Columna | Qué muestra |
|---------|-------------|
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

---

## Cambios de otros usuarios

Esta pantalla **no se actualiza sola**. Si otra persona cambia el vendedor de una sucursal mientras la mira, recargue la ficha para ver la lista al día.

---

## Preguntas frecuentes

**¿Por qué la lista cambia según el vendedor que abro?**
Porque muestra las sucursales que atiende **otro** vendedor. Cada vendedor tiene su propia lista.

**¿Qué significa Sin vendedor en la columna Vendedor actual?**
La sucursal no tiene vendedor registrado. Revise la sucursal en la ficha del cliente.

**¿Esta pestaña cambia el vendedor de un cliente?**
No. Es solo de consulta: muestra quién atiende cada sucursal, pero no cambia el vendedor de ninguna.

---

## Relacionado

- [Ficha del vendedor · Clientes asignados](ficha-clientes-asignados.md)
- [Ficha del vendedor · Ventas](ficha-ventas.md)
- [Ficha del vendedor · Cartera](ficha-cartera.md)
- [Ficha del vendedor · Comisiones](ficha-comisiones.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
