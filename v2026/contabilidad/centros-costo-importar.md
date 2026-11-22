[Regresar a Contabilidad](readme.md)

---

# IMPORTAR CENTROS DE COSTO

## Qué es

La importación carga muchos centros de costo desde un archivo de Excel. Sirve para crear centros nuevos y para actualizar los que ya existen.

La importación **nunca elimina centros**. Tampoco cambia los tipos de movimiento de los centros que ya existen.

## Cómo llegar

- Abra **Contabilidad** en el menú principal y luego **Maestros > Centro de costos**.
- Pulse **Importar** en la lista.
- Necesita permiso de **Exportar** sobre Centro de costos. Si no ve el botón **Importar**, pida a su administrador que se lo asigne.

La importación tiene tres pasos, que se ven arriba de la pantalla: **Cargar archivo**, **Revisar** y **Resultado**.

## Paso 1: descargar la plantilla y cargar el archivo

1. Pulse **Descargar plantilla**. Es una hoja de Excel con 6 columnas, en este orden:
   - **Código**: obligatorio.
   - **Nombre**: obligatorio.
   - **Administrativo**.
   - **Ventas**.
   - **Producción**.
   - **Otras ventas**.
2. Complete la hoja desde la **fila 2**. La fila 1 tiene los encabezados.
3. En las cuatro columnas de clasificación escriba **1** para sí, o **0** o vacío para no. Cualquier otro valor es un error.
4. Cargue el archivo: arrástrelo a la pantalla o elíjalo desde su equipo.

Reglas del archivo:

- Formato **.xlsx**, con hasta **5.000 filas** y **2 MB**. Se usa la primera hoja.
- Si el archivo supera el tamaño o el número de filas, la pantalla no lo procesa y le pide dividirlo en varios archivos.
- Si el archivo no es un Excel válido, la pantalla no lo procesa. Si no tiene filas para importar, lo indica.
- Las filas vacías se omiten. La pantalla dice cuántas omitió.

## Paso 2: revisar la vista previa

Antes de guardar, la pantalla revisa todas las filas y muestra la vista previa. Arriba aparece un resumen con cuatro conteos: **Nuevos**, **Se actualizan**, **Sin cambios** y **Con error**.

Cada fila tiene un estado:

- **Nuevo**: el centro no existe y se va a crear.
- **Se actualiza**: el centro ya existe y tiene cambios. Si cambia el nombre, la fila muestra el nombre anterior.
- **Sin cambios**: el centro ya está igual en la lista.
- **Error**: la fila tiene un problema, con el motivo al lado.

Puede filtrar las filas por estado. La vista previa no guarda nada.

### Filas con error

Si hay filas con error, la pantalla lo indica y no se puede aplicar nada. Para corregirlas:

1. Corrija esas filas en su Excel.
2. Pulse **Cargar otro archivo** y vuelva a cargar el archivo corregido, o pulse **Volver a validar**.

Los motivos más comunes:

- **Falta el código.** Y **Falta el nombre.**
- **El código tiene más de 10 caracteres.**
- **El código solo admite letras, números y guion.**
- **El código no puede tener comas ni punto y coma.**
- **El nombre tiene más de 50 caracteres.**
- **El nombre no puede tener comas ni punto y coma.**
- **Columna ... solo admite 1, 0 o vacío.** Aplica a las cuatro columnas de clasificación.
- **El código está repetido en las filas ...** Un mismo código no puede aparecer dos veces en el archivo.
- **La fila está vacía.**

## Paso 3: aplicar la importación

Cuando no quede ninguna fila con error, pulse **Aplicar** con el número de cambios (por ejemplo, **Aplicar 40 cambios**). Si solo hay uno, dice **Aplicar 1 cambio**.

- La importación es **todo o nada**: si algo falla al aplicar, no se guarda ninguna fila.
- Los centros nuevos se crean con sus seis tipos de movimiento en **ninguno**.
- Los centros que ya existen reciben el nombre y las cuatro casillas del archivo. Sus tipos de movimiento **no cambian**.
- Los centros que no están en el archivo no se modifican.

Mientras se aplica, la pantalla muestra **Aplicando…**.

Al terminar, la pantalla muestra **Importación terminada**, con el resultado. Desde ahí pulse **Ver centros de costo** para revisarlos, o **Importar otro archivo**.

## Si algo sale mal

- **Otro usuario modificó los centros de costo mientras revisaba el archivo.** La pantalla no guarda nada. Pulse **Volver a validar** para ver el estado actual.
- **El archivo supera el límite.** La pantalla no lo procesa. Divídalo en archivos de hasta 5.000 filas y 2 MB.
- **Error del servidor.** La pantalla indica que no se pudo completar y que no se guardó nada. Pulse **Reintentar**.
- **Sin permiso de Exportar.** No ve el botón **Importar**.

## Preguntas frecuentes

**¿Puedo borrar centros con la importación?**
No. La importación solo crea o actualiza. Para eliminar un centro, use **Eliminar** en la lista.

**¿Por qué no se guardó ningún centro si solo había una fila mala?**
La importación es todo o nada. Si una fila tiene error, no se guarda ninguna. Corrija la fila y vuelva a cargar el archivo.

**¿Por qué el botón Aplicar no se puede pulsar?**
Hay filas con error. Corríjalas en el archivo y vuelva a cargarlo.

**¿Qué pasa con los tipos de movimiento de un centro que ya existe?**
No cambian. La importación solo actualiza el nombre y las cuatro casillas. Para cambiar los tipos de movimiento, edite el centro.

**¿Cómo cargo más de 5.000 centros?**
Divida el archivo en varios archivos de hasta 5.000 filas y 2 MB, y cargue cada uno.
