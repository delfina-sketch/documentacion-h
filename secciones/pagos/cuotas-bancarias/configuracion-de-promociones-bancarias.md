# Configuración de promociones bancarias

Las promociones bancarias o de financiación son aquellas promociones que pueden aplicarse siempre y cuando se tenga:

* Códigos de comercio propios de cada tarjeta.
* Integración de algún procesador de pagos que procesen esas operaciones.&#x20;

{% hint style="info" %}
Consultá los procesadores de pagos nativos integrados en Hermes desde App Store.
{% endhint %}

#### **Combinaciones de Financiación & Medios de Pago** <a href="#combinaciones-de-financiacion-and-medios-de-pago" id="combinaciones-de-financiacion-and-medios-de-pago"></a>

Cada combinación posible entre las cuotas y medios de pago deben crearse como una promoción aparte. Veamos los ejemplos a continuación:

**Ejemplo plan "Ahora":**

Promoción Ahora 3 y Ahora 6 con Visa, Master y Amex.

Promociones a crear/cargar:

1. 3 cuotas Visa
2. 3 cuotas Master
3. 3 cuotas Amex
4. 6 Cuotas Visa
5. 6 Cuotas Master
6. 6 Cuotas Amex

**Ejemplo descuentos especiales:**

Promoción Especial Santander 25% Ahorro Cartera General (visa & amex), 30% Tarjetas Select (visa & amex) + Hasta 3 Cuotas

Promociones a crear/cargar:

1. 1 Cuota y 25% Visa
2. 1 Cuota y 30% Visa Select
3. 2 Cuotas y 25% Visa
4. 2 Cuotas y 30% Visa Select
5. 3 Cuotas y 25% Visa
6. 3 Cuotas y 30% Visa Select
7. 1 Cuota y 25% Amex
8. 1 Cuota y 30%Amex Select
9. 2 Cuotas y 25%Amex
10. 2 Cuotas y 30%Amex Select
11. 3 Cuotas y 25%Amex
12. 3 Cuotas y 30%Amex Select

### Creación de promoción bancaria

1. Ir a Pagos > Cuotas bancarias > Nueva promoción

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-05 a las 16.06.24.png" alt=""><figcaption></figcaption></figure>

2. Completar los datos solicitados:&#x20;



<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

* Nombre: Nombre de la promo que se verá en el selector del checkout. Ejemplo: _20% off con Santander Rio_
* Descripción: Es de uso interno para dejar anotaciones adicionales. No se visualiza en el front.
* Tipo de promoción: Elegir siempre "Común".
* Estado:&#x20;
  * Pendiente: La promoción está en formato borrador.
  * Activo: Si la promo está dentro de la fecha y días configurados, se encuentra activa y visible para el usuario.&#x20;
  * Standby: La promoción está pausada. Se activará nuevamente según la configuración de días y fechas y si es recurrente o no.&#x20;
  * Completado: La promoción ya finalizó; es decir, se cumplió la fecha de vencimiento configurada.&#x20;
* Posición: Determina la posición de la promoción dentro del selector del checkout. Se utiliza generalmente para dejar en las primeras posiciones las promociones más relevantes.&#x20;
* Configuración de bancos y tarjetas:
  * Banco: Seleccionar los bancos a los que aplica la promoción. Si no se encuentra el banco, crear uno mediante el botón "Crear nuevo banco".&#x20;
  * Tarjeta de crédito: Seleccionar las tarjetas a las que aplica la promoción. Si no se encuentra la tarjeta, crearla mediante el botón "Crear nueva tarjeta".&#x20;
  * Cuotas (obligatorio): Configurar la cantidad de cuotas de la promoción. El campo no puede quedar vacío; si la promo es de una cuota, colocar 1.&#x20;
  * Descuento banco (opcional): Colocar el valor del descuento que hace el banco
  * Interés (obligatorio): Colocar el valor numérico si corresponde cobrar un interés por las cuotas.
    * Si no se desea cobrar interés, dejar 0.
    * Si se desea cobrar interés completar con el porcentaje de interés. Importante: Se debe colocar en decimales. Ejemplo: Si el descuento otorgado por el banco es del 10% se debe colocar 0,1.&#x20;
  * Valor mínimo (opcional): Configurar el valor mínimo de compra para que la promoción sea visible en el checkout.
    * Si no se tiene valor mínimo, dejar en 0.
    * Si se tiene un valor mínimo, completar con número entero (sin comas ni puntos) y la promoción aplicará siempre que se supere ese valor.
