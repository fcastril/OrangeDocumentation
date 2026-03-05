[Regresar al Inicio](../readme.md)

---

# Comparativo de Inventarios Físicos

## Ruta

Inventarios → Procesos → Comparativo de Inventarios

## Objetivo

Comparar el inventario teórico contra el inventario físico para una bodega y fecha de corte específica, identificando diferencias en unidades y su impacto en valor.

## Filtros

- **Fecha de Corte:** fecha sobre la cual se calcula el inventario teórico y se cruza con el inventario físico.
- **Bodega:** bodega a consultar.

## Consulta

1. Ingrese la **Fecha de Corte**.
2. Seleccione la **Bodega**.
3. Haga clic en **Consultar**.

El sistema muestra una tabla paginada con:

- Referencia
- Descripción
- Atributo principal
- Atributo secundario
- Inventario teórico
- Inventario físico
- Diferencia
- Costo teórico
- Valor diferencia

## Exportaciones

- **Excel:** exporta el resultado consultado con encabezado de empresa, filtros, usuario y total de valor diferencia.
- **PDF:** genera la impresión del comparativo con los mismos filtros y total de valor diferencia.

## Notas funcionales

- La paginación se realiza en la grilla de la interfaz (DataTable).
- No se requiere ajuste adicional de la función SQL para paginación en esta primera versión.
- El resultado depende de la información registrada en inventario físico y movimientos de inventario a la fecha de corte.
