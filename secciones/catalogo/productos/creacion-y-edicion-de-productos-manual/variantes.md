# Variantes

### Variantes

La pestaña **Variantes** permite crear diferentes versiones de un mismo producto, por ejemplo:

* Talle (S, M, L)
* Color (Negro, Blanco)
* Combinaciones (ej: Negro - M)

{% hint style="info" %}
Para poder crear variantes es necesario crear previamente un **Prototipo** con sus respectivas **Propiedades**.

Dentro de cada propiedad deberán configurarse los valores correspondientes (por ejemplo: S, M, L para talle; Negro, Blanco para color).

Consultá [Prototipos](../../prototipos/) y [Propiedades](../../propiedades/) para más información.&#x20;
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Para agregar una variante:

1. Hacer click en "Agregar primera variante".
2. Completar los campos obligatorios que se detallan a continuación.&#x20;

#### Campos de la variable

1. SKU (obligatorio): es el código interno único del producto, por lo que no puede repetirse. Ejemplo: <mark style="color:$success;">001</mark><mark style="color:$danger;">RO</mark><mark style="color:blue;">01</mark>; siendo <mark style="color:$success;">001</mark> el código de producto, <mark style="color:$danger;">RO</mark> el código de color (rojo) y <mark style="color:$primary;">01</mark>, el talle.&#x20;
2. Stock (si no se completa es 0): Cantidad de unidades disponibles para la venta. Solamente debe cargarse el stock de depósito central. El stock de locales se informará vía api.&#x20;

* Si el stock llega a 0, el producto no se mostrará en la web para comprar.

3. Pre-stock (opcional): Es el stock de preventa. Se utiliza cuando el producto está por ingresar.

{% hint style="info" %}
Para conocer la funcionalidad consultá Pre order.
{% endhint %}

4. Recomendados de carrito (opcional): Permite mostrar variantes específicas en el carrito, como productos sugeridos.&#x20;

{% hint style="info" %}
Para más información, consultá [Productos sugeridos del carrito](https://pow-ecommerce.gitbook.io/hermes/productos/catalogacion-de-productos/carga-manual/informacion-de-variantes/funcionalidades/productos-sugeridos-del-carrito) .
{% endhint %}

5. Precio (si no se completa es 0): Precio normal de venta de la variante.&#x20;

* Colocar solo números.&#x20;
* No colocar centavos.
* No colocar símbolo de moneda.

6. Precio especial (opcional): Precio promocional de venta de la variante. Si se completa, se mostrará el precio original tachado.

* Colocar solo números.&#x20;
* No colocar centavos.
* No colocar símbolo de moneda.

7. Propiedades de la variante (obligatorio): En esta sección se asignan los valores específicos de cada variante según las propiedades definidas en el **Prototipo** (por ejemplo: Color, Talle, Material, etc.). Cada variante debe tener asignado un único valor por propiedad.

{% hint style="info" %}
Esta sección solo estará disponible si previamente se seleccionó un Prototipo en la pestaña **Información básica**.
{% endhint %}

8. Variantes relacionadas (opcional): Permite vincular productos relacionados en la ficha del producto. Se pueden buscar por SKU o nombre. Sirve principalmente para cross-selling.

Ejemplo: Mismo modelo en otro color. O productos de misma categoría.

{% hint style="info" %}
Para más información, consultá Productos relacionados en ficha.
{% endhint %}

9. Imágenes de la variante (si no se completa no se visualiza la variante en la web): Se pueden cargar hasta 8 imágenes específicas para cada variante.
10. Video (opcional): Permite subir un video específico para esa variante.

{% hint style="info" %}
Con el fin de evitar demoras en la carga de sábana y ficha, recomendamos tener en cuenta las siguientes consideraciones de video:

1. Características del video:
   * Formato: MP4
   * Peso máximo: 2MB
   * Compresión: Media
   * Dimensión: debe tener mismas dimensiones que las imágenes de la sábana
   * Tamaño: debe tener el tamaño que las imágenes de la ficha.
   * Duración máxima: 15 segundos
2. El video puede estar ubicado en la primer o última posición de la ficha y de la sábana, no entre medio de imágenes.
3. En ficha, dicho video tendrá un ícono por encima del mismo para que el usuario interprete que es un video
{% endhint %}

## Checklist final antes de crear el producto

Antes de hacer clic en **Crear**, verificar:

☑ Prototipo seleccionado\
☑ Categorías asignadas\
☑ Imagen principal cargada\
☑ Producto habilitado\
☑ Precio cargado\
☑ Stock cargado\
☑ SEO completo\
☑ Dimensiones completas
