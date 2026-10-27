[Regresar a Ventas](../readme.md)

---

# Ficha del vendedor · Comisiones

![Static Badge](https://img.shields.io/badge/Tipo-Configuracion-red)
![Static Badge](https://img.shields.io/badge/Module-Ventas-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Vendedores-blue)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## Descripción

La pestaña **Comisiones** define **cuánto gana cada vendedor** por lo que vende y por lo que recauda. Puede fijar:

- **Ventas**: una tarifa general del vendedor y excepciones por cliente.
- **Referencias**: un porcentaje propio para una referencia concreta.
- **Recaudo**: una escala general por edad de la cartera y escalas por cliente.
- **Valores por defecto de la compañía**: para los vendedores que no tienen reglas propias.

Cada regla se guarda **por separado**, con su propio botón. La pestaña **no usa el botón Guardar** de la ficha del vendedor, y cambiar una regla no altera los datos del vendedor.

Para revisar qué comisión resulta de un periodo, use la subsección **Informe** de esta pestaña, o la consulta [Comisión calculada](../comisiones/comision-calculada.md) para cualquier vendedor.

> Para el uso general de las tablas y la ayuda vea [Manejo general de la información](../../Generales/manejo-general-informacion.md).

---

## Acceso

1. En el menú principal, haga clic en **Ventas**.
2. En **Maestros de Ventas**, haga clic en **Vendedores**.
3. Busque el vendedor y haga clic en el lápiz (**Editar**) de su fila.
4. Haga clic en la pestaña **Comisiones**.

La pestaña solo aparece en un vendedor **guardado** y solo si su perfil puede consultar **Comisiones de vendedores**. En un vendedor nuevo no la verá.

La subsección **Informe** solo aparece si su perfil puede consultar, además, **Comisión calculada**.

---

## Pantalla principal

![Comisiones por ventas del vendedor](../recursos/img/vendedores-comisiones/01-ventas.png)

Dentro de la pestaña hay hasta cinco subsecciones:

| Subsección | Qué configura o muestra |
|------------|-------------------------|
| **Informe** | Cuánta comisión dejan las reglas en un periodo, con el vendedor de esta ficha. Solo consulta. Ver [Informe](#informe). |
| **Ventas** | La tarifa general del vendedor y las excepciones por cliente. |
| **Referencias** | Las reglas por referencia. |
| **Recaudo** | La escala general del vendedor y las escalas por cliente. |
| **Valores por defecto de la compañía** | La tarifa de ventas y la escala de recaudo de la compañía. Solo se ve con permiso para actualizar. |

Cada subsección muestra sus reglas en una tabla. Cada regla tiene **Editar** y **Dar de baja** en su fila.

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral. |
| **Probar regla** | Simula qué regla se aplicaría a un caso. No guarda nada. No aparece en la subsección **Informe**. Ver [Probar regla](#probar-regla). |
| **Registrar tarifa general**, **Nueva excepción**, **Nueva regla por referencia**, **Definir escala general**, **Nueva escala por cliente** | Crean una regla nueva en la subsección. |

### Estado de cada regla

Cada regla muestra su **vigencia** y su **estado**:

| Estado | Significado |
|--------|-------------|
| **Vigente** | Aplica a la fecha de hoy. |
| **Vencida** | Su fecha final ya pasó. No aplica. |
| **Futura** | Empieza después de hoy. Todavía no aplica. |

La vigencia se muestra como **Del [fecha] al [fecha]** o como **Desde el [fecha], sin fecha de fin**. Use **Solo vigentes** para ocultar las vencidas y futuras.

---

## Informe

El **Informe** es la comisión calculada de **este vendedor** en un periodo, con las reglas que están vigentes hoy. Es el mismo informe de la consulta [Comisión calculada](../comisiones/comision-calculada.md), con el vendedor ya fijado: no tiene que elegirlo.

Solo consulta: no liquida, no paga y no guarda resultados.

Es la primera subsección de la pestaña. Solo aparece si su perfil puede consultar **Comisión calculada**, además de **Comisiones de vendedores**. Si no tiene ese permiso, la pestaña abre en **Ventas**.

*(captura pendiente: subsección Informe con resultado)*

### Periodo y filtros

- **Vendedor**: es el de esta ficha y no se cambia.
- **Desde** y **Hasta**: al abrir la subsección, el periodo es el **mes en curso** y el informe se calcula solo. Para otro periodo, cambie las fechas y pulse **Consultar**. Máximo 366 días y sin fechas futuras.
- **Regla aplicada**: filtra las líneas por la regla usada.

### Qué muestra

- **Tarjetas de resumen**: comisión por ventas, comisión por recaudo y comisión total del periodo.
- **Comisión por regla aplicada**: cuánta comisión dejó cada regla, con su base y su número de líneas.
- **Líneas sin regla**: si hay líneas sin ninguna regla vigente, aparece el aviso con el botón **Ver solo esas líneas**. Ver [Líneas sin regla](../comisiones/comision-calculada.md#resumen-de-ventas-y-resumen-de-recaudo).
- **Ventas** y **Recaudo**: el detalle de cada línea, con la regla aplicada. En recaudo se ve también el tramo de la edad. Cada tabla tiene su buscador por cliente y su fila de total del filtro.

### Exportar

Con el permiso **Exportar** en **Comisión calculada**, el informe tiene **Exportar Excel** y **Exportar PDF**. Están deshabilitados hasta que haya un resultado.

- **Exportar Excel**: ver [Exportar a Excel](../comisiones/comision-calculada.md#exportar-a-excel).
- **Exportar PDF**: elija el papel (**Carta** o **A4**) y **Imprimir en** (**Blanco y negro**, por defecto, o **Color**). El detalle del contenido y el límite de líneas están en [Exportar a PDF](../comisiones/comision-calculada.md#exportar-a-pdf).

*(captura pendiente: exportar PDF desde el informe, con papel e imprimir en)*

### Abrir en pantalla completa

El enlace **Abrir en pantalla completa** abre la consulta [Comisión calculada](../comisiones/comision-calculada.md) con este vendedor y el periodo del informe ya elegidos.

### Cuando cambian las reglas

El informe **no se recalcula solo**, para que las cifras no cambien mientras las mira.

- Si otra persona guarda o da de baja una regla de este vendedor, aparece el aviso **Las reglas cambiaron**, con el texto **Otra persona modificó las reglas de este vendedor. Las cifras del informe pueden estar desactualizadas.** Pulse **Actualizar** para recalcular con las reglas vigentes.
- Si va a otra subsección para usar **Probar regla** o para editar reglas, el informe conserva sus cifras y no se recalcula hasta que pulse **Actualizar**.

### Mensajes del informe

| Mensaje | Qué hacer |
|---------|-----------|
| **Calculando la comisión…** | El cálculo está en curso. Espere. |
| **Sin ventas ni recaudo en el periodo** | Cambie el periodo y pulse **Consultar**. |
| **No se puede calcular para este vendedor** | El tercero tiene más de un registro de vendedor en la compañía. Pida que se revise el dato antes de consultar el informe. |
| **Vendedor no disponible** | El vendedor de la ficha ya no está disponible en la compañía. Revise el maestro de vendedores. |
| **No tiene permiso para ver el informe de comisión calculada.** | Las reglas siguen disponibles en las otras subsecciones. Pida el permiso a un administrador. |
| **Las reglas cambiaron** | Pulse **Actualizar**. |

---

## Qué regla se aplica

Cuando una venta o un recaudo se calcula, el sistema usa **una sola regla**: la más específica que esté vigente en la fecha del documento. Lo específico **ignora** a lo general: las reglas no se promedian ni se suman.

### Ventas

El orden de prioridad vigente es:

1. **Referencia**: la regla de la referencia vendida.
2. **Cliente**: la excepción del cliente.
3. **General del vendedor**: la tarifa general del vendedor.
4. **Compañía**: la tarifa general de la compañía.

Si una venta tiene una regla de **Referencia**, esa regla se usa aunque el cliente tenga otra excepción. Si no hay regla de referencia, se usa la del cliente; si tampoco, la general del vendedor; y si tampoco existe, la de la compañía.

> **Configuración vigente:** el orden anterior (Referencia, Cliente, General, Compañía) es el que usa hoy el sistema para ventas.

### Recaudo

El orden de prioridad vigente es:

1. **Cliente**: la escala del cliente.
2. **General del vendedor**: la escala general del vendedor.
3. **Compañía**: la escala de la compañía.

La escala del cliente reemplaza a la general **completa**: no se combinan tramos de las dos.

### Reglas que no cuentan

- Las reglas **vencidas** o **dadas de baja** no se aplican.
- Si ningún nivel tiene una regla vigente en la fecha del documento, la comisión es **0 %** y la línea aparece como **sin regla** en la consulta.

---

## Ventas

### Tarifa general del vendedor

Es el porcentaje que el vendedor gana por todas sus ventas que no tienen una regla más específica.

1. Pulse **Registrar tarifa general** (o **Editar**, si ya existe).
2. Escriba el **Porcentaje de comisión**: entre 0 y 100, con hasta 4 decimales.
3. Indique **Vigente desde** y, si aplica, **Vigente hasta**.
4. Pulse **Guardar regla**.

Solo puede haber una tarifa general **vigente** a la vez. Si la nueva debe reemplazar a la anterior, cierre la vigencia de la anterior (ponga su fecha final) antes de crear la nueva.

Si no hay tarifa general, el mensaje indica **Sin tarifa general**.

### Excepciones por cliente

Sirven para pagar un porcentaje distinto a un cliente concreto.

1. Pulse **Nueva excepción**.
2. Busque el cliente por código o nombre y elíjalo de la lista.
3. Escriba el porcentaje y las fechas, y pulse **Guardar regla**.

No puede haber dos excepciones del mismo cliente con fechas que se crucen. Si la fecha se cruza, el sistema muestra **Ya existe una regla vigente en esas fechas**: cierre la vigencia de la anterior o cambie las fechas.

![Nueva excepción por cliente](../recursos/img/vendedores-comisiones/05-nueva-excepcion.png)

---

## Referencias

Una regla por referencia da un porcentaje propio a esa referencia, por ejemplo para un producto con mejor margen.

1. Pulse **Nueva regla por referencia**.
2. Busque la referencia por código o nombre y elíjala de la lista.
3. Escriba el porcentaje y las fechas, y pulse **Guardar regla**.

La regla de referencia es la de **mayor prioridad** en ventas: si existe y está vigente, se usa aunque el cliente tenga otra excepción.

Si no hay reglas, el mensaje indica que se usa la tarifa del cliente, la general o la de la compañía.

![Subsección Referencias de la pestaña Comisiones](../recursos/img/vendedores-comisiones/02-referencias.png)

---

## Recaudo

El recaudo se comisiona según **cuántos días pasaron** entre el vencimiento de la factura y la fecha del recibo. Esa diferencia se llama **edad**: es negativa si el cliente pagó antes del vencimiento.

### Cómo se escribe una escala

Una escala es una lista de **tramos** en días. Cada tramo tiene su comisión.

| Tramo | Cómo se lee |
|-------|-------------|
| Primero | **hasta [n] días** (sin límite inferior). |
| Intermedio | **de [a] a [b] días**. |
| Último | **[n] días en adelante** (sin límite superior). |

Las reglas de la escala:

- Los tramos siguen uno tras otro, **sin huecos ni traslapes**: cada tramo empieza el día siguiente al que termina el anterior.
- Toda edad cae en algún tramo, así que siempre hay una comisión aplicable.
- Cada tramo tiene su porcentaje, entre 0 y 100, con hasta 4 decimales.

Si el servidor encuentra un problema en los tramos, marca la fila con el error y muestra **La escala no es válida**. Corrija esa fila y guarde de nuevo.

![Editor de escala de recaudo](../recursos/img/vendedores-comisiones/07-editor-escala.png)

### Escala general y escalas por cliente

1. En **Escala general del vendedor**, pulse **Definir escala general** (o **Editar**).
2. Agregue los tramos, indique las fechas y pulse **Guardar regla**.

Para un cliente con condiciones especiales, use **Nueva escala por cliente** y elija el cliente de la lista. Si el cliente tiene escala vigente, esa escala se usa en lugar de la general.

Si no hay escala general, el mensaje indica **Sin escala general**.

![Subsección Recaudo de la pestaña Comisiones](../recursos/img/vendedores-comisiones/03-recaudo.png)

---

## Valores por defecto de la compañía

Estos valores aplican a los vendedores que no tienen reglas propias. **Cambiarlos afecta a todos esos vendedores.**

- **Tarifa general de ventas de la compañía**.
- **Escala general de recaudo de la compañía**.

Esta sección solo aparece si su perfil puede **actualizar** Comisiones de vendedores. Si no hay valor de la compañía, el mensaje indica **Sin tarifa de la compañía** o **Sin escala de la compañía**.

![Valores por defecto de la compañía](../recursos/img/vendedores-comisiones/04-valores-compania.png)

---

## Probar regla

Sirve para comprobar qué regla se aplicaría a un caso antes de guardarla.

1. Pulse **Probar regla**.
2. Elija el **Tipo de comisión**: **Ventas** o **Recaudo**.
3. Opcional: busque un **cliente** y una **referencia**.
4. Indique la **fecha del documento**. Para recaudo, escriba también la **edad en días**.
5. Pulse **Probar**.

El resultado muestra:

- **Regla que se aplicaría**, con su porcentaje.
- **Cómo se decidió**: cada nivel con uno de estos textos:
  - **Se aplica**: es la regla usada.
  - **Existe, pero se ignora**: hay regla, pero otra más específica manda.
  - **Sin regla vigente**: no hay regla en esa fecha.
  - **Menos específica: no se evaluó**: no hizo falta revisarla.
- Para recaudo, el **tramo aplicado**.

Probar no guarda nada. Si todavía no ha guardado el vendedor, el sistema pide guardarlo antes de probar.

![Probar regla](../recursos/img/vendedores-comisiones/09-probar-regla.png)

---

## Crear, editar y dar de baja

| Acción | Cómo |
|--------|------|
| **Crear** | Use el botón de la subsección (por ejemplo, **Nueva excepción**). Complete el formulario y pulse **Guardar regla**. |
| **Editar** | Pulse **Editar** en la fila de la regla. Cambie lo necesario y pulse **Guardar regla**. |
| **Dar de baja** | Pulse **Dar de baja**, lea la confirmación y confirme. |

**Dar de baja** no borra la regla. Deja de aplicar y queda en la bitácora. Los documentos anteriores conservan la comisión que se les calculó.

Mensaje de confirmación: **La regla deja de aplicar y queda en la bitácora. No se borra: los documentos anteriores conservan su cálculo histórico.**

Después de guardar aparece **La regla se guardó.**; después de dar de baja, **La regla se dio de baja.**

![Confirmación para dar de baja una regla](../recursos/img/vendedores-comisiones/08-baja-confirmacion.png)

---

## Mensajes

| Mensaje | Qué hacer |
|---------|-----------|
| **Escriba un porcentaje entre 0 y 100 con hasta 4 decimales.** | Corrija el porcentaje. |
| **Escriba la fecha de inicio.** | Indique **Vigente desde**. |
| **La fecha final no puede ser anterior a la inicial.** | Corrija las fechas. |
| **Elija un cliente de la lista.** / **Elija una referencia de la lista.** | Busque y elija el registro; no escriba el nombre sin elegirlo. |
| **Ya existe una regla vigente en esas fechas** | Cierre la vigencia de la regla en conflicto o cambie las fechas. Se indica la regla y sus fechas. |
| **Otro usuario cambió esta regla** | No se guardó para no sobrescribir su trabajo. Pulse **Recargar la regla** y aplique su cambio otra vez. |
| **Reglas en edición** | Otra persona está editando las reglas de este vendedor. Intente de nuevo en unos segundos. |
| **La escala no es válida** | Corrija la fila marcada y guarde de nuevo. |
| **No se puede configurar este vendedor** | El tercero tiene más de un registro de vendedor en la compañía. Pida a su administrador que revise ese dato. |
| **No se pudo guardar. Revise la conexión e intente de nuevo.** | Revise su conexión y pulse **Guardar regla** otra vez. |

Ejemplo del aviso cuando una regla se cruza con otra vigente:

![Aviso de vigencias traslapadas](../recursos/img/vendedores-comisiones/06-traslape.png)

---

## Qué ve cada permiso

| Permiso | Qué ve |
|---------|--------|
| Consultar **Comisiones de vendedores** | Las reglas de las subsecciones, sin botones de cambio. Aparece el aviso **Solo puede consultar las reglas. Para crearlas o cambiarlas pida el permiso a un administrador.** |
| Consultar **Comisiones de vendedores** y **Comisión calculada** | Además, la subsección **Informe**. |
| Consultar **Comisión calculada** y **Exportar** en esa opción | Además, en el **Informe**, los botones **Exportar Excel** y **Exportar PDF**. |
| Crear o Actualizar **Comisiones de vendedores** | Los botones **Registrar**, **Nueva**, **Definir**, **Editar** y **Guardar regla**. |
| Eliminar (dar de baja) **Comisiones de vendedores** | El botón **Dar de baja**. |
| Actualizar **Comisiones de vendedores** | Además, la subsección **Valores por defecto de la compañía**. |

Sin permiso de consulta, la pestaña no aparece.

---

## Cambios de otros usuarios

Si otra persona guarda o da de baja una regla de este vendedor mientras usted tiene la pestaña abierta, verá el aviso **Otro usuario modificó las reglas**, con el texto **Los datos que ve pueden estar desactualizados**. Pulse **Actualizar** para recargar las reglas.

En la subsección **Informe** el aviso es **Las reglas cambiaron**. Pulse **Actualizar** para recalcular el informe. Ver [Cuando cambian las reglas](#cuando-cambian-las-reglas).

---

## Preguntas frecuentes

**¿Por qué una venta me comisiona 0 %?**
Ninguna regla vigente aplica a esa venta en la fecha del documento. Revise la tarifa general del vendedor y la de la compañía, y sus fechas de vigencia.

**¿Por qué no cambió la comisión al editar la tarifa general?**
Revise si existe una excepción por cliente o una regla por referencia para esa venta. Lo específico manda sobre lo general.

**¿Por qué no veo la subsección Informe?**
Además de **Comisiones de vendedores**, necesita el permiso para consultar **Comisión calculada**. Pida el acceso a un administrador.

**¿Por qué el informe no cambió después de editar una regla?**
El informe no se recalcula solo. Cuando el aviso **Las reglas cambiaron** aparezca, pulse **Actualizar**.

**¿Puedo tener dos tarifas generales vigentes?**
No. Solo puede haber una vigente a la vez.

**¿Cambiar una regla altera las comisiones de meses pasados?**
Las reglas se aplican según la fecha de cada documento. Si cambia una regla con fechas pasadas, el cálculo de esos documentos cambia también. Por eso cada cambio queda en la bitácora de la compañía, con el valor anterior y el nuevo.

---

## Relacionado

- [Comisión calculada](../comisiones/comision-calculada.md)
- [Ficha del vendedor · Ventas](ficha-ventas.md)
- [Ficha del vendedor · Cartera](ficha-cartera.md)
- [Vendedores (maestro)](../maestros/vendedores.md)
