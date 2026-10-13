[Regresar a Inventarios](../readme.md)

---

# 📊 Lista de Precios

![Static Badge](https://img.shields.io/badge/Tipo-Consulta-red)
![Static Badge](https://img.shields.io/badge/Module-Inventarios-orange)
![Static Badge](https://img.shields.io/badge/Submodule-Consultas%2FReportes-blue)
![Static Badge](https://img.shields.io/badge/Opcion-Lista%20de%20Precios-green)
![Static Badge](https://img.shields.io/badge/Version-V2026-purple)

![Static Badge](https://img.shields.io/badge/Actualizacion-20261006-yellow)

---

## 📋 Descripción

Esta consulta muestra **todos los precios de venta de las referencias** que coinciden con la búsqueda. Es de **solo lectura**: no crea ni cambia información. Para cada variante de una referencia ve los cinco precios (Precio 1 a Precio 5). Puede **consultar, buscar, ver solo activas o incluir inactivas, y exportar a Excel**.

> 📘 El orden, la paginación y la ayuda funcionan como en las demás tablas: ver [Manejo general de la información](../../Generales/manejo-general-informacion.md).

> 💡 Cada pestaña del navegador trabaja con **una compañía**. El nombre de la compañía se ve en la barra superior.

---

## 🎯 Acceso

1. En el menú principal, haga clic en **Inventarios**.
2. En **Consultas/Reportes**, haga clic en **Lista de Precios**.

Permisos de la opción:

| Permiso | Qué permite |
|---------|-------------|
| **Consultar** | Ver la pantalla y consultar. Sin este permiso la pantalla muestra "No tienes acceso a esta consulta". |
| **Exportar** | Ver el botón **Exportar Excel**. Sin este permiso el botón no aparece. |

---

## 🖥️ Pantalla principal

Al entrar, la pantalla no muestra datos: escriba al menos **3 caracteres** en el cuadro de búsqueda y pulse **Consultar** (o presione **Enter**).

![Pantalla inicial](../recursos/img/lista-precios/01-inicial.png)

| Elemento | Para qué sirve |
|----------|----------------|
| **?** (junto al título) | Abre esta ayuda en un panel lateral. |
| **Buscar…** | Escriba código, EAN, nombre o variantes (mínimo 3 caracteres). La búsqueda se ejecuta al pulsar **Consultar** o **Enter**. El texto se conserva cuando consulta. |
| **Solo activas** | Por defecto está **encendido**. Si lo apaga, verá también las referencias inactivas con etiqueta "Inactiva". |
| **Consultar** | Trae el resultado con el texto de búsqueda. |

Si escribe menos de 3 caracteres, el botón **Consultar** está deshabilitado y la pantalla muestra "Escriba al menos 3 caracteres".

---

## 🔎 Leer el resultado

![Resultado con precios](../recursos/img/lista-precios/02-resultado.png)

1. **Aviso de truncado:** si la búsqueda coincide con más de 50 variantes, la pantalla muestra "Se mostraron los primeros 50 resultados" en rojo. Afine la búsqueda para ver otros resultados.

2. **Tabla:** Reference, Nombre, Atributo principal, Atributo secundario, Estado (Activa/Inactiva), Precio 1, Precio 2, Precio 3, Precio 4 y Precio 5. Puede elegir 10, 25, 50 o 100 filas por página.

3. **En el celular:** la tabla se convierte en tarjetas; cada tarjeta tiene la referencia, el nombre, los atributos y los precios apilados.

![Vista en el celular](../recursos/img/lista-precios/03-movil.png)

4. **Inactivas:** si apaga **Solo activas**, las referencias inactivas aparecen con una etiqueta **Inactiva** en gris.

Si no hay referencias que coincidan, la pantalla dice "Sin resultados para «…»"; pruebe con un texto diferente.

---

## 🔍 Tipos de búsqueda

Escriba cualquiera de estos datos de la referencia o la variante. La búsqueda es **exacta para códigos** (igualdad completa) **y parcial para nombres y etiquetas**. No distingue mayúsculas ni tildes.

| Qué buscar | Ejemplo | Resultado |
|-----------|---------|-----------|
| **Código de referencia** | `A-001` | Solo esa referencia con todas sus variantes. |
| **Código alterno** | `REF-ALT` | Solo referencias con ese código alterno con todas sus variantes. |
| **EAN-13 o EAN-8** | `5901234123457` | La variante con ese código de barras. |
| **Nombre de referencia** | `camiseta` | Todas las referencias que tengan "camiseta" en el nombre. |
| **Atributo principal** | `rojo` | Todas las variantes cuyo atributo principal (por ejemplo, color) sea "rojo". |
| **Atributo secundario** | `M` | Todas las variantes cuyo atributo secundario (por ejemplo, talla) sea "M". |

Escriba **al menos 3 caracteres**. Parciales más cortas (1–2 caracteres) no se buscan. Si no hay coincidencias, los caracteres no aparecen en ningún campo buscable.

---

## 🏷️ Solo activas o incluir inactivas

El interruptor **Solo activas** controla qué ve:

| Opción | Qué ve |
|--------|--------|
| **Encendido** (por defecto) | Solo referencias activas. Las inactivas no aparecen. |
| **Apagado** | Referencias activas e inactivas. Las inactivas llevan una etiqueta **Inactiva**. |

Cuando cambia el interruptor y consulta de nuevo, la tabla se actualiza. Los precios son los mismos: la actividad es un atributo de la referencia, no del precio.

---

## 💲 Costo: qué NO verá

Esta consulta muestra solo los precios de venta. **No contiene costos** (unitarios o totales): el costo promedio móvil está disponible en el Dashboard gerencial de Inventarios, en Inventarios por Bodega y en el maestro Referencias.

---

## 📤 Exportar a Excel

El botón **Exportar Excel** (solo con permiso **Exportar**) descarga un archivo con la búsqueda, el filtro "Solo activas" usado y **todas las filas** que cumplen (no solo la página visible). El archivo incluye un encabezado con el nombre de la compañía, la fecha de la consulta y los criterios de búsqueda.

Mientras se genera el archivo, el botón aparece ocupado y al terminar se indica el nombre del archivo descargado. Si algo falla, el mensaje pide intentar de nuevo; su búsqueda no se pierde.

---

## ❓ Preguntas frecuentes

**¿Cuántos resultados máximos veo?** 50. Si su búsqueda coincide con más, verá un aviso. Afine el texto para ver otros resultados.

**¿Por qué no aparecen referencias con ese código?** Escriba al menos 3 caracteres. Para un código de 2 caracteres, escriba el código completo (búsqueda exacta en códigos) y con 3 caracteres (para que entre en la búsqueda parcial).

**¿Por qué no veo botones de exportar?** Su usuario no tiene el permiso **Exportar** en esta opción. Pídalo al administrador.

**¿Dónde veo el costo de las referencias?** En el Dashboard gerencial de Inventarios (bajo Inventarios), en Inventarios por Bodega (consulta de saldo y costo) o en el maestro Referencias (pestaña Inventario).

**¿Por qué el interruptor "Solo activas" no filtra en tiempo real?** Porque la búsqueda se ejecuta al pulsar **Consultar** o presionar **Enter**, no al cambiar el interruptor. Primero apague el interruptor y luego consulte de nuevo.

---

[Regresar a Inventarios](../readme.md)
