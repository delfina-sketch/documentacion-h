# Locales

Esta pantalla centraliza la preparación de pedidos a nivel del local. A diferencia de la pantalla del depósito central, este panel incorpora de forma exclusiva el sub-módulo de Pickup, diseñado específicamente para administrar y controlar el ciclo completo de las órdenes destinadas a ser retiradas por el cliente final en el propio punto de venta.

## **Panel de Navegación Lateral** <a href="#panel-de-navegacion-lateral" id="panel-de-navegacion-lateral"></a>

Permite al personal del local alternar entre los flujos de trabajo del módulo:

* **Pendientes de armado:** Vista actual que contiene la lista de órdenes por procesar en el local. Son todas las órdenes que el local tiene para despachar al cliente, al depósito central y/o a un local(dependiendo de las reglas de negocio de la marca).
* **Control de Despacho**: son aquellos pedidos que fueron armados y están pendientes de que sean entregados al operador logístico correspondiente.
* **Pedidos de Pick up**: reúne los pedidos que el local debe entregar al cliente en el propio local.
* **Historial de pedidos:** Acceso al registro histórico de órdenes previamente procesadas y despachadas desde este local.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 14.58.59.png" alt=""><figcaption></figcaption></figure>

### Sección Pendientes de Armado <a href="#seccion-pendientes-de-armado" id="seccion-pendientes-de-armado"></a>

A diferencia del depósito central, las órdenes listadas en el panel general de un local físico pueden responder a tres naturalezas lógicas distintas según su destino(y si la marca tiene implementado omnicanalidad)

1. **Despacho Directo**: Pedidos asignados al local para ser preparados y entregados al operador logístico con destino final al domicilio del cliente.
2. **Transferencia Inter-Local:** Órdenes pendientes de armado cuyo propósito es abastecer o consolidar stock en otra sucursal de la marca.
3. **Retiro en Tienda Local**: Preparación preliminar de artículos que serán retirados físicamente por el cliente en ese mismo local.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.17.21.png" alt=""><figcaption></figcaption></figure>

## **Herramientas de Filtrado y Acciones Globales** <a href="#herramientas-de-filtrado-y-acciones-globales" id="herramientas-de-filtrado-y-acciones-globales"></a>

Ubicadas en la sección superior para facilitar la gestión en lote de altos volúmenes de pedidos propios del depósito:

* **Buscador por número de orden**: Campo de texto dinámico para localizar un pedido específico mediante su ID o código numérico.
* **Filtro "Todos los métodos":** Desplegable para segmentar las órdenes del depósito según la modalidad de entrega (ej. Envío a domicilio o Retiro en tienda/sucursal).
* **Filtro "Todos los operadores":** Desplegable que permite filtrar la cola de trabajo según el operador logístico encargado de la distribución general (ej. Mercado Envíos, Andreani, etc.).
* **Botón \[Imprimir PL]**: Acción masiva con menú desplegable para generar e imprimir las Listas de Picking (_Picking Lists_) de los registros seleccionados para el operario de bodega.
* **Botón \[Productos]**: Menú desplegable complementario para la gestión masiva de los artículos vinculados a las órdenes del depósito.

## Sección "Pedidos pendientes de armado" <a href="#seccion-pedidos-pendientes-de-armado" id="seccion-pedidos-pendientes-de-armado"></a>

Este módulo administra el ciclo de preparación y despacho de las órdenes asignadas al local. El comportamiento y la interfaz de usuario cambian dinámicamente según la configuración de la sucursal (Parámetro: `Pantalla de Pickeo` Activa / Inactiva).

