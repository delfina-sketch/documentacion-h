# Armado de matriz

Una vez recopilada la información, se procederá a armar la matriz que luego se subirá para la creación de los ítems.&#x20;

1. Ingresar a Catálogo > Carga masiva y descargar la tabla de equivalencias.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-03-02 a las 10.15.38.png" alt=""><figcaption></figcaption></figure>

#### Información de una matriz

La matriz de carga contiene:

* **Columnas** con los distintos campos de los productos.&#x20;
* **Cuerpo**: aquí se completará la información correspondientes a cada SKU.

<figure><img src="https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2F2844678769-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F2VP48tuPxvoNgMg0xOJT%252Fuploads%252F4BEWkjSjl6zhROJN1C0y%252FCaptura%2520de%2520pantalla%25202025-09-30%2520a%2520la%28s%29%25203.53.33%25E2%2580%25AFp.%25C2%25A0m..png%3Falt%3Dmedia%26token%3D1bc04cf9-a176-4755-9792-a0fb1d817d42&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=4a3e2c3b&#x26;sv=2" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Pestañas**: siempre trabajaremos sobre la pestaña "Productos". La misma debe estar ubicada en la primera posición a la izquierda. Las demás pestañas servirán como complemento/fuente de datos para completar la matriz.
{% endhint %}

Al descargar la Tabla de equivalencias vendrá con una sku ejemplo para saber como completar los campos de la matriz.

2.  Completar las filas con la información del ítem recopilada en el punto ["Recopilar información de productos"](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/4ixUGi3IayVNsRKEYT0I/~/edit/~/changes/4/secciones/catalogo/carga-masiva/carga-masiva-de-productos/recopilar-informacion-de-productos)

    * **Prototipo (obligatorio):** ID de prototipo (valor numérico). Por lo general, las marcas tienen un prototipo único para todos los productos, excepto si cambia la característica del ítem (ej: perfumes).
    * **Categoría (obligatorio)**: ID’s de categorías separados por coma (por ejemplo: 1,30,32).
    * **SKU (obligatorio)**: Valor único de cada producto. Recomendación: Generar una columna auxiliar con la fórmula _=LARGO_ para corroborar mismo largo en caracteres.
    * **ALT:** Es un atributo HTML para un texto que describe una imagen. El atributo ALT se coloca directamente en la etiqueta de la imagen. Si una imagen no se puede mostrar por alguna razón, el atributo ALT proporciona texto alternativo para mostrar en su lugar. Los motores de búsqueda utilizan este atributo para identificar el contenido de la imagen, ya que los archivos de imagen generalmente no pueden ser leídos por los crawlers de los motores de búsqueda. También es útil proporcionar un texto alternativo para los usuarios y específicamente para los usuarios con discapacidad visual que tienen sitios web leídos por programas de lectura.
    * **Stock (obligatorio)**: puede completarse con valor “0” y luego reemplazarse via CSV.
    * **Precio (obligatorio)**: se debe cargar con centavos y sin el signo de pesos. Ej: si el precio es $1000, se debe completar la celda como: 100000. Puede cargarse con valor “0” y luego reemplazarlo vía CSV.
    * **Color (obligatorio):** es un campo de texto, se debe completar con el mismo nombre de color que se creó en Hermes. Se puede utilizar una fórmula (buscarv) o validador de datos que levante el listado de colores creados en la pestaña “colores”.
    * **Color ID (obligatorio)**: Se debe cargar el ID del color (número) que se asignó en Hermes. Se pueden ver los ID de los colores en la pestaña "Color". Ej: el id del color negro es #4
    *   **Raíz Foto (obligatorio)**: Todas las fotos de una misma variante de color de un producto deben tener el mismo valor. Los más frecuentes son: Código ART + Código Color

        o NombrePrenda + NombreColor.
    * **Talle (obligatorio)**: Recomendamos utilizar un validador de datos que se alimente del listado de talles creados en la pestaña “talles”. Otra opción es levantar el código de talle del SKU en una columna auxiliar, y a partir de ahí tomar el color vs una tabla de equivalencias.
    * **Talle ID (obligatorio)**: ID único (número) correspondiente a cada valor de la propiedad "talle". Se puede obtener el ID desde la pestaña Talle.
    * **Título**: Nombre del producto (permite caracteres especiales)
    * **Descripción (obligatorio)**: Descripción de producto. Permite caracteres especiales.
    * **Descripción corta (opcional):** Descripción corta/alternativa de producto. Permite caracteres especiales. Puede utilizarse como campo auxiliar para definir keywords relacionados al producto (ayudará en búsquedas en el sitio luego)
    * **Dimensiones (obligatorio)**: es recomendable utilizar una columna auxiliar con “tipo de producto” y cruzarla contra una tabla de equivalencias con las medidas establecidas.
    * **Código de Fabricante (obligatorio)**: Distingue productos y define qué SKU's son variantes de un mismo Item. Todas aquellas variantes que pertenezcan a un mismo producto (ya sea color o talle) deben tener el mismo valor. Es recomendable utilizar código de artículo del SKU. Si utilizamos el Código de Fabricante de un ítem ya creado anteriormente, se crearán variantes dentro del ítem existente.
    * **Meta Title / Meta Description / Meta Keywords (opcionales):** Son descripciones para SEO.&#x20;
      * **Cantidad de caracteres recomendados:**
        * Meta title: Hasta 60 caracteres
        * Meta description: Hasta 155 caracteres
        * Meta Keywords: Hasta 40 caracteres


3. Una vez armado el archivo de la matriz, se debe guardar en **formato Excel (XLSX)**.&#x20;

{% hint style="info" %}
El archivo NO debe tener fórmulas, asegurarse que esté sin formato.&#x20;
{% endhint %}
