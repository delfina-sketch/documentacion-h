# Icomm

La integración con ICOMM está realizada por API y disponibiliza en tiempo real la información de órdenes, catálogo de productos y clientes mediante el intercambio de tokens de autenticación entre ambas partes (hermes/icomm).&#x20;

Ante fallos de la API, el sistema realiza 3 reintentos de re-informe y la integración es asincrónica, requiriendo revisión de la cola de tareas en Sidekiq si hay problemas con el procesamiento de información.

<figure><img src="../../../../.gitbook/assets/Diagrama en blanco (1).png" alt="" width="563"><figcaption></figcaption></figure>

#### Tipo de integración

* API en tiempo real (reemplaza integración anterior basada en archivos CSV por FTP)
* Asincrónica (con cola de procesamiento)

#### Flujo de datos

La integración contempla:

**Envío hacia Icomm:**

* Órdenes (cada vez que se generan)

**Consumo desde Icomm:**

* Catálogo de productos
* Clientes (compradores, suscriptores y registrados)

#### Autenticación

Para garantizar la seguridad en la transferencia de datos, se utilizan dos tokens de seguridad:<br>

* Token de **Icomm**
  * Provisto por **Icomm**
  * Usado para enviar órdenes
* App Token (Hermés)
  * Usado por **Icomm** para consumir catálogo y listas (compradores, registrados, suscriptores)
  * Generado por el equipo de Pow.

#### Configuración

En Icomm, cargar el “App token” brindado por Pow. en el campo “app token”

<figure><img src="../../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

\
En Hermes, cargar la Api Key y Token obtenidas desde Icomm:

<figure><img src="../../../../.gitbook/assets/FireShot Capture 092 - Hermés - Panel de Administración - [hermes.pow.la].png" alt=""><figcaption></figcaption></figure>

####

{% hint style="info" %}
#### Consideraciones adicionales

* Los datos de clientes se unifican en una única base llamada “Masterdata”
* Identificador único por cliente: email. Esto significa que si un mismo cliente compra con dos mails diferentes, se consideran dos clientes por separado.&#x20;
* La información de clientes se sobrescribe con el dato más reciente. Esto significa que si un cliente utiliza el mismo mail que una compra anterior, pero cambia los datos de compra de la orden (ej: dirección), los datos se “pisarán”, quedando los últimos utilizados como finales.
{% endhint %}

#### Procesamiento

La integración de Icomm es **asincrónica**.&#x20;

Una integración asincrónica es aquella en la que el envío y procesamiento de la información no ocurre de manera inmediata ni bloquea el flujo principal, sino que se realiza en segundo plano. Esto permite que el sistema continúe operando sin depender de la respuesta del sistema externo.

Ejemplo: al realizar una compra, la orden se confirma en la web de forma inmediata, mientras que el envío de esa información a un sistema externo (como Icomm) se procesa posteriormente en segundo plano.

#### Manejo de errores

* Se hacen hasta 3 reintentos automáticos
* Si la integración no funciona, la interfaz de Icomm muestra el error
* No hay implementadas alertas automáticas avanzadas

Recomendación:

* Si hay fallas prolongadas (como la caída temporal de la API), al restablecerse se reprocesan las órdenes del período afectado. Icomm ya evita información duplicada.&#x20;
* Se recomienda revisar estado de procesos en Sidekiq (worker: Icommapiworker)

<br>
