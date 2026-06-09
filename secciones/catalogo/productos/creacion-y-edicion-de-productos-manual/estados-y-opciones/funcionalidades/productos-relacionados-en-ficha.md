# Productos relacionados en ficha

El **carrusel de productos relacionados** es una funcionalidad de la ficha de producto que muestra artículos similares o complementarios al que el usuario está visualizando.

Su objetivo es enriquecer la experiencia de compra y potenciar la conversión mediante estrategias de:

* Cross-selling: Sugiere productos complementarios al que se está viendo. Ejemplo: si el usuario está visualizando una remera, el carrusel puede mostrar pantalones, mochilas o zapatos que completen el look.
* Up-selling: Sugiere versiones superiores o de mayor valor del producto actual.\
  Ejemplo: si el usuario está viendo una campera símil cuero, puede mostrarse una campera de cuero como alternativa premium.

De esta manera, el carrusel no solo mejora la navegación, sino que también contribuye a incrementar el ticket promedio al presentar opciones adicionales o de mayor valor.

<figure><img src="../../../../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

#### Configuración

Actualmente existen tres modalidades de configuración:

1.  Manual: Permite seleccionar productos específicos desde la ficha del ítem.

    1. Ingresar al producto > Variantes.
    2. En cada variante, colocar el nombre o SKU en el campo "Variantes relacionadas".&#x20;

    <figure><img src="../../../../../../.gitbook/assets/Captura de pantalla 2026-02-27 a las 14.07.11.png" alt="" width="563"><figcaption></figcaption></figure>

    c. Guardar los cambios.
2. Automática: El sistema toma productos de la misma categoría de manera automática.
3. Por categoría (CSV): Permite definir relaciones mediante una carga masiva por archivo CSV. Consultá la sección "[Actualización de productos masiva (CSV)](https://app.gitbook.com/o/YqXgoQkfPbRYP7oDCRpr/s/4ixUGi3IayVNsRKEYT0I/~/edit/~/changes/4/secciones/catalogo/productos/actualizacion-de-productos-masiva-csv)" para mas información.&#x20;

{% hint style="info" %}
**Consideraciones generales**

* Para que un producto se visualice en el carrusel debe:
  * Tener imagen y precios cargados.
  * Tener stock disponible.
  * Estar habilitado.
{% endhint %}

#### Prioridad de visualización

El sistema respetará el siguiente orden de prioridad:

1. Carga manual
2. Carga por CSV (por categoría)
3. Configuración automática (por categoría)

#### Cantidad de productos visibles

En la ficha de producto se mostrarán hasta **6 productos relacionados**.

Al aplicarse la regla de asignación por categoría, si la categoría contiene menos de 6 productos (por ejemplo, 3), los espacios restantes se completarán automáticamente con productos pertenecientes a la misma categoría del producto que se está visualizando.
