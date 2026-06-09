# Calculador de cuotas

El calculador de cuotas permite configurar la visualización de cuotas disponibles de los productos según el rango de montos configurado.&#x20;

Las cuotas se muestran en sábana y ficha o en alguna de ellas según preferencia.

Esta funcionalidad asegura que tanto en la sábana de productos como en la ficha de producto, los usuarios finales puedan ver las opciones de cuotas aplicables de manera clara y precisa.

La configuración de este calculador no afecta la lógica de pago ni las promociones bancarias, sino que controla exclusivamente cómo se muestra la información de cuotas en el front-end.

### **Configuración** <a href="#paso-a-paso-para-su-configuracion" id="paso-a-paso-para-su-configuracion"></a>



1. Desde Pagos > Configuración > sección Calculador de cuotas, definir las cuotas y rangos:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-05 a las 15.53.46.png" alt=""><figcaption></figcaption></figure>

* Introducir la cantidad de cuotas deseadas.
* Completar los campos de configuración para cada rango, especificando:
  * Cantidad de cuotas: Número de cuotas aplicables.
  * Desde - Hasta: Montos mínimo y máximo aplicables en formato número sin símbolos, ni comas o puntos.
  * Activo: Activar o desactivar el rango medianteopciones Sí/No.

#### Formato de configuración: <a href="#formato-de-configuracion" id="formato-de-configuracion"></a>

* **\[Nº de Cantidad de cuotas]** Cuotas en productos desde **\[valor mínimo]** hasta **\[valor máximo]**
* Estado: Habilitado/Deshabilitado

#### Ejemplo de Configuración: <a href="#ejemplo-de-configuracion" id="ejemplo-de-configuracion"></a>

Ejemplo 1: Configuración de Rangos Únicos

* 3 Cuotas en productos desde $0 hasta $999 (Habilitado: Sí)
* 6 Cuotas en productos desde $1000 hasta $1999 (Habilitado: Sí)
* 12 Cuotas en productos desde $2000 hasta $2999 (Habilitado: Sí)
* 18 Cuotas en productos desde $3000 hasta $3999 (Habilitado: Sí)

Comportamiento: Si un producto tiene un precio de **$2500**, en la versión desktop de la ficha de producto, se mostrará:

> "12 Cuotas sin interés de $ \[monto calculado]"

En la sábana y versión mobile, solo se mostrará la mayor cuota aplicable:

> "Hasta 12 Cuotas sin interés de $ \[monto calculado]"

Ejemplo 2: Configuración con Rangos Solapados

* 3 Cuotas en productos desde $0 hasta $999 (Habilitado: Sí)
* 6 Cuotas en productos desde $0 hasta $1999 (Habilitado: Sí)
* 12 Cuotas en productos desde $2000 hasta $2999 (Habilitado: Sí)
* 18 Cuotas en productos desde $2000 hasta $3999 (Habilitado: Sí)

Comportamiento: Si un producto tiene un precio de **$500**, en la versión desktop de la ficha de producto, se mostrará:

> "3 Cuotas sin interés de $ \[monto calculado]" "6 Cuotas sin interés de $ \[monto calculado]"

En la sábana y versión mobile, solo se mostrará la mayor cuota aplicable:

> "Hasta 6 Cuotas sin interés de $ \[monto calculado]"

#### Visualización en el Front-end <a href="#visualizacion-en-el-front-end" id="visualizacion-en-el-front-end"></a>

1.  Ficha de Producto

    * La cuota que se mostrará dependerá del rango correspondiente al precio del producto.
    * En dispositivos móviles, siempre se visualizará la **cuota** más grande aplicable.

    <figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-05 a las 15.55.55.png" alt=""><figcaption></figcaption></figure>
2. Sábana de Productos
   *   Tanto en desktop como en mobile, siempre se mostrará la **mayor cuota posible**, con el texto:

       _"Hasta \[nº de cuota mayor aplicable] cuotas de \[$monto calculado] sin interés"_

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-05 a las 15.56.51.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Esta es una App Custom. Para utilizar la funcionalidad, es necesario previamente solicitar el maquetado correspondiente al equipo de producto vía formulario.
{% endhint %}
