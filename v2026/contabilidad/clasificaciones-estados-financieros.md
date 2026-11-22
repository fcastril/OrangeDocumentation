[Regresar a Contabilidad](readme.md)

---

# CLASIFICACIÓN DE ESTADOS FINANCIEROS

## Qué es

Las **clasificaciones** agrupan las cuentas del plan de cuentas en los estados financieros: el **Balance** y el estado de **Pérdidas y ganancias** (P&G). Cada clasificación tiene un código, un tipo, un concepto y un nivel.

Desde aquí consulta, crea, edita y elimina las clasificaciones de su compañía.

## Cómo llegar

- Abra **Contabilidad** en el menú principal y luego **Maestros > Clasificación de estados financieros**.
- Necesita permiso de **Consultar** sobre esta opción. Si no ve la opción, pida a su administrador que se lo asigne.

## Permisos

- **Consultar**: ve el listado y puede buscar, ordenar y paginar.
- **Crear**: ve el botón **Nueva clasificación**.
- **Actualizar**: puede abrir una clasificación, cambiarla y guardarla.
- **Eliminar**: puede eliminar una clasificación.

Si solo tiene **Consultar**, no ve los botones de crear, editar ni eliminar.

## Pantalla principal

La pantalla muestra una tabla con las columnas **Código**, **Tipo**, **Concepto**, **Nivel** y **Última modificación**. La lista llega ordenada por **Concepto**.

- **Buscar**: escriba parte del código, del tipo, del concepto o del nivel. No importan las mayúsculas ni las tildes.
- **Ordenar**: pulse el encabezado de una columna.
- **Páginas**: la tabla se divide en páginas, con controles de abajo.

Estados de la pantalla:

- **Cargando**: mientras se obtiene la lista.
- **Vacío**: la compañía todavía no tiene clasificaciones.
- **Sin resultados**: la búsqueda no encuentra nada. Cambie el texto para buscar de nuevo.
- **Error**: la lista no carga. Pulse **Reintentar**.

## Crear una clasificación

1. Pulse **Nueva clasificación**.
2. Elija el **Tipo**: **P&G (Pérdidas y ganancias)** o **Balance**.
3. Escriba el **Código**, el **Concepto** y el **Nivel**.
4. Pulse **Guardar**.

Reglas de los campos:

- **Código**: obligatorio, hasta 10 caracteres. Se guarda en mayúsculas.
- **Tipo**: obligatorio. Solo hay dos opciones: **P&G (Pérdidas y ganancias)** y **Balance**.
- **Concepto**: obligatorio, hasta 100 caracteres. No admite comas ni punto y coma.
- **Nivel**: obligatorio. Es un número entero de 0 a 9999. Sin decimales.
- El código no puede repetirse en su compañía. Si ya existe, la pantalla no guarda y le indica que el código está en uso.

Si un campo no cumple, la pantalla lo señala y conserva lo que escribió en el diálogo.

## Editar una clasificación

1. Busque la clasificación y pulse **Editar** en su fila.
2. Cambie los datos que necesite.
3. Pulse **Guardar**.

Si cambia el código de una clasificación que ya existía, la pantalla le avisa antes de guardar. Las cuentas del plan se enlazan con la clasificación y no se pierden al cambiar su código.

## Eliminar una clasificación

1. Pulse **Eliminar** en la fila de la clasificación.
2. Revise los datos en el diálogo y confirme.

Si alguna cuenta del plan de cuentas usa la clasificación, no se elimina. La pantalla lo indica y la clasificación sigue en la lista. Para eliminarla, primero cambie esas cuentas a otra clasificación en el [Plan de cuentas](plan-cuentas.md).

## Cambios de otros usuarios en vivo

Si otro usuario crea, cambia o elimina una clasificación, la lista se actualiza sola, la fila cambiada se resalta y aparece un aviso.

## Preguntas frecuentes

**¿Por qué no veo el botón Nueva clasificación?**
Su usuario no tiene permiso para crear. Pida a su administrador que se lo asigne.

**¿Qué diferencia hay entre P&G y Balance?**
**Balance** agrupa las cuentas de la situación financiera. **P&G** agrupa las cuentas del estado de pérdidas y ganancias. Elija el tipo según el estado donde debe aparecer el concepto.

**¿Por qué el nivel no acepta decimales?**
El nivel es un número entero, de 0 a 9999.

**¿Por qué no puedo eliminar una clasificación?**
Hay cuentas del plan de cuentas que la usan. Cámbielas a otra clasificación y vuelva a intentarlo.

**¿Por qué una clasificación con otro tipo aparece en la lista?**
Las clasificaciones que ya existían se muestran como están guardadas. Puede editarlas para elegir uno de los dos tipos.
