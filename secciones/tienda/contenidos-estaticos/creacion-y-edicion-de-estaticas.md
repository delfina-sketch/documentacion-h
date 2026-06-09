# Creación y edición de estáticas

Para crear contenidos estáticos se debe tener un conocimiento básico de HTML.&#x20;

1. Ir a Tienda > Contenidos estáticos > Agregar contenido estático:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 13.09.24.png" alt=""><figcaption></figcaption></figure>

2. Completar los campos solicitados:&#x20;

* Sección: slug/URL a través de la cual se accederá al contenido. Deben ser minúsculas, sin caracteres especiales, y en caso de ser distintas palabras, separadas por guión medio ("-").
* Path: es una definición interna, no visible al usuario. Recomendado: ingresar mismo valor que "sección" pero separar por guión bajo.
* Título: es el título SEO de la página .
* Descripción: es la descripción SEO de la página.
* Visible en header: activar si se quiere mostrar el acceso en el header de la web. Si se quiere mostrar en otro lugar de la web, se deberá solicitar a Producto mediante formulario.
*   Contenido: es el contenido de la estática. Se debe cargar en formato HTML desde el icono de `<>` . El HTML puede contener imágenes, texto, links, etc. y siempre se debe cargar el HTML otorgado por Pow.

    * Para incorporar imágenes, previamente se deben alojar en un servidor público. Luego clickear en el ícono de imagen, y colocar la URL pública de la imagen:

    <figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 13.13.46.png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 13.12.37.png" alt="" width="563"><figcaption></figcaption></figure>

También se pueden sumar videos. Los mismos se cargan igual que las imágenes excepto la parte de borrar el "\_content" que, para los videos es importante que esté.

IMPORTANTE: para que se se visualice correctamente, el video debe estar correctamente maquetado en el HTML de la estática y la URL creada en el servidor tendrá que ser reemplazada siempre que se quiera subir un video nuevo.

### **Editar contenido estático** <a href="#editar-contenido-estatico" id="editar-contenido-estatico"></a>

{% hint style="info" %}
Antes de editar un contenido estático, es muy importante guardar un backup del contenido tal como lo tenemos, de manera que si llegamos a alterar algo de manera involuntaria, podemos volver a atrás simplemente volviendo a cargar el contenido estático anterior tal cual estaba. Este backup siempre debe hacerse desde el código del contenido estático. Es decir, habiendo clickeado el botón  `<>`
{% endhint %}

1. Desde la pantalla principal, buscar la estática a editar e ir al ícono de lápiz:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-12 a las 13.18.19.png" alt=""><figcaption></figcaption></figure>

2. Editar el contenido deseado en el HTML clickeando en el botón `<>` . Algunas de las acciones que podemos realizar desde el editor de contenidos:

* Cambiar/reemplazar una imagen/video: Para cambiar una imagen existente, simplemente debemos cargar la imagen en el servidor como se explicó anteriormente y editar la URL del HTML.

3. Guardar los cambios.
