# Acciones a realizar

Una vez descargado el csv de ítems, el siguiente paso es armar el archivo utilizando la información necesaria de lo que se quiera modificar.&#x20;

Se podrán realizar modificaciones sobre varios elementos en un mismo procesamiento de CSV, siempre y cuando el archivo en cuestión cumpla con las siguientes 2 reglas:

1. La modificación debe ser sobre un mismo criterio de columna, sea variantes o ítems
2. La acción a realizar debe ser la misma para todas las columnas (pisar, sumar o restar)

{% hint style="success" %}
**En el siguiente archivo podrás visualizar todas las acciones posibles de actualización:** [**Modificaciones vía CSV**](https://docs.google.com/spreadsheets/d/1watxVk29qfmzZMhgnbFIXE5oP-Z3hQ1o9QIHvMPvmSI/edit?gid=0#gid=0)
{% endhint %}

#### **Acciones** <a href="#acciones" id="acciones"></a>

Cada vez que se sube un csv, Hermés te da tres opciones de acción:

1. Pisar: reemplaza la información actual por la nueva del csvComment
2. Sumar: adiciona información a la ya existente. Sólo aplica a archivos de stock o categorías.
3. Restar: sustrae información de la ya existente. Sólo aplica a archivos de stock o categorías.

#### Ejemplo de actualización de ítems <a href="#ejemplo" id="ejemplo"></a>

Si procesáramos el siguiente CSV activaríamos las cucardas "sale" de los ítems cuyo id figuran en la columna #1, y desactivaríamos sus cucardas de descuento:

![](https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Fpow-hermes.zendesk.com%2Fhc%2Farticle_attachments%2F360056185554%2FCaptura_de_Pantalla_2020-01-28_a_la_s__18.14.11.png\&width=768\&dpr=3\&quality=100\&sign=7c72be9\&sv=2)

#### Ejemplo de actualización de variantes

Si procesáramos el siguiente CSV de variantes a través de la acción "pisar", los precios de lista de las 3 variantes de la columna #1 pasarían a ser ARS $1.500, y su stock 1, 1 y 0 respectivamente:

![](https://pow-ecommerce.gitbook.io/hermes/~gitbook/image?url=https%3A%2F%2Fpow-hermes.zendesk.com%2Fhc%2Farticle_attachments%2F360057066293%2FCaptura_de_Pantalla_2020-01-28_a_la_s__18.17.19.png\&width=768\&dpr=3\&quality=100\&sign=3568ad21\&sv=2)