* Duración de la promoción:&#x20;
  * Activo desde - hasta: Fecha y hora de inicio y fin de la promoción.&#x20;
  * Recurrencia: Si una promoción es recurrente, activar el toggle. La promo se activará los días configurados.
  * Días activo: configurar los días que debe estar activa la promoción.&#x20;
  * Restricciones y opciones:&#x20;
    * Full price: hace referencia a los productos que tienen precio tachado y define si la promoción se aplica sobre el special price o sobre el full price.
      * Si la promoción debe aplicarse sobre el **special price**, **no activar** el check.
        * &#x20;En caso de tener un cupón de descuento aplicado sobre special price y se tenga el check activo de Full price, el descuento se hará sobre full price.
      * Si debe aplicarse sobre el **full price**, **activar** el check.
    * Restringir cupones: Si se quiere restringir cupones para la promoción, se debe activar y colocar el código de los cupones. Si hay un cupón restringido, el usuario perderá el descuento aplicado al pagar con la promoción. Pagará el valor de producto sin el descuento del cupón.
    * Solo nacionales: Define si la promoción aparecerá en el selector de promociones del checkout según los ítems del carrito. Para que funcione correctamente, es necesario activar el check **“Producto nacional”** en los ítems correspondientes. Por ejemplo, si se desea excluir un producto de una promoción bancaria específica, se debe marcar este check en el producto y activar la restricción en la promoción.
      * Las promociones con restricción por **producto nacional** solo se aplicarán a los productos que tengan ese check habilitado.
      * Siempre que exista al menos una promoción aplicable sin restricciones, el **medio de pago y la promoción** se mostrarán en el checkout.
    *   Restringir promociones de carrito: define si la promoción bancaria es o no acumulable con promociones de carrito.

        *   Si se activa este check:

            * Si el carrito contiene una promoción de carrito, la promoción bancaria no aparecerá en el selector de promociones del checkout.
            * Si el carrito no contiene una promoción de carrito, la promoción bancaria sí aparecerá en el selector de promociones del checkout.

            Es decir, las promociones bancarias con esta restricción no se mostrarán cuando el carrito ya tenga aplicada una promoción de carrito.

            * Importante: esta configuración no aplica a las promociones de carrito del tipo “Envío gratis”. En esos casos, la promoción bancaria seguirá visible aunque el check “Restricción en promociones de carrito” esté activado.
            * Además, si todas las promociones bancarias tienen este check activo, el banner de Fiserv/Payway no se mostrará, ya que no habría promociones bancarias disponibles para aplicar.
            * Siempre que exista al menos una promoción sin restricciones aplicables, el medio de pago y la promoción correspondiente se mostrarán en el checkout.



        3.Guardar los cambios. <br>

{% hint style="info" %}
**Consideraciones adicionales**

* Si hay una promoción que se repite, se puede reutilizar una promoción completada alterando las fechas y su estado.
* Si las condiciones de la acción cambian, _**siempre**_ se debe crear una nueva.
* Las promociones aplican sobre precio actual de los artículos a menos que tengan aplicada la restricción por cupón. Si se quisiera evitar que determinados productos se puedan comprar por estas promociones, los mismos deben deshabilitarse durante la duración de la acción.
* Es importante aclarar que los códigos de comercio deben estar adheridos a los planes/promociones de entidades que correspondan (bancos, medios de pago, planes de gobierno, etc) para que las operaciones que se procesen sean identificadas como tales y respeten las condiciones acordadas. Por ejemplo: si no se encuentra adherido el código de comercio de online a una promoción de reintegro bancario, el usuario no recibirá el reintegro del banco, por más que la promoción esté configurada en web. Lo mismo aplica para planes de financiación.
{% endhint %}