{% hint style="info" %}
Si tenés dudas sobre esta configuración, podes consultar el apartado de [Locales](https://pow-ecommerce.gitbook.io/hermespow/sVt0oLIN0qrGaDdF8QjD/secciones/locales)
{% endhint %}

### **Con funcionalidad de "Pantalla de Pickeo"** <a href="#con-funcionalidad-de-pantalla-de-pickeo" id="con-funcionalidad-de-pantalla-de-pickeo"></a>

Cuando el local tiene habilitada la interfaz de validación por escaneo, el flujo operativo se compone de las siguientes etapas secuenciales:

**1. Pedidos Pendientes de Armado**

* **Comportamiento:** La columna de _Acciones_ presenta para cada orden de manera exclusiva el botón \[Pickear] (Ícono de código de barras).
* **Interacción**: Al pulsar sobre el botón \[Pickear], el sistema redirige automáticamente al operador a la interfaz de validación interna de la orden elegida.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.17.21 (1).png" alt=""><figcaption></figcaption></figure>

**2. Pantalla de Validación / Proceso de Pickeo (Estado Inicial)**

* **Encabezado**: Muestra el número único de pedido (ej. #1133471894659-01), el origen del canal y el operador logístico asignado (Andreani).
* I**ndicador de Progreso**: Un gráfico circular en el margen superior derecho detalla la relación de ítems validados frente al total general de la orden (Inicia en `0 / 1`).
* **Campo de Entrada Principal:** Dispone de una barra central de lectura (`Escaneá o ingresá el SKU...`) para la captura automatizada mediante lector de código de barras o ingreso manual, acompañada de un botón \[Escanear]. También está disponible el escaneo mediante smartphone.
* **Matriz de Artículos:** Detalla los productos asociados al pedido mediante las columnas: `SKU`, `Producto` (con descripción, color y talle), `Cant.` (unidades solicitadas), `Pickeado` (unidades validadas) y `Estado`.
* **Botones de Control Inferiores:**
  * \[Cancelar]: Revierte el proceso y regresa a la cola general.
  * \[Ver etiqueta]: Permite previsualizar el documento de envío de forma manual.
  * \[Confirmar]: Se encuentra deshabilitado nativamente hasta no completar la validación física.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.21.33.png" alt=""><figcaption></figcaption></figure>

**3. Finalización del Pickeo y Habilitación de Confirmación (Estado Completo)**

* **Validación Exitosa:** Al escanear la totalidad de las unidades requeridas, la columna `Pickeado` actualiza su valor, el `Estado` se marca con un ícono de verificación verde (Check) y el indicador de progreso alcanza el 100% (`1 / 1`).
* **Automatización del Sistema:** Una vez completada la recolección de manera conforme, el sistema despliega de forma automática la etiqueta correspondiente para su impresión física.
* **Habilitación de Acción:** El botón \[Confirmar] cambia su estado a activo (color verde). Al ser pulsado por el operario, consolida la orden y la transfiere a la sección de historial de pedidos o Control de despacho (según lo que se tenga configurado).

{% hint style="info" %}
Si al hacer clic en **Confirmar** el pedido todavía no tiene etiqueta, el sistema confirma la orden, genera la etiqueta y la abre automáticamente.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.23.02.png" alt=""><figcaption></figcaption></figure>

### **Sin funcionalidad de "Pantalla de Pickeo"** <a href="#sin-funcionalidad-de-pantalla-de-pickeo" id="sin-funcionalidad-de-pantalla-de-pickeo"></a>

En caso de que el local no requiera la instancia de validación intermedia por escaneo de SKUs, el sistema simplifica el flujo operativo directamente desde el panel principal:

**1. Acciones Directas**

* **Comportamiento**: La columna de _Acciones_ omite la opción de pickeo y expone directamente dos herramientas de ejecución por cada fila:
  * Botón \[Etiqueta] (Ícono de impresora): Permite al operador mandar a imprimir de manera individual el documento de envío o bulto correspondiente a la orden para su empaque directo.
  * Botón \[Despachar] (Color verde): Control directo que procesa y despacha el pedido de manera inmediata, omitiendo la pantalla de validación de ítems.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.26.12.png" alt=""><figcaption></figcaption></figure>

## Sección "Control de despacho" <a href="#seccion-historial-de-pedidos" id="seccion-historial-de-pedidos"></a>

El módulo Control de Despacho tiene como finalidad permitir al equipo de operaciones y logística gestionar, verificar y procesar la salida (despacho) de los pedidos que ya han sido armados, asegurando su correcta asignación al operador logístico correspondiente.

{% hint style="info" %}
Esta pantalla se puede habilitar o deshabilitar según la configuración operativa definida para el local
{% endhint %}

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.45.41.png" alt=""><figcaption></figcaption></figure>

### Proceso de control de despacho

El procesamiento de salidas en este módulo se puede ejecutar bajo dos modalidades operativas, únicamente después de haber realizado la entrega física de los paquetes al operador logístico correspondiente:

* **Procesamiento Unitario (1:1):** Permite al operador gestionar cada pedido de forma individual mediante la impresión de su etiqueta de envío y la posterior ejecución de la acción "Despachar" en la fila correspondiente.
* **Procesamiento Masivo (En lote)**: Permite seleccionar múltiples órdenes en simultáneo utilizando las casillas de verificación (checkboxes) y procesar su salida en un solo clic mediante el botón global "Despachar" ubicado en el margen superior derecho de la pantalla.

{% hint style="info" %}
Al ingresar o escanear el número de orden en esta pantalla, el sistema despacha el pedido de forma automática.
{% endhint %}

### Consideraciones

Los locales pueden operar con o sin la pantalla de Control de despacho.

**Si el local despacha pedidos:**

* Sin Control de despacho: los pedidos pasan de Pendientes de armado a Historial de pedidos.
* Con Control de despacho: los pedidos pasan de Pendientes de armado a Control de despacho y luego a Historial de pedidos.

**Si el local no despacha pedidos:**

* Sin Control de despacho: no hay pedidos en Pendientes de armado. Todas las órdenes quedan en Pendientes de confirmación.
* Con Control de despacho: esta pantalla no aplica, ya que el local no realiza despachos.

## Sección "Pedidos Pick up" <a href="#seccion-historial-de-pedidos" id="seccion-historial-de-pedidos"></a>

### Pedidos pendientes de confirmación

Esta pantalla tiene como propósito centralizar y listar todas las órdenes con modalidad de retiro en tienda físico (_Store Pickup_) que ingresaron al sistema y están a la espera de que el local valide y confirme la disponibilidad del pedido.

La confirmación es el paso previo y obligatorio para indicarle formalmente al cliente que su pedido está listo para ser retirado en la sucursal seleccionada.

{% hint style="info" %}
El comportamiento de esta pantalla también depende de si el local tiene activa la funcionalidad de pickeo.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.57.09.png" alt=""><figcaption></figcaption></figure>

#### Acciones

Por cada fila de pedido, el operador del local cuenta con tres opciones de interacción:

*   **Botón Ver Detalle**

    * Función: Permite abrir una ventana modal o vista expandida con el desglose de los productos que componen la orden (SKU, talle, color, cantidad).

    <figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 15.59.58.png" alt=""><figcaption></figcaption></figure>
*   **Botón "Pickear"**

    * Función: Al hacer clic, el sistema procesa la confirmación de la orden.

    <figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 16.00.47.png" alt=""><figcaption></figcaption></figure>
* **Botón "Rechazar"**
  * Función: Cancela el procesamiento del pedido en esa sucursal en particular.

### Pedidos pendientes de entrega

Esta pantalla tiene como propósito gestionar el tramo final del flujo de _Store Pickup_: la entrega física de la mercadería al cliente en la sucursal. Permite al personal del local validar la identidad del comprador, emitir el comprobante de retiro obligatorio para la firma física y registrar el cierre definitivo de la orden en el sistema.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 16.03.12.png" alt=""><figcaption></figcaption></figure>

#### Acciones

Por cada fila de pedido, el operador del local cuenta con dos opciones de interacción:

**Botón "Constancia"**

Su función es mostrar en pantalla y enviar a impresión el comprobante de retiro de la orden. El propósito operativo de esta acción es emitir el documento físico que el cliente debe firmar obligatoriamente al retirar el pedido; como efecto en el sistema, se registra la emisión de la constancia y se habilita automáticamente el botón "Entregar", el cual permanece bloqueado hasta completar este paso.

**Botón "Entregar"**

Tiene la función de registrar el cierre definitivo y la entrega física de la orden en la plataforma. Como regla de control, este botón permanece deshabilitado por defecto si la constancia de entrega no fue impresa previamente, lo que garantiza que ningún operador se saltee el paso de auditoría física en el local. Finalmente, el efecto en el sistema al presionarlo es que el pedido cambia al estado final "Entregado", se remueve de la lista de pendientes y se dispara un e-mail automático al cliente final con la leyenda: "Tu pedido fue entregado".



## Sección "Historial de Pedidos" <a href="#seccion-historial-de-pedidos" id="seccion-historial-de-pedidos"></a>

Esta vista de consulta almacena el registro histórico de todas las órdenes que ya han completado con éxito su proceso de preparación física y han sido despachadas desde el local los últimos meses.

Su propósito principal es permitir la trazabilidad de la operación y proveer herramientas rápidas de soporte post-despacho.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 16.20.22 (1).png" alt=""><figcaption></figcaption></figure>





