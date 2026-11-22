[Regresar a Contabilidad](readme.md)

---

# CENTROS DE COSTO

## Qué es

Los **centros de costo** son las áreas por las que la compañía separa sus costos y sus ingresos, por ejemplo, Administración o Producción. Cada centro tiene un código, un nombre, cuatro casillas de clasificación y seis tipos de movimiento que le asignan automáticamente las ventas y los recibos de caja.

Desde aquí consulta, crea, edita y elimina los centros de costo de su compañía, y puede importarlos desde Excel.

## Cómo llegar

- Abra **Contabilidad** en el menú principal y luego **Maestros > Centro de costos**.
- Necesita permiso de **Consultar** sobre Centro de costos. Si no ve la opción, pida a su administrador que se lo asigne.

## Permisos

- **Consultar**: ve el listado y puede buscar, ordenar y paginar.
- **Crear**: ve el botón **Nuevo centro de costos**.
- **Actualizar**: puede abrir un centro, cambiarlo y guardarlo.
- **Eliminar**: puede eliminar un centro.
- **Exportar**: ve el botón **Importar** para cargar centros desde Excel. Ver [Importar centros de costo](centros-costo-importar.md).

Si solo tiene **Consultar**, no ve los botones de crear, editar, eliminar ni importar.

## Pantalla principal

La pantalla muestra una tabla con las columnas **Código**, **Nombre** y **Última modificación**. La lista llega ordenada por **Nombre**.

- **Buscar**: escriba parte del código o del nombre. No importan las mayúsculas ni las tildes.
- **Ordenar**: pulse el encabezado de una columna.
- **Páginas**: la tabla se divide en páginas, con controles de abajo.

Estados de la pantalla:

- **Cargando**: mientras se obtiene la lista.
- **Vacío**: la compañía todavía no tiene centros de costo.
- **Sin resultados**: la búsqueda no encuentra nada. Cambie el texto para buscar de nuevo.
- **Error**: la lista no carga. Pulse **Reintentar**.

## Crear un centro de costos

1. Pulse **Nuevo centro de costos**.
2. Escriba el **Código** y el **Nombre**.
3. Marque las casillas de **Clasificación del centro** que correspondan.
4. Si el centro se usa en ventas o en recibos de caja, elija los tipos de movimiento en **Tipos de movimiento**. Si no, déjelos vacíos.
5. Pulse **Guardar**.

Campos:

- **Código**: obligatorio, hasta 10 caracteres. Solo admite letras, números y guion. Se guarda en mayúsculas.
- **Nombre**: obligatorio, hasta 50 caracteres. No admite comas ni punto y coma.
- **Clasificación del centro**: cuatro casillas que pueden marcarse juntas: **Administrativo**, **Ventas**, **Producción** y **Otras ventas**.
- **Tipos de movimiento**: seis campos opcionales. Vacío significa ninguno.
  - Cinco son de ventas: ventas de contado, devoluciones de ventas de contado, ventas a crédito, devoluciones de ventas a crédito y ventas manuales.
  - Uno es de recibos de caja.

Solo puede elegir los tipos de movimiento a los que su usuario tiene acceso.

- El código no puede repetirse en su compañía. Si ya existe, la pantalla no guarda y le indica que el código está en uso.

Si un campo no cumple, la pantalla lo señala y conserva lo que escribió en el diálogo.

## Editar un centro de costos

1. Busque el centro y pulse **Editar** en su fila.
2. Cambie los datos que necesite. El diálogo muestra las casillas y los tipos de movimiento actuales.
3. Pulse **Guardar**.

Si cambia el código de un centro que ya existía, la pantalla le avisa antes de guardar.

Si un centro tiene un tipo de movimiento que su usuario no tiene autorizado, ese tipo se conserva sin cambios al editar el centro. Solo puede cambiarlo si tiene acceso a ese tipo.

## Eliminar un centro de costos

1. Pulse **Eliminar** en la fila del centro.
2. Revise los datos en el diálogo y confirme.

Si el centro ya se usa en otros módulos (por ejemplo, en activos fijos, cajeros, diferidos, saldos contables, movimientos contables, documentos o tipos de movimiento), no se elimina. La pantalla lo indica y el centro sigue en la lista.

## Importar centros de costo

Desde la lista, con el botón **Importar**, puede cargar muchos centros a la vez desde un archivo de Excel. El proceso tiene tres pasos: **Cargar archivo**, **Revisar** (vista previa) y **Resultado**.

- **Plantilla**: pulse **Descargar plantilla**. Tiene 6 columnas: **Código** (obligatorio), **Nombre** (obligatorio), **Administrativo**, **Ventas**, **Producción** y **Otras ventas**. En las cuatro últimas escriba **1** para sí y **0** o vacío para no.
- **Vista previa**: cada fila dice si es **Nuevo**, **Se actualiza**, **Sin cambios** o **Error**, con el motivo. No se guarda nada hasta confirmar.
- **Errores**: si hay filas con error, no se aplica nada. Corrija el archivo y vuelva a cargarlo.
- **Aplicar**: guarda todo a la vez. Los centros que no están en el archivo no se modifican ni se eliminan, y los tipos de movimiento de los centros existentes no cambian.

El proceso completo, con sus mensajes y sus límites, está en [Importar centros de costo](centros-costo-importar.md).

## Cambios de otros usuarios en vivo

Si otro usuario crea, cambia o elimina un centro, la lista se actualiza sola, la fila cambiada se resalta y aparece un aviso. Si otro usuario importa centros, la lista se actualiza y aparece un aviso con la cantidad importada.

## Preguntas frecuentes

**¿Por qué no veo el botón Nuevo centro de costos?**
Su usuario no tiene permiso para crear. Pida a su administrador que se lo asigne.

**¿Por qué no veo el botón Importar?**
Importar requiere el permiso de **Exportar** sobre Centro de costos. Pida a su administrador que lo revise.

**¿Por qué no aparece un tipo de movimiento en la lista?**
Solo aparecen los tipos a los que su usuario tiene acceso. Si el centro ya tenía uno que no puede ver, se conserva al editar.

**¿Por qué no puedo eliminar un centro de costos?**
Otro módulo de la compañía lo está usando. Mientras esté en uso, no se elimina.

**¿Qué significa dejar un tipo de movimiento vacío?**
Que el centro no se usa para ese tipo de movimiento.
