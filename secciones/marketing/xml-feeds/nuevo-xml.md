# Nuevo XML

## Creación del XML en Hermés

### Dentro del backoffice de Hermes

1. Ir al módulo de Marketing y abrir el sub módulo de Sincronización de catálogo.&#x20;
   1. **URL:** `/admin/marketing/xml-feeds`
2. En la pantalla de este submódulo, se visualizarán todos los XML generados por la marca en un cuadro con la siguiente información:
   1. ID: es el ID que asignó Hermes al XML.&#x20;
   2. Nombre: es de uso interno. Sirve para identificar los XML's creados.&#x20;
   3. Plataforma: indica si el xml es de Facebook o Google
   4. Categoría: indica a qué categoría corresponde el XML
   5. SKUs: indica cuántos sku's tiene el XML
   6. URL: es el link del XML creado
   7.  Acciones: muestra los botones de acción sobre un XML ya creado. Los XML se podrán eliminar o editar según se necesite.

       <figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-05 a la(s) 9.36.09 a. m..png" alt=""><figcaption></figcaption></figure>
3. Hacer clic en el botón ¨Nuevo XML¨, ubicado en la misma pantalla en la parte superior derecha.
4. Completar la información general solicitada para la creación de un nuevo XML.
   1. Configuración básica del XML:
      1. Nombre: en el campo Name \* (campo obligatorio): este campo es de uso interno para poder identificar los xml's con mayor facilidad. Permite hasta 60 caracteres alfanuméricos, y no acepta espacios.
      2. Plataforma del XML: Xml type \* (select obligatorio): configurar si el xml a crear es de Facebook o Google
      3. Categoría: Category \* (select obligatorio): configurar la categoría de la cual se quiere generar el XML
      4. Incluir productos deshabilitados (check): tildar si se quiere incluir productos deshabilitados en el xml
      5. Incluir productos sin stock: tildar si se quiere incluir productos sin stock en el xml
5. Luego se debe asociar los tags del xml con la información correspondiente. Se debe tener en cuenta, que todos los campos que se pueden habilitar/deshabilitar pero los campos obligatorios si o si tienen que estar habilitados para su correcto funcionamiento.&#x20;

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-03-05 a la(s) 9.40.59 a. m..png" alt=""><figcaption></figcaption></figure>

En caso de querer agregar tags libres, se puede hacer clic en ¨Agregar campo¨ y completar el tag y la información que se desee traer.&#x20;

{% hint style="info" %}
Si esta información no existe en la columna Nombre Tag, solicitarla vía formulario.
{% endhint %}

7. Una vez completada la información, hacé clic en "Crear" y esperá a que se genere. El archivo se creará automáticamente cuando se ejecute el worker configurado para este propósito.

## Consideraciones

* &#x20;Se pueden generar hasta 10 XML y los mismos se actualizan con un worker cada 4 hs.
* Tener en cuenta que cuando se crear, hasta que el worker no corra, no podrán visualizar el XML.
