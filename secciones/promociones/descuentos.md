# Descuentos

### **Panel de Control**

La pantalla principal ofrece una visión global con indicadores de:

* Total de descuentos: Histórico acumulado.
* Activos: Promociones vigentes hoy.
* Programados: Promociones futuras.
* Usos hoy: Cantidad de veces que se aplicaron beneficios en las últimas 24hs.

### **Paso a Paso para Crear un Descuento**

Al hacer clic en "Crear descuento", se inicia un asistente de 7 pasos:

1. Tipo: Selecciona la lógica de la promoción:
   * Descuento Carrito: Porcentaje sobre el carrito total segun condiciones.
   * Descuento por Cantidad: Lógicas tipo 2x1, 3x2 segun condiciones.
   * Envío Gratis: Elimina el costo logístico segun condiciones.
   * Artículo Gratis: Regala un SKU específico segun condiciones.
   * Descuento por Categoría: Rebaja sobre el ítem más barato segun condiciones.
   * Producto con Bonificación: Descuento fijo o porcentual sobre un SKU puntual segun condiciones.
   * _Tip: Puedes usar la IA para describir la promo en lenguaje natural y que el sistema configure los pasos automáticamente._
2. Método: Define si es un **Descuento automático** (promoción en el carrito de compras) o un **Código de descuento** (cupón que aplicara al ingresarlo en el carrito de compras)
3. Condiciones: Define los requisitos de compra para que el método (paso 2) aplique. Pueden ser:
   * Monto mínimo de compra: El descuento aplicará cuando el carrito supere un valor X (ej: $100.000).
   * Cualquier articulo de las siguientes categorías: El descuento aplicará cuando el carrito contenga artículo/s de X categoría/s.
     * Atención: también se puede configurar una cantidad de aritulos de la categoría que estas configurando (ej: 2 articulos de la categoría SALE)
   * Excluir categorías de la promoción: El descuento NO aplicará a los carritos que contengan artículo/s de X categoría/s.
   * Items especificos en el carrito: El descuento se aplica solo si el carrito contiene determinados productos, puede ser uno solo, muchos o combinaciones dependiendo si se configura con Y (tiene que incluir todos los configurados) u O (tiene que incluir uno de los configurados)
4. Beneficio: Configura el valor real del descuento y a qué productos se aplicará dentro del carrito de compra.
   * Uso total: Cantidad máxima de veces que se puede usar la promoción en toda la tienda.
   * Uso por cliente: Limita el beneficio a un número de aplicaciones por usuario registrado.
   * Combinaciones: Activa si la promo puede acumularse con otros cupones activos.
5. Límites:
   * Límite de usos totales: Cantidad de veces que la promo puede usarse en toda la tienda.
   * Límite por cliente: Cuántas veces puede usarla un mismo usuario.
   * Combinable: Define si puede convivir con cupones de descuento.
6. Programación: Fecha y hora de inicio/fin, y selección de días de la semana activos.
7. Resumen: Revisión final y asignación de un nombre interno para el listado.
