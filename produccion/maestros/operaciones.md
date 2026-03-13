[Regresar a Producción](../readme.md)

---
# OPERACIONES DE PRODUCCIÓN

## Objetivo

Administrar el catálogo de operaciones de producción, incluyendo su tipo, código, descripción, ícono y color de visualización.

## Acceso

- Ruta: Producción > Maestros > Operaciones.

## Campos principales

- Tipo de Operación
- Código Operación
- Descripción Operación
- Ícono (Font Awesome)
- Color
- Última Operación

## Reglas visuales de ícono y color

- Si el campo **Ícono** está vacío, se usa por defecto `fa fa-black-tie`.
- Si el campo **Color** está vacío, se usa por defecto `black`.
- En el listado, la descripción se muestra con:
  - Ícono configurado.
  - Texto en el color configurado.

## Crear/Editar

En el formulario de creación/edición se dispone de:

- Selector de ícono (catálogo Font Awesome disponible en la aplicación).
- Campo de color (texto + selector de color).
- Ejemplo visual en tiempo real para validar cómo se verá la operación.

## Dónde se refleja esta configuración

La configuración de ícono y color se reutiliza en:

- Referencias (tab Operaciones).
- Movimientos de Producción.
- Trazabilidad.
- Estado de Órdenes de Producción.
- Reporte Órdenes Producción Resumen.
