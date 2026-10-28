[Regresar a Gastos](../readme.md)

---

# 📤 Causación de Gastos: enviar el documento soporte a SIIGO

![Static Badge](https://img.shields.io/badge/Tipo-Movimiento-red)
![Static Badge](https://img.shields.io/badge/Module-Gastos-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Movimientos-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Causación%20de%20Gastos-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

> ⚠️ **[pendiente: pantalla 102]** La pantalla **Causación de Gastos** (opción 102) y su botón **Enviar a SIIGO** todavía no están disponibles en V2026. Este manual describe cómo funcionará el envío cuando la pantalla esté lista. Los pasos, los nombres de los botones y las capturas se confirmarán entonces.

## 📋 Descripción

Un **documento soporte** es un comprobante de compra o gasto que se registra en Causación de Gastos con un tipo de movimiento de *documento soporte*.

Desde esa pantalla puede enviar el documento a **SIIGO**, el proveedor de facturación electrónica de la compañía, con el botón **Enviar a SIIGO**. El envío es **manual** y se hace **documento por documento**: Orange no envía documentos soporte solos, ni al guardar ni al cerrar.

El envío se hace en segundo plano. No tiene que quedarse esperando en la pantalla: el resultado le llega a sus notificaciones.

## 🎯 Acceso

1. En el menú principal, entre a **Gastos** y abra **Causación de Gastos**. [pendiente: pantalla 102; confirmar la ruta del menú al construir la pantalla]

Permisos:

| Acción | Permiso que necesita |
|--------|----------------------|
| Ver el estado del último envío | Consultar sobre *Causación de Gastos* |
| Enviar a SIIGO | Actualizar sobre *Causación de Gastos* |

Sin el permiso **Actualizar** el botón no aparece. Además, la compañía debe tener habilitada la facturación electrónica con SIIGO; si no lo está, el envío no se puede hacer y el sistema lo informa.

[captura pendiente: causacion-gastos-boton-enviar-siigo]

## ✅ Requisitos antes de enviar

El documento solo se envía si cumple todo lo siguiente. Si algo falta, no se envía nada a SIIGO y el aviso le dice qué corregir.

| Requisito | Qué revisar |
|-----------|-------------|
| **El documento está cerrado** | Un documento abierto o anulado no se envía. Ciérrelo antes. |
| **Es del tipo documento soporte** | Solo se envían los tipos de movimiento de documento soporte que la compañía tiene configurados. En los demás tipos el botón no aparece. [pendiente: pantalla 102] |
| **El proveedor existe en SIIGO** | El proveedor debe estar enviado a SIIGO. Si no lo está, envíelo desde su ficha con **Enviar a SIIGO** (vea [Proveedores de Gastos](../maestros/proveedores.md), sección *Enviar a SIIGO*), espere el aviso y luego envíe el documento. |
| **Los ítems existen en SIIGO** | Cada línea de gasto se busca en SIIGO por su código. Si un código no existe allá, el aviso lista los códigos que faltan. Créelos en SIIGO con el mismo código y reenvíe. |
| **Tiene el número del documento del proveedor** | Es el número de la factura o soporte del proveedor (campo *Documento de referencia*). Puede tener letras al principio y números al final, por ejemplo `GR-123`. Máximo 20 caracteres. Sin números al final, el aviso marca el campo *referencia*. |
| **Tiene forma de pago e impuestos configurados** | La forma de pago y el código de cada impuesto deben estar configurados en la compañía. Si no, el aviso indica qué falta. Si no sabe cómo configurarlos, pida ayuda al administrador. |
| **Sin retenciones ni fletes** | Por ahora no se envían documentos con retenciones, fletes ni otros valores. Vea las preguntas frecuentes. |

## ▶️ Cómo enviar un documento soporte

1. Abra el documento en **Causación de Gastos** y verifique que está cerrado y cumple los requisitos. [pendiente: pantalla 102]
2. Haga clic en **Enviar a SIIGO**.
3. El documento muestra el estado *Enviando*. Puede seguir trabajando.
4. Cuando termina, le llega un aviso a sus notificaciones (campana). En el documento queda el estado del último envío.

[captura pendiente: causacion-gastos-enviando]

Un documento que ya fue enviado no se envía dos veces. Si vuelve a pulsar **Enviar a SIIGO**, el sistema le informa que ya está enviado y muestra su número en SIIGO.

## 🏷️ Estados del envío

| Estado | Qué significa | Qué hacer |
|--------|---------------|-----------|
| **Sin enviar** | El documento nunca se ha enviado. | Verifique los requisitos y pulse **Enviar a SIIGO**. |
| **Enviando** | La solicitud está en curso. | Espere el aviso. No pulse de nuevo. |
| **Enviado** | SIIGO recibió el documento y guardó su número. Se muestra el número de SIIGO. | Nada. No se vuelve a enviar. |
| **Fallido** | SIIGO no aceptó el envío. El estado y el aviso indican el motivo. | Corrija lo que indique el motivo y reenvíe. |
| **Datos inválidos** | Falta un dato o un requisito no se cumple. **No se envió nada a SIIGO.** El aviso indica cuál. | Corrija el dato (vea *Requisitos antes de enviar*) y reenvíe. |
| **Resultado incierto** | Se intentó enviar, pero SIIGO no respondió con claridad y no se pudo comprobar si el documento se creó. Aparece como *fallido* con el motivo *resultado incierto*. | **Revise primero en SIIGO** si el documento ya existe (por número de soporte y proveedor). Si reenvía sin revisar, el documento puede quedar duplicado. |

[captura pendiente: causacion-gastos-estado-fallido]
[captura pendiente: causacion-gastos-estado-resultado-incierto]

### Avisos en notificaciones

| Aviso | Qué significa |
|-------|---------------|
| **Documento enviado** | SIIGO creó el documento. El aviso muestra su número en SIIGO. |
| **Ya estaba enviado** | El documento ya se había enviado. No se envió de nuevo. |
| **Datos inválidos** | Hay datos que corregir. El aviso indica cuáles. No se envió nada. |
| **Envío fallido** | SIIGO no aceptó el envío. El aviso trae el motivo. |

[captura pendiente: causacion-gastos-aviso-datos-invalidos]

## ❓ Preguntas frecuentes

**¿Por qué el aviso dice que el proveedor no existe en SIIGO?**
El proveedor todavía no está en SIIGO. Envíelo desde su ficha con **Enviar a SIIGO** (vea [Proveedores de Gastos](../maestros/proveedores.md)), espere el aviso de *Creado* o *Actualizado* y luego envíe el documento.

**¿Por qué dice que uno o más ítems no existen?**
El código de la línea no está creado en SIIGO. El aviso lista los códigos que faltan. Créelos en SIIGO con ese mismo código y reenvíe el documento.

**¿Por qué me pide revisar el documento de referencia?**
El número del proveedor debe terminar en números, por ejemplo `GR-123`, y tener máximo 20 caracteres. Corrija el número en el documento y reenvíe.

**¿Puedo enviar un documento con retención?**
Por ahora no. Un documento con retención en la factura (retefuente, ReteIVA o ReteICA) se marca como *datos inválidos*. Consulte con su contador cómo registrarlo mientras tanto.

**¿Puedo enviar un documento con fletes u otros valores?**
Por ahora no. Si el documento tiene fletes u otros valores, el total en SIIGO no coincidiría con el de Orange y el aviso lo marca como *datos inválidos*.

**¿Qué hago si sale *Resultado incierto*?**
No reenvíe de inmediato. Busque en SIIGO el documento por el número de soporte y el proveedor. Si está, no lo envíe otra vez. Si no está, puede reenviarlo desde Orange.

**¿El envío transmite el documento a la DIAN?**
Por defecto no. Orange no pide a SIIGO que transmita el documento a la DIAN desde este envío. Confirme con su contador cómo debe quedar en SIIGO.

**¿Se envía solo al guardar o al cerrar el documento?**
No. El envío siempre es manual: usted decide cuándo pulsar **Enviar a SIIGO**.

**¿Puedo corregir o anular en SIIGO lo que envié desde aquí?**
No desde Orange. Si necesita cambiar o anular el documento, hágalo en SIIGO.

**¿Por qué aparece un mensaje de error al pulsar Enviar a SIIGO?**

| Mensaje | Qué hacer |
|---------|-----------|
| El envío no está habilitado para la compañía. | Pida al administrador que habilite la facturación electrónica con SIIGO. |
| El documento debe estar cerrado. | Ciérrelo y vuelva a intentarlo. |
| Este documento no está configurado para enviarse a SIIGO. | Verifique que es un documento soporte. Si lo es, pida al administrador que lo configure. |
| Ya hay un envío de este documento en curso. | Espere el aviso. No pulse otra vez. |
| No se pudo enviar la solicitud. | Espere un momento e inténtelo de nuevo. |

## 📚 Relacionado

- [Proveedores de Gastos](../maestros/proveedores.md): sección *Enviar a SIIGO* (cómo enviar un proveedor antes de sus documentos).
- [Proveedores de Compras](../../compras/maestros/proveedores.md): sección *Enviar a SIIGO*.
- [Maestro de Gastos](../maestros/maestro-de-gastos.md): las referencias de gasto que se usan en las líneas.
- [Manejo general de la información](../../Generales/manejo-general-informacion.md)
