# Creación y Edición de Categorías

#### Creación/Edición manual

Al crear/editar una categoría en la nueva interfaz, los campos se agrupan en cuatro secciones clave:

1. Pestaña "General"&#x20;
   1. Nombre: Título público de la categoría.
   2. Slug: Identificador de la URL (ej: `remeras-2024`). Nota: Si se cambia, se rompen los links antiguos en campañas externas.
   3. Color de Texto: Selector para cambiar el color del nombre en el menú (solo para categorías Padre).
   4. Categoría de Variantes: Si se activa, permite ingresar SKUs manualmente (separados por espacio) para crear una selección curada.
      * Lógica de stock: Solo se mostrarán productos que tengan al menos una variante con stock > 0 y una foto asociada.
   5. Estilo de Grilla (Sábana): Selecciona la disposición de productos (ej: "Sábana 4-4-4" o "2-2-4").
   6. Visibilidad): Si está en "No", la categoría no aparece en el menú pero sigue siendo accesible vía URL directa.
2. Pestaña "Banners" (Imagen y Promoción)
   1. Top Banner Principal: Carga la imagen para Desktop y Mobile. Puedes definir fechas de inicio/fin y días de la semana activos.
   2. Programar Banner Secundario: Permite configurar un banner que reemplaza al principal en un rango de fechas específico (ideal para eventos).
   3. Banner en Sábana: Configura dos banners adicionales que aparecen mezclados entre los productos. Requiere Título, Botón, Link e imágenes independientes.
3.  Pestaña "Carrusel":

    Configura el acceso visual a las subcategorías:

    1. Carrusel de Imágenes: Aparece automáticamente si las categorías hijas tienen una "Imagen Preview" cargada.
    2. Botonera: Se muestra si las hijas no tienen imagen; solo aparecerá el nombre como un botón de texto (máximo 7 botones).
    3. Orden: Las categorías con "Posición" numérica van primero; luego las que no tienen posición, ordenadas alfabéticamente.
4.  Pestaña "Orden de Productos" (Priorización)

    Permite gestionar cómo se muestran los productos en la tienda:

    1. Drag and Drop: Haz clic sostenido en un producto y arrástralo. El sistema guarda el cambio al instante.
    2. Edición Manual: Escribe el número en el campo "Prioridad" y presiona el check (tilde) para confirmar.
    3. Buscador Interno: Permite localizar productos específicos para editarlos. Importante: El Drag and Drop se desactiva mientras el buscador está activo.

#### Gestión Masiva con CSV (Ejemplos)

1. Asignar productos a categorías: Para mover o sumar productos masivamente, ve a Productos -> Acciones en masa -> Actualizar variante. El CSV debe tener esta estructura:

| **id** | **category\_ids** |
| ------ | ----------------- |
| 2245   | 1, 4              |
| 2219   | 1, 4              |
| 1249   | 1, 2              |

* Pisar: Borra las categorías viejas del producto y deja solo las del CSV.
* Sumar: Agrega el producto a las categorías del CSV sin quitarlo de donde ya está.
* Restar: Quita el producto únicamente de las categorías listadas en el archivo.

2. Ordenar productos dentro de una categoría: Descarga el CSV desde la pestaña "Orden de Productos" de la categoría específica. Modifica solo la columna "Orden":

| **nombre**   | **color** | **sku**  | **category** | **orden** |
| ------------ | --------- | -------- | ------------ | --------- |
| Oxford Crop  | Blanco    | 0BPMD448 | 805          | 1         |
| Piloto Wet   | Blanco    | 0APMP4TU | 805          | 2         |
| Tunica Frida | Blanco    | 09PMP4QP | 805          | 3         |

* Reglas: No uses el valor 0 y no repitas números. Si repites, el sistema ordenará de forma aleatoria esos ítems.

#### Tips Técnicos de Performance

* Caché: Los cambios en los banners o el orden pueden tardar unos minutos en verse en la web pública debido a la "Caché de Sábana".
* Archivos: Los banners no deben pesar más de 200kb (imágenes) o 1mb (GIFs) para no ralentizar la carga.
* Nomenclatura: Siempre usa nombres únicos para los archivos (ej: `Top-Banner-Invierno-2026-Desktop.jpg`) para forzar la actualización en el servidor.

