[Regresar al módulo Inventarios](../readme.md)

---

# Ajuste de Inventario Físico

La opción **Ajuste de Inventario Físico** permite realizar ajustes automáticos de inventario con base en el comparativo entre inventario teórico y físico, generando los movimientos necesarios para cuadrar las diferencias detectadas.

## Ruta

Inventarios → Procesos → Ajuste de Inventario Físico

## ¿Qué se puede hacer?

- Generar movimientos de ajuste para cuadrar diferencias entre inventario teórico y físico.
- Permitir valores unitarios en cero exclusivamente desde este módulo, cumpliendo validaciones de negocio y seguridad.
- Validar automáticamente que el tercero asociado corresponda al NIT de la empresa activa. Si no existe, se solicita registrar el tercero antes de continuar.
- Limitar observaciones a 200 caracteres y mostrar mensajes claros de validación.

## Pasos de uso

1. Ingresar a la opción **Ajuste de Inventario Físico**.
2. Seleccionar la fecha de corte y la bodega a ajustar.
3. Consultar el comparativo y revisar las diferencias.
4. Ingresar observaciones (máx. 200 caracteres).
5. Generar el ajuste. El sistema validará automáticamente los datos y mostrará mensajes claros en caso de error.

## Notas funcionales

- Solo se permite valor unitario en cero desde este proceso.
- El tercero utilizado en el movimiento debe coincidir con el NIT de la empresa activa.
- Si no existe el tercero, se debe registrar previamente en el módulo de terceros.
- Los mensajes de validación y error se muestran en pantalla mediante alertas estándar.

---

> Para más información sobre el comparativo, consulte también: [Comparativo de Inventarios Físicos](comparativo-inventarios-fisicos.md)
