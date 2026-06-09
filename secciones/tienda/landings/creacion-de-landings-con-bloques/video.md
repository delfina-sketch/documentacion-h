# Video

Este bloque permite configurar videos, en diferentes formatos:&#x20;

* Vimeo (recomendado)
* YouTube (recomendado)
* MP4&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 12.13.30.png" alt=""><figcaption></figcaption></figure>

### Configuración

1. En "Agregar sección" elegir la opción Video:&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 12.15.21.png" alt=""><figcaption></figcaption></figure>

2. En el panel lateral, completar los campos solicitados:&#x20;



<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 12.16.04.png" alt=""><figcaption></figcaption></figure>

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

* Título: es el título que va sobre la imagen
  * Color del título: es el color que llevará el título del punto anterior.
* Subtítulo: es el subtítulo que va sobre la imagen y debajo del título con menor jerarquía
  * Color del subtítulo: es el color que llevará el título del punto anterior.
* Texto del botón CTA: es el texto del botón, ejemplo "Ver más".
  * Color del texto del botón: es el color que llevará el título del punto anterior.
* Fuente del video: se debe elegir si se cargará en MP4, Vimeo o Youtube.
  * MP4: si se elige esta opción, se deberá cargar:&#x20;
    * el video en desktop y mobile.
    * Link del botón CTA&#x20;
  * Vimeo: si se elige esta opción, se deberá cargar:&#x20;
    * &#x20;URL completa o el ID del video. Si se coloca la URL completa, el sistema dejará solamente el ID del video que es lo que se necesita.
      * Adicionalmente hay algunas configuraciones posibles de realizar para que el video tenga sonido, que se encuentran en la URL del video: **controls=0\&background=1\&autoplay=1\&loop=1\&muted=1**&#x20;
        * Teniendo en cuenta que la información adicional es activada con el número 1 y desactivada con el número 0. Para configurarla, a continuación se explica cada uno de los campos que componen la información adicional dentro de la URL:
          * Controls: Este parámetro ocultará todos los elementos del reproductor (barra de reproducción, botones para compartir, etc.) para una experiencia sin bordes.
            * Activado: controls=1
            * Desactivado: controls=0
          * Autoplay: Este parámetro hará que se inicie automáticamente la reproducción del video.
            * Activado: autoplay=1
            * Desactivado: autoplay=0
          * Loop: Este parámetro hará que se vuelva a reproducir el vídeo cuando llegue al final, infinitamente.
            * Activado: loop=1
            * Desactivado: loop=1
          * Muted: Este parámetro hará que el video sea silenciado al cargar. Los espectadores aún pueden ajustar las preferencias de volumen en el reproductor.
            * Activado: muted=1
            * Desactivado: muted=0
  * Youtube: de la URL que se quiera colocar, solo se deberá llenar el campo con lo que está luego del signo igual (=). Ejemplo: de la URL [https://www.youtube.com/watch?v=BgH9sY98lTE](https://www.youtube.com/watch?v=BgH9sY98lTE) solo se deberá colocar **BgH9sY98lTE**.

{% hint style="info" %}
Por limitaciones de los navegadores no es posible reproducir un video en autoplay y con sonido al mismo tiempo. En caso de necesitar que el video tenga sonido, será necesario habilitar los controles del reproductor. Si se prefiere no mostrar todos los controles, pueden solicitar a través del formulario el maquetado de un botón personalizado.
{% endhint %}

* Link del botón CTA: es la URL del botón, a la que será redireccionado el usuario si clickea en el mismo.&#x20;
* Estilos de botón:&#x20;
  * Estado normal: Se debe definir color de fondo y borde en condiciones normales (sin hover)
  * Estado hover: Se debe definir color de texto, fondo y borde en condiciones de hover (posicionándonos por encima del botón)
* **Programación:** una vez cargados todos los productos, se deben configurar los días y horarios de inicio y fin de visualización del banner.

{% hint style="info" %}
Consideraciones

* **Duración**: 10 a 30 segundos.
* **Resolución**: 720p es ideal. Evita 4K o resoluciones muy altas para no sobrecargar la web.
* **Peso**: Lo ideal es que el archivo no pese más de 5 MB para no comprometer la velocidad de carga de la web.
* **Compresión**: Usa herramientas de compresión como [HandBrake](https://handbrake.fr/) o [FFmpeg](https://ffmpeg.org/) para reducir el tamaño del archivo sin perder mucha calidad.
{% endhint %}

3. En la pestaña de SEO completar:

* Slug (URL): es el slug que estará al final de la URL. Ejemplo: www.misitio.com<mark style="color:$success;">**/faqs**</mark>
* Título de la landing: Es de uso interno y sirve para identificar las landings.
* Descripción interna: Es de uso interno, explicar brevemente de que se trata la landing.
* SEO:
  *   Completar:

      * Título: corresponde al meta title del HTML. Sirve para indicar el título de la página en buscadores (como Google) y mejorar su posicionamiento SEO.
      * Descripción: corresponde al meta description del HTML. Sirve para indicar el título de la página en buscadores (como Google) y mejorar su posicionamiento SEO.

      <figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 13.34.58.png" alt=""><figcaption></figcaption></figure>

4. Si se quiere publicar, ir a "Publicar", caso contrario guardar los cambios desde "Guardar".&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 13.43.23.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
La visualización de bloques se podrá activar y desactivar con el ícono del ojo ubicado al lado de cada bloque creado.
{% endhint %}

