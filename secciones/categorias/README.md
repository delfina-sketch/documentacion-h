# Categorias

**URL:** `/admin/categories`

Gestion del arbol de categorias de productos con soporte para subcategorias y carpetas.

## Tarjetas de resumen

| Metrica              | Color | Descripcion                               |
| -------------------- | ----- | ----------------------------------------- |
| **Total categorias** | Azul  | Total de categorias creadas               |
| **Visibles**         | Verde | Categorias visibles en la tienda          |
| **Ocultas**          | Gris  | Categorias no visibles                    |
| **Con productos**    | Verde | Categorias que tienen productos asignados |

## Filtros por carpeta (tabs)

* Todas (35)
* Carpetas numeradas y con nombre (ej: "6", "9", "Archivadas", "Auxiliares", "Test QA")
* Boton para crear nueva carpeta

## Barra de busqueda

Buscar por ID, nombre o slug.

## Acciones

* **+ Nueva categoria:** Crear una categoria nueva

## Columnas de la tabla

| Columna   | Ordenable | Descripcion                                                            |
| --------- | --------- | ---------------------------------------------------------------------- |
| ID        | Si (desc) | Numero identificador con #                                             |
| Nombre    | Si        | Nombre de la categoria. Si tiene subcategorias muestra ">" y "(N sub)" |
| Slug      | No        | URL amigable de la categoria                                           |
| Productos | No        | Cantidad de productos (con icono)                                      |
| Estado    | Si        | Badge: **Visible** (verde) / **Oculta** (gris)                         |
| Acciones  | No        | Editar (lapiz), Mover (flecha), Eliminar (papelera)                    |
