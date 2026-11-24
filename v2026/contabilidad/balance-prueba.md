[Regresar a Contabilidad](readme.md)

---

# BALANCE DE PRUEBA

## Qué es

El **Balance de prueba** muestra, para un **período contable completo**, los saldos inicial, débitos, créditos y saldo final de cada cuenta del plan. Según la opción que elija, lo ve:

- **General**: una fila por cuenta, con sus saldos.
- **Por tercero**: cuentas y terceros, con sus saldos.
- **Por centros de costo**: cuentas y centros de costo, con sus saldos.

Sirve para revisar que los débitos y los créditos del período cuadren y para tener a mano los saldos de cierre de cada cuenta.

La consulta no se ejecuta sola: elija el período y los filtros, y pulse **Consultar**.

Para ver las líneas de un documento, use el [Movimiento contable](movimiento-contable.md). Para ver los movimientos de una cuenta en un rango de fechas dentro de un período, use el [Auxiliar contable](auxiliar-contable.md).

## Cómo llegar

- Abra **Contabilidad** en el menú principal y luego **Consultas/Reportes > Balance de prueba**.
- Necesita permiso de **Consultar** sobre el Balance de prueba. Si no ve la opción, pida a su administrador que se lo asigne.

## Permisos

Lo que ve depende de sus permisos:

- **Consultar**: puede elegir el período, los filtros, consultar y ver el resultado.
- **Exportar**: puede descargar el resultado en **Exportar Excel**.
- **Imprimir**: puede descargar el resultado en **Exportar PDF**.

Sin **Exportar** o sin **Imprimir**, el botón correspondiente no aparece. La consulta sigue funcionando.

## Período

El balance se consulta **siempre por período completo**. Por eso no tiene campos de fecha: en su lugar, elija el período en el selector **Período**.

- La lista muestra cada período con su estado: **Abierto** o **Cerrado**. Puede escribir en **Buscar período** para encontrar uno.
- Al elegir un período, el balance toma automáticamente su primer y último día.
- Mientras no haya un período elegido, el botón **Consultar** está deshabilitado.

Si la lista de períodos no carga, la pantalla muestra **No se pudieron cargar los períodos.** con el botón **Reintentar**. Si la compañía no tiene períodos configurados, aparece **No hay períodos configurados**: en ese caso, pida a su administrador que los configure.

Si el servidor rechaza la consulta porque el rango no corresponde a un período completo, la pantalla muestra: **El balance de prueba se consulta por período completo. Elija un período de la lista.**

![Selector de período](recursos/img/balance-prueba/01-periodo.png)

## Filtros

Filtros de la consulta:

| Filtro | Qué hace |
|---|---|
| **Período** | Período contable que se consulta. Es obligatorio. |
| **Opción del reporte** | Elige **General**, **Por tercero** o **Por centros de costo**. Cambiar la opción no cambia el resultado que ya ve: hasta que pulse **Consultar**, la tabla sigue mostrando la opción anterior. |
| **Planes de cuentas** | Muestra solo las cuentas elegidas. Si lo deja vacío, incluye todas. |
| **Nivel** | Solo en **General**. Va de 0 a 100 y se escribe con la ayuda **De 0 a 100. Vacío o 0 muestra todos.** Con un nivel, muestra las cuentas hasta ese nivel. |
| **Terceros** | Solo en **Por tercero**. Muestra solo los terceros elegidos. |
| **Centros de costos** | Solo en **Por centros de costo**. Muestra solo los centros elegidos. |

**Limpiar filtros** deja vacíos los filtros opcionales. El período no se borra.

## Cómo se lee el resultado

La tabla de **General** tiene estas columnas:

- **Código plan cta.** y **Nombre plan cta.**
- **Saldo inicial**
- **Débitos** y **Créditos**
- **Saldo final**

En **Por tercero** y en **Por centros de costo** aparecen además las filas o los datos del tercero o del centro de costos que corresponda a cada cuenta.

Los importes están en pesos (COP), con separador de miles y dos decimales. Un importe en cero aparece vacío.

