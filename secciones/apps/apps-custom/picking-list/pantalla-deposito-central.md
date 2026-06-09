# Pantalla Depósito Central

Esta pantalla constituye el panel de trabajo exclusivo para el depósito central. Su objetivo es listar de forma centralizada todas las órdenes con pago aprobado que han sido asignadas al depósito central y que se encuentran listas para iniciar el proceso de armado y despacho.

## **Panel de Navegación Lateral** <a href="#panel-de-navegacion-lateral" id="panel-de-navegacion-lateral"></a>

Permite al operario del depósito alternar entre los flujos de trabajo del módulo:

* **Pendientes de armado:** Vista actual que contiene la cola de órdenes por procesar en el depósito central. Son todas las órdenes que el central tiene para despachar al cliente y/o a un local.
* **Control de Despacho**: son aquellos pedidos que fueron armados y están pendientes de que sean entregados al operador logístico correspondiente.
* **Historial de pedidos:** Acceso al registro histórico de órdenes previamente procesadas y despachadas desde este depósito.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-26 a la(s) 12.36.20.png" alt=""><figcaption></figcaption></figure>

## **Herramientas de Filtrado y Acciones Globales** <a href="#herramientas-de-filtrado-y-acciones-globales" id="herramientas-de-filtrado-y-acciones-globales"></a>

Ubicadas en la sección superior para facilitar la gestión en lote de altos volúmenes de pedidos propios del depósito:

* **Buscador por número de orden**: Campo de texto dinámico para localizar un pedido específico mediante su ID o código numérico.
* **Filtro "Todos los métodos":** Desplegable para segmentar las órdenes del depósito según la modalidad de entrega (ej. Envío a domicilio o Retiro en tienda/sucursal).
* **Filtro "Todos los operadores":** Desplegable que permite filtrar la cola de trabajo según el operador logístico encargado de la distribución general (ej. Mercado Envíos, Andreani, etc.).
* **Botón \[Imprimir PL]**: Acción masiva con menú desplegable para generar e imprimir las Listas de Picking (_Picking Lists_) de los registros seleccionados para el operario de bodega.
* **Botón \[Productos]**: Menú desplegable complementario para la gestión masiva de los artículos vinculados a las órdenes del depósito.
* **Botón \[Ticket de cambio]**: Para imprimir ticket de cambio de manera individual o masiva.

## Sección "Pedidos pendientes de armado" <a href="#seccion-pedidos-pendientes-de-armado" id="seccion-pedidos-pendientes-de-armado"></a>

Este módulo administra el ciclo de preparación y despacho de las órdenes asignadas al depósito central. El comportamiento y la interfaz de usuario cambian dinámicamente según la configuración de la sucursal (Parámetro: `Pantalla de Pickeo` Activa / Inactiva).

