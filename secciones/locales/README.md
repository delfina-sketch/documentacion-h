# Locales

**URL:** `/admin/locales`

Gestion de locales físicos y puntos de venta desde un unico listado, con configuracion de funcionalidades como retiro, stock y omnicanalidad.

Desde esta pantalla se define como opera cada local dentro de la tienda y del flujo logistico. Cada local puede estar visible para clientes, habilitado para retiro en tienda, mostrar stock disponible o participar en circuitos omnicanal para preparacion y derivacion de pedidos.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 16.43.06.png" alt=""><figcaption></figcaption></figure>

#### Tarjetas de resumen

| Metrica           | Color | Descripcion                                  |
| ----------------- | ----- | -------------------------------------------- |
| **Total locales** | Verde | Cantidad total de locales                    |
| **Visibles**      | Verde | Locales visibles para clientes               |
| **Con retiro**    | Azul  | Locales habilitados para retiro en tienda    |
| **Mostrar stock** | Verde | Locales que muestran disponibilidad de stock |

#### Columnas de la tabla

| Columna   | Descripcion                                                                     |
| --------- | ------------------------------------------------------------------------------- |
| Checkbox  | Selección multiple                                                              |
| ID        | Número identificador (#)                                                        |
| Nombre    | Nombre del local (negrita)                                                      |
| Direccion | Dirección completa                                                              |
| Provincia | Provincia/estado                                                                |
| Opciones  | Badges de servicios: **Retiro** (azul), **Stock** (naranja), **Omni** (violeta) |
| Estado    | Badge: **Visible** (verde)                                                      |
| Acciones  | Ver (ojo), Editar (lápiz)                                                       |

Al hacer clic en **Editar**, Hermés abre una pantalla distinta según el tipo de registro seleccionado.

* **Depósito central:** abre una configuración más amplia, orientada al flujo logístico general. Desde allí se definen opciones como control de despacho, pantalla de peso y participación del warehouse en pedidos con retiro en tienda. Ver [Editar depósito central](editar-deposito-central.md).
* **Local:** abre la configuración operativa del local. Desde allí se administran funciones propias del local, como pickeo, recepción, rotación interna o visibilidad dentro de los circuitos de stock y retiro. Ver [Editar local](editar-local.md).

