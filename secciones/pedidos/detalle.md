# Detalle de Pedido

## Descripción

Existen dos formas de acceder a una orden:

* **URL:** `/admin/orders/[id]` (ejemplo: `/admin/orders/233727`)
* Al seleccionar el icono del **ojo** en el listado de los pedidos.

Vista completa de un pedido individual con toda la información asociada: productos, cliente, pago, envio, facturacion y comunicaciones.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-03-03 a la(s) 9.50.21 a. m..png" alt=""><figcaption></figcaption></figure>

## Header

* **Breadcrumb:** Volver > Pedidos completos > Pedido #XXXXX
* **Numero de pedido** con badges de estado (ej: "Aprobado" verde, "Pendiente" amarillo)
* **Fecha y hora** de creacion del pedido
* **Botones de accion:**
  * **Editar** (azul): Abre el formulario de edicion del pedido
  * **Trazabilidad de la Orden:** Muestra el historial completo de estados
  * **Mas acciones** (dropdown): Opciones adicionales como cancelar, reembolsar, etc.

## Detalle de la compra

Sección con la tabla de productos del pedido:

| Columna      | Descripcion                                          |
| ------------ | ---------------------------------------------------- |
| Producto     | Imagen thumbnail + nombre (link al producto)         |
| SKU          | Codigo SKU de la variante especifica                 |
| Deposito     | Deposito de donde sale el producto                   |
| Precio unit. | Precio unitario                                      |
| Cant.        | Cantidad comprada                                    |
| Descuento    | Porcentaje de descuento aplicado                     |
| Subtotal     | Subtotal de la linea (precio x cantidad - descuento) |

### <sub>Resumen de montos</sub>

* Subtotal productos
* Descuentos productos (en rojo, valor negativo)
* Costo de envio
* **Monto total** (destacado en verde, tamaño grande)

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-03-03 a la(s) 9.50.53 a. m..png" alt=""><figcaption></figcaption></figure>

## Panel lateral derecho

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-03-03 a la(s) 9.56.04 a. m..png" alt=""><figcaption></figcaption></figure>

### Cliente

* Nombre completo
* Email
* Telefono
* DNI/Documento

### Información de pago

* **Metodo de Pago:** Tipo general (ej: Transferencia)
* **Medio de Pago:** Gateway especifico (ej: Mercado pago agregador)
* **Estado:** Badge con el estado del pago (Aprobado, Pendiente, Cancelado)
* **ID de pago:** Identificador de la transaccion

### Etiquetas de retiro

Etiquetas de retiro en tienda generadas para este pedido.

### Etiquetas de reenvio

Etiquetas de reenvio generadas.

### Notas de credito

Notas de crédito emitidas para este pedido.

## Información de envío

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-03-03 a la(s) 10.00.14 a. m..png" alt=""><figcaption></figcaption></figure>

Sección con los datos del envío:

* **Numero de envío:** Código único (ej: ENV-233727) con badge de estado
* **Método:** Tipo de envio (ej: Envio a domicilio)
* **Dirección:** Dirección completa de entrega
* **Operador logístico:** Empresa de transporte (ej: ANDREANI)
* **Costo total envío:** Monto del envío

### Paquetes

Lista de paquetes con:

* Numero de envio y estado
* Costo del paquete
* Productos incluidos (badges con nombre y cantidad)

## Información de facturación

Sección con los datos fiscales:

| Campo               | Descripcion                        |
| ------------------- | ---------------------------------- |
| Estado              | Badge: Pendiente, Facturado        |
| Nombre y apellido   | Datos del comprador                |
| Documento           | DNI/CUIT                           |
| Nro. de Comprobante | Numero de factura (si fue emitida) |
| Direccion           | Direccion fiscal                   |
| Localidad           | Ciudad                             |
| CP                  | Codigo postal                      |
| Telefono            | Telefono de contacto               |

## Mensajes al cliente

Tabla con el historial de comunicaciones enviadas al cliente:

| Columna         | Descripcion                                             |
| --------------- | ------------------------------------------------------- |
| Fecha de envio  | Fecha y hora del envio                                  |
| Nombre del mail | Tipo de email (ej: Pago Pendiente, Confirmacion compra) |
| Asunto          | Linea de asunto del email                               |
| Ver             | Icono de ojo para previsualizar el email enviado        |

## Comentarios

Seccion para notas internas del equipo:

* Lista de comentarios existentes
* Boton **+ Agregar comentario** para agregar una nota interna
