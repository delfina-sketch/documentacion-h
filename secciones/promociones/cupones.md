# Cupones

### Panel de Control de Cupones

La pantalla principal ofrece una visión global del estado de los códigos mediante indicadores y herramientas de gestión:

* Total cupones: Histórico completo de todos los cupones generados en la plataforma.
* Sin usar: Cantidad de códigos que aún no han sido aplicados en ninguna transacción.
* Usados: Total de cupones que ya han sido validados satisfactoriamente.
* Vencidos: Cantidad de códigos cuya fecha de vigencia ha expirado.
* Buscador dinámico: Localización de códigos específicos en tiempo real por nombre o caracteres.
* Filtros Avanzados: Permite segmentar por Tipo (monto fijo o porcentaje), estado de uso y fecha de vencimiento y rangos de fecha de la misma.

### Paso a Paso para Crear un Nuevo Cupón manualmente

Al hacer clic en el botón "+ Nuevo cupón", se despliega una interfaz unificada con los siguientes bloques de configuración:

1. **Tipo de Cupón:** Define la naturaleza del beneficio económico:

* Monto Fijo: Un valor monetario específico (ej: $10.000).
* Porcentaje: Un descuento basado en una tasa sobre el total (ej: 20%).

2. **Código y Descuento**

* Código del cupón: Es el texto que el usuario ingresará. Se puede escribir manualmente (debe ser siempre en MAYÚSCULAS) o utilizar el botón "Generar" para que el sistema asigne uno aleatorio.
* Monto de descuento: Define numéricamente el valor del beneficio (ya sea el monto en pesos o el porcentaje seleccionado en el paso anterior).

3. **Vigencia**

* Válido desde / Válido hasta: Calendario obligatorio para establecer el periodo exacto de tiempo en el que el código será reconocido por el carrito. El cupón dejará de funcionar automáticamente a las 00:00 del día siguiente a la fecha de vencimiento.

4. **Restricciones:** Configura las reglas de uso para proteger la rentabilidad:

* Cantidad máxima de usos: Define cuántas veces se puede aplicar el cupón en total en la tienda. Importante: El uso se descuenta en el momento en que el cliente lo aplica en el carrito, aunque no finalice la compra, para evitar que códigos limitados queden bloqueados en carritos abandonados.
* Monto mínimo de compra: El cupón solo será válido si el subtotal del carrito iguala o supera este valor.
* Límite por mail: Si se configura, restringe el uso del código a una cantidad determinada de veces por cada dirección de correo electrónico única.
* Límite por categorías: Permite seleccionar qué categorías de productos están habilitadas para recibir el descuento del cupón. Si se deja vacío, aplica a todo el catálogo.

### Gestión Masiva (Acciones en Masa)

Para operaciones de gran volumen, utilice el botón "Acciones en masa".

#### Creación Masiva vía CSV

1. Seleccione "Crear cupones".
2. Cargue un archivo CSV respetando la siguiente estructura:
   1. Columna 1 (code): Opcional. Código personalizado o automático si se deja vacío.
   2. Columna 2 (type): Obligatorio. Completar con `AmountCoupon` (fijo) o `PercentageCoupon` (porcentaje).
   3. Columna 3 (discount\_cents): Obligatorio. Monto en centavos sin puntos ni comas (ej: para $10.000 colocar `1000000`).
   4. Columna 4 (from\_date): Opcional. Fecha de inicio (DD/MM/YYYY).
   5. Columna 5 (expiration\_date): Obligatorio. Fecha de vencimiento (DD/MM/YYYY).
   6. Columna 6 (general\_uses): Opcional. Cantidad de usos totales (por defecto 1).
   7. Columna 7 (email\_uses): Opcional. Límite por email (por defecto 1).
   8. Columna 8 (minimum\_amount\_cents): Opcional. Monto mínimo en centavos.
   9. Columna 9 (category\_ids): Opcional. IDs de categorías separados por coma.
   10. Columnas 10-14 (free\_shipping, outlet, no\_outlet, credit\_coupon, active\_status): Valores `true`/`false` o `1`/`0` para configurar los atributos y el estado inicial.
3. Haga clic en **"Importar"** para iniciar el proceso de carga. Un pop up indicara si el csv importó correctamente. En caso de corregir los errores, si es necesario puede volver a cargar el archivo teniendo en cuenta solo subir los errores y no repetir la matriz.

{% hint style="info" icon="folder" %}
Ejemplo de modelo de archivo a subir: [Link](https://docs.google.com/spreadsheets/d/1DRv9zlruYcPk9D9liqmSOl8CfbWAXNvFFfJzwEp6rDg/edit?gid=15857427#gid=15857427)
{% endhint %}

#### Actualización Masiva vía CSV

Permite modificar masivamente solo los campos actualizables de cupones existentes.

1. Seleccione "Actualizar cupones".
2. Estructura del archivo:
   1. Columna 1 (id): Obligatorio. Identificador interno único del cupón.
   2. Columna 2 (expiration\_date): Nueva fecha de vencimiento (DD/MM/YYYY).
   3. Columna 3 (active\_status): Nuevo estado (`1` para Activo, `0` para Inactivo).
3. Haga clic en **"Importar"** para iniciar el proceso de carga. Un pop up indicara si el csv importó correctamente. En caso de corregir los errores, si es necesario puede volver a cargar el archivo teniendo en cuenta solo subir los errores y no repetir la matriz.

{% hint style="info" icon="folder" %}
Ejemplo de modelo de archivo a subir: [Link](https://docs.google.com/spreadsheets/d/14wTy7vWN4ihvu1aLhDY4PFCjimPSLjQ9lhs9E0FrAkE/edit?gid=15857427#gid=15857427)
{% endhint %}

{% hint style="info" icon="triangle-exclamation" %}
Importante:

* **No se podrán modificar otros campos del cupón** como el código, el tipo, el monto, las condiciones o el alcance.
* Solo se permiten cambios sobre **fecha de expiración** y **estado de actividad**.
{% endhint %}

### Botón Exportar

El sistema permite descargar el detalle de los cupones configurados.<a class="button secondary"></a>

* Función: Genera un archivo CSV con toda la información técnica de los cupones (IDs, códigos, usos restantes, fechas, etc.).
* Recomendación: Para evitar sobrecargar el servidor y obtener archivos muy pesados, se recomienda aplicar filtros previamente (ej: filtrar por cupones "Activos" o por una fecha determinada) y luego realizar la exportación.

### Gestión de Usos y Aplicaciones

Es fundamental comprender la lógica técnica detrás del consumo de beneficios para brindar soporte al usuario que interactúa con la web:

* Descuento de uso inmediato: Cada vez que un cupón se aplica exitosamente en el carrito, el contador de "aplicaciones disponibles" disminuye.
* Carritos abandonados: Si un usuario aplica un cupón pero no finaliza la compra, ese uso ya se considera consumido. Esto previene que códigos con stock limitado queden bloqueados en sesiones inactivas.
* Recuperación de uso: Si el cliente elimina el cupón antes de salir del carrito, el sistema le devuelve la posibilidad de usarlo nuevamente.

Nota Técnica: No se recomienda eliminar cupones o promociones antiguas del Backoffice, ya que esto afecta la integridad de los datos históricos en el reporte de órdenes y facturación.
