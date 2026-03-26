[Regresar a Contabilidad](../readme.md)

---

# Cierre Contable Anual

## Ruta

Contabilidad → Procesos → Cierres Contables

## Objetivo

Ejecutar el cierre contable anual de resultados para la empresa activa, generando los movimientos y asientos contables del proceso de cierre.

## Parámetros requeridos

- **Año:** año a cerrar.
- **Cierre Actual:** tipo de movimiento usado para el cierre del año actual.
- **Cierre Anterior:** tipo de movimiento usado para el cierre del año anterior.
- **PUC Actual Utilidad:** cuenta contable de utilidad del año actual.
- **PUC Actual Pérdida:** cuenta contable de pérdida del año actual.
- **PUC Anterior Utilidad:** cuenta contable de utilidad del año anterior.
- **PUC Anterior Pérdida:** cuenta contable de pérdida del año anterior.

Los campos de tipos de movimiento y PUC se seleccionan con listas desplegables **Select2** con búsqueda y paginación.

## Procedimiento

1. Ingrese el **Año** que desea cerrar.
2. Seleccione los tipos de movimiento de **Cierre Actual** y **Cierre Anterior**.
3. Seleccione las cuentas PUC para utilidad y pérdida (actual y anterior).
4. Haga clic en **Aceptar**.

## Validaciones del sistema

Antes de ejecutar el cierre, el sistema valida:

- Que todos los parámetros obligatorios estén diligenciados.
- Que el año sea válido.
- Que no exista un cierre anual previo para el mismo año y tipos de movimiento, tomando como base los **movimientos contables** registrados.

Si alguna validación falla, se muestra un mensaje de advertencia indicando los parámetros faltantes o la causa funcional.

## Resultado esperado

- Si el proceso termina correctamente, se muestra el mensaje:
  - **"Cierre contable anual ejecutado correctamente."**
- Si existe un cierre previo o ocurre una validación de negocio, se informa el motivo y no se ejecuta nuevamente el cierre.

## Recomendaciones

- Ejecutar el cierre con un usuario autorizado de Contabilidad.
- Verificar previamente que los tipos de movimiento y cuentas PUC correspondan a la parametrización contable de la empresa.
- Realizar el proceso fuera de horas pico, ya que puede tardar según el volumen de información.

## Reproceso del cierre anual

Si se requiere volver a ejecutar el cierre anual y ya existe un cierre realizado para el mismo año y tipos de movimiento:

1. Ingrese a **Contabilidad → Movimientos → Asientos Contables** (o la consulta de movimientos contables habilitada en su perfil).
2. Ubique los **dos movimientos contables de cierre** generados en la ejecución anterior (cierre actual y cierre anterior).
3. Realice la acción correspondiente según políticas de la empresa:
  - **Anular** los dos movimientos, o
  - **Eliminar** los dos movimientos.
4. Una vez anulados/eliminados ambos movimientos de cierre, vuelva al formulario de **Cierre Contable Anual** y ejecute nuevamente el proceso.

> Nota: si solo se anula/elimina uno de los dos movimientos, el sistema puede seguir bloqueando la nueva ejecución por validación de cierre previo.