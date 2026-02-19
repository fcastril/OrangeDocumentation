[Regresar al Inicio](../readme.md)

---

# 🏢 Áreas

> **Tipo:** Maestro Tipo I  
> **Módulo:** Administrativos → Maestros  
> **Última actualización:** Febrero 18, 2026

---

## 📋 Descripción

El módulo de **Áreas** es un [Maestro Tipo I](../../Generales/maestros-tipoI.md) que permite gestionar las diferentes áreas organizacionales de la empresa. Este maestro es fundamental para la correcta estructuración de la información corporativa y se utiliza en múltiples módulos del sistema.

**Ejemplos de uso:**
- Asignación de empleados a áreas específicas en el módulo de Talento Humano
- Clasificación de gastos por área en el módulo de Gastos
- Segmentación de reportes y análisis por área organizacional
- Control de presupuestos por área
- Generación de informes de estructura organizacional

**¿Para qué sirve este maestro?**  
Las áreas permiten organizar la estructura departamental de la empresa, facilitando la administración, distribución de recursos, control presupuestal y generación de reportes segmentados por unidad organizacional.

---

## 🎯 Acceso al Módulo

### Ruta de Navegación

1. Ingresar al sistema Orange.NET con sus credenciales
2. En el menú principal, seleccionar **Administrativos**
3. En el submenú, seleccionar **Maestros**
4. Hacer clic en **Áreas**

![Pantalla principal](../recursos/img/areas/01-principal.png)

---

## 🖥️ Pantalla Principal

La pantalla principal del módulo muestra una tabla interactiva con todas las áreas registradas en el sistema. La interfaz ha sido diseñada con animaciones suaves y feedback visual para mejorar la experiencia del usuario.

### Elementos de la Pantalla

| Elemento | Descripción |
|----------|-------------|
| **Título del Módulo** | Muestra el nombre "Áreas" con su icono correspondiente |
| **Badge "Maestro Tipo I"** | Indica el tipo de maestro (solo Código y Nombre) |
| **Botón de Ayuda** | Enlace a la ayuda contextual del sistema |
| **Botón "Crear Área"** | Permite crear una nueva área (visible solo con permiso de Crear) |
| **Campo de Búsqueda** | Permite buscar áreas en tiempo real (con debounce de 500ms) |
| **Tabla de Datos** | Muestra ID, Código, Nombre y Acciones de cada área |
| **Botones de Acción** | Editar (verde) y Eliminar (rojo) por cada registro |
| **Controles de Paginación** | Navegación entre páginas de resultados |
| **Selector de Cantidad** | Permite elegir cuántos registros ver por página (10, 25, 50, 100) |

---

## ➕ Crear un Nuevo Registro

### Paso a Paso

1. **Acceder al formulario de creación**
   
   Haga clic en el botón **"Crear Área"** ubicado en la parte superior izquierda de la tabla.

   ![Botón Crear](../recursos/img/areas/02-boton-crear.png)

2. **Completar los campos del formulario**

   Se abrirá un formulario con los siguientes campos:

   | Campo | ¿Es obligatorio? | Descripción | Ejemplo | Validaciones |
   |-------|------------------|-------------|---------|--------------|
   | **Código** | ✅ Sí | Código único identificador del área (alfanumérico) | `ADM`, `RRHH`, `TI` | Max. 20 caracteres, se convierte automáticamente a mayúsculas |
   | **Nombre** | ✅ Sí | Nombre descriptivo del área | `Recursos Humanos`, `Tecnología` | Max. 200 caracteres, no permite comas ni punto y coma |

   ![Formulario de creación](../recursos/img/areas/03-crear-registro.png)

   > 💡 **Tip:** El código es el identificador clave del área. Use códigos cortos y memorables (ej: ADM, COM, FIN). El sistema lo convertirá automáticamente a mayúsculas.

3. **Validación automática**

   El sistema valida en tiempo real:
   - ✅ Campos obligatorios completados
   - ✅ Código único (no duplicado)
   - ✅ Longitud máxima respetada
   - ✅ Caracteres no permitidos removidos

