# Creación de plantillas

### Creación de nueva plantilla <a href="#creacion-de-nueva-plantilla" id="creacion-de-nueva-plantilla"></a>

1. Ingresar al módulo de Whatsapp

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

2. Ir a 'Nueva plantilla':

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.40.16.png" alt=""><figcaption></figcaption></figure>

3. Configurar los tres campos solicitados:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.40.41.png" alt=""><figcaption></figcaption></figure>

* **Nombre de la plantilla:** Es de uso interno, se debe colocar un nombre representativo de la plantilla. Ejemplo: PagoAprobado para el mensaje que informa que el pago del pedido fue aprobado. Consideraciones:
  * El nombre **de la plantilla tiene que estar completamente en minúscula y sin espacios (no acepta caracteres** especiales)
  * La plantilla **no debe comenzar con variables**. Ejemplo: "\{{first\_name\}}, tu pedido fue despachado". Se sugiere utilizar una palabra antes de la variable. Ej: "Hola \{{first\_name\}}..."
  * La creación de plantillas es ilimitada.&#x20;
* **Contenido:** Es el mensaje que recibirá el usuario. Para que sea mas personalizado, se pueden utilizar las diferentes variables disponibles:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.42.53.png" alt=""><figcaption></figcaption></figure>

* **Trigger:** Los mensajes se enviarán según el disparador que se haya configurado para el mismo. Los disparadores disponibles corresponden a envío (domicilio/sucursal) y retiro en local (pickup):

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.43.55.png" alt=""><figcaption></figcaption></figure>

4. Habilitar la plantilla:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.46.25.png" alt=""><figcaption></figcaption></figure>

5. Hermes enviará la plantilla a Meta para que sea aprobada (approved) o rechazada (rejected)
   * Si es **aprobada**, el mensaje se comenzará a enviar a los usuarios cuando suceda la acción definida.
   * Si es **rechazada**, se debe crear una nueva plantilla y el nombre de la plantilla no se puede repetir con otra creada previamente. Para saber el motivo del rechazo podes realizar la consulta por formulario.

Para verificar si la plantilla fue aprobada o rechazada, en la pantalla principal de plantillas figurará el estado correspondiente:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-04-30 a las 15.48.44.png" alt=""><figcaption></figcaption></figure>

### Motivos por los cuales Meta puede rechazar una plantilla <a href="#motivos-por-los-cuales-meta-puede-rechazar-una-plantilla" id="motivos-por-los-cuales-meta-puede-rechazar-una-plantilla"></a>

Meta puede rechazar una plantilla de mensajes de WhatsApp por varias razones, generalmente relacionadas con el cumplimiento de sus políticas para evitar spam y asegurar una buena experiencia del usuario. Aquí se detallan las razones más comunes:

#### **Problemas de formato y variables** <a href="#problemas-de-formato-y-variables" id="problemas-de-formato-y-variables"></a>

* **Errores en las variables:** Falta de parámetros variables (`{{#}}`), llaves desalineadas, variables no secuenciales (ej: \{{1\}}, \{{2\}}, \{{4\}}), variables adyacentes (`{{1}} {{2}}`), o caracteres especiales en las variables (`#`, `$`, `%`).
* **Variables al inicio o final:** La plantilla comienza o termina con una variable (ej: `{{1}} gracias!`).
* **Formato incorrecto:** Errores de puntuación, exceso de líneas nuevas consecutivas en el cuerpo del mensaje (`\n\n`), o formato incorrecto en los encabezados de texto (uso de emojis, asteriscos, etc.).

#### **Contenido inapropiado o confuso** <a href="#contenido-inapropiado-o-confuso" id="contenido-inapropiado-o-confuso"></a>

* **Contenido engañoso o deshonesto:** Afirmaciones falsas, ofertas demasiado buenas para ser verdad.
* **Promoción pura:** Plantillas enfocadas únicamente en vender sin ofrecer valor informativo o de servicio al cliente.
* **Contenido confuso o irrelevante:** El propósito del mensaje no es claro, o el contenido no está relacionado con la interacción del cliente con tu negocio.
* **Violación de términos:** Contenido abusivo, amenazante, discriminatorio, o que incite al odio o la violencia, así como cualquier contenido ilegal.
* **Errores gramaticales o de ortografía:** Mensajes con errores que pueden parecer spam o fraudulentos.
* **Lenguaje inconsistente:** El idioma definido para la plantilla no coincide con el contenido del mensaje.
* **Propósito poco claro de las variables:** No se entiende qué información debe ir en cada parámetro variable.

#### Ejemplo de plantilla para retiro en local <a href="#ejemplo-de-plantilla-para-retiro-en-local" id="ejemplo-de-plantilla-para-retiro-en-local"></a>

¡Ya podés retirar tu pedido de Pow! 🖤✨ Tu pedido #\{{order\_id\}} está listo para ser retirado en la sucursal \{{store\_name\}} 📍Dirección: \{{store\_address\}}
