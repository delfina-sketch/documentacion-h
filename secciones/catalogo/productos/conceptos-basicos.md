# Conceptos básicos

#### **Ítem** <a href="#item" id="item"></a>

Se refiere a un producto genérico, que no distingue entre variantes. Por ejemplo, "**Camisa Ford**" (sin especificar color o talle).

#### **Variante** <a href="#variante" id="variante"></a>

Son aquellas variaciones de producto que se distinguen según el valor de sus propiedades (Por ejemplo, "**Camisa Ford Roja XL**" es una variante de la Camisa Ford).

#### **Item & Variantes** <a href="#item-and-variantes" id="item-and-variantes"></a>

Cada producto tiene asignado un id de ítem, y dentro de cada ítem se encuentran las diferentes variantes de talle y color. A su vez, cada variante de talle y color tiene un SKU único con el que se identifica a la hora de despachar los pedidos.

Ejemplo:

**Producto:** Remera Feli

**Item:** 00345

**Item ID:** 43

**Variantes:**

* Variante 1: rojo - talle 1 -> SKU 00345RO01
* Variante 2: rojo - talle 2 -> SKU 00345RO02
* Variante 3: rojo - talle 3 -> SKU 00345RO03
* Variante 4: blanco - talle 1 -> SKU 00345BL01
* Variante 5: blanco - talle 2 -> SKU 00345BL02
* Variante 6: blanco - talle 3 -> SKU 00345BL03

Al crear un producto, se podrá distinguir el ítem de la variante visualmente en cajas/bloques.

Cada producto cuenta con características que son generales a todas sus variantes (en estos casos, son características del ítem), y otras que son propias de cada variación. Algunas de estas pueden ser:
