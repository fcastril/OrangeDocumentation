[Regresar a Producción](../readme.md)

---
# ORDENES DE PRODUCCIÓN

Permite crear, consultar y administrar las órdenes de producción, incluyendo su seguimiento operativo y el registro de observaciones asociadas a cada OP.

## Ubicación

- Ruta: Producción > Movimientos > Ordenes de Producción.

## Propósito

- Registrar órdenes de producción.
- Consultar el detalle de una OP y su estado general.
- Llevar trazabilidad de novedades y comentarios relevantes del proceso.

## Información principal de una OP

Dependiendo de la configuración y permisos del usuario, la opción permite visualizar entre otros:

- Tipo de movimiento.
- Consecutivo de la orden.
- Fecha de la orden.
- Fecha estimada de entrega.
- Documento de referencia.
- Observaciones generales.
- Referencias y cantidades relacionadas.
- Detalle operativo de la orden.

## Observaciones de la orden de producción

Las órdenes de producción ahora pueden recibir observaciones mediante integración API, permitiendo registrar novedades operativas sin modificar la estructura principal de la OP.

### Datos registrados por observación

Cada observación guarda:

- Id de la orden de producción.
- Texto de la observación.
- Usuario asociado al registro.
- Relevancia.
- Fecha y hora de creación.

### Reglas de registro

- La fecha y hora se guardan con la hora del servidor.
- La relevancia es opcional; si no se envía, el sistema registra `0`.
- Si el usuario se identifica desde el token de autenticación, el sistema antepone en el texto de la observación el nombre del reportante para dejar trazabilidad visible.
- Si la orden no existe, la observación no se registra.

### Ejemplo de observación registrada

```text
[Carlos Mesa] Se reporta retraso por falta de materia prima.
```

## Integración API

Se dispone del endpoint `SetObservations` para registrar observaciones de una OP.

### Ruta principal

- `POST /api/v1/ordenesproduccion/observaciones/SetObservations`

### Body esperado

```json
{
	"idOrdenProduccion": 123,
	"Observacion": "Se agregó observación desde API",
	"Usuario": "Carlos Mesa",
	"Relevancia": 5
}
```

### Respuesta exitosa

```json
{
	"ok": true,
	"mensaje": "Observación registrada correctamente",
	"data": {
		"idOrdenProduccion": 123,
		"idObservacion": 10,
		"usuario": "jdoe",
		"fecha": "2026-03-20T10:30:00",
		"relevancia": 5
	}
}
```

## Consideraciones

- El endpoint requiere autenticación.
- El usuario puede resolverse desde el token o desde el body cuando aplique.
- La observación debe enviarse con contenido; no se permiten textos vacíos.

