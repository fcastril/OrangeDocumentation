[Regresar a Ventas](../readme.md)

---

# Ficha del vendedor · Clientes asignados

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Vendedores-blue)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## Descripción

La pestaña **Clientes asignados** muestra las **sucursales** de clientes que atiende este vendedor. La asignación se hace por sucursal, no por cliente: un mismo cliente puede tener sucursales atendidas por distintos vendedores.

Es una pantalla de **consulta**: no cambia el vendedor de ninguna sucursal.

> Para el uso general de las tablas (orden, paginación y ayuda) vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Maestros de Ventas**, haga clic en **Vendedores**.
3. Busque el vendedor y haga clic en el lápiz (**Editar**) de su fila.
4. Haga clic en la pestaña **Clientes asignados**.

---

## Pantalla principal

![Clientes asignados del vendedor](../recursos/img/vendedores-ficha/05-clientes-asignados.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la ficha. |
| **Buscar cliente, sucursal o ciudad** | Filtra la lista. Escriba al menos 2 letras; la búsqueda se aplica sola mientras escribe. Para quitar el texto, use **Quitar la búsqueda**. |
| **Exportar Excel** | Descarga la lista filtrada. Ver [Exportar a Excel](#exportar-a-excel). |
| **Sucursales** y **Clientes distintos** | Cuántas sucursales tiene asignadas el vendedor y cuántos clientes diferentes son. |
| **Tabla de sucursales** | Una sucursal por fila. Los encabezados ordenan la lista. |

### Columnas de la tabla

| Columna | Qué muestra |
|---------|-------------|
| **Cliente** | Nombre del cliente. |
| **Código** | Código de la sucursal. |
| **Sucursal** | Nombre de la sucursal. |
| **Ciudad** | Ciudad de la sucursal. |
| **Zona** | Zona de la sucursal. |
| **Lista de precios** | Lista de precios que tiene asignada la sucursal. |

Por defecto la lista va por **Cliente** y **Código**, de la A a la Z.

---

## Mensajes

| Mensaje | Qué hacer |
|---------|-----------|
| **Este vendedor no tiene sucursales asignadas** | Ninguna sucursal de cliente tiene a este vendedor. Cuando se le asigne una sucursal, aparecerá aquí. |
| **Ninguna sucursal coincide con la búsqueda** | Pruebe con otro texto o pulse **Quitar la búsqueda**. |
| **No se pudo cargar la información** | Sus filtros se conservaron. Pulse **Reintentar**. |
| **No se pudo exportar. Intente de nuevo.** | Pulse **Exportar Excel** otra vez. |
| **Hay más de 50.000 filas con este filtro.** | Acote la búsqueda y exporte de nuevo. |
| **No tiene permiso para ver esta información** | Su perfil no puede consultar los clientes del vendedor. Pida el acceso a su administrador. |

---

## Exportar a Excel

1. Escriba la búsqueda que necesite y ordene la lista como quiera verla.
2. Pulse **Exportar Excel**.
3. El archivo trae las sucursales filtradas, con el encabezado de la compañía, los filtros usados, su usuario y la fecha.

Si el resultado supera **50.000 filas**, el sistema no exporta. Acote la búsqueda y vuelva a intentar.

---

## Qué ve cada permiso

| Permiso | Qué ve |
|---------|--------|
| Consultar **Vendedores** y **Clientes** | La pestaña **Clientes asignados** completa. |
| Consultar **Vendedores** sin **Clientes** | La pestaña no aparece. |
| Exportar **Vendedores** | El botón **Exportar Excel**. Sin este permiso no aparece. |

---

## Cambios de otros usuarios

Esta pantalla **no se actualiza sola**. Si otra persona cambia el vendedor de una sucursal mientras la mira, recargue la ficha para ver la lista al día.

---

## Preguntas frecuentes

**¿Por qué un cliente aparece aquí pero no todas sus sucursales?**
La lista es por sucursal. Cada sucursal tiene su propio vendedor; las que no tienen a este vendedor aparecen en **Clientes no asignados**.

**¿Qué diferencia hay entre esta pestaña y las ventas del vendedor?**
Esta pestaña muestra a quién atiende el vendedor según la configuración de sus sucursales. Las ventas muestran lo que realmente facturó en un periodo.

---

## Relacionado

- [Ficha del vendedor · Clientes no asignados](ficha-clientes-no-asignados.md)
- [Ficha del vendedor · Ventas](ficha-ventas.md)
- [Ficha del vendedor · Cartera](ficha-cartera.md)
- [Ficha del vendedor · Comisiones](ficha-comisiones.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
