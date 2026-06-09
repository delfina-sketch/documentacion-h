# Sincronización de catálogo

## **Acceso**

**URL:** `/admin/marketing/xml-feeds`

Integración de catalogo para Google Shopping y Facebook Ads mediante feeds XML.

## Descripción

El XML es un formato de archivo. Está definido por una estructura de datos (al igual que un CSV, XSL, etc.) y sirve para presentar información estructurada en una página web de modo que esta información pueda ser almacenada, transmitida, procesada, visualizada e impresa por diversas aplicaciones y dispositivos.

Es decir, el XML es un archivo web que sirve principalmente para la transmisión de datos agregados (en bases de datos) entre diferentes aplicaciones y plataformas de forma universal.

## Acciones

* **+ Nuevo XML:** Crear un nuevo feed XML

## Ventajas de archivos XML

* Es un lenguaje fácilmente procesable y entendible por todos los navegadores.
* Separa el contenido de la presentación. Es decir no es un documento de representación gráfica como puede ser el HTML, el CSS o el Javascript. Este formato es ideal para presentar datos.
* Diseñado para cualquier lenguaje y alfabeto. **Es universal.**
* Fácilmente entendible para software y para personas usuarias.
* Tiene unas sencillas pero estrictas reglas de composición. Esto hace sencillo su análisis ya que siempre el proceso para realizar este tipo de archivos está muy definido.
* Posee una estructura jerárquica.
* En el contexto del SEO, el XML desempeña un papel crucial en la optimización y la visibilidad de un sitio web en los motores de búsqueda. La utilización de estos archivos, proporcionan una guía clara para los motores de búsqueda sobre la estructura y el contenido del sitio web.

## Contenido de un XML

Un XML contiene información detallada sobre todos los atributos de una variante de ítem, los cuales pueden ser editables o no.

En Hermes existen dos tipos de XML: uno para Google y otro para Meta. Cada uno debe cumplir con una estructura específica y contener ciertos parámetros obligatorios para asegurar su correcto funcionamiento en las respectivas plataformas publicitarias.

#### XML de Google

1. Los parámetros **obligatorios** para la creación de un XML de Google son:
   1. ID de producto: tag llamado \<g:id>
   2. Título del producto: tag llamado \<g:title>
   3. Color del producto: tag llamado \<g:color>
   4. Descripción del producto: tag llamado\<g:description>
   5. Link del producto: tag llamado \<g:link>
   6. Imagen del producto: tag llamado \<g:image\_link>
   7. Disponibilidad del producto o stock: tag llamado \<g:availability>
   8. Precio del producto:  tag llamado \<g:price>
   9. Condición del producto: tag llamado \<g:condition>.
   10. Marca: tag llamado \<brand>
2. Los parámetros **opcionales** son:
   1. Enlace de imagen adicional: llamado \<additional\_image\_link>
   2. Envío: tag llamado \<g:shipping\_weight>
   3. Tipo de producto: tag llamado \<g:product\_type>
   4. Cuotas: tag llamado \<g:installment> > este es el único parámetro que activandolo se activan más parámetros complementarios que lo hacen obligatorios:
      1. Meses: tag llamado \<g:months>
      2. Monto: tag llamado \<g:amount>
   5. Tags libres: tags llamado \<custom\_label\_0>,\<custom\_label\_1>, etc.

#### XML de Meta

1. Los parámetros **obligatorios** para la creación de un XML de Meta son:
   1. Item ID: tag llamado \<id> . En la columna 'Nombre del tag', asociarlo con 'ID de variante'.&#x20;
   2. Título del producto: tag llamado\<title>
   3. Descripción del producto: tag llamado\<description>
   4. Disponibilidad del producto: tag llamado \<availability>
   5. Condición del producto: tag llamado \<condition>
   6. Precio del producto:  tag llamado \<price>
   7. Link del producto: tag llamado \<link>
   8. Imagen del producto: tag llamado \<image\_link>
   9. Marca: tag llamado \<brand>
2. Los parámetros **opcionales** son:
   1. Variant ID: tag llamado \<variant\_id>
   2. Tipo de producto: tag llamado \<product\_type>
   3. Cuotas: tag llamado \<installment> . Este es el único parámetro que activandolo se activan más parámetros complementarios que lo hacen obligatorios:
      1. Meses: tag llamado \<months>
      2. Monto: tag llamado \<amount>
   4.  Tags libres: tags llamado \<custom\_label\_0>,\<custom\_label\_1>, etc.



