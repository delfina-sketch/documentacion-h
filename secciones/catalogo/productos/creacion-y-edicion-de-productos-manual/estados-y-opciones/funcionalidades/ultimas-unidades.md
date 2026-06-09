# Últimas unidades

La funcionalidad **Últimas Unidades** permite informar al cliente cuando un producto se encuentra próximo a agotarse.\
Su objetivo es generar un sentido de urgencia que incentive la decisión de compra.

Esta funcionalidad se compone de dos elementos:

1\. Cucarda “Últimas Unidades”: Cuando una variante alcanza un nivel bajo de stock (según la configuración del sistema), se activa automáticamente una **cucarda** que destaca la disponibilidad limitada del producto.

2. Leyenda informativa en la ficha: Además de la cucarda, se muestra una **leyenda en la ficha del producto** indicando la cantidad de unidades disponibles para cada variante (por ejemplo, por talle y color). Esto brinda información clara al usuario sobre el stock restante.

### Condiciones para que ambos elementos se visualicen en la web

Para que la cucarda y leyenda aparezcan en la card y ficha del ítem, deben cumplirse ambas condiciones:

* La cucarda **“Últimas Unidades”** debe estar activa en el ítem.
* El total de unidades de las variantes del color seleccionado debe ser **igual o menor al umbral configurado en el sistema**.

### Visualización en web

Cucarda:

<figure><img src="../../../../../../.gitbook/assets/image (24).png" alt="" width="563"><figcaption></figcaption></figure>

Leyenda

<figure><img src="../../../../../../.gitbook/assets/image (25).png" alt="" width="563"><figcaption></figcaption></figure>

### Lógica de la funcionalidad

Luego de activar la cucarda, se deberá configurar el umbral de unidades disponibles.&#x20;

* Si el total de las variantes del ítem es igual o menor al umbral configurado -> La cucarda y leyenda se activarán en el ítem.&#x20;
* Si el total de las variantes del ítem es mayor al umbral configurado -> La cucarda y leyenda no se activarán en el ítem.&#x20;

{% hint style="info" %}
Consideraciones adicionales

* Si el producto tiene todas sus variantes de color creadas dentro del mismo ítem, en la sábana la cucarda se mostrará en la card del producto de todos los colores.
* En la ficha de producto, el stock se valida a nivel variante. Por lo tanto, no se mostrará hasta que el usuario seleccione un talle. La misma solo aparecerá cuando la combinación específica de talle y color tenga un stock igual o menor al umbral configurado en el sistema.
{% endhint %}

{% hint style="info" %}
Consultá como activar la cucarda y leyenda en la sección "[Últimas unidades](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/4ixUGi3IayVNsRKEYT0I/~/edit/~/changes/4/secciones/catalogo/productos/creacion-y-edicion-de-productos-manual/estados-y-opciones/cucardas/ultimas-unidades)" de "Cucardas".
{% endhint %}
