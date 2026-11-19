[Regresar a Cartera](../readme.md)

---

# 📞 Panel de Cobro

![Static Badge](https://img.shields.io/badge/Tipo-Movimiento-red)
![Static Badge](https://img.shields.io/badge/Module-Cartera-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-300-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261118-yellow)

---

## 📋 Descripción

El **Panel de Cobro** es la pantalla de trabajo diario del cobrador. Reúne en una sola vista a quién cobrar hoy, en orden, con todo lo necesario para llamar, escribir, registrar lo que el cliente dijo y cobrar: la cartera del cliente, su historia, sus alertas y el recibo de caja.

Responde a la pregunta **¿a quién llamo ahora?** Va cliente por cliente y, cuando termina uno, pasa al siguiente que todavía no ha gestionado hoy.

> 💡 Reemplaza el trabajo diario de la [Cola de cobro](cola.md), que ya no aparece en el menú. La cola de cobro ya no aparece en el menú: el trabajo del día se hace desde el Panel de Cobro.

> 💡 El Panel de Cobro trabaja con **clientes** (cuentas por cobrar). Los proveedores no aparecen aquí.

> ℹ️ Si su administrador no ha habilitado la fase de cobro, esta pantalla no aparece en el menú. Use [Seguimiento de Cartera](seguimiento.md).

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Cartera**.
2. En **Movimientos**, haga clic en **Panel de Cobro**. Aparece justo debajo de **Seguimiento de Cartera**.

[captura pendiente: menú Movimientos de Cartera con Panel de Cobro debajo de Seguimiento de Cartera]

También puede llegar desde el aviso de alertas que aparece al entrar a Cartera (ver [Alertas al entrar a Cartera](#-alertas-al-entrar-a-cartera)).

---

## 🖥️ Pantalla principal

[captura pendiente: Panel de Cobro completo con la cabecera, la columna del cliente y las pestañas]

La pantalla tiene tres partes que no se mueven al desplazarse ni al cambiar de pestaña:

1. **Cabecera**: el avance de su cola, los botones de navegación y las acciones generales.
2. **Columna del cliente** (fondo azul), a la izquierda: los datos del cliente y sus acciones.
3. **Pestañas** (a la derecha): **Cartera**, **Gestiones y compromisos** y **Mis alertas**.

### Cabecera

| Elemento | Para qué sirve |
|----------|----------------|
| **Termómetro** | Cuántos clientes de su cola ya gestionó hoy, por ejemplo **12 de 47**, con la barra de avance. |
| **Botones de navegación** | Cuatro botones solo con icono, de colores distintos. Al pasar el cursor sobre cada uno aparece su nombre: **Buscar**, **Anterior**, **Siguiente** y **Continuar automático**. |
| **Pantalla completa** | Ocupa toda la pantalla para trabajar con más espacio. Para salir, pulse **Esc**. |
| **Actualizar** | Vuelve a leer la cartera y la cola con datos nuevos. |
| **Actualizado a las…** | La hora en que se leyó la información que está viendo. |
| **Desde caché** | Indica que la información se tomó de una lectura reciente, guardada por el sistema. |

> 💡 La información se guarda por **15 minutos**. Si pulsa **Actualizar**, el sistema vuelve a leer la cartera. Cada madrugada el sistema deja la cartera preparada, de modo que al empezar el día la información ya está lista.

### Buscar un cliente

Pulse la **lupa** (**Buscar**) para encontrar un cliente de su cola. Puede escribir:

- el **documento**;
- el **nombre completo**;
- el **nombre comercial**.

Si el nombre comercial es distinto del nombre, aparece entre paréntesis. Los clientes que ya gestionó hoy salen marcados con **✓**.

Al elegir un cliente, el panel se abre en él. Cuando guarda una gestión de ese cliente, el panel **vuelve al cliente que seguía en la cola**, no al siguiente de la búsqueda.

### Moverse por la cola

- **Siguiente**: pasa al siguiente cliente de la cola.
- **Anterior**: vuelve al cliente anterior.
- **Continuar automático**: al guardar una gestión, pasa solo al siguiente cliente **que no ha gestionado hoy**. Si todos los que quedan ya están gestionados, aparece **Terminaste la cola**. Con este botón apagado, el panel se queda en el mismo cliente después de guardar. La preferencia se recuerda para su usuario.

Si el guardado de la gestión falla, el panel **no avanza** al siguiente cliente.

### Retomar el trabajo

Si se cayó la sesión o recargó la página, al volver al Panel de Cobro:

- los clientes con una gestión registrada hoy salen marcados con **✓ gestionado**;
- el termómetro cuenta lo que ya hizo hoy;
- la cola arranca en el **primer cliente sin gestionar**.

No tiene que buscar dónde iba.

---

## 🧍 Columna del cliente

[captura pendiente: columna del cliente con sus datos, sucursal e iconos de acción]

En la columna azul aparecen:

- el **nombre** del cliente y, si es distinto, su **nombre comercial**;
- la **sucursal** (si el cliente tiene varias). Elija una para ver su cartera, su historia y sus datos de contacto. **Todas** muestra el total del cliente;
- el **teléfono**, el **celular**, el **correo** y el **cobrador** que lo atiende (con su suplente, si hay ausencia).

### Acciones con icono

| Acción | Qué hace |
|--------|----------|
| **Llamar** | Inicia la llamada al teléfono del cliente. Si no tiene teléfono, no está disponible. |
| **Enviar mensaje** | Abre un mensaje de WhatsApp al celular del cliente. Si no tiene celular, no está disponible y la pantalla le dice por qué. |
| **Detalle** | Abre la ficha del cliente. Solo aparece con el permiso correspondiente. |
| **Historial del cliente en PDF** | Descarga un PDF con las facturas del cliente y los recibos que las afectan. Ver [Historial del cliente en PDF](#historial-del-cliente-en-pdf). |
| **Registrar pago** (icono de billetera) | Abre el recibo de caja con el cliente ya cargado. Ver [Registrar un pago](#-registrar-un-pago). |
| **Enviar estado de cuenta** | Envía por correo el estado de cuenta del cliente. Ver [Estado de cuenta por correo](estado-cuenta.md). |

### Historial del cliente en PDF

1. Haga clic en el icono de **Historial del cliente en PDF**.
2. Elija el rango de fechas: **Desde** y **Hasta**.
3. Si quiere ver también los documentos anulados, marque **Incluir anulados**.
4. Si lo necesita, marque la opción de **color**.
5. Descargue el PDF.

El PDF lista las facturas del cliente y los recibos de caja que las afectan.

Este PDF requiere el permiso de **Facturas de venta**. Si además no tiene el permiso de **Recibos de caja**, la pantalla le avisa que falta ese permiso, porque el historial no puede mostrar los recibos.

[captura pendiente: diálogo del historial del cliente en PDF con rango de fechas y opciones]

---

## 📊 Pestaña Cartera

[captura pendiente: pestaña Cartera con las dos tablas y una factura seleccionada]

La pestaña tiene dos tablas, cada una con su propio desplazamiento:

- **A la izquierda**, las **facturas** del cliente con su saldo, su vencido y su mora.
- **A la derecha**, la **historia**: los movimientos que han afectado la factura que eligió.

Haga clic en una factura para ver su historia a la derecha. Los saldos y la mora llevan colores para verlos de un vistazo.

---

## ✍️ Pestaña Gestiones y compromisos

[captura pendiente: formulario de gestión con el panel de acento, listas de canal y resultado, e historial a la derecha]

Aquí registra lo que pasó con el cliente. El formulario está a la izquierda, con su propio desplazamiento, y el historial a la derecha.

### Llenar el formulario

1. Pulse **Cargar datos del cliente**. La pantalla llena el campo **Contacto** con el nombre del cliente y el campo **Teléfono** con su celular o, si no tiene, con su teléfono.
2. Elija el **Canal** (cómo se contactó):
   - **Llamada** (azul)
   - **WhatsApp** (verde)
   - **Correo** (naranja)
   - **Visita** (ámbar)
3. Elija el **Resultado**:
   - **Contactado** (azul)
   - **No contesta** (ámbar)
   - **Promesa** (verde)
   - **Rechaza** (rojo)
   - **Número errado** (gris)
4. Si el cliente se comprometió a pagar, registre el **compromiso de pago**.
5. Si el cliente pagó, elija el **Medio de pago**:
   - **Efectivo** (verde)
   - **Transferencia** (azul)
   - **Consignación** (naranja)
   - **Cheque** (ámbar)
   - **Otro** (gris)
6. Elija la **Fecha de alerta** para volver a llamar. El calendario funciona también en pantalla completa.
7. Guarde la gestión.

Si la lista de opciones no cabe debajo del campo, se abre hacia arriba.

### Historial de gestiones

A la derecha aparecen las gestiones y los compromisos del cliente.

- Cada gestión muestra su **canal** en color y su **resultado**.
- Las gestiones anteriores que no tienen canal dicen **Sin canal**. Son solo para consultar: al registrar una gestión nueva, no puede elegir **Sin canal**.
- Cada compromiso muestra **Pagado X de Y**, con su barra de avance.
- El compromiso pasa a **Cumplido** solo cuando los recibos de caja completan el valor comprometido. **No se marca a mano.**

---

## 💰 Registrar un pago

Cuando el cliente le dice que ya pagó, puede registrar el recibo sin salir del Panel de Cobro.

1. Pulse **Registrar pago** (icono de billetera) en la columna del cliente o en el formulario de gestión.
2. Se abre en **otra pestaña** el **Nuevo recibo de caja** de Tesorería, con el cliente ya cargado.
3. Al elegir el **Tipo de movimiento**, se cargan la factura y su saldo.
4. Revise el recibo y guárdelo en Tesorería.

El Panel de Cobro queda abierto donde estaba. Cuando vuelva a él, sigue en el mismo cliente.

> ℹ️ El botón **Registrar pago** solo aparece para **clientes** y si tiene permiso de **Crear** en **Recibos de caja**. El recibo se guarda en Tesorería, como cualquier otro. Para más detalle, vea [Recibos de caja y egresos](../../tesoreria/movimientos/recibos-egresos.md#-llegar-desde-el-panel-de-cobro).

Si el cliente tiene un compromiso de pago y el recibo lo cubre por completo, el compromiso pasa a **Cumplido** solo.

---

## 🔔 Alertas al entrar a Cartera

Al entrar a **Cartera**, una vez por sesión, aparece el aviso **Tienes alertas de cobro por atender** si tiene alertas. Muestra:

- las alertas **vencidas**;
- las alertas **de hoy**;
- las alertas de clientes que **apoya** a otro cobrador.

Los botones son:

- **Ir a gestionar**: abre el Panel de Cobro en la pestaña **Mis alertas**.
- **Más tarde**: cierra el aviso. No vuelve a salir en esa sesión.

Si no tiene alertas, el aviso no aparece.

[captura pendiente: aviso «Tienes alertas de cobro por atender» con sus botones]

---

## ⏰ Mis alertas

La pestaña **Mis alertas** lista los clientes cuya fecha de alerta venció o es hoy, y los que tiene asignados como titular o suplente. Si usted es apoyo de un cliente, aparece marcado como **En apoyo**.

Cada alerta lleva al cliente para gestionarlo. Ver también [Seguimiento de Cartera](seguimiento.md#-mis-alertas), donde las alertas funcionan igual.

---

## 📄 Estado de cuenta

Desde la columna del cliente, el icono **Enviar estado de cuenta** envía por correo el PDF con los documentos pendientes del cliente. El envío y su registro funcionan como se describe en [Estado de cuenta por correo](estado-cuenta.md).

---

---

## 🔐 Permisos

| Permiso (opción 300) | Qué puede hacer |
|----------------------|-----------------|
| **Consultar** | Ver el Panel de Cobro, la cartera del cliente, la historia de sus facturas y **Mis alertas**. |
| **Crear** | Registrar gestiones y compromisos nuevos. |
| **Actualizar** | Editar las gestiones ya registradas. |

Además:

- **Detalle** (ficha del cliente) aparece solo si tiene permiso para ver la ficha.
- **Historial del cliente en PDF** requiere el permiso de **Facturas de venta**. Si falta el de **Recibos de caja**, la pantalla se lo avisa.
- **Registrar pago** requiere el permiso de **Crear** en **Recibos de caja** (opción 73).

> ⚠️ Si no ve una acción, pida a su administrador el permiso que corresponde.

---

## ❓ Preguntas frecuentes

**¿Por qué un cliente aparece con ✓ gestionado?**
Porque ya tiene una gestión registrada hoy, por usted o por otro usuario.

**¿Por qué la cola arrancó en otro cliente?**
Porque se arranca en el primer cliente sin gestionar. Si recargó la página, el panel retoma ahí.

**¿Por qué el compromiso no aparece como cumplido si el cliente ya pagó?**
El compromiso pasa a **Cumplido** solo cuando los recibos de caja cubren el valor completo. Revise que el recibo esté guardado y que su valor alcance el compromiso.

**¿Por qué no aparece el botón de Registrar pago?**
Solo aparece para clientes y con permiso de **Crear** en **Recibos de caja**. Si lo necesita, pida ese permiso a su administrador.

**¿Por qué no aparece el aviso de alertas?**
Porque no tiene alertas vencidas ni de hoy, o ya cerró el aviso en esta sesión. Puede ver sus alertas en la pestaña **Mis alertas**.

**¿Cómo salgo de la pantalla completa?**
Pulse **Esc**.

**¿Por qué los datos no son de hoy?**
Mire la hora de **Actualizado a las…**. Si dice **Desde caché**, pulse **Actualizar** para leer la cartera de nuevo.

---

## 🧷 Relacionado

- [Seguimiento de Cartera](seguimiento.md): la lista de clientes y proveedores, y el panel de gestión.
- [Cola de cobro](cola.md): la cola del día, ya fuera del menú.
- [Estado de cuenta por correo](estado-cuenta.md)
- [Recibos de caja y egresos](../../tesoreria/movimientos/recibos-egresos.md)
- [Cobradores](../cobradores.md)