4. **Guardar el registro**

   Haga clic en el botón **"Guardar"**. El botón mostrará un indicador de carga mientras procesa:
   
   ```
   🔄 Guardando...
   ```

   Una vez completado con éxito, aparecerá un mensaje de confirmación:

   ![Mensaje de éxito](../recursos/img/areas/05-mensaje-exito.png)

   El sistema lo redirigirá automáticamente a la pantalla principal en 2 segundos.

### ¿Qué puede salir mal?

| Error | Causa | Solución |
|-------|-------|----------|
| "El código es obligatorio" | Campo Código vacío | Complete el campo Código antes de guardar |
| "El nombre es obligatorio" | Campo Nombre vacío | Complete el campo Nombre antes de guardar |
| "Ya existe un área con ese código" | Código duplicado | Use un código diferente y único |
| "Error al comunicarse con el servidor" | Pérdida de conexión o error del servidor | Verifique su conexión a internet y vuelva a intentar |

---

## ✏️ Editar un Registro Existente

### Pasos para Editar

1. **Localizar el área** que desea editar en la tabla principal
   - Use el campo de búsqueda si es necesario
   - Navegue por las páginas usando los controles de paginación

2. **Hacer clic en el botón de Editar** (botón verde con icono de lápiz)

   ![Botón Editar](../recursos/img/areas/06-boton-editar.png)

3. **Modificar los campos** deseados en el formulario

   ![Editar registro](../recursos/img/areas/07-editar-registro.png)

4. **Guardar los cambios** haciendo clic en el botón **"Guardar"**

5. **Confirmar actualización**

   ![Mensaje actualización](../recursos/img/areas/08-mensaje-actualizacion.png)

### ⚠️ Restricciones Importantes

- **No se puede modificar el código** de un área que ya está siendo utilizada en otros módulos (esto podría afectar la integridad de los datos)
- Los cambios en el nombre se reflejarán inmediatamente en todos los módulos que utilizan esta área
- El sistema registra automáticamente quién y cuándo modificó el registro (auditoría)

---

## 🗑️ Eliminar un Registro

### Procedimiento de Eliminación

1. **Localizar el área** que desea eliminar

2. **Hacer clic en el botón Eliminar** (botón rojo con icono de basurero)

   ![Botón Eliminar](../recursos/img/areas/09-boton-eliminar.png)

3. **Confirmar la eliminación** en el diálogo de confirmación

   El sistema mostrará un mensaje con los detalles del área a eliminar:

   ![Confirmar eliminación](../recursos/img/areas/10-confirmar-eliminar.png)

   **⚠️ ADVERTENCIA:** Esta acción no se puede deshacer.

4. **Eliminación exitosa**

   Si la operación es exitosa, verá un mensaje de confirmación:

   ![Área eliminada](../recursos/img/areas/11-mensaje-eliminado.png)

   La tabla se actualizará automáticamente sin recargar la página completa.

### ⛔ ¿Cuándo NO puedo eliminar?

No podrá eliminar un área si:

- **Tiene empleados asignados** en el módulo de Talento Humano
- **Tiene movimientos contables** asociados en Contabilidad
- **Está siendo utilizada** en Presupuestos activos
- **Está referenciada** en Gastos o cualquier otro módulo transaccional

**Solución:** Primero debe reasignar o eliminar todas las referencias a esta área en los demás módulos. El sistema mostrará un mensaje específico indicando dónde está siendo utilizada.

---

## 🔍 Buscar Registros

El módulo de Áreas cuenta con un potente sistema de búsqueda optimizado:

### Características de la Búsqueda

- **Búsqueda en tiempo real** con debounce de 500ms (no sobrecarga el servidor)
- **Búsqueda global:** busca en ID, Código y Nombre simultáneamente
- **Mínimo 3 caracteres** para iniciar búsqueda automática
- **Resaltado de resultados** en la tabla
- **Case-insensitive:** no distingue mayúsculas de minúsculas

![Búsqueda en acción](../recursos/img/areas/12-buscar.png)

