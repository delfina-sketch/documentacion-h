# Recopilar información de productos

Lo primero que se debe hacer es recolectar toda la información de los ítems.&#x20;

### Datos obligatorios requeridos para la carga

* Prototipos creados con sus propiedades correspondientes
* Categorías creadas
* SKU
* Color
* Color ID
* Talle ID
* Título del producto
* Descripción larga y corta
* Alto de producto
* Largo de producto
* Profundidad de producto
* Peso de producto
*   Raíz foto: Es el naming definido para las imágenes de producto. Este dato permite que, al cargarse las fotos, Hermes pueda asociarlas correctamente al producto correspondiente.

    Es un campo obligatorio y no debe quedar vacío. La raíz foto se compone de: **código de ítem + color**. Ejemplo: **1497NE**.
*   Código de fabricante: Este dato se utiliza para unificar variantes dentro de un mismo ítem.

    Por ejemplo, si un producto se comercializa en color rojo y verde y se desea que ambas opciones se visualicen dentro de la misma ficha de producto, el código de fabricante debe ser el mismo para ambos colores. De esta manera, el sistema interpreta que se trata de variantes de un mismo producto y las agrupa correctamente.

### Datos opcionales de carga

* Alt de imágenes
* Stock: Pueden cargarse con valor "0" y luego modificarse. No deben quedar vacíos.
* Precios: Pueden cargarse con valor "0" y luego modificarse. No deben quedar vacíos.
* Meta title
* Meta description
* Meta keywords
