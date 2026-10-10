[Regresar a Inventarios](../readme.md)

---

# 🔄 Rotación de Inventarios

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Consultas%2FReportes-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Rotaci%C3%B3n%20de%20Inventarios-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

---

## 📋 Descripción

Esta consulta responde una pregunta: **¿qué tan rápido se mueve cada referencia?** Para cada referencia muestra cuánto se consumió en un periodo, cuánto inventario tuvo en promedio y, a partir de eso, la **rotación**, los **días de inventario** (cuántos días alcanza el inventario al ritmo de consumo del periodo), la **cobertura** y una **clasificación**: Alta, Media, Baja, Sin rotación u Obsoleto.

Es de **solo lectura**: no crea ni cambia información. Puede **consultar, buscar, ver los movimientos de cada referencia, exportar a Excel y exportar a PDF**.

> ℹ️ **Esta consulta es nueva en V2026.** El sistema anterior no tiene un informe de rotación, de días de inventario ni de cobertura. Las fórmulas y los criterios de esta página son los del sistema actual.

> 📘 La paginación, los botones de tabla y la ayuda funcionan como en las demás tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Cada pestaña del navegador trabaja con **una compañía**. El nombre de la compañía se ve en la barra superior.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Inventarios**.
2. En **Consultas/Reportes**, haga clic en **Rotación de Inventarios**.

Permisos de la opción:

| Permiso | Qué permite |
|---------|-------------|
| **Consultar** | Ver la pantalla, consultar la rotación, ver las cifras y abrir el detalle de movimientos de cada referencia. Sin este permiso la pantalla muestra "No tienes acceso a esta consulta". |
| **Exportar** | Ver los botones **Exportar Excel** y **Exportar PDF**. Sin este permiso los botones no aparecen. |

> 🔗 El enlace **Abrir en Kardex** del detalle de movimientos necesita, además, el permiso **Consultar** sobre la opción **Kardex de Inventarios**. Si no lo tiene, el enlace no aparece.

---

## 🖥️ Pantalla principal

Al entrar, la pantalla no muestra datos. Elija los filtros y pulse **Consultar**: la consulta no se ejecuta sola ni al cambiar un filtro.

