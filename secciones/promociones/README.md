# Promociones

### Introducción

El módulo de Promociones de Hermes es el motor de beneficios del e-commerce, diseñado para incentivar la conversión mediante reglas de negocio flexibles. Técnicamente, este módulo centraliza la lógica de descuentos y créditos.

Este módulo se divide estructuralmente en dos apartados principales: Descuentos y Cupones.

### Estructura del Módulo

* Descuentos (Promociones Automáticas): Son reglas lógicas que el sistema evalúa en tiempo real. Se aplican de forma automática cuando el carrito del usuario cumple con las condiciones predefinidas (monto mínimo, categorías específicas, cantidad de ítems, etc.).
* Cupones (Validación por Código): Son beneficios vinculados a una cadena alfanumérica única que el cliente debe ingresar manualmente. A diferencia de los descuentos automáticos, los cupones permiten un control estricto sobre la distribución del beneficio y cuentan con una gestión de usos limitada por sistema.

### Interacción y Tipología Técnica

Es fundamental comprender que, aunque aparecen en apartados distintos, comparten motores de validación similares pero con finalidades diferentes:

1. Descuentos vs. Cupones de Descuento: El sistema permite crear un beneficio porcentual o de monto fijo de dos maneras:
   1. Como Descuento: Se visualiza directamente en el resumen de compra si el usuario cumple los requisitos (ej. "Hot Sale - 20% OFF automático").
   2. Como Cupón: Requiere el ingreso del código para activar la misma lógica de descuento (ej. "CUPON20").
2. Cupones de Crédito (No comerciales): Técnicamente, el apartado de Cupones tiene una función adicional que no poseen los Descuentos: la gestión de Créditos de Cliente.
   1. Estos cupones se emiten generalmente por procesos de post-venta (cambios o devoluciones).
   2. A diferencia de un cupón promocional, el Cupón de Crédito representa un saldo a favor del usuario y suele configurarse para ser acumulable con cualquier otra promoción activa en el sitio.
3. Lógica de Convivencia y Prioridades: Cuando múltiples beneficios coinciden en un mismo carrito, el sistema aplica una jerarquía técnica para evitar conflictos:
   1. Prioridad por número: En los descuentos automáticos, el sistema otorga precedencia a la regla con menor valor numérico (Prioridad 1 es la más alta).
   2. Acumulación: Cada cupón o descuento posee un atributo de "Combinable" que determina si el sistema debe sumar los beneficios o aplicar solo el de mayor relevancia económica para el usuario.
