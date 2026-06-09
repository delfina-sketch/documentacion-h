# Pedidos Completos

**URL:** `/admin/orders` o `/admin/orders?status=completed`

Listado de todos los pedidos que completaron el proceso de checkout.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-03 a la(s) 8.53.05 a. m..png" alt=""><figcaption></figcaption></figure>

## Barra de busqueda y filtros

Permite buscar por ID de pedido, email, nombre del cliente o DNI/CUIT.

A su vez, el módulo cuenta con filtros que sirven para _optimizar la búsqueda de órdenes_:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-03 a la(s) 8.57.19 a. m..png" alt=""><figcaption></figcaption></figure>

A continuación veremos los distintos _filtros_ que podremos utilizar:

* **Estado de pago**: filtra entre los estados de pago de una orden. Para más información sobre los estados de pago consultá [Estados de pago](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/4ixUGi3IayVNsRKEYT0I/~/edit/~/changes/8/secciones/pedidos/completos/estados-de-pago)
* **Método de pago:** filtra las órdenes con los distintos métodos de pago disponibles en el administrador (mercado pago agregador, transferencia, efectivo, etc.)
* **Fecha de pago**: muestra órdenes de un período de fecha especificado de pago.
* **Estado de envío**: filtra entre los estados de envío de una orden. Para más información consultá [Estados de envío](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/4ixUGi3IayVNsRKEYT0I/~/edit/~/changes/8/secciones/pedidos/completos/estados-de-envio)
* **Método de envio - Operador:** filtra las órdenes por operador logístico y tipo de envío.
* **Estado de Facturación**: filtra entre los estados de facturación de una orden. Para más información consultá [Estados de facturación](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/4ixUGi3IayVNsRKEYT0I/~/edit/~/changes/8/secciones/pedidos/completos/estados-de-facturacion)
* **Fecha de facturación**: muestra órdenes de un período de fecha especificado de facturación.
* **Código cupón:** filtra órdenes que contienen el código de cupón especificado.&#x20;
* **Omnicanalidad**: filtra las órdenes omnicanales.
* **Depósito:** filtra las ordenes entre central o sucursales especificadas.
* **Fuente de venta**: filtra órdenes según marketplace (tienda online, mercado libre, etc.)



## Columnas de la tabla

| Columna               | Ordenable             | Descripcion                                                                          |
| --------------------- | --------------------- | ------------------------------------------------------------------------------------ |
| Pedido                | Si (desc por defecto) | Numero de pedido                                                                     |
| Cliente               | Si                    | Nombre completo del cliente                                                          |
| Total                 | Si                    | Monto total del pedido en formato argentino                                          |
| Deposito              | No                    | Deposito o sucursal asignada (ej: "Central")                                         |
| Fecha de pago         | Si                    | Fecha en que se registro el pago                                                     |
| Estado de pago        | Si                    | Badge de color: **Aprobado** (verde), **Cancelado** (rojo), **Pendiente** (amarillo) |
| Metodo de envio       | Si                    | Operador logistico (ej: Andreani, Andreani Sucursal)                                 |
| Estado de envio       | Si                    | **Pendiente** (amarillo), **Despachado** (azul), **Entregado** (verde)               |
| Estado de facturación | Si                    | **Pendiente** (amarillo), **Reembolsado** (rojo), **Facturado** (verde)              |
| Acciones              | No                    | Ver (ojo), Editar (lapiz), Eliminar (X rojo)                                         |

## Paginado

Navegación por paginas  en la parte inferior con indicador "1-N" del total.

## Acciones por pedido

* Al hacer click en el icono del **ojo** se accede al [detalle del pedido](../detalle.md).&#x20;
* Al hacer click en el icono del **lapiz** se accede a editar el pedido.&#x20;
* Al hacer click en el icono de la **cruz** se cancela la orden.&#x20;