Bajo la tabla aparecen los **Totales del resultado**: **Débitos** y **Créditos** de todo el resultado, no solo de la página que ve. Si los débitos y los créditos no son iguales, aparece **Descuadre** con la diferencia. Si cuadran, el descuadre no aparece.

![Balance de prueba general](recursos/img/balance-prueba/02-general.png)

![Balance de prueba por tercero](recursos/img/balance-prueba/03-por-tercero.png)

![Balance de prueba por centros de costo](recursos/img/balance-prueba/04-por-centros.png)

### Páginas

La tabla muestra 25 filas por página. Puede cambiar a 10, 50 o 100 filas por página, y ver el total de filas y la página en la que está.

## Consultar

1. Elija el **Período**.
2. Elija la **Opción del reporte**.
3. Elija los filtros que necesite; los demás déjelos vacíos.
4. Pulse **Consultar**. Mientras se consulta, la pantalla muestra el estado de carga.
5. Revise el resultado y cambie de página con los controles de abajo.

Si cambia un filtro o la opción, el resultado anterior no se actualiza: pulse **Consultar** otra vez.

Si no hay saldos ni movimientos con esos filtros, la pantalla muestra **No hay saldos ni movimientos con esos filtros**. Cambie el período o quite algún filtro.

Si la consulta falla, la pantalla muestra un mensaje de error con el botón **Reintentar**. Sus filtros se conservan.

## Exportar

Puede descargar el resultado con los filtros que tiene puestos al pulsar el botón. Si cambió algún filtro, consulte otra vez antes de exportar.

- **Exportar Excel**: necesita permiso de **Exportar**. El límite es de **50.000 filas**.
- **Exportar PDF**: necesita permiso de **Imprimir**. El límite es de **4.000 filas**.

Mientras se genera el archivo, la pantalla muestra **Generando el archivo…**. Si la generación falla, aparece **No se pudo generar el archivo. Inténtelo de nuevo.** y no se descarga nada.

Si el resultado supera el límite, la pantalla no genera el archivo y le indica cuántas filas se permiten. Acote el período, agregue filtros, pulse **Consultar** y exporte otra vez.

### Cuando la generación en segundo plano esté disponible

> Esta sección describe una función que se habilita por compañía. Si su pantalla muestra **Exportar Excel** y **Exportar PDF**, la función todavía no está disponible para usted: siga la sección anterior.

Cuando el administrador la habilite, en **General** y **Por tercero** los botones cambian a **Generar Excel** y **Generar PDF**. El informe se genera en segundo plano: puede seguir trabajando y la pantalla le avisa cuando el archivo está listo. Para verlo y descargarlo después, use **Mis reportes**.

En **Por centros de costo** el botón sigue siendo **Exportar Excel** / **Exportar PDF** y el archivo se descarga directamente.

## Preguntas frecuentes

**¿Por qué no puedo poner fechas en el balance?**
El balance de prueba se consulta solo por período completo. Elija el período en el selector.

**¿Por qué el botón Consultar está deshabilitado?**
Falta elegir el período. Elija uno de la lista.

**¿Qué significa Abierto o Cerrado en la lista de períodos?**
Indica el estado del período en la compañía. La lista lo muestra para que sepa qué período está consultando. Si necesita saber si un período puede recibir movimientos, pregunte a su administrador.

**¿Por qué cambió la tabla al cambiar la opción del reporte?**
No cambió: la tabla muestra la opción con la que consultó. Pulse **Consultar** para ver la nueva opción.

**¿Por qué aparece Descuadre?**
Los débitos y los créditos del resultado no son iguales. Revise el período y los filtros, y el detalle en el [Movimiento contable](movimiento-contable.md).

**¿Por qué no veo Exportar Excel ni Exportar PDF?**
Su usuario no tiene el permiso de **Exportar** o de **Imprimir** sobre el Balance de prueba. Pida a su administrador que lo revise.

**¿Por qué no aparece la columna de tercero o de centro?**
Esa columna solo aparece en la opción **Por tercero** o **Por centros de costo**. En **General** no se muestra.

**¿Por qué no aparece el campo Nivel?**
El nivel solo aplica a la opción **General**.
