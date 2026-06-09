# Carrusel de banners

Este bloque permite configurar un carrusel de banners que se van mostrando dinámicamente.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.41.34.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Consideraciones**

* Formato de archivo permitido (cada banner): JPG / PNG / GIF
* Peso recomendado: 200-400 kb
* Restricción peso: 2MB
{% endhint %}

### Configuración

1. En "Agregar sección" elegir la opción Carrusel de banners:

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.42.49.png" alt=""><figcaption></figcaption></figure>

2. En el panel lateral, completar los campos solicitados:&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.43.20.png" alt=""><figcaption></figcaption></figure>

* **Nombre interno:** Es de uso interno para identificar y organizar los bloques más fácilmente.
* **Ancho**: es el ancho que tendrá el carrousel de imágenes en la home versión desktop. Se pueden combinar las opciones de ancho dispuestas (33%, 66%, 25%, 50%, 75% & 100%) según quiera, siempre teniendo en cuenta que deberá sumar 100% al completar una fila. Las variantes de combinaciones pueden ser:
  * 100% (full width / full ancho)
  * 50% - 50%
  * 75% - 25% (o viceversa)
  * 66% - 33% (o viceversa)
  * 33% - 33% - 33%
  * 25% - 25% - 50% (cualquiera sea su orden)

El alto de las imágenes/elementos a implementar debe ser el mismo para los bloques que correspondan a una misma fila.

En la versión mobile siempre habrá un solo ancho del 100%.

* **Título del carrusel**: es un texto visible que se muestra sobre el carrusel.
* **Posición del texto**: hace referencia a la ubicación de Título, subtítulo y botón y pueden ser, left (izquierda), right (derecha) o center (Centro).&#x20;
* Items del carrusel: en esta sección se deberá ir cargando los banners a mostrar desde "Agregar item" y completar la configuración de cada uno.&#x20;
  * Título: es el título que va sobre la imagen
  * Subtítulo: es el subtítulo que va sobre la imagen y debajo del título con menor jerarquía
  * Texto del botón: es el texto del botón, ejemplo "Ver más".
  * URL: es la URL del botón, a la que será redireccionado el usuario si clickea en el mismo.&#x20;
  * Estilos de botón:&#x20;
    * Estado normal: Se debe definir color de fondo y borde en condiciones normales (sin hover)
    * Estado hover: Se debe definir color de texto, fondo y borde en condiciones de hover (posicionándonos por encima del botón)
  * Imagen desktop: corresponde a la imagen del banner que se visualizará en la versión de desktop.
  * Imagen mobile: corresponde a la imagen del banner que se visualizará en la versión de mobile.
  * Programación: una vez cargados todos los banners con sus configuraciones, se deben configurar los días y horarios de inicio y fin de visualización del banner.

3. Luego de configurar todo, guardar los cambios. El bloque se guardará con estado oculto, y se deberá activar su visualización clickeando en el ícono de ojo:&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 10.49.52.png" alt=""><figcaption></figcaption></figure>
