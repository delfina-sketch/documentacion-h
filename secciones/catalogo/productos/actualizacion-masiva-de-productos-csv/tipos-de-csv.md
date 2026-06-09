# Tipos de CSV

Como mencionamos en el apartado anterior, para poder armar un csv de forma correcta, es necesario entender qué es lo que se quiere editar e identificar si la edición es a nivel ítem o variante.

{% hint style="info" %}
En el siguiente archivo podrás visualizar todas las acciones posibles de actualización: [Modificaciones vía CSV](https://docs.google.com/spreadsheets/d/1watxVk29qfmzZMhgnbFIXE5oP-Z3hQ1o9QIHvMPvmSI/edit?gid=0#gid=0)
{% endhint %}

### Tipos de CSV <a href="#tipos-de-csv" id="tipos-de-csv"></a>

#### CSV Numéricos: <a href="#csv-numericos" id="csv-numericos"></a>

1. **Para activación/desactivación de items/variantes,** tomamos la nomenclatura:

* 1 = para indicar ' verdadero' (activación)
* 0 = para indicar 'falso' (desactivación)

Aplica a la actualización de ítems de los siguientes csv:

* Habilitado #1
* Habilitado #2
* Out of stock
* Outlet
* Excluír promociones bancarias
* Buscador activo
* Pre Order
* Cucardas:
  * Sale
  * Descuento
  * Últimas Unidades
  * Exclusivo
  * Cucarda de imagen #1&#x20;
  * Cucarda de imagen #2
  * Cucarda de texto #1&#x20;
  * Cucarda de texto #2
  * Nuevo

2. **Para edición de parámetros numéricos**: solo se coloca el numero entero por el que se quiere reemplazar la información. Aplican en ítem en los casos de:

* Peso
* Ancho
* Profundidad
* Altura

Aplican en variantes en los casos de:

* Stock
* Pre-Order Stock (si aplica)
* Precio (con centavos y sin coma)
* Precio Especial (con centavos y sin coma)
* Orden de Productos



3. **Para edición de otro parámetro con id (categoría):** solo se coloca el numero del id de la categoría a modificar.
4. Aplican en ítems en los casos de:
   1. Categorías: categoria/s a la cual pertenece
5. Aplican en variantes en los casos de:
   1. Categoría Orden de Productos

**4. Para edición de fechas:** Para estos CSV tomamos la nomenclatura fecha de la siguiente manera: AAAA/MM/DD. Es decir \[Año]/\[Mes]/\[Día]

Aplican en ítems en los casos de:

1. New In Date (Desde)
2. New In Date (Hasta)
3. Pre Order Stock Date

Ejemplo: Si procesáramos el siguiente CSV de variantes a través de la acción "pisar" para modificar la fecha de la cucarda New In para la opción 'Desde', al ítem de id 400 se le activará la cucarda New in desde la fecha subida por csv

![](https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2F2844678769-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F2VP48tuPxvoNgMg0xOJT%252Fuploads%252F8QMAUX4rWDkSl9LbAnFE%252FCaptura%2520de%2520Pantalla%25202024-10-02%2520a%2520la%28s%29%252014.55.11.png%3Falt%3Dmedia%26token%3Daf130475-9d0b-423b-8132-57c7f7badee9\&width=768\&dpr=3\&quality=100\&sign=617234da\&sv=2)

**5. Para edición de parámetros alfanuméricos:** Se colocan los caracteres por los que se quiere cambiar el contenido ya sea para SKU o descripciones que contienen letras, números y caracteres especiales.

Aplican en ítems en los casos de:

1. Cucardas:
   1. Cucarda de texto #1 y #2
2. Propiedades del ítem:
   1. Título
      1. Descripción
      2. Descripción Corta
      3. Solapas descriptivas:
         1. Nota Descripción (si se tiene maquetada)
         2. Nota Composición (si se tiene maquetada)
         3. Nota Cuidado (si se tiene maquetada)
      4. Meta Title
      5. Meta Description
      6. Meta Keywords
3. Aplican en ítems en los casos de:
   1. Título de Variante
   2. Descripción de Variante
   3. Raíz foto

{% hint style="info" %}
Es importante prestar especial atención al contenido de cada columna: si se incluyen comas dentro de un campo que no corresponde dividir (por ejemplo, en descripciones o textos), esto puede generar errores en la estructura del archivo y afectar el procesamiento.

Se recomienda revisar cuidadosamente el archivo antes de subirlo para evitar inconsistencias en la importación.
{% endhint %}

Ejemplo: Se tiene un archivo donde se utilizan comas (,) como carácter especial:

![](https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Flh7-rt.googleusercontent.com%2Fdocsz%2FAD_4nXcZn6Xo6bUhmmqg-HehSGYo9iGSzNjNNdw5eCnUsEoNzVgDm1bhmev2WWJXbDS6J6kttV3Gla91WnjpWVmoYJSr2eSGMAda78p_lzjRN_Ou4TEadWcAdV-O-NbeTwumGBEK5EqlwjTPPEie5JaQmwFGqig%3Fkey%3DtfkwEj1aV71M_FFnShmGKQ\&width=768\&dpr=3\&quality=100\&sign=19311f25\&sv=2)

En caso de querer subir correctamente este archivo, te recomendamos que:

1. Antes de descargar el archivo armado (para subir a Hermés) como formato csv, reemplazar esas comas (,) por algún carácter especial no utilizado (ejemplo guión medio (-), dos puntos (:) o asterisco (\*).

![](https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Flh7-rt.googleusercontent.com%2Fdocsz%2FAD_4nXeG6ocAQp-QnmDq_SHRpn_em6S73SKe4d3V-sviXONmDcNkf0jd5TCdUaSDfu2w7VN9B6MYh3og9BeDU8Yqeyz73wdJHWq8tAepzpl3KMui1_uOYVSnl0s8FNh5LUbWma9SvvfIlY3c0i99Qry3OXxw9WWs%3Fkey%3DtfkwEj1aV71M_FFnShmGKQ\&width=768\&dpr=3\&quality=100\&sign=48861098\&sv=2)

2. Descargar el archivo en formato csv. Ver que al abrirlo en algun editor de texto, las columnas están separadas por comas (,):

<figure><img src="https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Flh7-rt.googleusercontent.com%2Fdocsz%2FAD_4nXcMh4l7R1H29CAA8WUvLQknAtfmA_O0bAlHGLM5ZTgfnm1dreZatWBTROKfFHWOT9per5Xni0CvlbT-qZOK5iEPUHD2bT-lNjioDqnxoDnrN0K8MWlaQZyx61pVDNwU0zoGKPp2NPBEWEfigQrn1s2jM7E1%3Fkey%3DtfkwEj1aV71M_FFnShmGKQ&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=be29b4c9&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

3. Reemplazar las comas (,) por punto y coma (;) utilizando la edición del programa de visualización en formato texto (block de notas o textedit):

<figure><img src="https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Flh7-rt.googleusercontent.com%2Fdocsz%2FAD_4nXedE5oygdWFkecwG3AxQCVGPQl7nP4jg9nnVpQbTjY-8EMZAB8tD30oLMb2aG2nkTwpafhIDPbFgYMJ0sJH73aNnjTxf0EW547L3FggKZAxdxFOr9KXDdHwFPlUI6mVnfKOOZwEXWnBClVLMLpqi4K2gkFc%3Fkey%3DtfkwEj1aV71M_FFnShmGKQ&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=fd0c449&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

4. Reemplazar finalmente el guión medio (-) o caracter utilizado por la coma (,) utilizando la edición del programa de visualización en formato texto (block de notas o textedit):

<figure><img src="https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Flh7-rt.googleusercontent.com%2Fdocsz%2FAD_4nXdgMZLNzGvqMztLd0am72BbaUd9r2f_XGZ6gAJTrmtsb3X88kWVonRZ0mgmLwwguoi7rNSBZQNzyIvfG-EIcralM7lAeAMR2LmeLm7ORmJvLsv4fH6aUNHsXc1rIUfBfupXHolSeiFeUoJQ3TIMZ7i3vRHA%3Fkey%3DtfkwEj1aV71M_FFnShmGKQ&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=b6d310e1&#x26;sv=2" alt="" width="375"><figcaption></figcaption></figure>

**\*En caso de no tener coma como carácter especial, únicamente realizar el punto 2 y 3.**

5. Subir el archivo teniendo en cuenta los pasos explicados en > [Subir CSV](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/2VP48tuPxvoNgMg0xOJT/~/changes/39/productos/edicion-de-productos/edicion-masiva/mediante-archivo-csv/subir-csv)
