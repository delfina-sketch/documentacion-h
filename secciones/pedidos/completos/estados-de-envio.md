# Estados de envío

## Descripción

Los estados de envío existentes en Hermes son:&#x20;

### **Envíos**

* Pendiente -> la orden se encuentra pendiente de envío por parte del depósito
* Armado parcial -> el depósito cuenta con productos faltantes de la orden
* Envío no entregado -> el pedido no pudo ser entregado al destinatario
* Despachado -> la orden fue enviada
* En sucursal ->  la orden se encuentra lista para ser retirada por la sucursal de correo elegida por el usuario&#x20;
* Confirmado -> la etiqueta de envío fue generada por el depósito encargado del despacho
* Entregado -> la orden fue entregada al destinatario
* Preorden: la orden cuenta con un producto que aún no fue ingresado a depósito&#x20;

### **Pick up in store**

* Confirmado -> el pedido fue armado por el local
* Rechazado por tienda -> la orden fue rechazada por la tienda
* Entregado -> el pedido fue entregado al usuario

### **Logística inversa**

* Esperando devolución -> la devolución de los productos se encuentra en camino&#x20;
* Devuelto -> la devolución de los productos arribó al depósito de la marca
* Devolución en camino -> la devolución de los productos se encuentra en camino
* Devolución completada -> la devolución de los productos arribó al depósito de la marca
