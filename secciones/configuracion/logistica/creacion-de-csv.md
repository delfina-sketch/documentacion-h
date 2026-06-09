# Creación de csv

## Descripción

En la pantalla de configuración de envíos se tiene un apartado de costo de envio/retiro por código postal y operadores logísticos.&#x20;

Este apartado sirve para configurar los montos vía csv por cada uno de los cp existentes.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-12 a la(s) 7.25.46 p. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Tener en cuenta que, a diferencia del apartado anterior, esta configuración es **unificada** tanto para envío como para retiro, es decir que no se tendrá que subir un csv en la sección de retiro y otro en la sección de envío si no que es una para ambos casos. Además, estará diferenciada por el select de operador logístico.&#x20;
{% endhint %}

## Armado del csv

Cada operador logístico tiene identificadas ¨zonas¨ a las cuales se le aplica cada envío y cada monto de envío.

El equipo de Producto, realizó un relevamiento de cada uno de los operadores logísticos y sus zonas para que sea sencillo completar los montos y no tener que realizar un trabajo manual.

{% hint style="info" %}
Para acceder al archivo base realizado por el equipo de Producto para cada cliente, solicitar el archivo al equipo.
{% endhint %}

1. Armar el archivo csv por operador logístico y sus métodos de envío teniendo en cuenta el archivo base enviado por el equipo de producto. Ejemplo:

<figure><img src="../../../.gitbook/assets/Captura de Pantalla 2023-12-11 a la(s) 10.54.40.png" alt=""><figcaption></figcaption></figure>

2. Seleccionar en el selector el operador logístico, el operador del cual se desee subir los montos asociados y luego seleccionar el archivo csv que se quiere cargar.

{% hint style="danger" %}
Cada operador logístico tiene asociado su archivo con los tipos de envío que ofrece. Si tenés dudas consultá con el especialista de Producto
{% endhint %}

3. Tocar el botón ¨Subir¨ para que el archivo quede impactado.&#x20;
4. Corroborar que el pop up que indica la finalización del proceso de carga haya indicado que se subió correctamente.

### Consideraciones al momento de cargar un csv

* El csv deberá tener las columnas correspondientes al operador logístico que se está configurando
* Los montos del mismo deberán estar centavos y no deberá contener caracteres especiales.
* **Si el campo monto se completa con un 0 corresponderá envío gratis en ese código postal.**
* **Si el campo monto NO se completa, se considerará que ese operador logístico no ofrece entregas a ese código postal.**
* Si se quiere cambiar el monto de un solo código postal, no hace falta subir el archivo completo si no que basta con solo subir un archivo con ese código postal y sus montos.
* Si se quiere saber qué es lo que se tiene configurado, al tocar el botón ¨Descargar¨ se descargará, también en formato csv, el archivo del operador logístico seleccionado con sus respectivos montos cargados.
* En caso de tocar el botón ¨Eliminar¨ se eliminará todos los montos configurados vía csv y la base de datos quedará vacía.
* En las columnas donde se hacer referencia a los retiros, hay que tener en cuenta que se deberá completar el campo con la suma de (retiro + envío) en caso de que se quieran cobrar ambas cosas.

## Visualización de montos por operador logístico

En el Checkout de Hermés los montos que se configuren en el csv serán visualizados por el usuario de la siguiente manera cuando se elija la opción de entrega:

1. Envío a domicilio: **\[Operador Logístico + Monto (sea $X o Envío gratis)]**&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/KSMHJqM2ILexov_pBL2Ocsq1mUdp5IqRykNgo9DmxwMlfJPOWHO1oI36MFfXcG-n3q3Q0bKiNhHMtqVLM66mzc5xMAKVq3B5AIpyBwyo3blOBTavp-5E6wCwiCQVz9rAbeEXtOyAK2l_BVmaiLcx4CA" alt=""><figcaption></figcaption></figure>

2. Envío a sucursal de correo: **\[Tipo de Sucursal + Ciudad + Monto (sea $X o Envío gratis)]**&#x20;