![Pantalla inicial](../recursos/img/rotacion-inventarios/01-inicial.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral, sin salir de la consulta. |
| **Rotación del … al …** | El periodo al que corresponde lo que está viendo y su número de días. |
| **Información con corte al …** | La fecha de los datos. |
| **Calculado a las HH:MM** | La hora en que se calculó el resultado que ve. Los movimientos registrados después de esa hora no aparecen hasta que pulse **Actualizar**. |
| **Actualizar** | Descarta el cálculo guardado y lo vuelve a ejecutar con los movimientos registrados hasta ahora. Está deshabilitado mientras no haya resultado o mientras se calcula. |
| **Exportar Excel** / **Exportar PDF** | Descargan lo que cumple los filtros, los umbrales, la búsqueda y el orden de la pantalla. Están deshabilitados mientras no haya resultados. |
| **Filtros** | Ver *Cómo consultar*. |
| **Umbrales de clasificación** | Panel plegable para cambiar los días que separan Alta, Media y Baja. Ver *Clasificación y umbrales*. |
| **KPIs** | Cuatro cifras del periodo completo: rotación global, días de inventario global, inventario promedio y consumo. Debajo, cuántas referencias hay en cada clasificación. |
| **Buscar referencia, grupo o subgrupo** | Filtra la tabla mientras escribe. Ver *Leer la tabla*. |
| **Tabla** | Una fila por referencia, agrupada por grupo. |

![Resultado con KPIs y tabla](../recursos/img/rotacion-inventarios/02-resultado.png)

El botón **?** abre este manual sin salir de la consulta:

![Ayuda en el panel lateral](../recursos/img/rotacion-inventarios/17-ayuda.png)

---

## 🔎 Cómo consultar

Los filtros son:

| Filtro | Qué hace |
|--------|----------|
| **Fecha inicial** y **Fecha final** | El periodo. Por defecto son los **12 meses terminados ayer**. La fecha final no puede ser futura y el periodo no puede superar **12 meses**. |
| **Bodegas** | Escriba para buscar por código o nombre y marque una o varias (hasta 50). Vacío significa **todas las bodegas**. |
| **Grupo** y **Subgrupo** | Limitan las referencias. El subgrupo solo se activa después de elegir un grupo. Vacío significa **todos**. |
| **Referencia** | Opcional. Escriba para buscar por código o nombre. También encuentra las referencias inactivas, marcadas "(inactiva)". |
| **Clasificación** | Muestra solo las clases que elija (Alta, Media, Baja, Sin rotación, Obsoleto). Vacío significa **todas**. |
| **Incluir sin consumo** | Activado por defecto. Muestra las referencias que tienen existencia pero no tuvieron consumo en el periodo. Son las candidatas a obsoletas. |
| **Ocultar sin existencia ni consumo** | Activado por defecto. Oculta las referencias que no tienen existencia ni consumo. |
| **Consultar** | Trae el resultado con los filtros elegidos. |

![Filtros](../recursos/img/rotacion-inventarios/03-filtros.png)

### Fechas que no se aceptan

El campo marca el error y no se consulta cuando:

- Falta la fecha inicial: "Elige una fecha inicial".
- La fecha final es futura: "Elige una fecha final que no sea futura".
- La fecha inicial es posterior a la final: "La fecha inicial no puede ser posterior a la final".
- El periodo supera 12 meses: "El periodo no puede superar 12 meses". Divida la consulta en periodos más cortos.

![Fecha inválida](../recursos/img/rotacion-inventarios/14-fecha-invalida.png)

### Bodegas

Con una o varias bodegas elegidas verá solo los movimientos de esas bodegas. Hay una limitación importante: **el sistema no conoce el inventario inicial por bodega**. Por eso, con bodegas filtradas, el inventario promedio parte del movimiento neto de esas bodegas desde cero, y la pantalla lo avisa con este mensaje:

> "Bodegas filtradas: el inventario inicial no se conoce por bodega; el inventario promedio parte del movimiento neto de las bodegas elegidas."

![Bodegas filtradas](../recursos/img/rotacion-inventarios/07-bodegas-filtradas.png)

Para ver la rotación de la referencia completa, deje las bodegas vacías. Para ver cuánto hay en cada bodega, use [Inventario por bodega](inventario-por-bodega.md).

---

## 📊 Leer los indicadores

Los KPIs resumen todo el periodo y todas las referencias que cumplen los filtros:

| KPI | Qué es |
|-----|--------|
| **Rotación global** | Consumo en pesos ÷ inventario promedio en pesos. Cuántas veces se "renovó" el inventario en el periodo. |
| **Días de inventario** | Cuántos días alcanza el inventario al ritmo de consumo del periodo. |
| **Inventario promedio** | Valor promedio del inventario en el periodo, en pesos. |
| **Consumo** | Valor de las salidas que cuentan como consumo, en pesos. |

Debajo de los KPIs verá cuántas referencias hay en cada clasificación. Cada clasificación aparece con su **nombre**, no solo con un color.

![KPIs y conteo por clasificación](../recursos/img/rotacion-inventarios/04-kpis.png)

En la parte superior de la pantalla aparece también la línea **Cuenta como consumo**, con los tipos de movimiento que el sistema toma como consumo en esta consulta (ver *Qué cuenta como consumo*).

---

## 📑 Leer la tabla

![Tabla agrupada por grupo](../recursos/img/rotacion-inventarios/05-grupos.png)

La tabla tiene **una fila por referencia**, agrupada por grupo:

1. **Encabezado de grupo** (fila gris): por ejemplo, "GRUPO: CAM - Camisetas". Si el grupo continúa en la página siguiente, aparece con la marca **(continúa)**.
2. **Renglones**: una referencia por línea, con estas columnas:

| Columna | Qué significa |
|---------|---------------|
| **Referencia** | Código y nombre. |
| **Subgrupo**, **UM** | Subgrupo y unidad de medida. |
| **Existencia inicial** y **Existencia final** | Existencia al inicio y al final del periodo, en unidades. |
| **Inv. promedio** e **Inv. promedio ($)** | Inventario promedio, en unidades y en pesos. |
| **Consumo** y **Consumo ($)** | Consumo del periodo, en unidades y en pesos. |
| **Rotación ($)** y **Rotación (U)** | Rotación calculada con pesos y con unidades. El valor en pesos es el principal. |
| **DIO (días)** | Días de inventario. Pase el mouse sobre el encabezado para ver la fórmula. |
| **Cobertura (días)** | Cuántos días alcanzaría la existencia final al ritmo de consumo del periodo. |
| **Clasificación** | Alta, Media, Baja, Sin rotación, Obsoleto o Sin movimiento. |
| **Acciones** | El botón **Ver movimientos**. |

3. **TOTAL GRUPO** (fila gris): al final de cada grupo, con el número de referencias y los totales del grupo.
4. **TOTAL GENERAL** (fila gris): es la última fila de la última página y suma todas las referencias del filtro.

![Total de grupo y total general](../recursos/img/rotacion-inventarios/06-total-general.png)

Algunas precisiones:

- **Valores vacíos:** cuando no se puede calcular (por ejemplo, la referencia no tuvo consumo), la celda muestra **—**.
- **Negativos:** se muestran con el signo **−**.
- **Totales:** los totales de grupo y el general se calculan sobre **todas** las referencias del filtro, no solo sobre la página que ve. Si el grupo continúa en otra página, su total aparece al final de esa última página.
- **Totales en unidades:** las cantidades (U) suman unidades de medida distintas (unidades, metros, kilos…). Para comparar valores use las columnas en **pesos**.
- **Orden:** por defecto, la tabla va de mayor a menor **DIO**: las referencias más lentas aparecen primero. Puede ordenar por Referencia, Inv. promedio ($), Consumo ($), Rotación ($), DIO y Cobertura. El orden se aplica dentro de cada grupo.
- **Búsqueda:** escriba al menos 2 caracteres. La búsqueda encuentra por código o nombre de la referencia, grupo o subgrupo, sin distinguir mayúsculas ni tildes.

![Búsqueda](../recursos/img/rotacion-inventarios/08-busqueda.png)

Si nada coincide verá "Sin resultados para «…»" con el botón **Limpiar búsqueda**.

### Páginas

Puede elegir 10, 25, 50 o 100 filas por página (25 por defecto). El conteo ("1–25 de 120") cuenta solo las referencias; las filas grises no cuentan.

---

## 🧭 Clasificación y umbrales

Cada referencia se clasifica según sus **días de inventario**:

| Clasificación | Regla |
|---------------|-------|
| **Alta** | Días de inventario hasta **30**. Se vende o se consume rápido. |
| **Media** | De 31 a **90** días. |
| **Baja** | De 91 a **180** días. Si el DIO supera 180 pero hubo consumo, sigue como Baja. |
| **Sin rotación** | Tiene existencia al final del periodo y **no tuvo consumo**. |
| **Obsoleto** | Sin rotación y **sin ningún movimiento** (ni entradas ni salidas) en el periodo, y el periodo tiene al menos **365 días**. Con un periodo más corto, la referencia aparece como Sin rotación, porque los datos no alcanzan para afirmar que es obsoleta. |
| **Sin movimiento** | No tiene existencia ni consumo. No se clasifica. Se oculta con el filtro **Ocultar sin existencia ni consumo**. |

Si el inventario promedio es cero o negativo y hubo consumo, la rotación no se puede calcular (aparece **—**) y la referencia se clasifica como **Alta**, porque se agotó.

### Cambiar los umbrales

Los días de corte (30, 90 y 180 por defecto) se pueden cambiar en el panel **Umbrales de clasificación**:

![Panel de umbrales](../recursos/img/rotacion-inventarios/09-umbrales.png)

1. Escriba los nuevos días en **Alta hasta**, **Media hasta** y **Baja hasta**.
2. Pulse **Consultar**.

Reglas:

- Cada umbral debe ser mayor que el anterior y ninguno puede superar **3650 días**. Si no se cumple, aparece "Cada umbral debe ser mayor que el anterior (máximo 3650 días)" y no se consulta.
- **Restablecer** vuelve a los valores por defecto.
- Los umbrales **se usan solo en esa consulta** y en los archivos que exporte. **No se guardan** para la compañía: al volver a entrar, la pantalla usa los valores por defecto.

---

## 🧾 Ver movimientos de una referencia

Con el botón **Ver movimientos** de una fila se abre un panel lateral con el detalle de esa referencia en el periodo y en las bodegas elegidas.

![Panel Ver movimientos](../recursos/img/rotacion-inventarios/10-movimientos.png)

- **Cifras de la fila**: consumo, inventario promedio, rotación, DIO y clasificación, iguales a los de la tabla.
- **Suma de verificación**: "Suma de los renglones que cuentan como consumo (salidas − entradas)". Esa suma debe coincidir con el consumo de la fila. Así puede revisar cómo se llegó a la cifra.
- **Tabla de movimientos**: fecha, tipo, documento, tercero, bodega, entradas, salidas (en unidades y en pesos), costo, **¿Cuenta como consumo?** y **saldo de la bodega**. Se ordenan por fecha. Son 25 renglones por página.

### ¿Cuenta como consumo?

Cada renglón dice **Sí** o **No**, con el motivo cuando no cuenta:

| Motivo que se muestra | Qué significa |
|-----------------------|---------------|
| **Sí** | Cuenta como consumo. |
| **No — Traslado entre bodegas** | Pasa mercancía de una bodega a otra. La compañía no la consume. Aparece como dos renglones: salida en la bodega de origen y entrada en la de destino. |
| **No — Ajuste de inventario** | Corrección de un inventario físico o de un ajuste. |
| **No — Compra o devolución a proveedor** | Entrada por compra o salida por devolución al proveedor. |
| **No — Entrada o salida manual sin orden de producción** | Movimiento manual que no viene de una orden de producción. |
| **No — Tipo que no es de consumo** | Otros tipos de movimiento, por ejemplo la entrada de productos terminados por producción. |

![Renglones con y sin consumo](../recursos/img/rotacion-inventarios/11-consumo-si-no.png)

La columna **Saldo de la bodega** muestra cuánto suma esa bodega desde cero en el periodo, después de cada renglón. Con bodegas filtradas, esa cifra también se calcula desde cero.

### Abrir en Kardex

El enlace **Abrir en Kardex** lleva al [Kardex de Inventarios](kardex-inventarios.md) con la misma referencia y el mismo periodo, para ver cada movimiento con su existencia corrida. Aparece solo si tiene permiso para el Kardex.

---

## ⏳ Cálculo en segundo plano

Para calcular la rotación el sistema revisa el historial de movimientos. En compañías pequeñas el resultado aparece de inmediato. En compañías **grandes** el cálculo puede tardar **varios minutos**:

1. Al pulsar **Consultar** verá "Calculando la rotación del … al …; puede tardar varios minutos" y el aviso "Te avisaremos en la campana cuando termine; puedes seguir trabajando".
2. Mientras tanto, los filtros siguen visibles, pero **Consultar** y **Actualizar** quedan deshabilitados.
3. Puede **seguir trabajando** en otras pantallas. Cuando termine, recibirá en la **campana** el aviso **"Rotación lista"**, con un enlace a la pantalla. Si el cálculo falla, el aviso lo indica y puede intentarlo de nuevo.
4. Al terminar, la pantalla se llena sola y la banda muestra **Calculado a las HH:MM**.

![Calculando en segundo plano](../recursos/img/rotacion-inventarios/12-calculando.png)

Una vez calculado, el resultado se conserva unos **15 minutos**: cambiar de página, buscar, abrir movimientos o exportar es inmediato. Si pasa ese tiempo, o si el servicio se reinició, la pantalla **vuelve a calcular sola** y la banda muestra la hora nueva.

Para incluir los movimientos registrados **después** de la hora de la banda, pulse **Actualizar**. Puede volver a tardar varios minutos en compañías grandes.

![Calculado a las HH:MM y Actualizar](../recursos/img/rotacion-inventarios/13-calculado-actualizar.png)

Si el panel **Ver movimientos** está abierto cuando se actualiza el resultado, el panel se cierra y debe abrirlo de nuevo.

### Mensajes de error

| Mensaje | Qué hacer |
|---------|-----------|
| **El resultado es demasiado grande**: "Supera las {máximo} filas. Acorta el periodo o elige un grupo." | Acorte el periodo o filtre por grupo y consulte de nuevo. Repetir la misma consulta daría el mismo resultado, por eso no hay botón **Reintentar**. |
| **La rotación no está disponible por ahora**: "La fuente de datos no está disponible. Inténtalo más tarde." | Pulse **Reintentar** más tarde. Si sigue igual, avise a soporte. |
| **No se pudo cargar la rotación**: "Tus filtros se conservan; inténtalo de nuevo." | Pulse **Reintentar**. Sus filtros no se pierden. |
| **El cálculo ya no está vigente** (en el panel de movimientos) | Cierre el panel y pulse **Consultar**. |

![Resultado demasiado grande](../recursos/img/rotacion-inventarios/16-demasiado-grande.png)

---

## 📤 Exportar a Excel y a PDF

Los botones **Exportar Excel** y **Exportar PDF** (solo con permiso **Exportar**) descargan un archivo con **los mismos filtros, los mismos umbrales, la misma búsqueda y el mismo orden** que tiene en pantalla, y **todas las filas** (no solo la página visible).

![Exportando](../recursos/img/rotacion-inventarios/14b-exportando.png)

- **Encabezado:** datos de la compañía, el título, el periodo, las bodegas, el grupo, el subgrupo, la referencia, las clasificaciones, los umbrales usados, los tipos que cuentan como consumo, la búsqueda, la fecha y hora de generación y el usuario que lo generó.
- **Contenido:** las mismas columnas de la pantalla, agrupadas por grupo, con la fila **TOTAL GRUPO** y la fila **TOTAL GENERAL**. En Excel los números quedan como números, listos para sumar o filtrar. El PDF sale en hoja horizontal, con un ancho pensado para que se imprima completo en papel carta y también en oficio, y numera las páginas.
- **Nombre del archivo:** `rotacion-inventarios_` seguido de la fecha inicial y la fecha final, por ejemplo `rotacion-inventarios_2025-10-10_2026-10-09.xlsx` o `.pdf`.

| Formato | Máximo de filas |
|---------|-----------------|
| **Excel** | 50.000 |
| **PDF** | 4.000 |

Si supera el máximo, verá "El resultado supera las {máximo} filas del Excel. Acota el periodo o filtra por grupo." (o el mensaje equivalente del PDF, que sugiere exportar a Excel). Acote los filtros y vuelva a exportar.

Mientras se genera el archivo aparece "Generando el archivo…" y el botón queda ocupado. Si algo falla, el mensaje pide intentar de nuevo; sus filtros no se pierden.

---

## ⚠️ Datos de origen incompletos

La información viene de los movimientos registrados en el sistema, y algunos registros están **incompletos**:

- Las líneas de documento a las que les falta información (tercero, atributos o grupo de la referencia) **no entran** en el consumo.
- Los movimientos con fecha vacía (**01/01/0001**) no pertenecen a ningún periodo, así que **no entran**.

Por eso, la existencia inicial o final puede **no cuadrar al centavo** con la suma de lo que ve. La diferencia suele ser pequeña. El pie de la tabla lo advierte. Si necesita revisar un caso, avise a soporte con la referencia y el periodo.

El costo que usa esta consulta viene de la misma fuente que el [Kardex de Inventarios](kardex-inventarios.md), así que puede tener pequeñas diferencias de redondeo con esa consulta.

---

## 🧮 Qué cuenta como consumo

Solo cuentan como consumo las salidas de estos tipos de movimiento:

- **Ventas**.
- **Remisiones**.
- **Punto de venta**. Las devoluciones de venta restan.
- **Descarga de insumos de una orden de producción**: salidas de materia prima o insumos ligados a una orden de producción.

**No cuentan como consumo:** traslados entre bodegas, ajustes de inventario, inventario físico, compras y devoluciones a proveedor, entradas y salidas manuales sin orden de producción, y la **entrada de productos terminados por producción**. Esa entrada aumenta el inventario, no lo consume.

En el encabezado de la pantalla aparece la línea **Cuenta como consumo** con los tipos que se aplicaron. En el panel **Ver movimientos** cada renglón indica si cuenta y por qué.

> ℹ️ La lista de tipos que cuentan como consumo la define el sistema. Esta pantalla no permite cambiarla.

---

## 📐 Cómo se calcula

Para un periodo, por cada referencia:

1. **Consumo** = salidas que cuentan como consumo − entradas de esos mismos tipos (las devoluciones restan). Se calcula en unidades y en pesos.
2. **Inventario promedio** = promedio de los saldos al inicio del periodo y al final de cada mes del periodo. Por ejemplo, un periodo de tres meses tiene cuatro saldos: el inicial y los tres finales.
3. **Rotación** = consumo ÷ inventario promedio. Se muestra en pesos (principal) y en unidades.
4. **Días de inventario (DIO)** = días del periodo ÷ rotación. Si la rotación es cero, no hay DIO.
5. **Cobertura (días)** = existencia final ÷ (consumo en unidades ÷ días del periodo). Si no hubo consumo, no hay cobertura.

### Ejemplo con cifras ficticias

Referencia **CAM-001 Camiseta básica** (ejemplo), periodo de **90 días**:

| Paso | Cálculo | Resultado |
|------|---------|-----------|
| Consumo ($) | Salidas por venta en el periodo | **3.000.000** |
| Inventario promedio ($) | Saldos al inicio (800.000), al final del mes 1 (1.200.000), del mes 2 (1.000.000) y del mes 3 (1.000.000): (800.000 + 1.200.000 + 1.000.000 + 1.000.000) ÷ 4 | **1.000.000** |
| Rotación ($) | 3.000.000 ÷ 1.000.000 | **3,00** |
| DIO | 90 días ÷ 3,00 | **30 días** |
| Clasificación | 30 días está en el rango de Alta (hasta 30) | **Alta** |

Cobertura de la misma referencia: consumo de **300** unidades en 90 días y existencia final de **100** unidades.

- Consumo diario = 300 ÷ 90 = 3,33 unidades por día.
- Cobertura = 100 ÷ 3,33 = **30 días**. Con el ritmo del periodo, el inventario alcanza para 30 días más.

---

## 📖 Glosario

| Término | Significado |
|---------|-------------|
| **Consumo** | Salidas de los tipos que cuentan como consumo, menos las entradas de esos mismos tipos. |
| **Existencia inicial / final** | Lo que hay de la referencia al inicio y al final del periodo. |
| **Inventario promedio** | Promedio de los saldos al inicio y al final de cada mes. |
| **Rotación** | Cuántas veces el inventario se consumió en el periodo (consumo ÷ inventario promedio). Más alta, más rápido se mueve. |
| **DIO (días de inventario)** | Días que alcanzaría el inventario al ritmo del periodo. Más bajo, más rápido se mueve. |
| **Cobertura** | Días que alcanzaría la existencia final al ritmo de consumo del periodo. |
| **Clasificación** | Alta, Media, Baja, Sin rotación, Obsoleto o Sin movimiento, según los días de inventario y los umbrales. |
| **Umbral** | Días que separan una clasificación de la siguiente. Se cambian solo para la consulta actual. |
| **Renglón** | Cada línea de movimiento de la referencia en el panel **Ver movimientos**. |

---

## ❓ Preguntas frecuentes

**¿Por qué la rotación no aparece (muestra —)?** La referencia no tuvo consumo en el periodo, o su inventario promedio es cero. Si hubo consumo y el inventario promedio es cero, la referencia aparece como Alta.

**¿Por qué una referencia que sé que se movió no aparece?** Probablemente la oculta el filtro **Ocultar sin existencia ni consumo**, porque no tiene existencia ni consumo en el periodo. Desactívelo para verla.

**¿Por qué una referencia dice Sin rotación y no Obsoleta, si no se ha movido?** Con un periodo menor de 365 días, los datos no alcanzan para afirmar que es obsoleta. Consulte un periodo de al menos un año.

**¿Por qué el consumo no coincide con mis ventas?** El consumo solo cuenta los tipos de la lista de la pantalla y resta las devoluciones. Revise el panel **Ver movimientos** para ver qué renglones cuentan y cuáles no.

**¿Por qué las cifras cambian si consulto de nuevo?** Porque hubo movimientos nuevos o porque el resultado guardado venció. Pulse **Actualizar** para recalcular con los movimientos registrados hasta ahora.

**¿Por qué no puedo consultar más de 12 meses?** Para que la consulta responda en un tiempo razonable. Divida el periodo en partes de hasta 12 meses.

**¿Por qué dice "Calculando…" y tarda?** Su compañía tiene mucho historial. Puede seguir trabajando: la campana le avisará con "Rotación lista".

**¿Por qué no veo los botones de exportar?** Su usuario no tiene el permiso **Exportar** en esta opción. Pídalo al administrador.

**¿Por qué no veo el enlace "Abrir en Kardex"?** Su usuario no tiene permiso para el Kardex de Inventarios.

**¿Puedo guardar mis umbrales para la próxima vez?** No. Los umbrales se usan solo en la consulta actual y en los archivos que exporte.

**¿Este informe existe en el sistema anterior?** No. La rotación de inventarios, los días de inventario y la cobertura son nuevos en V2026.

---

## 📸 Capturas pendientes

<!--
Capturas pendientes (tomar desde las stories de Storybook, PNG, ancho máximo 800 px, peso máximo 500 KB).
Carpeta: v2026/inventarios/recursos/img/rotacion-inventarios/

- 01-inicial.png: pantalla inicial, "Elige los filtros y pulsa Consultar" (story Consulta/Inicial).
- 02-resultado.png: banda, KPIs y tabla con grupos (story Consulta/ConDatos).
- 03-filtros.png: filtros completos (Consulta/ConDatos).
- 04-kpis.png: KPIs y conteo por clasificación (Consulta/KpisYFormulas).
- 05-grupos.png: encabezado de grupo, renglones y TOTAL GRUPO (Consulta/FiltroGrupoYClase).
- 06-total-general.png: última página con TOTAL GENERAL (Consulta/ConDatos).
- 07-bodegas-filtradas.png: banda de advertencia con bodegas filtradas (Consulta/BodegasFiltradas).
- 08-busqueda.png: búsqueda con resultados (Consulta/Busqueda).
- 09-umbrales.png: panel de umbrales abierto (Consulta/UmbralesPropios).
- 10-movimientos.png: panel Ver movimientos con cifras de la fila (Movimientos/AbrirPanel).
- 11-consumo-si-no.png: renglones con Sí y No con motivo (Movimientos/ConExclusiones).
- 12-calculando.png: estado calculando (Estados/Calculando).
- 13-calculado-actualizar.png: banda Calculado a las HH:MM y Actualizar (Estados/CalculadoYActualizar).
- 14-fecha-invalida.png: error de fecha (Estados/FechaInvalida).
- 14b-exportando.png: exportando a Excel (Estados/ExportandoExcel).
- 16-demasiado-grande.png: resultado demasiado grande (Estados/ResultadoDemasiadoGrande).
- 17-ayuda.png: panel de ayuda abierto (Ayuda/Ayuda abierta).
-->

---

[Regresar a Inventarios](../readme.md)
