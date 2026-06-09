# Conceptos básicos

### ¿Qué es una integración?

Es la conexión entre dos sistemas que permite intercambiar información automáticamente.

Su objetivo es:

* Enviar datos (ej: órdenes, clientes, stock)
* Recibir datos
* Mantener sistemas sincronizados&#x20;

### Tipos de integración

Existen 3 tipos de integración:

#### 1. Integración por API

La API es la opción estándar recomendada para integraciones.

Se compone de:

* **Método:**
  * <mark style="color:$success;">GET</mark> → consulta datos
  * <mark style="color:$success;">POST</mark> → envía/modifica datos
* **Endpoint:** URL donde se envía la request
* **Formato:** Estructura de datos (generalmente JSON si es api)
* **Autenticación:** Token / credenciales para validar acceso a la información

A su vez, una integración por API puede ser de dos formas:

* Activa (con polling): El sistema **consulta periódicamente** a otro sistema para detectar cambios o nueva información. La acción siempre la inicia el propio sistema. Ejemplo: consultar órdenes cada 5 minutos.
* Reactiva (sin polling): El sistema **envía información automáticamente** cuando ocurre un evento, sin necesidad de consultas periódicas. La acción también la inicia el propio sistema. Ejemplo: enviar una orden al momento de su aprobación.

#### 2. Integración por Webhooks

Es una integración basada en eventos, donde un sistema externo notifica automáticamente a otro cuando ocurre un evento, enviando la información a un endpoint definido.&#x20;

Ejemplo: recibir una notificación cuando una orden pasa a “pagada”.

***

#### Diferencia clave entre integración por API activa, reactiva y webhooks

* Activa → consulta
* Reactiva → envía
* Webhook → recibe notificación externa&#x20;

***

#### 3. Integración por archivos (FTP / CSV)

Es el método más antiguo, donde los sistemas intercambian información mediante archivos, generalmente en formato CSV, que se envían o descargan desde un servidor (FTP/SFTP). Funciona en intervalos (no en tiempo real).&#x20;

Este tipo de integración es el menos recomendado porque tiene baja trazabilidad, no permite validación inmediata de errores y tiene mayor riesgo de inconsistencias.

Ejemplo: subir un archivo con órdenes una vez al día.

### Consideraciones Generales

* Las integraciones son mayormente similares en concepto de envío y recepción de datos por lo que se tiene que:
  * Priorizar APIs sobre archivos
  * Implementar procesos asincrónicos
  * Implementar manejo de errores y reintentos