{% hint style="info" %}
Si tenés dudas sobre esta configuración, podes consultar el apartado de [Locales](https://pow-ecommerce.gitbook.io/hermespow/sVt0oLIN0qrGaDdF8QjD/secciones/locales)
{% endhint %}

### **Con funcionalidad de "Pantalla de Pickeo"** <a href="#con-funcionalidad-de-pantalla-de-pickeo" id="con-funcionalidad-de-pantalla-de-pickeo"></a>

Cuando el local tiene habilitada la interfaz de validación por escaneo, el flujo operativo se compone de las siguientes etapas secuenciales:

**1. Pedidos Pendientes de Armado**

* **Comportamiento:** La columna de _Acciones_ presenta para cada orden de manera exclusiva el botón \[Pickear] (Ícono de código de barras).
* **Interacción**: Al pulsar sobre el botón \[Pickear], el sistema redirige automáticamente al operador a la interfaz de validación interna de la orden elegida.

{% hint style="info" %}
En esta pantalla también podrás visualizar los pedidos que son de cambio y cuales tienen asociado un ticket de cambio.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 10.16.35.png" alt=""><figcaption></figcaption></figure>

**2. Pantalla de Validación / Proceso de Pickeo (Estado Inicial)**

* **Encabezado**: Muestra el número único de pedido (ej. #1733471894659-01), el origen del canal y el operador logístico asignado (Andreani).
* I**ndicador de Progreso**: Un gráfico circular en el margen superior derecho detalla la relación de ítems validados frente al total general de la orden (Inicia en `0 / 1`).
* **Campo de Entrada Principal:** Dispone de una barra central de lectura (`Escaneá o ingresá el SKU...`) para la captura automatizada mediante lector de código de barras o ingreso manual, acompañada de un botón \[Escanear]. También está disponible el escaneo mediante smartphone.
* **Matriz de Artículos:** Detalla los productos asociados al pedido mediante las columnas: `SKU`, `Producto` (con descripción, color y talle), `Cant.` (unidades solicitadas), `Pickeado` (unidades validadas) y `Estado`.
* **Botones de Control Inferiores:**
  * \[Cancelar]: Revierte el proceso y regresa a la cola general.
  * \[Ver etiqueta]: Permite previsualizar el documento de envío de forma manual.
  * \[Confirmar]: Se encuentra deshabilitado nativamente hasta no completar la validación física.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 10.17.26 (1).png" alt=""><figcaption></figcaption></figure>

**3. Finalización del Pickeo y Habilitación de Confirmación (Estado Completo)**

* **Validación Exitosa:** Al escanear la totalidad de las unidades requeridas, la columna `Pickeado` actualiza su valor, el `Estado` se marca con un ícono de verificación verde (Check) y el indicador de progreso alcanza el 100% (`1 / 1`).
* **Automatización del Sistema:** Una vez completada la recolección de manera conforme, el sistema despliega de forma automática la etiqueta correspondiente para su impresión física.
* **Habilitación de Acción:** El botón \[Confirmar] cambia su estado a activo (color verde). Al ser pulsado por el operario, consolida la orden y la transfiere a la sección de "Control de despacho".

{% hint style="info" %}
Si al hacer clic en **Confirmar** el pedido todavía no tiene etiqueta, el sistema confirma la orden, genera la etiqueta y la abre automáticamente.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 10.22.14.png" alt=""><figcaption></figcaption></figure>

### **Sin funcionalidad de "Pantalla de Pickeo"** <a href="#sin-funcionalidad-de-pantalla-de-pickeo" id="sin-funcionalidad-de-pantalla-de-pickeo"></a>

En caso de que el depósito no requiera la instancia de validación intermedia por escaneo de SKUs, el sistema simplifica el flujo operativo directamente desde el panel principal:

**1. Acciones Directas**

* **Comportamiento**: La columna de _Acciones_ omite la opción de pickeo y expone directamente dos herramientas de ejecución por cada fila:
  * Botón \[Etiqueta] (Ícono de impresora): Permite al operador mandar a imprimir de manera individual el documento de envío o bulto correspondiente a la orden para su empaque directo.
  * Botón \[Confirmar] (Color verde): Control directo que procesa y confirma el pedido de manera inmediata, omitiendo la pantalla de validación de ítems.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 10.31.16.png" alt=""><figcaption></figcaption></figure>

### Pedidos de cambio <a href="#seccion-historial-de-pedidos" id="seccion-historial-de-pedidos"></a>

Los pedidos de cambio generados desde Undo también aparecen en este listado. Para habilitar el pickeo, la orden debe estar confirmada en Undo como recibida correctamente.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-06-02 a la(s) 08.48.20.png" alt=""><figcaption></figcaption></figure>

Si el botón **Pickear** está habilitado, significa que en Undo ya se confirmó que el pedido llegó en buenas condiciones. Si esa confirmación todavía no existe, el botón **Pickear** o **Despachar** se muestra en gris. En ese caso, el pedido igualmente puede armarse, pero el sistema muestra una alerta para indicar que falta la confirmación en Undo.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-06-02 a la(s) 08.48.38.png" alt=""><figcaption></figcaption></figure>

## Sección "Control de despacho" <a href="#seccion-historial-de-pedidos" id="seccion-historial-de-pedidos"></a>

El módulo Control de Despacho tiene como finalidad permitir al equipo de operaciones y logística gestionar, verificar y procesar la salida (despacho) de los pedidos que ya han sido armados, asegurando su correcta asignación al operador logístico correspondiente.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 10.34.16.png" alt=""><figcaption></figcaption></figure>

### Proceso de control de despacho

El procesamiento de salidas en este módulo se puede ejecutar bajo dos modalidades operativas, únicamente después de haber realizado la entrega física de los paquetes al operador logístico correspondiente:

* **Procesamiento Unitario (1:1):** Permite al operador gestionar cada pedido de forma individual mediante la impresión de su etiqueta de envío y la posterior ejecución de la acción "Despachar" en la fila correspondiente.
* **Procesamiento Masivo (En lote)**: Permite seleccionar múltiples órdenes en simultáneo utilizando las casillas de verificación (checkboxes) y procesar su salida en un solo clic mediante el botón global "Despachar" ubicado en el margen superior derecho de la pantalla.

{% hint style="info" %}
Al ingresar o escanear el número de orden en esta pantalla, el sistema despacha el pedido de forma automática.
{% endhint %}

## Sección "Historial de Pedidos" <a href="#seccion-historial-de-pedidos" id="seccion-historial-de-pedidos"></a>

Esta vista de consulta almacena el registro histórico de todas las órdenes que ya han completado con éxito su proceso de preparación física y han sido despachadas desde el depósito central los últimos meses.

Su propósito principal es permitir la trazabilidad de la operación y proveer herramientas rápidas de soporte post-despacho.

<figure><img src="../../../../.gitbook/assets/Captura de pantalla 2026-05-28 a la(s) 10.50.20.png" alt=""><figcaption></figcaption></figure>

### **Herramientas de Filtrado y Búsqueda Avanzada** <a href="#herramientas-de-filtrado-y-busqueda-avanzada" id="herramientas-de-filtrado-y-busqueda-avanzada"></a>

Ubicadas en la sección superior, facilitan la localización expedita de órdenes en escenarios de alto volumen de datos:

* **Buscador General:** Campo de texto dinámico que permite rastrear y filtrar registros mediante tres variables clave: Número de orden (ID de pedido), código de tracking o nombre del operador logístico.
* **Filtro "Todos los métodos"**: Menú desplegable para segmentar el listado histórico según la modalidad de entrega seleccionada por el cliente (ej. Envío a domicilio o Retiro en tienda).
* **Filtro "Todos los operadores":** Menú desplegable para aislar las órdenes procesadas según la empresa de transporte encargada de la distribución (ej. Jipink, Mercado Envíos, Andreani).

### **Tabla de Órdenes Procesadas** <a href="#tabla-de-ordenes-procesadas" id="tabla-de-ordenes-procesadas"></a>

Presenta un desglose estructurado de la información histórica a través de las siguientes columnas:

* **Pedido**: Muestra el número identificador único de la orden (con opción de copiado rápido al portapapeles) secundado por un código de referencia interno entre paréntesis.
* **Fecha**: Registra de forma exacta el día, mes y año en el que se procesó la transacción en el sistema.
* **Monto**: Expone el valor monetario total del pedido facturado.
* **Operador Logístico:** Detalla de manera explícita el courier o método de distribución bajo el cual fue despachado el paquete (ej. _Jipink_, _Andreani_, _Mercado Envíos_).
* **Acciones**:
  * Botón \[Etiqueta]: Componente interactivo clave de la pantalla. Permite al operario invocar y abrir nuevamente el documento de envío o bulto original vinculado a la orden. Esta función está diseñada específicamente para dar soporte ante contingencias operativas, posibilitando la reimpresión inmediata de la etiqueta en caso de daño físico, extravío o necesidad de re-etiquetado antes del retiro del transportista.
