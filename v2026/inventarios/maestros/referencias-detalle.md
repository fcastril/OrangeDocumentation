[Regresar a Referencias](referencias.md)

---

# 🏷️ Detalle de una referencia

![Static Badge](https://img.shields.io/badge/Tipo-MaestroTipoII-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Maestros-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Referencias-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20260927-yellow)

---

## 📋 Descripción

La **página de detalle** es donde se crea, se consulta y se modifica una referencia. Reúne todos sus datos en pestañas:

| Pestaña | Qué contiene |
|---------|--------------|
| **General** | Código, nombres, clasificación (subgrupo y unidad), comportamiento, tipo de producto y control sanitario. |
| **Impuestos y costos** | IVA y porcentajes de costo. |
| **Contabilidad** | Cuentas contables de ventas y de devoluciones. |
| **Variantes** | Las combinaciones de la referencia (por ejemplo talla y color), cada una con su código de barras, precios y niveles de inventario. |
| **Proveedores** | Los proveedores que venden la referencia, con su código y su valor. |

Las tres primeras pestañas forman la **cabecera** de la referencia y se guardan juntas con **Guardar referencia**. Las variantes y los proveedores se guardan **cada uno en su propio diálogo**, en el momento.

> 📘 Para buscar, copiar, eliminar o exportar referencias, vea [Referencias](referencias.md).

---

## 🎯 Acceso

- **Crear:** en [Referencias](referencias.md), haga clic en **Nueva referencia**.
- **Consultar o editar:** en [Referencias](referencias.md), haga clic en el **lápiz** de la referencia (o en el **ojo**, si su perfil solo permite consultar).

Puede guardar el enlace de la página en favoritos o compartirlo: el enlace incluye la pestaña que está viendo (por ejemplo, abre directamente **Contabilidad**).

---

## 🖥️ Partes de la página

![Detalle de una referencia: pestaña General](../recursos/img/referencias/05-editar-general.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral. |
| **Volver a referencias** | Regresa al listado. Si hay cambios sin guardar, le pregunta antes (ver *Salir sin guardar*). |
| **Código y nombre** | Identifican la referencia que tiene abierta. |
| **Etiquetas** | Resumen de la referencia: **Activa** o **Inactiva**, **Maneja inventario**, **Comercializada**, **Material**, **Semielaborada**. Cambian en cuanto marca o desmarca las casillas. |
| **En vivo** | La página está conectada y le avisa si otro usuario cambia esta referencia. |
| **Pestañas** | Cambian la sección visible sin perder lo escrito. Una pestaña con errores muestra un **contador rojo**; **Variantes** muestra cuántas variantes hay. |
| **Copiar** / **Eliminar** (abajo a la izquierda) | Solo al editar. Funcionan igual que en el listado: ver [Referencias](referencias.md). |
| **Cancelar** / **Guardar referencia** (abajo a la derecha) | Descartan o guardan los cambios de la cabecera (General, Impuestos y costos, Contabilidad). La barra queda fija abajo mientras se desplaza. |

---

## ➕ Crear una referencia

1. En el listado, haga clic en **Nueva referencia**. El cursor queda en **Código**.
2. Llene la pestaña **General** (como mínimo: código, nombre, subgrupo y unidad de medida).
3. Revise **Impuestos y costos** (si la referencia liquida IVA, elija los tres impuestos) y, si aplica, **Contabilidad**.
4. Haga clic en **Guardar referencia**.

![Nueva referencia](../recursos/img/referencias/03-crear.png)

Al crear vienen marcadas **Activa**, **Maneja inventarios (kardex)** y **Liquida IVA**; revíselas antes de guardar. Las pestañas **Variantes** y **Proveedores** están deshabilitadas con el aviso *"Guarda la referencia para agregar variantes y proveedores."*

Al guardar verá **"Referencia … creada"** y la página pasa sola a la pestaña **Variantes**, con el aviso *"Referencia creada. Ahora agrega sus variantes con su precio y código de barras."* Continúe en *Variantes*.

> 💡 Una referencia sin variantes no se puede usar en compras, ventas ni movimientos de inventario: agregue al menos una.

---

## 📝 Pestaña General

| Sección | Campo | Obligatorio | Reglas y ejemplo |
|---------|-------|:-----------:|------------------|
| **Identificación** | **Código** | ✅ | Hasta 20 caracteres: letras (incluida la Ñ), números y `. _ / -`, **sin espacios**. Se escribe **en MAYÚSCULAS** automáticamente. No se puede repetir en la compañía. Ej.: `CAM-BAS-001`, `PIÑA-01`, `A.10/2`. |
| | **Código alterno** | | Otro código con que conoce la referencia (por ejemplo, el del fabricante). Hasta 20 caracteres, en mayúsculas. Se puede repetir. También sirve para buscarla en el listado. |
| | **Nombre** | ✅ | Hasta 100 caracteres, **sin comas ni punto y coma**. Ej.: `Camiseta básica cuello redondo`. |
| | **Nombre alterno** | | Hasta 100 caracteres, sin comas ni punto y coma. Ej.: el nombre en otro idioma. |
| **Clasificación** | **Subgrupo** | ✅ | Búsquelo por código o nombre. Debajo aparece su grupo (`Grupo: ROP - Ropa y calzado`). |
| | **Unidad de medida** | ✅ | Búsquela por código o nombre. Ej.: `UND - Unidad`. |
| | **Bodega por defecto** | | La bodega que se propone en los movimientos. |
| | **Tercero principal** | | Busque por documento o nombre. Solo aparecen terceros **activos**. |
| | **Categoría** | | Hasta 5 caracteres. |
| | **Composición** | | Hasta 100 caracteres. Ej.: `100 % algodón`. |
| | **Posición arancelaria** | | Hasta 50 caracteres. |
| **Comportamiento** | **Activa** | | Desmarcada, la referencia deja de verse en el listado por defecto (filtro *Activas*). |
| | **Maneja inventarios (kardex)** | | Lleva existencias y costo por bodega. |
| | **Aparece en el catálogo del punto de venta** / **Favorita en el punto de venta** / **Se imprime en la comanda** | | Cómo se comporta en el punto de venta. |
| **Tipo de producto** | **Comercializada** | | Se compra y se vende sin transformarla. Al marcarla se desmarcan y deshabilitan *Es material* y *Semielaborada*: una referencia comercializada no puede ser ninguna de las dos. |
| | **Es material o insumo** | | Al marcarla aparece **Tipo de material** (obligatorio): Materia prima, Insumos, Proceso, Mano de obra, Indirecto (CIF), Herramienta o Aseo y papelería. |
| | **Semielaborada o producida** | | La referencia se fabrica. Ver la nota de abajo. |
| **Control sanitario y de calidad** | **Tipo de riesgo** | | Bajo (I), Moderado (II) o Alto (III). |
| | **Tipo de clasificación** | | Reactivo o Dispositivo médico. |
| | **Registro sanitario Invima** / **Clasificación IARC** | | Texto de hasta 50 caracteres (acepta letras y guiones). |
| | **Exige fecha de vencimiento en los movimientos** / **Verifica criterios de aceptación al recibir** / **Exige lote en los movimientos** | | Controles que se aplican al registrar movimientos. |

### Elegir un dato de otra tabla (subgrupo, unidad, bodega, tercero, impuestos, cuentas…)

1. Haga clic en el campo. Se abre una lista con los primeros datos, como `Código - Nombre`.
2. Escriba parte del código o del nombre para filtrar; si hay muchos, desplácese hacia abajo y se cargan más.
3. Elija el dato. Con la **✕** del campo lo deja vacío (en los campos que no son obligatorios).

Si un dato que tenía la referencia ya no existe en la compañía, el campo aparece en rojo con *"Ya no está disponible. Elige otro valor."*: elija otro para poder guardar.

### Cambiar el código

Puede cambiar el código de una referencia existente. Verá el aviso *"Vas a cambiar el código … Los movimientos conservan la relación, pero los informes, las exportaciones y las plantillas de importación mostrarán o buscarán el código nuevo."* Si vuelve a escribir el código original, el aviso desaparece.

> ℹ️ **Referencias semielaboradas:** en esta versión los **consumos** y las **operaciones de producción** de una referencia semielaborada se siguen gestionando en la **versión anterior de OrangeERP**. Al marcar *Semielaborada* verá un aviso que lo recuerda.

---

## 💰 Pestaña Impuestos y costos

![Pestaña Impuestos y costos](../recursos/img/referencias/06-impuestos.png)

**IVA**

| Campo | Qué hace |
|-------|----------|
| **Liquida IVA** | Encendido (por defecto), la referencia se compra y se vende con IVA y se muestran los tres impuestos. Apagado, se ocultan y al guardar **se borran los tres impuestos** y la marca de IVA incluido. |
| **IVA generado (ventas)** ✅ | El IVA que se cobra al vender. |
| **IVA descontable (compras)** ✅ | El IVA que se descuenta al comprar. |
| **IVA en devoluciones** ✅ | El IVA de las devoluciones. |
| **El precio de venta incluye IVA** | Marque si los precios de las variantes ya traen el IVA. |

Los tres impuestos son **obligatorios** cuando la referencia liquida IVA.

**Porcentajes de costo**: **Utilidad**, **Indirectos de fabricación**, **Indirectos administrativos** e **Indirectos de ventas**, en porcentaje de **0 a 100** con hasta 2 decimales (escriba `35` para 35 %).

---

## 📒 Pestaña Contabilidad

![Pestaña Contabilidad](../recursos/img/referencias/07-contabilidad.png)

Las cuentas se agrupan en dos secciones. **Todas son opcionales.**

| Sección | Conceptos |
|---------|-----------|
| **Ventas** | Valor bruto · IVA · Descuento · Costos · Inventario |
| **Devoluciones** | Valor bruto · Descuento · IVA |

En cada fila:

1. En la cuenta, busque por código o nombre. Solo aparecen **cuentas de movimiento**.
2. Si la **Naturaleza** estaba vacía, se propone la de la cuenta (*Propuesta según la cuenta*); puede cambiarla a **Crédito** o **Débito**.
3. Si elige una cuenta, la naturaleza es obligatoria. Si borra la cuenta, la naturaleza se borra y se deshabilita.

---

## 💾 Guardar los cambios

Haga clic en **Guardar referencia**. Se guardan juntas las pestañas **General**, **Impuestos y costos** y **Contabilidad**; verá **"Referencia … actualizada"** y **se queda en la página**, para seguir con las variantes o los proveedores.

### Si hay errores: el contador de errores

![Guardar con errores: resumen y contador por pestaña](../recursos/img/referencias/04-crear-validacion.png)

Si falta algo o hay un dato inválido, no se guarda nada y:

- Arriba aparece *"Revisa los campos marcados: hay N errores."*
- Cada pestaña con errores muestra un **contador rojo** con su número de errores.
- Se abre la **primera pestaña con errores** (en el orden General → Impuestos y costos → Contabilidad) y el cursor va al primer campo marcado.

Corrija los campos marcados en cada pestaña y vuelva a guardar. Lo que escribió no se pierde.

| Mensaje | Qué hacer |
|---------|-----------|
| Escribe el código de la referencia. / Escribe el nombre de la referencia. | Complete el campo. |
| Usa hasta 20 caracteres: letras (incluida la Ñ), números y . _ / - (sin espacios). | Quite espacios, tildes u otros símbolos del código, o acórtelo. |
| El nombre admite hasta 100 caracteres y no puede tener comas ni punto y coma. | Corrija o acorte el nombre. |
| Ya existe una referencia con el código … | Use otro código. |
| Elige el subgrupo. / Elige la unidad de medida. | Elija el dato en el buscador. |
| Elige el tipo de material. | Marcó *Es material o insumo*: elija el tipo. |
| Elige el impuesto: la referencia liquida IVA. | Complete los tres impuestos, o apague *Liquida IVA*. |
| Escribe un porcentaje de 0 a 100 con hasta 2 decimales. | Corrija el porcentaje. |
| Indica la naturaleza de la cuenta. | Eligió una cuenta sin naturaleza: elija Crédito o Débito. |
| Ya no está disponible. Elige otro valor. | El dato (subgrupo, impuesto, cuenta…) ya no existe o lo eliminó otro usuario: elija otro. |
| Tu perfil ya no permite esta acción. Recarga la página para ver tus permisos actuales. | Sus permisos cambiaron mientras trabajaba. Recargue la página. |
| No se pudo guardar la referencia. Inténtalo de nuevo. | Falló la conexión o el servidor. Lo escrito se conserva: vuelva a guardar. |
| La referencia ya no existe. Otro usuario la eliminó. | No se puede guardar. Vuelva al listado. |

---

## 🎨 Pestaña Variantes

![Pestaña Variantes](../recursos/img/referencias/08-variantes.png)

Cada **variante** es una combinación de **atributo principal** y **atributo secundario** (por ejemplo, talla *M - Mediana* y color *NEG - Negro*), con su propio código de barras, precios y niveles de inventario. La variante se nombra así: *Mediana / Negro*.

La tabla muestra: Atributo principal · Atributo secundario · Unidad · Cantidad · EAN13 · Asignación EAN13 · Precio 1 · Costo esperado · Participación. Con el **lápiz** la edita y con la **papelera** la elimina.

### Agregar o editar una variante

1. Haga clic en **Agregar variante** (o en el **lápiz** de una variante).
2. Llene los datos del diálogo.
3. Haga clic en **Guardar variante**. Verá **"Variante … agregada"** (o *actualizada*) y la tabla se actualiza.

![Diálogo de una variante](../recursos/img/referencias/09-variante.png)

| Sección | Campo | Reglas |
|---------|-------|--------|
| **Combinación** | **Atributo principal** ✅, **Atributo secundario** ✅ | Búsquelos por código o nombre. La combinación no se puede repetir en la referencia (*"Ya existe la variante … en esta referencia."*). |
| | **Unidad de empaque** ✅ | Por defecto, la unidad de la referencia. |
| | **Cantidad por empaque** ✅ | Número entero de 0 o más. |
| **Códigos de barras y códigos abiertos** | **EAN13** | 13 dígitos; el último es el **dígito de control**. Si no cuadra, el mensaje le dice cuál debería ser (*"… (debería ser 8)"*). No se puede repetir en la compañía. |
| | **Fecha de asignación del EAN13** | Solo lectura. Ver abajo. |
| | **EAN8** | Opcional. 8 dígitos. |
| | **Código abierto (20)**, **(40)**, **(100)** | Opcionales. Texto libre de hasta 20, 40 o 100 caracteres. |
| **Costos y precios** | **Costo esperado**, **Costo calculado**, **Precio 1** a **Precio 5** | Valores de 0 o más, con hasta 2 decimales. |
| | **Descuento en el punto de venta (%)** | De 0 a 100, hasta 2 decimales. |
| **Inventario y producción** | **Mínimo**, **Máximo**, **Crítico** | Unidades enteras de 0 a 32.767. |
| | **Peso**, **Tiempo estándar (min)** | Hasta 2 decimales. |
| | **Participación (%)** | De 0 a 100. |

> 📱 En el celular el diálogo ocupa toda la pantalla y las secciones se apilan.

### Generar EAN13

Si la variante no tiene código de barras propio, haga clic en **Generar EAN13**: el sistema arma un código válido y único con el **prefijo EAN13 de la compañía** y su consecutivo, y lo escribe en el campo.

- El número queda **reservado** aunque después no guarde la variante: la próxima vez se genera el siguiente.
- Si aparece *"La compañía no tiene configurado el prefijo para generar códigos EAN13."*, pida que se configure el prefijo en los datos de la compañía o escriba el código a mano.

### Fecha de asignación del EAN13

Debajo del EAN13 se ve la **Fecha de asignación del EAN13**. No se escribe: la pone el sistema.

| Lo que ve | Significa |
|-----------|-----------|
| 📅 una fecha (por ejemplo `2/03/2026`) | Día en que se asignó el EAN13 actual. |
| **Se asignará hoy al guardar** | Escribió o generó un EAN13 nuevo: al guardar, la fecha será la de hoy. |
| **Sin EAN13** | La variante no tiene código de barras. |
| **—** | El código viene de la versión anterior sin fecha registrada. |

Si cambia otros datos de la variante sin tocar el EAN13, la fecha no cambia.

### Calcular precios

Con **Calcular precios** no tiene que calcular a mano el costo y los cinco precios:

1. Escriba el **Costo esperado** (mayor que 0).
2. Haga clic en **Calcular precios**. Se llenan el **Costo calculado** y **Precio 1** a **Precio 5** con los porcentajes configurados en la compañía, y verá *"Precios calculados con los porcentajes de la compañía. Revísalos antes de guardar."*
3. Revise o ajuste los valores y haga clic en **Guardar variante**. Nada se guarda hasta ese momento.

> 💡 Si la compañía no tiene porcentajes de precios configurados, el diálogo lo avisa y, al calcular, el costo calculado y los precios quedan iguales al costo esperado.

### Aplicar precios a todas

Al **editar** una variante, abajo a la izquierda está **Aplicar precios a todas**. Copia el **costo esperado**, el **costo calculado**, los **5 precios** y el **descuento** de esa variante a **todas** las variantes de la referencia (útil cuando todas las tallas valen lo mismo).

1. Deje la variante con los precios correctos.
2. Haga clic en **Aplicar precios a todas** y confirme con **Aplicar a todas**.
3. Verá **"Precios aplicados a N variantes"** y las filas se resaltan.

### Eliminar una variante

Haga clic en la **papelera** de la variante y confirme con **Eliminar variante**. Si la variante ya se usó (tiene movimientos u otra información), no se elimina: *"No se puede eliminar la variante …: tiene movimientos u otra información relacionada."*

---

## 🚚 Pestaña Proveedores

![Pestaña Proveedores](../recursos/img/referencias/10-proveedores.png)

Aquí registra los **proveedores que venden esta referencia**, con el código y el valor con que la manejan. La tabla muestra **Proveedor** (`NIT - Nombre`), **Código del proveedor** y **Valor**.

**Agregar o editar un proveedor**

1. Haga clic en **Agregar proveedor** (o en el **lápiz** de un proveedor).
2. En **Proveedor**, busque por NIT o nombre.
3. Escriba el **Código de la referencia en el proveedor** (hasta 20 caracteres; se escribe en mayúsculas).
4. Escriba el **Valor** (mayor que 0, hasta 2 decimales).
5. Haga clic en **Guardar proveedor**. Verá **"Proveedor … agregado"** (o *actualizado*).

Un proveedor no se puede repetir en la misma referencia: *"Este proveedor ya está en la referencia."*

**Quitar un proveedor**: haga clic en la **papelera** (**Quitar proveedor**) y confirme. Solo se quita la relación con esta referencia; el proveedor sigue existiendo.

---

## 🚪 Salir sin guardar

Si cambió algo de la cabecera (General, Impuestos y costos o Contabilidad) y sin guardar intenta irse —con **Volver a referencias**, **Cancelar**, las migas, otra opción del menú, o cerrando o recargando la pestaña del navegador—, aparece **"¿Salir sin guardar?"**:

- **Seguir editando**: vuelve a la página con todo lo que escribió.
- **Salir sin guardar**: sale y descarta los cambios.

No pregunta si no hay cambios, si ya guardó, o si solo trabajó en variantes o proveedores (esos se guardan al cerrar su diálogo). Cambiar de pestaña dentro de la página nunca pierde lo escrito.

---

## 🔒 Solo consulta

Si su perfil tiene permiso de **consultar** pero no de **actualizar** la opción Referencias, la página se abre con el aviso *"Solo consulta: tu perfil no permite modificar referencias."*: todos los campos son de solo lectura, no hay **Guardar referencia** y las tablas de variantes y proveedores no tienen botones para agregar, editar ni eliminar. **Copiar** y **Eliminar** aparecen solo si su perfil tiene esos permisos.

---

## 🔄 Cambios de otros usuarios (en vivo)

| Qué hizo el otro usuario | Qué verá | Qué puede hacer |
|--------------------------|----------|-----------------|
| Modificó la referencia que usted tiene abierta | *"Otro usuario modificó esta referencia mientras la editabas. Si guardas, reemplazarás sus cambios."* | **Ver sus cambios** para cargar lo que la otra persona guardó (si usted tenía cambios sin guardar, le avisa que se perderán), o **Guardar referencia** para dejar lo suyo. |
| Eliminó la referencia | *"Otro usuario eliminó esta referencia. Ya no se puede guardar."* | Volver al listado. Guardar y las acciones de las tablas quedan deshabilitados. |
| Cambió variantes o proveedores | *"Otro usuario cambió las variantes o los proveedores; la lista se actualizó."* | Nada: la tabla se actualiza sola y resalta las filas. Si usted tenía un diálogo abierto, se actualiza al cerrarlo. |

---

## 🕰️ Referencias creadas en la versión anterior

Muchas referencias vienen de la versión anterior de OrangeERP con datos que hoy no cumplirían las reglas (un código con espacios como `OF 2019`, un nombre con coma, un EAN13 con dígito de control incorrecto, una variante con cantidad 0…). Para no obligarlo a corregir todo de una vez:

- **Se muestran tal cual y se pueden guardar** mientras no cambie ese dato. Las reglas solo se aplican al campo que usted modifique.
- Si una referencia antigua está marcada como *Comercializada* y a la vez *Es material* o *Semielaborada*, verá *"Viene así de la versión anterior: se guarda sin cambios. Si marcas o desmarcas estas casillas, se aplica la regla."*
- **Siempre se exigen**, aunque no los haya tocado: el nombre, el código, el subgrupo, la unidad de medida y, si liquida IVA, **los tres impuestos**. Muchas referencias antiguas no tienen **IVA descontable** o **IVA en devoluciones**: la primera vez que las guarde, complete esos campos en **Impuestos y costos**.
- Si el subgrupo, un impuesto o una cuenta ya no existen, el campo aparece *no disponible* y hay que elegir otro.
- La **participación** de algunas variantes antiguas se ve multiplicada por 100 (por ejemplo, 15.000). No impide guardar mientras no la cambie; si la corrige, escriba un valor de 0 a 100.

---

## 🧭 Lo que por ahora sigue en la versión anterior

Esta pantalla se entrega por partes. Mientras no se publiquen en la nueva versión, estas tareas se hacen en la **versión anterior de OrangeERP**:

| Tarea | Dónde hacerla por ahora |
|-------|-------------------------|
| Consumos y operaciones de producción de las referencias semielaboradas | Versión anterior, pestañas de producción de la referencia. |
| Consultar el inventario (saldos por bodega) y los movimientos (kardex) de la referencia | Versión anterior, detalle de la referencia. |
| Foto principal y documentos adjuntos | Versión anterior. Los que ya tenga se **conservan** al editar la referencia aquí. Una referencia copiada aquí queda sin foto ni documentos. |
| Importar referencias desde Excel | Versión anterior, opción de importación de referencias. |
| Enviar el producto a **facturación electrónica** | La nueva versión **no** envía la referencia al proveedor de facturación electrónica al guardar. Si crea o modifica aquí una referencia que se factura electrónicamente, guárdela también desde la versión anterior para que se sincronice. |

---

## ❓ Preguntas frecuentes

**¿Por qué no puedo agregar variantes a una referencia nueva?**
Primero hay que guardar la referencia. Al guardarla, la página pasa sola a **Variantes**.

**Guardé y la página no volvió al listado.**
Es a propósito: después de guardar se queda en el detalle para que siga con las variantes o los proveedores. Use **Volver a referencias** cuando termine.

**¿Guardar referencia guarda también las variantes?**
No hace falta: cada variante y cada proveedor se guarda al hacer clic en **Guardar variante** o **Guardar proveedor**. **Guardar referencia** guarda solo General, Impuestos y costos y Contabilidad.

**El EAN13 que escribí dice que el dígito de control no es correcto.**
El último dígito se calcula con los doce anteriores. Revise que copió bien el código; el mensaje le dice cuál debería ser el último dígito. Si no tiene un código propio, use **Generar EAN13**.

**Dice que el EAN13 ya está asignado a otra variante.**
Cada código de barras identifica una sola variante en la compañía. Búsquelo en el listado de referencias (pegue el código en la búsqueda) para ver cuál lo tiene.

**Calcular precios dejó los precios iguales al costo.**
La compañía no tiene porcentajes de precios configurados. Escriba los precios a mano o pida que se configuren esos porcentajes en la compañía.

**¿Por qué no puedo marcar "Es material" en una referencia comercializada?**
Una referencia comercializada se compra y se vende sin transformarla, así que no puede ser material ni semielaborada. Desmarque *Comercializada* si la referencia se usa en producción.

**¿Qué pasa si desactivo "Liquida IVA"?**
Al guardar se borran los tres impuestos y la marca de IVA incluido. Si la vuelve a activar, debe elegir de nuevo los tres impuestos.

**¿Por qué el código quedó en mayúsculas?**
Los códigos siempre se guardan en mayúsculas para que no haya dos referencias "iguales" escritas distinto (`cam-01` y `CAM-01`).
