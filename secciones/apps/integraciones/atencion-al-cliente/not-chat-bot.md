# Not Chat Bot

**NotChatBot** es un chatbot de atención al cliente disponible 24/7. La integración con Hermes se realiza mediante **webhooks**, lo que permite mantener la información sincronizada en tiempo real a partir de eventos.

Esto significa que, cada vez que ocurre una acción relevante —como la creación de un pedido, un cambio de estado o la generación de un carrito abandonado—, Hermes notifica automáticamente a NotChatBot, asegurando que el cliente siempre reciba información actualizada.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-04-28 a las 17.14.45.png" alt="" width="375"><figcaption></figcaption></figure>

#### Funcionamiento&#x20;

1. NotChatBot se suscribe a eventos de Hermes mediante un endpoint de suscripciones (/webhooks\_suscriptions)
2. Ocurre un evento en Hermes (actualización en producto, orden o creación de carrito abandonado).
3. Hermes envía automáticamente un webhook al endpoint correspondiente de NotChatBot.
4. NotChatBot procesa la actualización en tiempo real.&#x20;

#### Manejo de errores

En caso de error en el endpoint receptor (NotChatBot):

* HTTP 500+ o timeout (>10s): se realizan reintentos automáticos (máx. 3 intentos: 1 min, 5 min, 15 min)
* HTTP 4xx: no se reintenta

<figure><img src="../../../../.gitbook/assets/Diagrama en blanco (3).png" alt=""><figcaption></figcaption></figure>

#### Eventos implementados

**Productos**

* product/created - Creación de productos
* product/updated - Actualización de productos
* product/deleted - Eliminación de productos

**Órdenes**

* order/created - Creación de orden
* order/status\_changed - Cambio de estado de una orden
* order/paid - Orden pagada
* order/canceled - Orden cancelada
* order/shipping\_updated - Actualización de estado de envío de la orden
* order/deleted - Orden eliminada

**Carritos abandonados**

* abandoned\_cart/created - Creación de carritos abandonados

**Endpoints internos (Hermes)**

* POST /api/hermes/product
* POST /api/hermes/order
* POST /api/hermes/abandoned\_cart

**Endpoints destino (NotChatBot)**

* https://next.notchatbot.com/api/hermes/product
* https://next.notchatbot.com/api/hermes/order
* https://next.notchatbot.com/api/hermes/abandoned\_cart

{% hint style="info" %}
La integración utiliza autenticación por _access token_, el cual se incluye en los headers de cada webhook. Este token es validado por NotChatBot para asegurar la autenticidad de la solicitud y permitir el procesamiento seguro de los datos.
{% endhint %}

#### Suscripción a eventos

Las suscripciones se crean vía API REST.\
Se pueden utilizar wildcards para recibir todos los eventos de un recurso:

* product/\*
* order/\*
* abandoned\_cart/\*

#### Crear suscripción

Método: POST\
Endpoint: https://www.misitio.com.ar/api/hermes/webhook\_subscriptions

Headers

* Content-Type: application/json
* token: \<TOKEN\_DE\_AUTENTICACION>&#x20;

Body

```
"event": "product/*",
"url": "https://next.notchatbot.com/api/hermes/product",
"access_token": "<token_que_recibirá_notchatbot_en_authorization>",
"secret": "<clave_que_recibirá_notchatbot_en_header_notchatbot-key>"
}
```

#### Listar suscripciones

* Método: GET
* Endpoint: https://www.misitio.com.ar/api/hermes/webhook\_subscriptions

Headers

* token: \<TOKEN\_DE\_AUTENTICACION>

#### Eliminar suscripción

Método: DELETE\
Endpoint: https://www.misitio.com.ar/api/hermes/webhook\_subscriptions/{id}

Headers

* token: \<TOKEN\_DE\_AUTENTICACION>

### Formato de webhook recibido

#### Headers

| **Header**      | **Valor**               |
| --------------- | ----------------------- |
| Content-Type    | application/json        |
| X-Webhook-Event | ej: product/updated     |
| Authorization   | Bearer \<access\_token> |
| notchatbot-key  | \<secret>               |

***

#### Body

{

&#x20;"event": "product/updated",

&#x20;"timestamp": "2026-03-27T15:45:00-03:00",

&#x20;"...": "campos completos del recurso"

}

#### Estructura por recurso

* Productos: mismo formato que GET /api/hermes/catalog
* Órdenes: mismo formato que GET /api/hermes/order\_search (incluye clientProfileData.phone requerido por NotChatBot)
* Carritos abandonados: mismo formato que GET /api/hermes/abandoned\_checkouts (incluye contact\_phone requerido por NotChatBot)

Ejemplo

```
{
 "event": "product/created",
 "product": {
   "id": 1,
   "nombre_producto": "Ejemplo",
   "precio_producto": 123
 }
}
```

#### API de consulta (fallback)

Hermes expone endpoints para consultas puntuales cuando sea necesario:

* GET /products/{id}
* GET /orders/{id}
* Categorías
* Carritos abandonados

