[Regresar al Inicio](../readme.md)

---

# Referencias

## Copiar Referencias

La funcionalidad de **Copiar Referencias** permite duplicar una referencia existente junto con toda su configuración, facilitando la creación de referencias similares sin tener que configurar cada elemento manualmente.

### Acceso a la Funcionalidad

1. Navegar a **Inventarios > Maestros > Referencias**
2. En el listado de referencias, localizar la referencia que desea copiar
3. En la columna de acciones, hacer clic en el botón azul con ícono de copiar ![icono copiar](../../inventarios/recursos/img/referencias/copiar-referencia.png)

> **Nota:** El botón de copiar solo está disponible para referencias de tipo 'R' (Referencias) y requiere el permiso de **Crear** en el módulo de Referencias.

### Proceso de Copia

#### 1. Abrir Modal de Copia

Al hacer clic en el botón de copiar, se abrirá una ventana modal con los siguientes campos:

| Campo | Descripción | Obligatorio |
|-------|-------------|-------------|
| **Código Referencia Origen** | Código de la referencia que se está copiando (solo lectura) | N/A |
| **Nuevo Código** | Código único para la nueva referencia | Sí |
| **Nuevo Nombre** | Nombre/descripción para la nueva referencia | Sí |

#### 2. Validaciones

- El **Nuevo Código** no puede estar vacío
- El **Nuevo Nombre** no puede estar vacío
- El **Nuevo Código** debe ser único en el sistema

#### 3. Confirmación

Después de ingresar los datos, el sistema mostrará un mensaje de confirmación:

```
¿Está seguro de copiar la referencia [CÓDIGO-ORIGEN]?
Se creará una nueva referencia con código: [NUEVO-CÓDIGO]
```

### Elementos Copiados

Cuando se confirma la copia, el sistema duplica los siguientes elementos:

- ✅ **Atributos de Movimiento** - Todos los pares de atributos principal/secundario configurados
- ✅ **Materiales** - Referencias de materiales asociados con sus propiedades
- ✅ **Proveedores** - Lista de proveedores con códigos y precios
- ✅ **Consumos** - Materiales y cantidades necesarias para producción
- ✅ **Operaciones** - Procesos de fabricación con tiempos y secuencias
- ✅ **Consumos por Atributos** - Consumos específicos según combinación de atributos

### Resultado de la Copia

Al finalizar el proceso exitosamente:

1. Se muestra un mensaje con el resumen de la operación:
   ```
   Referencia copiada exitosamente
   
   • Total de registros copiados: [X]
   • Atributos de movimiento: [X]
   • Materiales: [X]
   • Proveedores: [X]
   • Consumos: [X]
   • Operaciones: [X]
   • Consumos por atributos: [X]
   ```

2. El sistema redirige automáticamente a la página de **Crear/Editar** de la nueva referencia creada, permitiendo realizar ajustes adicionales si es necesario.

### Casos de Uso

Esta funcionalidad es especialmente útil en los siguientes escenarios:

- **Referencias Similares:** Crear variantes de un producto con estructuras parecidas
- **Nuevas Líneas de Producto:** Iniciar una nueva línea basándose en productos existentes
- **Versiones de Referencias:** Crear nuevas versiones manteniendo la configuración base
- **Migración de Configuraciones:** Replicar estructuras probadas hacia nuevos productos

### Consideraciones Importantes

⚠️ **Permisos:** Se requiere el permiso de **Crear Referencias** para utilizar esta funcionalidad.

⚠️ **Código Único:** El nuevo código debe ser único. Si ya existe, el sistema mostrará un error.

⚠️ **Revisión Post-Copia:** Aunque la copia es completa, se recomienda revisar la nueva referencia para ajustar:
- Precios específicos
- Proveedores activos
- Tiempos de operación según capacidad de planta
- Cantidades de consumo si aplican ajustes

⚠️ **Datos No Copiados:** Los siguientes elementos NO se copian:
- Inventarios y saldos existentes
- Movimientos históricos
- Listas de precios específicas
- Imágenes y fotografías

### Solución de Problemas

| Problema | Causa Probable | Solución |
|----------|----------------|----------|
| No aparece el botón de copiar | Falta permiso de Crear o la referencia no es tipo 'R' | Verificar permisos con el administrador del sistema |
| Error "El código ya existe" | El código ingresado está en uso | Cambiar el código por uno único |
| Error al copiar | Problema de conexión o validación en datos origen | Verificar que la referencia origen esté completa y válida |
| No redirige a la nueva referencia | Error en la respuesta del servidor | Buscar manualmente la referencia con el nuevo código creado |

---

[Regresar al Inicio](../readme.md)
