[Regresar a Contabilidad](readme.md)

---

# MIS REPORTES

> **Disponible cuando el administrador la habilite.** Hoy esta función no está activa para su compañía: los informes de Contabilidad se exportan directamente con los botones **Exportar Excel** y **Exportar PDF**. Este manual describe cómo funcionará cuando se habilite.

## Qué es

**Mis reportes** es la bandeja donde encuentra los informes de Contabilidad que pidió en segundo plano. Un informe grande no bloquea la pantalla: usted lo pide, sigue trabajando y, cuando está listo, lo descarga desde la bandeja.

Aquí ve:

- los informes que están en cola o en generación, con su avance;
- los informes listos, para descargarlos;
- los informes con error o cancelados.

La bandeja muestra solo los informes que usted pidió en la compañía en la que está trabajando.

## Cómo llegar

Mis reportes **no aparece en el menú**: no tiene una opción propia ni un permiso aparte. Se llega desde:

- el enlace **Ver en Mis reportes** que aparece debajo del informe que pidió; también puede llegar desde el aviso de la campana cuando el informe queda listo.

Para pedir un informe en segundo plano, vaya a la pantalla del informe (por ejemplo, **Consultas/Reportes > Balance de prueba**) y use **Generar Excel** o **Generar PDF**. Vea el [Balance de prueba](balance-prueba.md).

## Permisos

- Para pedir un informe necesita el mismo permiso que tiene para exportarlo: **Exportar** para Excel e **Imprimir** para PDF.
- Si pierde el permiso de un informe que ya pidió, la bandeja le indica **Ya no tiene permiso para este informe.**

## Cómo se lee la bandeja

La tabla se titula **Informes solicitados, del más reciente al más antiguo** y tiene estas columnas:

- **Informe**: nombre del informe.
- **Formato**: **Excel** o **PDF**.
- **Estado**: en qué va el informe (ver la tabla de estados).
- **Solicitado**: fecha y hora en que lo pidió.
- **Disponible hasta**: fecha hasta la que puede descargar el archivo. Los archivos se conservan **7 días** desde que quedan listos.
- **Acciones**: los botones que aplican a ese informe.

### Estados

| Estado | Qué significa |
|---|---|
| **En cola** | El informe espera su turno. Le indica cuántos hay por delante o si es el siguiente. |
| **Generando** | El informe se está generando. La barra muestra el avance en porcentaje. |
| **Reintentando** | El sistema vuelve a intentar generarlo. |
| **Interrumpido** | La generación se detuvo antes de terminar. |
| **Listo** | El archivo está listo para descargar. |
| **Con error** | No se pudo generar. La bandeja indica el motivo. |
| **Cancelado** | Usted lo canceló. |
| **Vencido** | El archivo pasó los 7 días y ya no se puede descargar. Genere el informe de nuevo. |

### Acciones

- **Descargar**: disponible cuando el informe está **Listo**. Si el navegador bloquea la descarga automática, descárguelo con un clic.
- **Cancelar**: disponible mientras el informe está en cola o generándose.
- **Reintentar**: disponible cuando el informe falló. Un informe se reintenta una vez; si vuelve a fallar, genérelo de nuevo.

Si la acción no se puede completar, la pantalla muestra **No se pudo completar la acción. Inténtelo de nuevo.**

![Bandeja con informes de distintos estados](recursos/img/mis-reportes/01-bandeja.png)

![Informe en curso con su avance](recursos/img/mis-reportes/02-generando.png)

![Informe listo para descargar](recursos/img/mis-reportes/03-listo.png)

## Filtrar

En **Estado** puede elegir:

- **Todos**
- **En curso**
- **Listos**
- **Con error o cancelados**

Para ver la lista al día, pulse **Actualizar**.

## Límites

- Puede tener **3 informes en curso** a la vez. Si pide un cuarto, la pantalla le indica que espere a que termine alguno o que cancele uno en **Mis reportes**.
- Si el sistema está ocupado generando otros informes, la pantalla le indica cuántos segundos esperar antes de intentarlo de nuevo.
- Si un informe supera el máximo de filas permitido, no se genera. Acote los filtros, por ejemplo con un rango de fechas menor, y pídalo otra vez.

## Antes de pedir un informe grande

Si el informe es grande, la pantalla muestra una advertencia antes de generarlo:

- **Este informe puede tardar**: informa las filas y los minutos estimados. Puede generarlo en segundo plano y seguir trabajando.
- **Esta consulta es muy grande para verla en pantalla**: indica el motivo (por ejemplo, un rango de muchos días o una consulta con muchos movimientos) y le ofrece alternativas: reducir el rango de fechas, elegir cuentas o terceros concretos, o usar un nivel de cuentas más alto.

Si continúa con una consulta grande en pantalla, queda registrado quién la pidió y con qué filtros.

## Exportar: qué botón verá

Hoy, y mientras la función no esté habilitada, los botones dicen **Exportar Excel** y **Exportar PDF**.

Cuando se habilite, el cambio es el siguiente:

- En el **Balance de prueba**, en las opciones **General** y **Por tercero**, los botones pasan a **Generar Excel** y **Generar PDF**. Por centros de costo sigue con **Exportar Excel** y **Exportar PDF**.
- El **Auxiliar contable** y el **Movimiento contable** mantienen **Exportar Excel** (y **Exportar PDF** en el Auxiliar).

## Preguntas frecuentes

**¿Por qué no veo Mis reportes en el menú?**
No tiene opción propia. Llegue desde el enlace **Ver en Mis reportes** del informe que pidió.

**¿Por qué no aparece mi informe?**
La bandeja muestra solo los informes que usted pidió en la compañía en la que está trabajando. Si el informe es muy antiguo, puede haber vencido.

**¿Por qué no puedo descargar el archivo?**
El informe puede estar aún en cola o generándose, o haber vencido. Revise el **Estado**. Si está **Vencido**, genérelo de nuevo.

**¿Por qué aparece Ya no tiene permiso para este informe?**
Su permiso de exportación cambió. Pida a su administrador que lo revise.

**¿Puedo cancelar un informe?**
Sí, mientras esté en cola o generándose. Use **Cancelar**.

**¿Se actualiza sola la lista?**
Pulse **Actualizar** para ver el avance y el estado al día.
