# Emails

#### Descripción <a href="#descripcion" id="descripcion"></a>

En los clientes de Hermés, desde Notificaciones > Emails, se podrán editar vía HTML todos los mails transaccionales que se envían desde Hermés.

Estos son:

* Confirmación de Compra
* Pago Rechazado
* Pago Pendiente
* Pedido Despachado
* Pedido en Sucursal de Correo
* Pedido Cancelado
* Carrito abandonado

Para editarlos, se deberán tener en cuenta variables (datos dinámicos) que no se podrán modificar ya que sino el mail se enviará de manera incorrecta o no se enviará. Las mismas se detallan más adelante.

#### Edición de emails <a href="#paso-a-paso-de-como-editar-los-mails" id="paso-a-paso-de-como-editar-los-mails"></a>

1\. Acceder a Notificaciones > Emails. Allí seleccionar el tipo de mail que se quiere editar:

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 14.45.02.png" alt=""><figcaption></figcaption></figure>

2. En la pantalla de edición del email, se deberá editar el cuerpo del email en HTML.&#x20;
   1. Lateral izquierdo: Se mostrará el HTML editable
   2. Lateral derecho: Se muestra la preview del email. A medida que es editado en el HTML, los cambios se van viendo reflejados en esta sección.&#x20;

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 14.45.31.png" alt=""><figcaption></figcaption></figure>

También hay 3 botones accionables:

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.21.09.png" alt=""><figcaption></figcaption></figure>

* Restaurar: si se editó el HTML y se necesita volver a la versión inicial, al clickear en este botón se restaurará con el HTML inicial.
* Variables: muestra las variables disponibles para su uso. Se trata de información dinámica que no debe ser editada.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 14.47.57.png" alt=""><figcaption></figcaption></figure>

* Enviar Test: mediante este botón se podrá enviar un email de prueba al correo colocado en el campo "Email" del modal. También se puede enviar un email de una orden específica.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.22.51.png" alt=""><figcaption></figcaption></figure>

### Variables <a href="#variables" id="variables"></a>

Son datos dinámicos que se muestran en los mails. Es muy importante que se incluyan estas variables en los mails para que el cliente pueda recibir la información correspondiente a su orden.

**Estas variables NO deben ser modificadas. Siempre se encuentran entre < >.**

* Mail de confirmación:
* ID de la orden: <%= decorated\_order.id %>
* Datos de envío:
  * Nombre: <%= decorated\_bill.full\_name %>
  * Dirección: <%= @order.choice.decorate.full\_address %
* Método de envío: <%= decorated\_order.shipping\_method %>
* Facturación:
  * Nombre: <%= decorated\_bill.full\_name %>
  * Dirección: <%= decorated\_bill.full\_address %>
  * Dirección: <%= decorated\_bill.location %>
  * País: <%= decorated\_bill.country\_name %>
* Método de pago: <%= decorated\_order.payment\_method %>
* Mail de Recupero:
  * Link recupero de carrito: <%= link\_to 'Recuperar carrito', order\_restore\_url(@order, utm\_source: 'newsletter', utm\_campaign: 'recupero\_de\_carritos', utm\_medium: 'email'), class:'common-btn' %>

#### Asuntos de los emails (no editables)

Cada email tiene un asunto correspondiente a la acción:&#x20;

| Nombre         | Asunto                                               |
| -------------- | ---------------------------------------------------- |
| `pendiente`    | Tu pedido #order.id se encuentra en estado pendiente |
| `confirmacion` | Tu pedido #order.id fue realizado con exito          |
| `recupero`     | full\_name tu compra en brand te esta esperando      |
| `cancelado`    | Tu pedido #order.id fue cancelado                    |
| `rechazo`      | Tu pedido #order.id fue rechazado                    |
| `Despacho1`    | Tu pedido #order.id fue despachado                   |
| `en sucursal`  | Tu pedido se encuentra en la sucursal listo para...  |
