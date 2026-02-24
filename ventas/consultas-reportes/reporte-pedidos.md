[Regresar a Ventas](../readme.md)

---

# 📊 Reporte de Pedidos

## Descripción General

El **Reporte de Pedidos** es una herramienta que permite visualizar y analizar el estado de los pedidos en diferentes niveles de detalle, organizados de tres formas distintas:

- **Reporte General:** Pedidos individuales con desglose de líneas (referencias/productos)
- **Reporte por Cliente:** Pedidos agrupados y resumidos por cliente
- **Reporte por Referencia:** Pedidos agrupados por producto/referencia

Esta funcionalidad facilita el seguimiento de pedidos pendientes, despachos y control de inventario en tránsito.

---

## 🚀 Acceso al Reporte

### Ubicación en el Sistema

1. En el **Menú Principal**, selecciona **Ventas**
2. Busca la opción **Reporte de Pedidos**
3. Se abrirá la pantalla de consulta

### Pantalla Principal

La pantalla muestra:
- Campos de filtro (Fechas)
- Opciones de filtrado adicional
- Selector de tipo de reporte
- Botón de consulta
- Tabla de resultados

---

## 🔍 Filtros Disponibles

### Rango de Fechas

| Campo | Descripción |
|---|---|
| **Fecha Inicial** | Fecha de inicio para filtrar pedidos |
| **Fecha Final** | Fecha de corte del reporte |

**Ejemplo:** Para ver pedidos de enero (2026-02-01 a 2026-02-28)

### Opciones Adicionales

| Opción | Efecto |
|---|---|
| **Incluir Saldo 0** | Muestra también los pedidos completamente despachados (sin saldo pendiente) |

---

## 📋 Tipos de Reporte

### 1. Reporte General

**Propósito:** Visualizar cada pedido con sus líneas detalladas

**Columnas principales:**
- **Documento:** Código del tipo de movimiento + Consecutivo (ej: `PD-001234`)
- **Fecha Pedido:** Cuando se registró el pedido
- **Fecha Entrega:** Fecha estimada de entrega
- **Cliente:** Documento y nombre del cliente
- **Estado:** Indicador visual de plazo:
  - 🔴 **Rojo:** Vencido o faltan ≤2 días
  - 🟠 **Amarillo:** Faltan 3-20 días
  - 🟢 **Verde:** Faltan >20 días
  - ⚫ **Negro:** Vencido
- **Cant. Pedida:** Total de unidades solicitadas
- **Cant. Despachada:** Unidades enviadas
- **Cant. Saldo:** Unidades pendientes
- **Total Pedido:** Valor monetario

**Expandir Detalle:** Haz clic en el icono **▶** para ver todas las referencias (productos) que incluye el pedido

### 2. Reporte por Cliente

**Propósito:** Agrupar y resumir pedidos por cliente

**Columnas principales:**
- **Cliente:** Nombre/documento del cliente
- **# Pedidos:** Cantidad de pedidos del cliente en el rango
- **Cant. Pedida:** Total de unidades en todos los pedidos
- **Cant. Despachada:** Total de unidades despachadas
- **Cant. Saldo:** Total de unidades pendientes
- **Valor Total:** Suma de todos los pedidos del cliente

**Expandir Detalle (Nivel 1):** Haz clic en **▶** para ver la lista de pedidos de ese cliente

**Expandir Detalle (Nivel 2):** Haz clic en **▶** en un pedido para ver las referencias incluidas

### 3. Reporte por Referencia

**Propósito:** Agrupar pedidos por producto/referencia

**Columnas principales:**
- **Referencia:** Código y nombre del producto
- **# Pedidos:** Cantidad de pedidos que contienen este producto
- **Total Pedido:** Unidades pedidas en total
- **Total Despachado:** Unidades despachadas
- **Total Saldo:** Unidades pendientes de despacho
- **Valor Total:** Suma del valor de este producto en todos los pedidos

**Expandir Detalle:** Haz clic en **▶** para ver todos los pedidos que incluyen este producto

---

## 📌 Ejemplo de Uso Paso a Paso

### Escenario: Revisar pedidos vencidos de enero

1. **Abre** el Reporte de Pedidos
2. **Configura** las fechas:
   - Fecha Inicial: `2026-01-01`
   - Fecha Final: `2026-01-31`
3. **Deja sin marcar** "Incluir Saldo 0" (para ver solo lo pendiente)
4. **Selecciona** el tipo de reporte que necesites:
   - "General" para detalles completos por pedido
   - "Por Cliente" para resumir por cliente
   - "Por Referencia" para ver qué productos están pendientes
5. **Haz clic** en "Consultar"
6. **Expande** las filas con ▶ para ver más detalles

### Escenario: Identificar clientes con mayor volumen pendiente

1. Selecciona **"Por Cliente"**
2. Ordena por **"Cant. Saldo"** (descendente)
3. Verás inmediatamente qué clientes tienen más pendiente por despachar

### Escenario: Monitorear disponibilidad de un producto específico

1. Selecciona **"Por Referencia"**
2. Busca o filtra por el código de referencia
3. **Expande** para ver en qué pedidos se requiere
4. Planifica el despacho en consecuencia

---

## 💡 Funcionalidades Especiales

### El Icono Semáforo (Estado de Plazo)

Cada pedido muestra un indicador visual intuitivo:

| Color | Significado |
|---|---|
| 🔴 Rojo | **Crítico:** Vencido o con plazo muy cercano (≤2 días) |
| 🟠 Amarillo | **Atención:** Plazo próximo (3-20 días) |
| 🟢 Verde | **Holgura:** Plazo cómodo (>20 días) |
| ⚫ Negro | **Vencido:** Sobrepasó la fecha de entrega |

Esta información te ayuda a **priorizar despachos** y negociar plazos si es necesario.

### Totales Filtrados

En el pie de la tabla se muestran los **totales** de las columnas numéricas para los registros visibles (aplicando búsquedas/filtros si existen).

---

## 🔧 Configuración Avanzada

### Exportar Resultados (si está disponible)

Algunos navegadores e instalaciones permiten:
- **Copiar** la tabla a Excel
- **Imprimir** la consulta

Consulta con tu administrador si estas opciones están habilitadas.

### Búsqueda/Filtrado en Tabla

Una vez cargados los resultados, puedes:
- Escribir en la caja de **búsqueda** para filtrar por cualquier columna
- **Ordenar** haciendo clic en los encabezados de columna

---

## ⚠️ Notas Importantes

1. **Rango de fechas:** El sistema solo muestra los pedidos registrados en el rango seleccionado
2. **Permisos:** Solo ves pedidos de tu empresa si tienes acceso configurado
3. **Datos en tiempo real:** El reporte trae la información actual de la base de datos
4. **Límite de registros:** Si el rango es muy amplio, el sistema puede tardar en cargar. Intenta acotar fechas si es lento

---

## 📞 Soporte

Si encuentras problemas:

- **Pantalla en blanco:** Verifica que hayas seleccionado un rango de fechas válido
- **Sin datos:** Confirma que existan pedidos en el rango seleccionado
- **Lentitud:** Intenta reducir el rango de fechas
- **Otros problemas:** Contacta al equipo de soporte técnico

---

[Regresar a Ventas](../readme.md)