### 💡 Tips de Búsqueda

- **Buscar por código:** escriba directamente el código (ej: `ADM`)
- **Buscar por nombre:** escriba parte del nombre (ej: `recursos` encontrará "Recursos Humanos")
- **Buscar por ID:** ingrese el número de identificador
- **Limpiar búsqueda:** borre el campo de búsqueda para ver todos los registros nuevamente

---

## 📊 Funcionalidades de la Tabla

### Selección de Filas

Al hacer clic en una fila, esta se **resalta visualmente** con:
- Color de fondo azul claro (#e3f2fd)
- Borde izquierdo azul de 4px
- Efecto de transición suave

![Fila seleccionada](../recursos/img/areas/13-fila-seleccionada.png)

### Ordenamiento de Columnas

Haga clic en los **encabezados de columna** para ordenar:
- **Un clic:** orden ascendente ▲
- **Dos clics:** orden descendente ▼

Las columnas ordenables son: ID, Código y Nombre.

![Ordenamiento](../recursos/img/areas/15-ordenamiento.png)

### Paginación

Los controles de paginación permiten:
- **Navegar** entre páginas: Anterior, Siguiente, Primera, Última
- **Cambiar cantidad** de registros por página: 10, 25, 50, 100
- **Ver información** de registros mostrados: "Mostrando 1 a 10 de 45 registros"

![Paginación](../recursos/img/areas/14-paginacion.png)

### Animaciones y Efectos Visuales

El módulo incluye:
- ✨ **Animación de entrada** (fadeInUp) al cargar la página
- 🎯 **Hover effects** en filas (elevación con sombra)
- 🎨 **Transiciones suaves** en todos los botones
- 💫 **Indicadores de carga** durante operaciones asíncronas

---

## 🔐 Permisos Requeridos

El módulo de Áreas está protegido por un sistema de permisos granular:

| Acción | Permiso Requerido | Consecuencia si NO tiene el permiso |
|--------|-------------------|-------------------------------------|
| Ver la lista de áreas | **Lectura** | No puede acceder al módulo |
| Crear nueva área | **Crear** | Botón "Crear Área" no visible |
| Editar área existente | **Actualizar** | Botón "Editar" no visible en la tabla |
| Eliminar área | **Eliminar** | Botón "Eliminar" no visible en la tabla |

**Contacte al administrador del sistema** si necesita algún permiso adicional.

---

## ❓ Preguntas Frecuentes

### 1. ¿Cuál es la diferencia entre Código y Nombre de Área?

**R:** El **Código** es un identificador único, corto y alfanumérico (máx. 20 caracteres) usado internamente por el sistema para referencias rápidas. El **Nombre** es descriptivo (máx. 200 caracteres) y es lo que los usuarios ven principalmente. 

**Ejemplo:**
- Código: `RRHH`
- Nombre: `Recursos Humanos y Desarrollo Organizacional`

---

### 2. ¿Puedo tener dos áreas con el mismo nombre pero diferente código?

**R:** Técnicamente sí, el sistema solo valida que el **código sea único**. Sin embargo, **no es recomendable** por razones de claridad organizacional. Si necesita diferenciar áreas similares, use nombres más específicos.

---

### 3. ¿Qué pasa si elimino un área por error?

**R:** La eliminación es **permanente y no se puede deshacer** desde la interfaz. Sin embargo, el sistema mantiene registros de auditoría. Contacte al administrador del sistema quien puede:
- Consultar el log de Application Insights
- Verificar si hay backups disponibles
- Restaurar el registro si es crítico

**Recomendación:** Siempre verifique dos veces antes de confirmar una eliminación.

---

### 4. ¿Por qué no puedo eliminar un área aunque tenga el permiso?

**R:** Aunque tenga el permiso de eliminación, el sistema **protege la integridad referencial**. Si el área está siendo utilizada en:
- Empleados asignados
- Movimientos contables
- Presupuestos
- Cualquier transacción

No podrá eliminarse. El mensaje de error indicará dónde está siendo utilizada. Primero debe reasignar o eliminar esas referencias.

---

### 5. ¿Cuándo debo usar mayúsculas o minúsculas en el código?

**R:** No importa, el sistema **convierte automáticamente el código a MAYÚSCULAS** al guardar. Puede escribir `rrhh`, `Rrhh` o `RRHH` y todos se guardarán como `RRHH`.

---

### 6. ¿Puedo importar áreas desde un archivo Excel?

**R:** Actualmente el módulo no tiene funcionalidad de importación masiva desde la interfaz web. Para cargas masivas, contacte al equipo de soporte técnico que puede:
- Realizar la carga mediante scripts SQL
- Proporcionar una solución personalizada
- Evaluar añadir esta funcionalidad en futuras versiones

---

### 7. ¿Cómo sé quién creó o modificó un área?

**R:** El sistema registra automáticamente:
- Usuario que creó el registro
- Fecha y hora de creación
- Usuario que realizó la última modificación
- Fecha y hora de modificación

Esta información está disponible en:
- Logs del sistema (Application Insights)
- Informes de auditoría
- Solicitar al administrador acceso a estos datos

---

### 8. ¿La búsqueda distingue entre mayúsculas y minúsculas?

**R:** **No**, la búsqueda es **case-insensitive**. Puede buscar `adm`, `Adm` o `ADM` y obtendrá los mismos resultados.

---

### 9. ¿Qué significa el debounce de 500ms en la búsqueda?

**R:** Es una optimización de rendimiento. El sistema **espera 500 milisegundos** después de que deja de escribir antes de realizar la búsqueda. Esto evita:
- Sobrecargar el servidor con búsquedas por cada letra
- Mejorar la experiencia del usuario
- Reducir el consumo de recursos

Solo necesita tres o más caracteres para que la búsqueda se active automáticamente.

---

### 10. ¿Puedo exportar la lista de áreas a Excel o PDF?

**R:** Actualmente esta funcionalidad no está implementada en la interfaz web. Para obtener un reporte de áreas:

**Opción 1 - Screenshot:** Use la tecla `Impr Pant` o herramientas de captura  
**Opción 2 - Reporte formal:** Solicite al departamento de TI un reporte personalizado  
**Opción 3 - Acceso directo a BD:** Si tiene permisos, puede consultar la tabla `Areas` directamente

---

### 11. ¿Por qué el botón Guardar se queda en "Guardando..." y no responde?

**R:** Esto puede deberse a:
- **Pérdida de conexión a internet:** Verifique su conectividad
- **Sesión expirada:** Recargue la página y vuelva a iniciar sesión
- **Error del servidor:** Contacte a soporte técnico

**Solución temporal:** Refresque la página (F5) y verifique si el registro se guardó antes de volver a intentar.

---

### 12. ¿Puedo crear áreas con caracteres especiales o tildes?

**R:** 
- **En el Código:** Solo alfanuméricos (A-Z, 0-9). No se permiten tildes, ñ, ni caracteres especiales.
- **En el Nombre:** Se permiten tildes y ñ. **NO** se permiten comas (,) ni punto y coma (;) ya que pueden interferir con exportaciones CSV.

---

## 📱 Compatibilidad

| Dispositivo | Navegador | Versión Mínima | Estado |
|-------------|-----------|----------------|--------|
| 🖥️ PC Windows | Chrome | 90+ | ✅ Totalmente soportado |
| 🖥️ PC Windows | Edge | 90+ | ✅ Totalmente soportado |
| 🖥️ PC Windows | Firefox | 88+ | ✅ Totalmente soportado |
| 🖥️ PC Windows | Opera | 76+ | ✅ Totalmente soportado |
| 🍎 Mac | Safari | 14+ | ✅ Totalmente soportado |
| 🍎 Mac | Chrome | 90+ | ✅ Totalmente soportado |
| 📱 Móvil/Tablet | Cualquiera | - | ⚠️ Uso limitado (responsive básico) |

**Nota:** Para una experiencia óptima, use navegadores modernos actualizados. Internet Explorer **NO** está soportado.

---

## 🎓 Buenas Prácticas

### Nomenclatura de Códigos

✅ **Recomendado:**

- Usar siglas o acrónimos cortos: `ADM`, `COM`, `FIN`, `RRHH`
- Mantener consistencia: si usa 3 letras, úselo para todas
- Evitar códigos genéricos como `A1`, `A2`, `A3`
- Usar códigos mnemotécnicos (fáciles de recordar)

❌ **Evite:**

- Códigos demasiado largos: `ADMINISTRACION_GENERAL`
- Números consecutivos sin significado: `001`, `002`, `003`
- Mezclar idiomas: `ADM_ADMIN`
- Caracteres especiales: `ADM-01`, `RRHH/2024`

### Organización de Áreas

✅ **Recomendado:**

- Crear una estructura jerárquica clara
- Usar nombres descriptivos pero concisos
- Mantener actualizado (eliminar áreas obsoletas con precaución)
- Documentar cambios importantes en áreas críticas

❌ **Evite:**

- Crear demasiadas áreas sin uso real
- Duplicar áreas con nombres similares
- Usar nombres ambiguos: "Área 1", "Departamento X"
- Eliminar áreas sin verificar dependencias

---

## 🔗 Información Relacionada

### Maestros Relacionados

- [Ciudades](ciudades.md) - Configuración de ubicaciones geográficas
- [Departamentos](departamentos.md) - Divisiones administrativas
- [Zonas](zonas.md) - Segmentación territorial
- [Actividades Económicas](actividades-economicas.md) - Clasificación de actividades

### Movimientos y Procesos Relacionados

- **Talento Humano:** Asignación de empleados a áreas
- **Gastos:** Registro de gastos por área
- **Presupuestos:** Control presupuestal por área
- **Contabilidad:** Centros de costo asociados a áreas
- **Reportes Gerenciales:** Análisis por estructura organizacional

### Documentación General

- [Maestros Tipo I - Guía General](../../Generales/maestros-tipoI.md)
- [Manejo General de Información](../../Generales/manejo-general-informacion.md)

---

## 📞 Soporte Técnico

¿Necesita ayuda adicional con el módulo de Áreas?

**Soporte Orange ERP**

- 📧 **Email:** soporte@orange.net
- 📱 **WhatsApp:** +57 300 123 4567
- ☎️ **Teléfono:** (601) 123 4567
- 🕐 **Horario:** Lunes a Viernes, 8:00 AM - 6:00 PM (hora de Colombia)
- 💬 **Chat en vivo:** Disponible desde el menú de ayuda del sistema

**Canal de soporte por severidad:**

- 🔴 **Crítico** (sistema caído): Llamar directamente
- 🟠 **Alto** (funcionalidad bloqueada): WhatsApp o teléfono
- 🟡 **Medio** (dudas o problemas menores): Email
- 🟢 **Bajo** (consultas generales): Chat en vivo

---

## 📝 Historial de Cambios

| Versión | Fecha | Autor | Cambios |
|---------|-------|-------|---------|
| 2.0 | Feb 18, 2026 | Equipo Orange.NET | Refactorización completa: Application Insights, DataTables, SweetAlert2, JavaScript modular, documentación extendida |
| 1.5 | - | - | Migración a anexGrid personalizado |
| 1.0 | - | - | Versión inicial del módulo |

---

**[⬅️ Volver a Maestros](../readme.md)** | **[🏠 Inicio](../../README.md)**

---

> 📌 **Última revisión:** Febrero 18, 2026  
> 📄 **Documento:** `administrativos/maestros/areas.md`  
> ✍️ **Mantenido por:** Equipo Orange ERP  
> 🔖 **Versión del Sistema:** Orange.NET v2.x  
> 📋 **ID del Módulo:** Opciones.IdOpcion.Areas

---

## 🏷️ Etiquetas

`Maestro` `Maestro Tipo I` `Administrativos` `Áreas` `Estructura Organizacional` `Departamentos` `Gestión Empresarial`
