# Prototipos

**URL:** `/admin/prototipos`

Un **prototipo** es un agrupador de propiedades.

Todos aquellos ítems que compartan propiedades serán parte del mismo prototipo. Por ejemplo:

* Camisas, remeras, pantalones y vestidos formarán parte del prototipo "**prendas**", ya que sus propiedades son las mismas: color y talle.
* Un producto "**Perfume**" en cambio, no tiene "color" y "talle", si no que solo cuenta con Volumen/Capacidad, por lo que se deberá crear una propiedad "volumen", que pertenecerá a un nuevo prototipo llamado "perfumes", y los valores que tendrán serán 50ml, 100ml, etc, según corresponda.

Desde este módulo podrás crear prototipos de productos.&#x20;

### Acceso

Para acceder al módulo, ingresar a Catálogo > Prototipos:&#x20;

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-02 a las 09.01.33.png" alt=""><figcaption></figcaption></figure>



Al acceder al módulo se verán 4 tarjetas de información:

| Métrica                         | Descripcion                                      |
| ------------------------------- | ------------------------------------------------ |
| **Total**                       | Total de prototipos creados                      |
| **Con propiedades de producto** | Prototipos con propiedades de producto asignadas |
| **Con propiedades de variante** | Prototipos con propiedades de variante asignadas |
| **Con productos**               | Prototipos que tienen productos asociados        |

También se podrá utilizar el buscador y los filtros para una búsqueda avanzada.&#x20;

En la pantalla principal del módulo, se encuentra un resumen de los prototipos creados con la información más relevante:

<table><thead><tr><th width="178.74609375">Columna</th><th>Descripcion</th></tr></thead><tbody><tr><td>Checkbox</td><td>Seleccion multiple</td></tr><tr><td>ID</td><td>Numero identificador (#)</td></tr><tr><td>Nombre</td><td>Nombre interno del prototipo (codigo, ej: <code>Generico</code>, <code>Prendas</code>, <code>Gift_Card</code>)</td></tr><tr><td>Nombre visible</td><td>Nombre que se muestra al crear un ítem (ej: "Generico", "Prendas", "Monto")</td></tr><tr><td>Props. producto</td><td>Cantidad de propiedades de producto</td></tr><tr><td>Props. variante</td><td>Cantidad de propiedades de variante</td></tr><tr><td>Productos</td><td>Cantidad de productos asociados</td></tr><tr><td>Acciones</td><td>Ver, Editar, Eliminar</td></tr></tbody></table>

## Ejemplo de uso

Un prototipo "Prendas" podria tener:

* **Propiedades de variante:** Talle, Color
* **Propiedades de ítem:** Tipo, Material

Todos los productos creados con este prototipo heredaran esas propiedades.
