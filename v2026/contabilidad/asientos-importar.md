[Regresar a Contabilidad](readme.md)

---

# IMPORTAR ASIENTOS CONTABLES

> **Estado de esta importación.** Esta opción todavía no está activa en el menú. Mientras no se habilite, no se importa ningún archivo. Cuando se habilite, siga los pasos de este manual. Los asientos que se importan **quedan cerrados** (ver [Asientos importados](#asientos-importados)). Los **documentos adjuntos** todavía no están disponibles en la pantalla de asientos.

## Qué es

La importación carga **asientos contables** desde un archivo de Excel. Un archivo puede traer varios asientos, y cada asiento puede tener varias líneas.

Antes de crear nada, la pantalla le muestra una **vista previa** de todo el archivo. Usted decide si aplica la importación.

## Cómo llegar

- Abra **Contabilidad** en el menú principal y luego la opción **Importar asientos contables**, en el grupo de **Importaciones**.
- Necesita permiso de **Crear** sobre la importación de asientos. Si no tiene el permiso, la pantalla dice **No tienes permiso para importar asientos contables.** y no muestra la carga del archivo.

La importación tiene tres pasos, que se ven arriba de la pantalla: **Archivo**, **Vista previa** y **Resultado**.

![Cargar el archivo](recursos/img/asientos-importar/01-plantilla-y-archivo.png)

## Paso 1: descargar la plantilla y cargar el archivo

1. Pulse **Descargar PlantillaImportarAsientosContables.xlsx**. Es una hoja de Excel con 13 columnas, de la A a la M.
2. Complete la hoja. Cada encabezado tiene un comentario que explica el dato.
3. Arrastre el archivo a la pantalla o elíjalo desde su equipo.

### Columnas de la plantilla

Los datos empiezan en la fila 2. La fila 1 tiene los encabezados.

| Columna | Encabezado | Regla |
|---|---|---|
| A | Cód. Tipo Movimiento | Código de un tipo de asiento autorizado para su usuario. |
| B | Consecutivo | 0 = automático. Otro número solo si el tipo permite editarlo. |
| C | Documento Referencia General | Obligatorio. Agrupa las filas del mismo asiento. |
| D | Fecha [YYYY-MM-DD] | Por ejemplo, 2026-03-31. Debe caer en un período abierto. |
| E | Observaciones | Hasta 200 caracteres. |
| F | Cuenta Contable | Cuenta de movimiento de la compañía. |
| G | Nit Tercero | Obligatorio si la cuenta pide tercero. |
| H | Centro de Costos | Obligatorio si la cuenta pide centro de costos. |
| I | Documento Referencia | Obligatorio si la cuenta pide referencia. |
| J | Detalle | Hasta 100 caracteres. |
| K | Débitos | Número, sin separadores de miles. |
| L | Créditos | Número, sin separadores de miles. |
| M | Base Tributaria | Número, sin separadores de miles. |

La cuenta, el tercero, el centro de costos y la referencia se escriben como **texto**.

### Reglas del archivo

- Formato **.xlsx**. Se lee la **primera hoja**.
- Un archivo puede tener hasta el **número máximo de filas** que indica la pantalla, y **2 MB** como máximo. Si supera alguno de los dos límites, la pantalla dice **El archivo supera los límites** y no procesa nada. Divida el archivo en varios.
- Las filas con el mismo **tipo**, el mismo **consecutivo** y el mismo **documento de referencia general** forman un asiento.
- Todas las filas de un mismo asiento deben tener la misma fecha, el mismo documento de referencia general y las mismas observaciones. Si no coinciden, la fila aparece con error.
- Las reglas de cada línea son las mismas que al crear un asiento a mano (ver [Asientos contables](asientos.md#las-lineas)): la cuenta debe ser de movimiento y de su compañía; el tercero, el centro de costos y la referencia deben existir cuando la cuenta los pide; débitos y créditos no pueden ser los dos cero ni los dos con valor.

Si el archivo no es un Excel válido o no trae las columnas de la plantilla, la pantalla dice **El archivo no es un .xlsx válido o no trae las 13 columnas de la plantilla.** y no lo procesa.

Mientras lee el archivo, la pantalla muestra **Leyendo el archivo y validando las filas…**

## Paso 2: revisar la vista previa

La vista previa revisa **todo** el archivo y no escribe nada. Muestra:

- Los conteos: **Asientos**, **Filas**, **Filas correctas** y **Filas con error**.
- La tabla **Asientos detectados en el archivo**, con el tipo, el consecutivo, el documento de referencia, la fecha, el número de líneas, las sumas de débitos y de créditos, y el estado: **Se crea** o **Con errores**.
- La tabla **Filas del archivo con su validación**, con el número de fila, su estado (**Correcta** o **Error**) y el motivo.

Arriba aparece el aviso **Vista previa: todavía no se escribió nada.**

![Vista previa con errores](recursos/img/asientos-importar/02-vista-previa-con-errores.png)

### Filas con error

Si hay filas con error, la pantalla dice **Hay N fila(s) con error. Corrige el archivo y súbelo de nuevo: no se puede aplicar parcialmente.** El botón **Aplicar** queda deshabilitado, con el aviso **Aplicar está deshabilitado mientras haya errores.**

Para corregir:

1. Revise la columna **Motivo** de cada fila con error.
2. Corrija esas filas en su Excel.
3. Pulse **Elegir otro archivo** y cargue el archivo corregido.

Los motivos más comunes son:

- **Fecha en período cerrado**: la fecha cae en un período cerrado.
- **Cuenta no válida para la compañía**: la cuenta no existe o no es de su compañía.
- **La cuenta no es de movimiento**: la cuenta es de mayor.
- **El NIT no existe o está inactivo**: el tercero no existe o está inactivo.
- **Débitos y Créditos ambos cero**: la línea no tiene valor.
- **El asiento queda descuadrado**: débitos y créditos del asiento no son iguales.
- **Tipo de movimiento no válido**: el tipo no existe, no es de asientos o no está autorizado para su usuario.
- **El consecutivo solo se acepta si el tipo permite editarlo (0 = automático).**

Una advertencia no impide aplicar. Por ejemplo, si escribe un tercero o un centro de costos que la cuenta no pide, se ignora y la pantalla lo indica en la vista previa.

## Paso 3: aplicar la importación

Cuando la vista previa no tiene errores, pulse **Aplicar** con el número de asientos que se van a crear (por ejemplo, **Aplicar (3 asientos)**).

- **Todo o nada**: se crean todos los asientos del archivo o ninguno. Si un asiento falla, no queda escrito ninguno.
- La pantalla dice **Aplicando la importación…** y la importación corre en segundo plano. Puede cerrar la pantalla: el resultado llegará como un **aviso del sistema**.

Al terminar, la pantalla muestra el **Resultado de la importación**:

- Si todo salió bien: **Se crearon N asientos con M líneas. Quedaron cerrados; los consecutivos son X a Y.** Desde ahí pulse **Ir a Asientos contables** para revisarlos.
- Si falló: **La importación falló y no se escribió ningún asiento. Motivo: {motivo}.** Corrija el motivo y vuelva a cargar el archivo.

Si cierra la pantalla antes de terminar, el aviso final le dice cuántos asientos se crearon, o por qué no se crearon.

Mientras la importación está en curso, la pantalla dice **Importación en curso** y no garantiza que los asientos ya existan.
## Asientos importados

Los asientos que se importan **quedan cerrados**, igual que un asiento cerrado a mano. Por eso:

- No se pueden editar, salvo con el permiso de editar documentos cerrados, y siempre deben quedar cuadrados.
- Solo se importan asientos que cuadran. Si un asiento del archivo no cuadra, toda la importación se rechaza.

Puede revisarlos en **Asientos contables**, en el listado.

## Si algo sale mal

- **El archivo no es un .xlsx válido** o no trae las 13 columnas: no se procesa nada. Use la plantilla.
- **El archivo supera los límites** (filas o 2 MB): no se procesa nada. Divídalo.
- **Vuelva a elegir el archivo para generar una vista previa nueva**: el archivo cambió después de la vista previa. Elíjalo otra vez.
- **No se pudo leer el archivo** / **Hubo un problema en el servidor. No se escribió nada: inténtalo de nuevo.**: pulse **Reintentar**.
- **No se aplicó la importación**: no se escribió ningún asiento. Revise el motivo y vuelva a intentar.
- **No se pudo descargar la plantilla. Inténtalo de nuevo.**: vuelva a pulsar el botón de descarga.

## Preguntas frecuentes

**¿Puedo importar solo algunos asientos del archivo?**
No. La importación es todo o nada. Si una fila tiene error, no se crea ningún asiento. Corrija el archivo y cárguelo otra vez.

**¿Por qué el botón Aplicar está deshabilitado?**
Hay filas con error. Corrija las filas indicadas en la columna **Motivo** y vuelva a cargar el archivo.

**¿Qué pasa con los asientos importados?**
Quedan cerrados. Para corregirlos, use la pantalla de [Asientos contables](asientos.md), con el permiso de editar documentos cerrados.

**¿Cómo cargo más asientos de los que permite el archivo?**
Divida el archivo en varios, cada uno dentro del límite de filas y de 2 MB, y cargue cada uno. Recuerde que cada asiento debe quedar completo dentro de un mismo archivo.

**¿Puedo cerrar la pantalla mientras se importa?**
Sí. La importación sigue en segundo plano y el resultado llega como aviso del sistema.
