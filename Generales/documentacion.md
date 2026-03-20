[Regresar al Inicio](../README.md)

---

# Documentación del Sistema

## Indicadores de Carga (Loading)

El sistema Orange.NET utiliza un **sistema centralizado de indicadores de carga** denominado **OrangeLoading** para mostrar al usuario que la aplicación está procesando solicitudes.

### Características

- **Consistencia Visual:** Todos los indicadores de carga en el sistema siguen el mismo diseño y comportamiento, mejorando la experiencia del usuario.
- **Rendimiento:** El sistema está optimizado para no bloquear la interacción del usuario y funciona correctamente con tecnologías como DataTables.
- **Robustez:** En caso de que el sistema OrangeLoading no esté disponible, la aplicación implementa un fallback automático a indicadores manuales.
- **Configurabilidad:** Cada operación puede personalizar el texto, subtexto y alcance del indicador de carga.

### Ubicación Visual

Los indicadores de carga aparecen:

1. **En consultas principales (Index):** Cuando se carga la lista de registros o se aplican filtros de búsqueda.
2. **En formularios de creación/edición:** Cuando se envían datos al servidor para guardar o validar.
3. **En operaciones especiales:** Cuando se realizan acciones como anular, congelar, exportar o sincronizar datos.
4. **En reportes:** Cuando se generan o cargan reportes/gráficos.

### Funcionalidad

- El indicador aparece automáticamente cuando inicia una solicitud al servidor.
- Desaparece cuando la solicitud se completa o si ocurre un error.
- En algunos casos, permanece visible para operaciones de larga duración, indicando al usuario que debe esperar.
- **No bloquea la interacción:** El usuario puede seguir navegando en la mayoría de casos mientras se procesa la solicitud.

### Notas Técnicas

El sistema de loading implementa un patrón de helpers con fallback:

```javascript
function mostrarLoading() {
    if (window.OrangeLoading && typeof window.OrangeLoading.showIn === 'function') {
        window.OrangeLoading.showIn(form, { 
            scope: 'local', 
            source: 'module-id',
            text: 'Cargando...',
            subtext: 'Por favor espere'
        });
        return;
    }
    // Fallback automático si OrangeLoading no está disponible
    form.prepend($('<div class="block-loading" />'));
}
```
