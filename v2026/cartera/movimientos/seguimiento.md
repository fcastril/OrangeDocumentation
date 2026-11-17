[Regresar a Cartera](../readme.md)

---

# 📞 Seguimiento de Cartera

![Static Badge](https://img.shields.io/badge/Tipo-Listado-red)
![Static Badge](https://img.shields.io/badge/Module-Cartera-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-300-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261117-yellow)

---

## 📋 Descripción

**Seguimiento de Cartera** es la lista de quién le debe a la compañía (**por cobrar**, clientes) o a quién le debe la compañía (**por pagar**, proveedores), con su saldo, lo que está vencido y la **última gestión** que se hizo con cada tercero. Le sirve para decidir a quién llamar hoy y para no olvidar una llamada pendiente.

Desde la lista puede:

- **Registrar una gestión** (a quién se llamó, qué se habló, qué se acordó y cuándo volver a revisar) en un **panel lateral**, sin salir de la lista.
- Ver sus **alertas**: los terceros que debe volver a llamar hoy o que ya están vencidos.
- **Exportar** la lista a Excel o a PDF.

> 📘 La búsqueda, el orden y la exportación de las tablas funcionan igual en todas las pantallas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Los **importes** están en pesos colombianos. En cuentas por pagar los importes salen en **negativo**.

> 💡 Los **totales** (terceros, saldo y vencido) cubren **todo el filtro**, no solo la página que está viendo.

> ℹ️ Los mensajes de las gestiones **no aparecen en la lista, en el Excel ni en el PDF**. Para leerlos, abra el panel del tercero.

> ⚠️ Los cobradores, la asignación, la gestión estructurada y los compromisos de pago (**fase 2**) requieren que el administrador haya habilitado sus tablas y permisos. Si no los ve, la pantalla funciona como antes.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Cartera**.
2. En **Movimientos**, haga clic en **Seguimiento de Cartera**.

---

## 🖥️ Pantalla principal

![Seguimiento de cartera de clientes](../recursos/img/seguimiento/l-01-por-cobrar.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la pantalla. |
| **Tipo de cartera** | **Por cobrar (clientes)** o **Por pagar (proveedores)**. Al cambiarlo, la lista se vuelve a consultar y se limpian los filtros que no aplican a ese tipo. |
| **Fecha de corte** | Día con el que se calculan el saldo, lo vencido y la mora. Por defecto es hoy. No puede ser una fecha posterior a hoy. |
| **Filtros** | Limitan la lista. Ver *Filtros* más abajo. Use **Aplicar filtros** para verlos y **Limpiar filtros** para quitarlos. |
| **Mis alertas** | Abre el panel de sus alertas, con un contador de **vencidas** y **para hoy**. Ver *Mis alertas*. |
| **Exportar Excel** | Descarga la lista completa del filtro. Ver *Exportar a Excel*. |
| **Exportar PDF** | Descarga la lista completa del filtro en PDF horizontal. Ver *Exportar a PDF*. |
| **Buscar por documento o nombre** | Escriba al menos 2 caracteres. |
| **Gestionar** | Abre el panel de gestión de ese tercero. También puede hacer clic en la fila. |
| **Tabla** | Un tercero por fila. Haga clic en un encabezado para ordenar por esa columna. |

### Columnas de la lista

| Columna | Qué muestra |
|---------|-------------|
| **Documento** | Número de identificación del tercero, con su dígito de verificación. |
| **Nombre** | Nombre del tercero. |
| **Teléfono** y **Correo** | Datos de contacto que tiene registrados. |
| **Saldo** | Lo que debe (por cobrar) o lo que se le debe (por pagar) a la fecha de corte. |
| **Vencido** | La parte del saldo que ya superó su plazo a la fecha de corte. |
| **Mora (días)** | Días de atraso del documento más atrasado del tercero. |
| **Cupo** | Semáforo del cupo de crédito. Ver *Semáforo de cupo*. |
| **Cobrador** | Solo en **Por cobrar**. El cobrador titular del cliente. Si tiene apoyos, aparece **+N**: al pasar el cursor (o enfocar con el teclado) ve cada cobrador con su rol. Sin cobrador, dice **Sin asignar**. Cada cliente se cuenta una sola vez en los totales, aunque tenga apoyos. |
| **Última gestión** | Fecha de la última gestión registrada y su acción. Si no hay gestiones, dice **Sin gestión**. |
| **Próxima alerta** | Próxima fecha de revisión que dejó una gestión. Si ya pasó, dice **Alerta vencida**; si es hoy, dice **Hoy**. Si no hay, dice **Sin alerta**. |

Los terceros aparecen **solo si tienen saldo** a la fecha de corte. Un tercero con saldo cero no aparece, salvo que incluya los saldos a favor (ver *Filtros*).

Cuando la fecha de corte no es hoy, aparece este aviso: *El saldo, lo vencido y la mora son a la fecha de corte. La última gestión y la próxima alerta son siempre las de hoy.*

![Fecha de corte anterior a hoy](../recursos/img/seguimiento/l-03-corte-anterior.png)

![Seguimiento de cartera de proveedores](../recursos/img/seguimiento/l-02-por-pagar.png)

### Qué ve cada permiso

| Permiso | Qué puede hacer |
|---------|-----------------|
| **Consultar** (opción 300) | Ver la lista, usar los filtros, ver las gestiones en el panel y ver **Mis alertas**. |
| **Crear** | Ver el botón **Nueva gestión** y registrar gestiones nuevas. |
| **Actualizar** | Ver **Editar** en cada gestión y guardar cambios. |
| **Exportar** | Ver **Exportar Excel**. |
| **Imprimir** | Ver **Exportar PDF**. |

Con la fase 2, **Actualizar** de la opción 349 (Cola de cobro) permite asignar, reasignar y repartir cartera, y ver **Equipo** y **Sin asignar**. **Crear** y **Actualizar** de esta opción permiten registrar, reprogramar y cancelar compromisos de pago.

No existe permiso para **eliminar** gestiones: las gestiones no se borran. Ver *Preguntas frecuentes*.

Si su perfil no tiene **Consultar**, verá el aviso **No tiene permiso para ver el seguimiento de cartera**, con la indicación de pedir a su administrador el permiso de la opción 300.

---

## 🔎 Filtros y orden

| Filtro | Qué hace |
|--------|----------|
| **Buscar por documento o nombre** | Busca un tercero por su documento o su nombre. |
| **Tercero** | Elige un tercero concreto. |
| **Cobrador** | Solo en **Por cobrar**. Muestra los clientes de uno o varios cobradores (hasta 50). |
| **Vendedor** (en por cobrar) o **Comprador** (en por pagar) | Muestra solo los terceros con documentos de ese vendedor o comprador. |
| **Zona** | Muestra solo los terceros de esa zona. |
| **Saldo entre** | Rango de saldo, desde y hasta. |
| **Mora máxima entre (días)** | Rango de días de atraso del documento más atrasado. |
| **Sin gestión hace** | **Cualquiera**, **15 días o más**, **30 días o más** o **60 días o más**. Incluye los terceros que nunca se han gestionado. |
| **Alerta** | **Vencida**, **Hoy**, **Próximos 7 días** o **Sin alerta**. |
| **Semáforo de cupo** | **En cupo**, **En alerta**, **Sobrecupo** o **Sin cupo asignado**. |
| **Incluir saldos a favor** | Muestra también los terceros cuyo saldo está a favor de ellos (saldo negativo). |

Los filtros se combinan: solo verá los terceros que cumplan **todos** a la vez.

Para ordenar, haga clic en el encabezado de la columna: un clic ordena de menor a mayor y otro clic de mayor a menor. Por defecto la lista va por **Nombre**. Puede mostrar **10, 25, 50 o 100** filas por página.

Al ordenar por **Última gestión** de menor a mayor, primero aparecen los terceros que nunca se han gestionado y luego los de gestión más antigua. Así ve primero a los más olvidados.

> ⚠️ Si la consulta falla, sus filtros se conservan. Pulse **Reintentar**.

---

## 👥 Vistas, cobrador y asignación

En la fase 2, cada cliente de **Por cobrar** tiene un **cobrador titular** y puede tener **cobradores de apoyo**. Los cobradores se administran en [Cobradores](../cobradores.md).

### Vistas del listado

Arriba del listado puede elegir la vista:

| Vista | Qué muestra | Permiso |
|-------|-------------|---------|
| **Mis cobros** | Los clientes donde usted es titular o apoyo. | Consultar. Es la vista por defecto si usted es cobrador y no tiene la asignación. |
| **Equipo** | Los clientes de todo el equipo. | 349 **Actualizar** |
| **Sin asignar** | Los clientes que no tienen cobrador. | 349 **Actualizar** |

![Vista Equipo](../recursos/img/seguimiento-f2/as-01-equipo.png)

![Vista Sin asignar](../recursos/img/seguimiento-f2/as-02-sin-asignar.png)

Mis cobros se ve en vivo: refleja la asignación de cada momento. La [Cola de cobro](cola.md) es la lista priorizada del día.

### Asignar y reasignar

Con permiso de **349 Actualizar**, en cada fila puede asignar un cobrador:

1. Haga clic en **Asignar** (o en **Reasignar**, si el cliente ya tiene cobrador).
2. Elija el **cobrador titular** y, si hace falta, los **cobradores de apoyo**.
3. Escriba el **motivo del cambio** y haga clic en **Guardar**.

![Asignar cobrador](../recursos/img/seguimiento-f2/as-03-asignar.png)

Al reasignar, el diálogo muestra el **historial reciente** del cliente: de quién a quién, cuándo y el origen (**Manual**, **Regla** o **Reparto**). Los cobradores anterior y nuevo reciben aviso en la campana.

![Reasignar cobrador](../recursos/img/seguimiento-f2/as-04-reasignar.png)

| Mensaje | Qué hacer |
|---------|-----------|
| **Escribe el motivo; queda en la bitácora.** | Escriba por qué cambia el cobrador. |

Un mismo cobrador no puede ser titular y apoyo del mismo cliente.

**Reasignar seleccionados (N)**: marque varias filas y reasígnelas juntas (hasta 500 clientes por vez).

### Repartir equitativamente

Para los clientes **Sin asignar**, puede pedir un **reparto equitativo**: el sistema reparte por carga (cantidad de cuentas y saldo vencido) entre los cobradores activos y no ausentes. No cambia las asignaciones manuales ni las de las reglas vigentes.

1. Haga clic en **Repartir equitativamente**.
2. Revise la **Vista previa**: muestra cuántos clientes recibiría cada cobrador. **La vista previa no guarda nada**.
3. Si está de acuerdo, haga clic en **Confirmar reparto**.

![Vista previa del reparto](../recursos/img/seguimiento-f2/as-05-repartir-vista.png)

Si la cantidad de clientes es muy grande, el sistema pide acotar la lista o usar [Generación de cobros](generacion.md).

Las reglas de cada cobrador se configuran en [Cobradores](../cobradores.md).

## 🚦 Semáforo de cupo

El semáforo compara el **saldo** con el **cupo de crédito** del tercero, con los mismos porcentajes de alerta que se usan en la ficha del cliente:

- **En cupo**: el saldo todavía está por debajo del umbral de alerta.
- **En alerta**: el saldo ya superó el umbral de alerta, pero no el cupo.
- **Sobrecupo**: el saldo supera el cupo.

El porcentaje indica cuánto del cupo está usado. El estado siempre se lee con texto, no solo con el color.

Para **proveedores**, el cupo es el **Cupo del proveedor** y se compara con lo que la compañía les debe.

Si el cupo es **0** o está vacío, no hay semáforo: la columna muestra **—** y el filtro **Sin cupo asignado** lo incluye.

---

## 🧾 Panel de gestión

El panel se abre al hacer clic en la fila o en **Gestionar**. Queda al lado de la lista: al cerrarlo, la lista y la página que estaba viendo se conservan.

![Panel de gestión abierto](../recursos/img/seguimiento/p-01-panel.png)

El panel muestra:

- El encabezado del tercero: documento, nombre, saldo, vencido y semáforo.
- El botón **Abrir ficha**, que lleva a la ficha del cliente (si es cliente) o a la del proveedor (si es proveedor).
- La lista de **gestiones**, de la más reciente a la más antigua.

Si el tercero no tiene gestiones, dice **Aún no hay gestiones de este tercero.**

### Registrar una gestión

1. Abra el panel del tercero.
2. Haga clic en **Nueva gestión**.
3. Complete los campos y haga clic en **Guardar gestión**.

![Registrar una gestión](../recursos/img/seguimiento/p-02-nueva-gestion.png)

| Campo | Qué escribir | Obligatorio |
|-------|--------------|:-----------:|
| **Contacto** | Nombre de la persona con la que habló. | ✅ |
| **Teléfono de contacto** | Teléfono por el que se comunicó. | ✅ |
| **Mensaje** | Lo que se habló. Puede escribir varias líneas. | ✅ |
| **Acción** | La acción acordada, por ejemplo *Llamar el 30/10*. | ✅ |
| **Fecha de alerta** | Día en que debe volver a revisar a este tercero. | No |

Si deja la **fecha de alerta** vacía, se programa **3 días después** de la gestión. La fecha y la hora de la gestión las pone el sistema al guardar.

Al guardar, el panel muestra la gestión nueva y la fila de la lista se actualiza con su **Última gestión** y su **Próxima alerta**. El aviso dice **Gestión registrada. La fila se actualizó.**

### Errores al registrar

Los mensajes aparecen debajo del campo que debe corregir, y lo que escribió se conserva:

![Validación de los campos de la gestión](../recursos/img/seguimiento/p-03-validacion.png)

| Mensaje | Qué hacer |
|---------|-----------|
| **Escriba el nombre de la persona contactada** | Complete el campo **Contacto**. |
| **Escriba un teléfono de contacto** | Complete el campo **Teléfono de contacto**. |
| **Escriba lo que se habló** | Complete el campo **Mensaje**. |
| **Indique la acción acordada** | Complete el campo **Acción**. |
| **La alerta no puede ser anterior a la gestión** | Elija una fecha igual a hoy o posterior. |
| **Revise N campos obligatorios.** | Los campos marcados están incompletos. |

### Editar una gestión

1. En la gestión que quiere corregir, haga clic en **Editar**.
2. Cambie lo que necesite y haga clic en **Guardar gestión**.

Las gestiones **no se eliminan**: quedan como historial de la gestión de cobro. Si se equivocó, edítela.

Para cerrar el panel, use **Cerrar panel** o **Cancelar**. Si cierra con cambios sin guardar, lo escrito se pierde.

---

## 📝 Gestión estructurada, advertencia y compromisos

La gestión de la fase 2 pide, además de lo de siempre, **cómo** se contactó al cliente y **qué resultado** tuvo.

![Gestión con compromiso](../recursos/img/seguimiento-f2/gs-01-compromisos.png)

### Canal y resultado

| Campo | Opciones |
|-------|----------|
| **Canal** | **Llamada**, **WhatsApp**, **Correo** o **Visita**. Obligatorio. |
| **Resultado** | **Contactado**, **No contesta**, **Promesa de pago**, **Rechaza** o **Número errado**. Obligatorio. |
| **Siguiente paso** | Es la **fecha de alerta** de siempre (vacía = 3 días después) más una **nota** opcional de hasta 100 caracteres. |

Los campos de siempre (contacto, teléfono, mensaje y acción) siguen siendo obligatorios.

![Nueva gestión con canal y resultado](../recursos/img/seguimiento-f2/gs-02-nueva.png)

El **cobrador** que hace la gestión se toma de su usuario: no hace falta escribirlo.

### Advertencia de horario y frecuencia (Ley 2300 de 2023)

Antes de guardar, el sistema revisa dos cosas para gestiones por **llamada**, **WhatsApp** o **visita**:

- **Horario**: si la hora está fuera del horario de contacto configurado (lunes a viernes, sábado y domingos o festivos según la empresa).
- **Frecuencia**: si el cliente ya tiene el máximo de contactos de la semana (últimos 7 días).

Si algo no cumple, aparece **Advertencia de contacto responsable** con el texto de la regla. Es **solo una advertencia**: el botón cambia a **Registrar de todos modos** y, si lo pulsa, la gestión se guarda y queda marcado que confirmó la advertencia. El correo no se revisa.

![Advertencia fuera de horario](../recursos/img/seguimiento-f2/gs-03-fuera-horario.png)

> ⚠️ Los horarios y la frecuencia son **parámetros por validar**: son una propuesta que debe revisar el área jurídica. **No son asesoría legal.** Revise los valores en [Parámetros de cartera](../parametros.md) antes de depender de ellos.

### Compromisos de pago

Cuando el resultado es **Promesa de pago**, el formulario ofrece un **compromiso de pago** (solo en cuentas por cobrar):

| Campo | Regla |
|-------|-------|
| **Valor prometido** | Mayor que cero. Si supera el saldo del cliente, aparece un aviso: puede guardarlo, pero conviene revisar la cifra. |
| **Fecha prometida** | No puede ser anterior a hoy. |
| **Medio de pago** | **Efectivo**, **Transferencia**, **Consignación**, **Cheque** u **Otro**. |
| **Nota del compromiso** | Opcional, hasta 200 caracteres. |

Un cliente solo puede tener **un compromiso pendiente**. Si registra otro, el anterior queda como **Reprogramado**.

En la lista del panel, cada compromiso muestra su estado:

| Estado | Qué significa |
|--------|---------------|
| **Pendiente** | Todavía no se paga todo. Si hay un pago parcial, dice **Pagado X de Y**. |
| **Cumplido** | El cliente pagó el valor prometido dentro de la fecha. |
| **Incumplido** | Venció la fecha prometida sin el pago. |
| **Reprogramado** | Lo reemplazó un compromiso nuevo. |
| **Cancelado** | Se canceló con un motivo. |

Los compromisos **se cumplen solos**: los decide el **recibo de caja** registrado. No hay botón para marcar un compromiso como cumplido a mano. Si un recibo se anula, el compromiso vuelve a **Pendiente** o pasa a **Incumplido**.

Para **cancelar** un compromiso, use **Cancelar compromiso**, escriba el motivo y confirme. Los compromisos no se eliminan.

![Compromisos de pago](../recursos/img/seguimiento-f2/gs-04-promesa.png)

Cuando el cliente cumple o incumple, quien tiene asignado el cliente recibe un aviso en la campana, sin importes en el texto.

En el panel, el encabezado muestra el **cobrador** del cliente y el botón **Cambiar cobrador** (con permiso de 349 Actualizar).

Las gestiones anteriores a la fase 2 aparecen como **Sin estructura**.

## ⏰ Mis alertas

El botón **Mis alertas** muestra cuántas alertas tiene: **vencidas** y **para hoy**.

![Mis alertas](../recursos/img/seguimiento/a-01-mis-alertas.png)

El panel lista los terceros cuya fecha de alerta venció o es hoy y que tiene asignados a usted, como titular o suplente. Si el cliente no tiene cobrador, lista los que gestionó usted. Si usted es apoyo de un cliente, aparece marcado **En apoyo**. Por cada uno ve el tercero, su saldo, la fecha de alerta y el botón **Gestionar** para abrir su panel.

No ve las alertas de gestiones registradas por otros usuarios. Si no tiene alertas, dice **No tiene alertas vencidas ni para hoy.**

### Aviso en la campana de notificaciones

Cada día, a las **5:00 a. m. (hora de Colombia)**, el sistema avisa en la campana de notificaciones al **cobrador asignado** de ese cliente, o a su suplente si el titular está ausente. Si el cliente no tiene cobrador, avisa a quien registró la gestión. Los apoyos no reciben aviso, salvo que el administrador lo active en [Parámetros de cartera](../parametros.md). Al pulsar el aviso, se abre **Seguimiento de Cartera** con el panel de ese tercero ya abierto. El aviso no incluye el mensaje de la gestión.

---

## 📤 Exportar a Excel

1. Aplique los filtros que necesita y haga clic en **Aplicar filtros**.
2. Haga clic en **Exportar Excel**.

El archivo tiene:

- El encabezado estándar de los reportes: empresa, NIT, nombre del reporte, tipo de cartera, fecha de corte, filtros usados, fecha y hora de la descarga y usuario que lo generó.
- Todas las filas del filtro, **no solo la página** que ve.
- Las columnas de la tabla, con **teléfono**, **correo** y **cobrador** (titular y **+N**), más el **celular**.
- Los totales al pie.
- **Ningún mensaje de gestión.**

Si el filtro supera **50.000 filas**, el sistema no genera el archivo y dice *El Excel supera 50.000 filas. Acote el corte o los filtros.*

![Excel que supera el tope](../recursos/img/seguimiento/l-05-exportar-413.png)

Si no ve el botón **Exportar Excel**, su perfil no tiene el permiso **Exportar** de la opción 300.

---

## 📄 Exportar a PDF

1. Aplique los filtros y haga clic en **Exportar PDF**.

El PDF es horizontal. Tiene las columnas de la tabla (con teléfono y correo, sin celular), todas las filas del filtro, los totales y el mismo encabezado. No tiene **mensajes de gestión**. La vista de impresión es el mismo PDF.

Si el filtro supera **4.000 filas**, el sistema dice *El PDF supera 4.000 filas. Use Excel o acote los filtros.* En ese caso, use el Excel o filtre más.

Si no ve **Exportar PDF**, su perfil no tiene el permiso **Imprimir** de la opción 300.

### Qué no se exporta

- Los **mensajes** de las gestiones (ni en el Excel ni en el PDF).
- El **celular**, que solo aparece en el Excel.
- Las filas de la página que no está viendo: siempre se exporta todo el filtro.

---

## ✉️ Enviar el estado de cuenta

Desde el listado y desde el panel de cada cliente puede enviarle su **estado de cuenta** por correo: un PDF con sus documentos pendientes a la fecha de corte. Con la fila seleccionada use **Estado de cuenta**; con varias filas, use la acción de envío en lote de la barra del listado.

Antes de enviar, revisa la vista previa del PDF y del correo. Si la compañía todavía no tiene el envío real habilitado, el correo **no se envía**: aparece **Modo de prueba**.

Los envíos, los lotes y sus estados se revisan en [Estado de cuenta por correo](estado-cuenta.md).

## 🔄 Cambios de otros usuarios (en vivo)

Esta pantalla **se actualiza sola**. Si otro usuario registra una gestión de un tercero que está en su lista, la fila de ese tercero se actualiza (**Última gestión** y **Próxima alerta**) sin recargar la pantalla y sin perder sus filtros.

Si tiene abierto el panel de ese tercero, aparece el aviso **Otro usuario registró una gestión de este tercero; la fila se actualizó.** Su usuario no recibe ese aviso por sus propias gestiones.

---

## 🆚 Diferencias con el sistema anterior

| Antes | Ahora |
|-------|-------|
| Solo mostraba **clientes**. | Muestra **clientes** (por cobrar) y **proveedores** (por pagar). Con el **Tipo de cartera** cambia de lado. |
| La fecha de corte era siempre hoy. | Puede elegir una **fecha de corte** anterior a hoy. |
| La lista era una sola tabla, sin filtros ni orden. | Tiene **filtros**, **orden** y **páginas** de 10 a 100 filas. |
| El saldo podía no coincidir con el reporte de cartera de terceros. | El saldo es el mismo que el del reporte **Cartera de terceros** y el de la pestaña **Cartera** de la ficha del cliente. |
| Mostraba la fecha de la última llamada. | Muestra la **última gestión** con su acción y la **próxima alerta**. |
| Para anotar la gestión había que entrar a la ficha de cada tercero. | El registro se hace en el **panel lateral**, sin salir de la lista. |
| No se podía exportar. | Se exporta a **Excel** y a **PDF**. |
| No había semáforo de cupo. | El **semáforo de cupo** aparece en clientes y proveedores. |
| No había alertas por pantalla. | **Mis alertas** lista sus alertas vencidas y de hoy. |
| No había cobradores ni reparto de clientes. | Cada cliente tiene un cobrador titular y apoyos, con reglas, ausencias, cola de cobro y compromisos de pago. |

Teléfono, correo, documento y nombre siguen en la lista como antes.

---

## ❓ Preguntas frecuentes

**¿Por qué un tercero no aparece en la lista?**
La lista solo muestra terceros con saldo a la fecha de corte. Revise la fecha de corte, los filtros y el aviso de **Incluir saldos a favor**.

**¿Por qué el saldo no es el de hoy?**
Porque la fecha de corte es anterior a hoy. Con la fecha de corte, el saldo y el vencido se calculan a ese día; la última gestión y la próxima alerta siempre son de hoy.

**¿Por qué no veo el semáforo de un tercero?**
El semáforo necesita un cupo de crédito mayor que cero. Si el cupo es 0 o está vacío, no hay semáforo.

**¿Por qué no puedo eliminar una gestión?**
Porque las gestiones son el historial de la gestión de cobro y no se borran. Si algo está mal, edite la gestión.

**¿Es la misma gestión que aparece en la ficha del cliente?**
Sí. Las gestiones que registra aquí son las mismas que aparecen en la pestaña [Seguimiento de Cartera](../../ventas/clientes/ficha-seguimiento-cartera.md) de la ficha del cliente.

**¿Por qué no veo el botón Exportar Excel o Exportar PDF?**
Su perfil no tiene el permiso **Exportar** (Excel) o **Imprimir** (PDF) de la opción 300. Pida el permiso a su administrador.

**¿Por qué no veo Nueva gestión?**
Su perfil puede consultar, pero no crear gestiones. Pida el permiso **Crear** a su administrador.

**¿Por qué no me llegó el aviso de una alerta?**
El aviso llega a quien registró la gestión, a las 5:00 a. m., y solo si la fecha de alerta es vencida o de hoy. Los avisos de otros usuarios no le llegan a usted.

---

**¿Por qué no veo la columna Cobrador?**
Solo aparece en cuentas por cobrar (clientes) y cuando su administrador habilitó los cobradores. Si no la ve, consulte con su administrador.

**¿Por qué un cliente aparece como Sin asignar?**
Porque ninguna regla le corresponde y nadie lo asignó a mano. Puede asignarlo, o pedir un reparto equitativo.

**¿Puedo marcar un compromiso como cumplido?**
No. Lo decide el recibo de caja: cuando el cliente paga lo prometido dentro de la fecha, el compromiso queda **Cumplido**.

**¿Por qué me sale la advertencia de horario?**
Porque la gestión está fuera del horario de contacto configurado para la empresa. Es solo una advertencia: si necesita registrar la gestión, pulse **Registrar de todos modos**.

## 🛠️ Errores comunes

| Mensaje | Qué hacer |
|---------|-----------|
| **No se pudo consultar la cartera** | Sus filtros se conservaron. Pulse **Reintentar**. |
| **No tiene permiso para ver el seguimiento de cartera** | Su perfil no tiene **Consultar** en la opción 300. Pida el permiso a su administrador. |
| **Ningún resultado coincide con la búsqueda** o **No hay terceros con saldo con estos filtros** | Pulse **Limpiar filtros** o cambie la fecha de corte. |
| **No se pudo generar el archivo. Intente de nuevo.** | Vuelva a exportar. Si sigue igual, consulte a su administrador. |
| **Escribe el motivo; queda en la bitácora.** | Escriba el motivo del cambio de cobrador. |
| **Elige el canal.** / **Elige el resultado.** | Elija una opción en el campo marcado. |
| **Escribe con quién hablaste.** / **Escribe el mensaje.** | Complete el campo marcado. |
| **La fecha prometida no puede ser anterior a hoy.** | Elija hoy o una fecha posterior. |
| **El valor debe ser mayor que cero.** / **Elige el medio de pago.** | Corrija el compromiso de pago. |
| **Revisa N campos obligatorios.** | Corrija los campos marcados. |

![Lista vacía con los filtros aplicados](../recursos/img/seguimiento/l-04-vacio.png)

---

## 🧷 Relacionado

- [Estado de cuenta por correo](estado-cuenta.md): enviar el estado de cuenta a un cliente o en lote, y su registro.
- [Cobradores](../cobradores.md): titulares, apoyos, reglas y ausencias.
- [Cola de cobro](cola.md): a quién cobrar hoy.
- [Generación de cobros](generacion.md): cómo se asignan los clientes y se arma la cola del día.
- [Maestros de Cartera por tipo](../maestros.md): Clientes, Vendedores, Proveedores y Compradores desde el menú de Cartera.
- [Ficha del cliente · Seguimiento de Cartera](../../ventas/clientes/ficha-seguimiento-cartera.md)
- [Ficha del cliente · Cartera](../../ventas/clientes/ficha-cartera.md)
- [Cartera de terceros](../reportes/terceros.md)
- [Parámetros de cartera](../parametros.md): los umbrales del semáforo de cupo.
