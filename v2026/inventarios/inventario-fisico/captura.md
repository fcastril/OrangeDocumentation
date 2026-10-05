[Regresar a Inventarios](../readme.md)

---

# 📸 Inventario físico — Captura de conteo

![Static Badge](https://img.shields.io/badge/Tipo-Transaccion-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-InventarioFisico-blue)
![Static Badge](https://img.shields.io/badge/Opcion-313-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261005-yellow)

---

## 📋 Descripción

En esta pantalla registra **lecturas** de un conteo abierto: escanea códigos de barras o de referencia, ingresa cantidades y ve el resumen en tiempo real. Está optimizada para **escáner tipo teclado** (sin app, sin cámara), funciona en el celular, tablet y computadora, y conserva el foco en el campo de código durante toda la captura.

Una **lectura** es un registro de cuántas unidades contó de una variante (talla, color, etc.). Puede registrar la misma variante varias veces: cada escaneo suma una lectura nueva.

> ⚠️ Esta pantalla solo está disponible si el conteo está en estado **Abierto**. Los conteos **Cerrados**, **Ajustados** o **Anulados** pasan a modo consulta sin campos ni eliminar.

---

## 🎯 Acceso

Desde **[Conteos](conteos.md)**:

1. Haga clic en **Capturar** en la fila del conteo (conteo Abierto con permiso de Crear).
2. O haga clic en **Ver** y, si el conteo está Abierto y tiene permiso de Crear, use la acción **Capturar** de la cabecera.

---

## 🖥️ Pantalla principal

<!-- CAPTURA PENDIENTE: story Pantallas/Inventario/Inventario físico/Captura/Captura -->

### Cabecera

| Elemento | Para qué sirve |
|----------|----------------|
| **Volver** | Regresa a Conteos. |
| **Ver detalle** | Abre el [resumen y detalle del conteo](detalle.md) en otra sección (sin perder el progreso de Captura). |
| **Bodega, Fecha, Tipo, Estado** | Información del conteo. Solo lectura. |
| **En vivo** | La pantalla está conectada. Ver *Cambios en vivo*. |
| **Cerrar conteo** | Botón disponible solo si el conteo está Abierto y usted tiene permiso de Actualizar. Ver *Cerrar desde Captura*. |

### Campo de código

| Elemento | Función |
|----------|---------|
| **Código de barras o de referencia** | Campo con el foco permanente. El cursor siempre está aquí después de registrar, de un error, o cuando abre la pantalla. |
| Placeholder | *"Escanea o escribe y pulsa Enter"* |
| Entrada | Acepta: códigos de barras (EAN13, EAN8), códigos de referencia (p. ej., `CAM-001`), y códigos abiertos de 20, 40 o 100 caracteres. Sin mayúsculas ni tildes para resolver. |
| **Enter** | Registra la lectura con la cantidad del campo de cantidad. Si hay una lectura en vuelo (esperando respuesta del servidor), Enter se ignora. |

**Tip de escaneo:** Si usa un escáner físico acoplado al celular, active **Ocultar teclado en pantalla** (ver abajo) para que no tape la pantalla.

### Campo de cantidad

| Elemento | Función |
|----------|---------|
| **Cantidad** | Número decimal hasta 4 decimales (p. ej., `10.5`). |
| Por defecto | 1 (si no escribe nada) |
| Rango válido | Mayor que 0 y hasta 999.999,9999 |
| Cambio | Tras registrar una lectura, vuelve automáticamente a 1. |
| Error | Si la cantidad es 0, negativa, o tiene más de 4 decimales, el servidor rechaza con el aviso *"La cantidad debe ser mayor que cero y no pasar de 999.999,9999."* |

**Corrección de cantidad:** Si registró una cantidad equivocada, **elimine la lectura** (ver *Eliminar lecturas*); no hay forma de restar. El siguiente escaneo suma una lectura nueva.

### Botón "Registrar lectura"

- Disponible para quién usa táctil o prefiere no usar Enter.
- Registra la lectura con el código y la cantidad del campo.
- Mismo efecto que presionar Enter.

### Buscar por nombre (lookup de variantes)

- Busque por nombre de referencia o variante.
- Útil si el código no se escanea bien o no lo tiene a mano.
- Exige **2 o más caracteres**.
- No distingue mayúsculas ni tildes.
- Al elegir una variante, se registra con cantidad 1 (ignora el campo de cantidad).

### Interruptor "Ocultar teclado en pantalla"

- Active si usa un **escáner físico acoplado al celular**.
- Cambia el comportamiento del teclado para que no tape la pantalla.
- El escaneo sigue funcionando igual: Enter lo registra.

---

## 📝 Registrar una lectura — Paso a paso

### Caso normal: escaneo con código resuelto

1. Coloque el foco en el **campo de código** (está ahí por defecto; si hizo clic en otro sitio, haga clic en el campo).
2. Con el escáner, escanee un código (p. ej., EAN13 `7701234567890` o código de referencia `CAM-001`).
3. El servidor resuelve el código a una variante (referencia + talla + color).
4. **Presione Enter** o haga clic en **Registrar lectura**.
5. La lectura aparece en **Últimas lecturas** con el nombre y la cantidad.
6. El campo de código se vacía y el foco regresa al campo (listo para el siguiente escaneo).
7. Los **totales** se actualizan: Lecturas, Variantes y Unidades.

### Caso: código ambiguo (varias variantes)

Si el código corresponde a varias variantes (p. ej., una referencia con 6 combinaciones de talla × color):

1. Tras escanear y presionar Enter, aparece el diálogo **"Elige la variante"**.
2. Se lista hasta 50 candidatos con: código, nombre de referencia, atributos (talla, color), y una marca de **Inactiva** si aplica.
3. Haga clic en la variante que contó.
4. Se registra la lectura con esa variante y la cantidad del campo.
5. El diálogo se cierra, el campo queda vacío y el foco regresa.

**Cancelar la selección:** Presione **Cancelar** o Esc. El código queda seleccionado en el campo; el siguiente escaneo lo reemplaza.

### Caso: código no encontrado

Si el código no existe en la compañía:

1. Aparece el aviso *"Código no encontrado: «...». No se registró ninguna lectura."*
2. El código **queda visible y seleccionado** en el campo.
3. El foco está en el campo.
4. **Su próximo escaneo reemplaza este código.**
5. **Alternativa:** Busque por nombre (lookup) si no tiene el código exacto.

### Caso: cantidad inválida

Si la cantidad es 0, negativa, o tiene más de 4 decimales:

1. Aparece el aviso *"La cantidad debe ser mayor que cero y no pasar de 999.999,9999."*
2. Se explica que *"Para corregir una lectura, elimina la línea; no se resta."*
3. No se crea ninguna lectura.
4. El foco está en el campo de código.

**Corrección:** Elimine la lectura (ver abajo) y escanee de nuevo con la cantidad correcta.

---

## 📋 Últimas lecturas

La sección muestra las **últimas 10 lecturas** registradas (más reciente primero) con:

- Código de referencia
- Nombre de referencia y variante (p. ej., *CAM-001 · Camisa polo · M / Azul*)
- Cantidad
- Botón **Eliminar** (44×44 píxeles, rojo)

---

## 🗑️ Eliminar una lectura

Solo disponible si el conteo está **Abierto** y usted tiene permiso de **Crear**.

1. En **Últimas lecturas**, haga clic en el botón **Eliminar** de la lectura (papelera roja).
2. La lectura se borra al instante (sin confirmación, como especifica el negocio).
3. Aparece el aviso *"Lectura eliminada: [Referencia] [Variante]."*
4. Los **totales** se recalculan.
5. El foco regresa al campo de código.

**No hay deshacer:** Una vez eliminada, la lectura no se recupera (pero puede escanear de nuevo).

> ℹ️ Si el conteo no está Abierto (p. ej., otro usuario lo cerró mientras capturaba), el botón Eliminar no aparece y la pantalla pasa a solo lectura.

---

## 📊 Totales

En la tarjeta **Totales del conteo** ve:

| Total | Significado |
|-------|------------|
| **Lecturas** | Número de líneas registradas (si escanea 2 veces la misma variante, suma 2). |
| **Variantes** | Número de variantes diferentes contadas (si escanea CAM-001 talla M y talla L, son 2 variantes). |
| **Unidades** | Suma de todas las cantidades (si registra CAM-001 × 5 y CAM-001 × 3, suma 8). |

---

## 🔄 Cambios en vivo

Si otro usuario cierra o anula el conteo mientras usted captura:

1. La pantalla **pasa a solo lectura**: desaparecen los campos de código y cantidad, el botón Registrar y el botón Eliminar.
2. Aparece el aviso *"El conteo ya no está abierto. Solo puedes consultarlo. Ábrelo de nuevo desde Conteos si necesitas seguir capturando."*
3. Las lecturas ya registradas siguen visibles.
4. Puede volver a **[Conteos](conteos.md)** para reabrirlo (si tiene permiso de Actualizar).

---

## 🔐 Sin permiso de Crear

Si abre la pantalla pero su perfil no tiene permiso de **Crear** en la opción 313:

1. La pantalla se muestra en solo lectura (sin campos).
2. Aparece el aviso *"No tienes permiso para registrar lecturas: solo puedes consultar."*
3. Puede ver las lecturas que otros registraron, pero no puede agregar nuevas ni eliminar.

---

## 🔴 Cerrar el conteo desde Captura

Cuando termina de capturar:

1. Haga clic en **Cerrar conteo** (botón en la cabecera).
2. Se abre un diálogo que muestra: *"El conteo tiene {{lecturas}} lecturas, {{variantes}} variantes y {{unidades}} unidades."*
3. Se explica: *"Al cerrarlo ya no se podrán registrar ni eliminar lecturas. Podrás reabrirlo mientras no se haya ajustado."*
4. Haga clic en **Cerrar conteo**.

El botón muestra *Procesando…* hasta que el servidor responde. El conteo cambia a estado **Cerrado** y aparece el aviso *"Conteo cerrado. Ya no se pueden registrar lecturas."*

Para más detalles, ver [Conteos — Cerrar un conteo](conteos.md#-cerrar-un-conteo).

---

## ❓ Preguntas frecuentes

**¿Por qué el foco no se queda en el campo de cantidad?**

El diseño deja el foco en el campo de código para que un capturista con escáner no tenga que mover el cursor: escanea, Enter registra, siguiente escaneo. La cantidad es por defecto 1 y se cambia antes de escanear.

**¿Qué pasa si escaneo dos veces la misma variante?**

Se registran dos lecturas diferentes. Cada una suma a los totales. Esto permite contar la misma referencia en varios pasos (p. ej., lotes de 10, 10 y 5). Para restar, debe eliminar la lectura.

**¿Puedo editar una lectura ya registrada?**

No. Elimine la lectura y escanee de nuevo con la cantidad correcta. El servidor registra solo lecturas nuevas; no hay edición.

**¿Funciona offline?**

No. Necesita conexión a internet. Si la conexión se pierde, aparecerá un error y podrá reintentar cuando se reconecte.

**¿Puedo usar esto desde la computadora sin escáner?**

Sí. Puede escribir el código a mano y presionar Enter o hacer clic en **Registrar lectura**. La cantidad por defecto es 1; cambie si es necesario.

**¿Qué significa "Inactiva" en el diálogo de variantes?**

Una referencia marcada como inactiva en el maestro puede seguir teniendo existencias físicas. Se muestra marcada, pero puede seleccionarla normalmente.

**¿Cómo busco una variante si no tengo el código?**

Use el campo **Buscar por nombre**. Escriba parte del nombre de la referencia (p. ej., *camisa*) o del atributo (p. ej., *azul*), presione Enter o espere 2 caracteres, y aparecerá un listado de variantes.

**¿Se pierde todo si cierro la pestaña del navegador?**

Las lecturas que el servidor ya confirmó (que aparecen en **Últimas lecturas**) se guardan. Si cierra antes de registrar, esa lectura se pierde. Pero el conteo sigue abierto, así que puede volver y continuar.

---

## 📍 Siguiente paso

- Vea el **[Resumen y detalle del conteo](detalle.md)** para revisar todas las lecturas agrupadas por variante.
