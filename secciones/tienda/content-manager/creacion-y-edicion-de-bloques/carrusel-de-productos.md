# Carrusel de productos

Este bloque permite mostrar un carrusel de productos destacados. Contiene elementos adicionales como título y banner (sujeto a maquetado).&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.51.35.png" alt=""><figcaption></figcaption></figure>

### Configuración <a href="#configuracion" id="configuracion"></a>

1. En "Agregar sección" elegir la opción Carrusel de productos:

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.54.16.png" alt=""><figcaption></figcaption></figure>

2. En el panel lateral, completar los campos solicitados:&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.55.31.png" alt=""><figcaption></figcaption></figure>

* **Nombre interno:** Es de uso interno para identificar y organizar los bloques más fácilmente.
* **Ancho**: en el caso de skucarrousel el ancho siempre será del 100% para desktop y mobile en Sku Carrousel que NO tiene imagen. En caso de que tenga imagen, el carrousel se dispondrá al 66% y la imagen al 33%.

Importante: No configurar en esta sección el ancho, se ajustará solo dependiendo si tiene o no imagen configurada.

* **Título**: arriba de cada carrusel de productos, se puede colocar un título que acompañe el contenido.
* **Productos:** se deberán colocar los skus que se deseen mostrar en el carousel (se permiten hasta 10 productos como máximo para la correcta performance de carga de la home).
  * Al escribir un SKU, se validará si el ítem se encuentra habilitado y si la variante cuenta con stock. En el caso de que alguna de las dos condiciones no se cumpla, no se visualizará el sku en el selector.
  * Al hacer Enter, el SKU se cargará en formato de tag. Se podrá modificar el orden del sku carrusel de productos sin necesidad de eliminar el bloque completo con un drag and drop.
* **Programación:** una vez cargados todos los productos, se deben configurar los días y horarios de inicio y fin de visualización del banner.
*   **Configuración adicional:** Si se tiene maquetado el carrusel de productos con banner, adicionalmente se deberá cargar el banner desktop y mobile:&#x20;

    * **Imagen desktop:** se puede cargar una imagen que se verá a la izquierda / derecha del carousel (según maquetado)
    * **Imagen mobile:** se debe cargar una imagen que se verá como fondo del sku carousel (según maquetado)

    <figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 11.00.42.png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 11.02.27.png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="info" %}
### Consideraciones de visualización <a href="#consideraciones-de-visualizacion" id="consideraciones-de-visualizacion"></a>

* Si en el sku carousel se carga una variante que **no tiene foto en ninguno de sus talles, pero sí la tiene el ítem (imagen principal)** el front levantará la foto del **ítem.**
* Si en el sku carousel se carga una variante que **no tiene foto pero su otra variante de talle sí la tiene**, el front levantará la foto de la variante que tiene la misma.
* Si en el sku carousel cargan una variante y **ni el ítem ni ninguna variante tiene foto**, no se mostrará en el front.
* Si el ítem del sku cargado en el carousel **está deshabilitado**, no se mostrará en el front (ver la información del tag antes de seleccionar)
* Si el SKU **no tiene stock** no se mostrará en el front (ver la información del tag antes de seleccionar).
{% endhint %}

3. Luego de configurar todo, guardar los cambios. El bloque se guardará con estado oculto, y se deberá activar su visualización clickeando en el ícono de ojo:&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 12.09.50.png" alt=""><figcaption></figcaption></figure>
