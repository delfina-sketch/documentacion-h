# Carga de imágenes

Una vez importados los productos, se debe proceder a la carga masiva de imágenes.

1. Ingresar a Catálogo > Carga masiva > Pestaña "Imágenes desde Dropbox.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-02 a las 11.30.33.png" alt=""><figcaption></figcaption></figure>

2. Elegir la carpeta que contiene las fotos a subir:&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-02 a las 12.04.28.png" alt=""><figcaption></figcaption></figure>

Si la carpeta no se visualiza puede ser por varios motivos:&#x20;

1. El token de la integración de Dropbox se encuentra desactualizado en Hermes. Para corroborarlo:

* En Dropbox: Ingresar a [https://www.dropbox.com/developers/apps/](https://www.dropbox.com/developers/apps/)  > ingresar a la carpeta de la aplicación > generar un nuevo token desde "Generated access token" y copiarlo.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-02 a las 12.09.08 (2).png" alt="" width="563"><figcaption></figcaption></figure>

* En Hermes: Buscar la integración de Dropbox en "App store" y copiar el token generado en Dropbox en el campo "Token":&#x20;

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-02 a las 12.15.29.png" alt="" width="563"><figcaption></figcaption></figure>

3. Hacer click en "Iniciar carga de fotos". Las fotos comenzarán a procesarse, y en Dropbox se crearán dos carpetas nuevas automáticamente:&#x20;

* **Procesadas:** en esta carpeta figurarán todas fotos cargadas exitosamente.
* **Descartadas:** en esta carpeta figurarán todas las fotos que no pudieron subirse por errores.

<figure><img src="https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2F2844678769-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F2VP48tuPxvoNgMg0xOJT%252Fuploads%252F79IdTJts96yTSZmPbg1S%252FCaptura%2520de%2520pantalla%25202025-05-22%2520a%2520las%25202.48.16%25E2%2580%25AFp.%25C2%25A0m..png%3Falt%3Dmedia%26token%3D62164fc4-dec4-47c3-8382-ee8d8240e294&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=6abcce4f&#x26;sv=2" alt=""><figcaption></figcaption></figure>

**Errores frecuentes:**

* Nomenclatura incorrecta.
  * Producto no creado en Hermes.
  * Tamaño no permitido.
  * Productos con nombre repetido&#x20;
  * El producto ya tiene fotos cargadas previamente.

{% hint style="info" %}
Hay imágenes que pueden quedar fuera de las dos carpetas mencionadas. Esto puede ocurrir por los siguientes motivos:

1. **El procesamiento se detuvo (time out):** en estos casos, la solución es volver a reprocesar las imágenes afectadas.
2. **La raíz foto del nombre de la imagen no coincide con ninguna raíz foto registrada en Hermes:** en este caso, se debe realizar una revisión manual para detectar el error, corregir el naming y luego volver a procesar las imágenes.
{% endhint %}

4. Una vez que terminamos de cargar los productos con las imágenes seleccionamos "Finalizar importación".

