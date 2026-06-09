# Estados de pago

## **Descripción**

Los estados de pago existentes en Hermes son:

* Aprobado -> el pago fue acreditado por la entidad bancaria del usuario.
* Rechazado -> el pago fue rechazado por la entidad bancaria del usuario. Algunos motivos posibles son fondos insuficientes, carga incorrecta de datos en el formulario, sospecha de fraude, entre otros.
* Pendiente -> el usuario eligió pagar en efectivo en un comercio de Rapipago o Pago Fácil habilitado.&#x20;
* Cancelado -> la orden fue cancelada por falta de pago.
* Reintegrado -> el usuario solicitó el reintegro del dinero.
* En proceso -> el pago quedó en evaluación por parte de Mercado Pago. Es un estado intermedio entre Pendiente y Aprobado/Rechazado.
