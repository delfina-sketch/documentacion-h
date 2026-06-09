# Pedidos Abandonados

**URL:** `/admin/orders?status=abandoned`

Listado de carritos que iniciaron el checkout pero no completaron la compra.

## Funcionalidad

La vista es identica a [Pedidos Completos](completos/) en cuanto a estructura:

* Mismas tarjetas de resumen superiores
* Misma barra de busqueda (por ID, email, nombre, DNI/CUIT)
* Mismas columnas de tabla y opciones de filtrado
* Mismas acciones por fila

La diferencia es que filtra automaticamente por pedidos con estado "abandonado".

## Uso tipico

Los pedidos abandonados permiten:

1. Identificar clientes que no completaron su compra
2. Contactarlos para recuperar la venta (via email de recupero)
3. Analizar patrones de abandono (metodo de pago, monto, etc.)
