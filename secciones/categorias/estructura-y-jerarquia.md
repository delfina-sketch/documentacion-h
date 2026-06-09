# Estructura y Jerarquía

### Conceptos Generales

Las categorías constituyen la estructura lógica y jerárquica de la tienda, permitiendo a los usuarios localizar productos de forma ágil.

Jerarquía del Árbol de Categorías:

* Padre: Categoría raíz que no depende de ninguna otra. Generalmente visible en el menú principal.
* Hija: Categoría anidada dentro de una Padre.
* Nieta/Bisnieta: Niveles sucesivos de anidación cuya visibilidad depende del diseño de la tienda.

Ejemplo de categoría Padre, Hija y Nieta y Bisnieta:

* **Rojo** = Niñas -> Padre
* **Verde** = Niñas (1 - 3 años) -> Hija
* **Azul** = Ropa -> Nieta
* **Amarillo** = Buzos y sweaters -> Bisnieta

![](https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2F2844678769-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F2VP48tuPxvoNgMg0xOJT%252Fuploads%252FITeyP8uXZX17SOKG1iVo%252FCaptura%2520de%2520pantalla%25202024-06-18%2520a%2520las%25205.30.21%25E2%2580%25AFp.%25C2%25A0m..png%3Falt%3Dmedia%26token%3D26b79c3c-724d-4b39-9f13-5537af41c243\&width=768\&dpr=3\&quality=100\&sign=4c2d2185\&sv=2)

### Visibilidad

#### **1. En Productos** <a href="#productos" id="productos"></a>

Los ítems de una categoría estarán visibles también en sus categorías padres, incluso si no están asignados a ella.

#### **2. De Banners** <a href="#banners" id="banners"></a>

En caso que un banner esté asignado a una categoría padre, y sus categorías hijas no tengan banner asignado, las mismas "tomarán" el banner de su categoría padre.

No se visualizará el banner si la categoría no tiene ningún producto asignado.

#### **3. De Categorías** <a href="#categorias" id="categorias"></a>

No se visualizarán aquellas categorías que no tengan ningún producto asignado (habilitado/visible) a ellas.

[<br>](https://pow-ecommerce.gitbook.io/hermes/categorias)
