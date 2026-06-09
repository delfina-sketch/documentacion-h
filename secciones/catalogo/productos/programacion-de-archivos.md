# Programación de archivos

### Programación de archivo

La opción **Programar procesamiento** permite definir una fecha específica para que el archivo CSV se procese de forma automática en un momento posterior, en lugar de ejecutarse inmediatamente después de la carga.

Esta funcionalidad resulta útil cuando se necesita:

* Coordinar actualizaciones de stock o precios en un horario determinado.
* Evitar impactos en horario comercial.
* Sincronizar cambios con campañas, lanzamientos o acciones promocionales.
* Planificar actualizaciones masivas fuera del horario pico.

#### Configuración

1. Seleccionar la acción a realizar sobre los valores:

* Pisar: reemplaza la información actual por la nueva del csv
* Sumar: adiciona información a la ya existente. Sólo aplica a archivos de stock o categorías.
* Restar: sustrae información de la ya existente. Sólo aplica a archivos de stock o categorías.

2. Cargar el archivo CSV correspondiente.
3. Activar el check **“Programar procesamiento”**.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-02-27 a las 14.52.29.png" alt="" width="563"><figcaption></figcaption></figure>

4. Seleccionar la fecha (y horario, si corresponde).

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2026-02-27 a las 14.52.38.png" alt="" width="563"><figcaption></figcaption></figure>

5. Hacer clic en **“Subir y procesar”**.

El archivo quedará pendiente y -de estar todo correcto- se ejecutará automáticamente en la fecha y hora indicada. En caso contrario, se informará "CSV inválido" y deberá revisarse su armado.&#x20;

{% hint style="info" %}
### 📌 Consideraciones importantes



* Hasta que llegue la fecha programada, los cambios no impactarán en la tienda.
* Es recomendable validar previamente el archivo para evitar errores en el procesamiento.
* Una vez procesado, los valores se actualizarán según la acción seleccionada (Pisar, Sumar o Restar).
* Si no se activa la opción de programación, el archivo se procesará de forma inmediata.
{% endhint %}



