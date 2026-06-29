# Configuración de cuotas

En la nueva versión de la integración de MODO, la configuración de las **credenciales de acceso** y la configuración de las **cuotas** pasan a administrarse por separado.

Las credenciales ya fueron configuradas por POW durante la implementación. Sin embargo, para que las cuotas se muestren correctamente en el checkout, es necesario realizar una configuración adicional desde Hermes.&#x20;

A partir de esta versión, **la definición y actualización de las cuotas ofrecidas será responsabilidad de la marca**. Esto les permitirá modificar las opciones de financiación sin necesidad de realizar cambios adicionales.

### Configuración del cc\_code

El **cc\_code** es el código provisto por MODO que define las cuotas que estarán disponibles para los clientes al momento de realizar una compra.

Para configurarlo:

1. Ingresar a **App Store > ModoV2 > Configurar:**

<figure><img src="../../../../../.gitbook/assets/Captura de pantalla 2026-06-29 a las 17.35.28.png" alt=""><figcaption></figcaption></figure>

2. En el selector **cc\_code**, elegir la opción correspondiente según las cuotas que deseen ofrecer, siendo:&#x20;
   * CSI -> Cuotas sin interés
   * CCI -> Cuotas con interés
     * Ejemplo práctico: Si se quiere ofrecer 3, 6, 9 cuotas sin interés y 12 con interés, entonces el cc\_code a configurar es **3CSI-6CSI-9CSI-12CCI**

{% hint style="info" %}
**Para conocer qué código corresponde a cada combinación de cuotas, consultar el archivo provisto por MODO:** [**Listado de cc\_codes**](https://docs.google.com/spreadsheets/d/1F89EGzymeOo7sa0Rq8NkQncrVvSNtTQ039GHJjNOK0k/edit?gid=0#gid=0)**.**&#x20;
{% endhint %}

<figure><img src="../../../../../.gitbook/assets/Captura de pantalla 2026-06-29 a las 17.36.52.png" alt=""><figcaption></figcaption></figure>

3. Guardar los cambios.

{% hint style="warning" %}
**Consideraciones importantes**

* La configuración del **cc\_code es obligatoria** para que las cuotas se muestren correctamente en el checkout.
* El **cc\_code es único**, por lo que deberán seleccionar uno que contemple todas las cuotas que deseen ofrecer.
* Si además de promociones bancarias desean ofrecer otras alternativas de financiación mediante MODO (por ejemplo, 3 cuotas con Santander y, adicionalmente, 3, 6, 9 y 12 cuotas mediante MODO), deberán seleccionar un **cc\_code** que contemple todas las cuotas que quieran ofrecer.
{% endhint %}

### Promociones bancarias

Si cuentan con promociones bancarias asociadas a MODO, deberán informar al banco correspondiente el **site ID (Payway)** o **store ID (Fiserv)** para que dichas promociones continúen funcionando correctamente.

Este dato puede obtenerse ingresando a **App Store > Payway/Fiserv > Configurar:**

**Payway**

<figure><img src="../../../../../.gitbook/assets/Captura de pantalla 2026-06-29 a las 13.20.48.png" alt=""><figcaption></figcaption></figure>

**Fiserv**

<figure><img src="../../../../../.gitbook/assets/Captura de pantalla 2026-06-29 a las 13.23.03.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
### ¿Tenés dudas sobre qué cc\_code utilizar?

La elección del **cc\_code** depende de la estrategia comercial definida para su cuenta de MODO.

Ante cualquier consulta sobre qué código corresponde utilizar o cómo configurar las condiciones comerciales, les recomendamos contactar a su ejecutivo de MODO, ya que se trata de una definición comercial propia de la plataforma.
{% endhint %}

