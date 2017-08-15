FormiikLabs APIs
===================

Para poder utilizar los servicios de formiikLabs es necesario realizar las siguientes operaciones

**1. Obtener una llave de prueba**

Ingresar al portal de desarrollador y crear una cuenta

https://formiiklabs.portal.azure-api.net

Es necesario suscribirse al producto formiiklabs_preview eso se hace en el tab Products en el portal.

<img src="https://formiiklabsapi1964.blob.core.windows.net/formiiklabssamples/tab_productos.png" width="300">
<img src="https://formiiklabsapi1964.blob.core.windows.net/formiiklabssamples/suscripcion.png" width="300">
<img src="https://formiiklabsapi1964.blob.core.windows.net/formiiklabssamples/confirmacion.png" width="300">

Una vez realizada la suscripción, en la sección PROFILE se muestran las llaves de acceso a la API.
<img src="https://formiiklabsapi1964.blob.core.windows.net/formiiklabssamples/llaves.png" width="300">


> **Nota:**
> - Se envía un correo electrónico de confirmación, es necesario dar click en el link para continuar con el proceso.
>  - En algunas ocasiones el correo electrónico se envía a la carpeta de spam.
>  - Este preview tiene un limite de llamadas de 10 llamadas por minuto y maximo 100 llamadas por mes.


**2. Consumir la API**

Para consumir cualquiera de las APIs, es necesario descargar de este repositorio el archivo con la especificación de la API que se quiera probar, dichos archivos tienen la siguiente nomenclatura "formiiklabs_NOMBREAPI_api.json" siendo **NOMBREAPI** el nombre del API a probar

Los archivos estan creados siguiendo la especificación OpenAPI 2.0 por lo que es necesario utilizar un visor de esa especificación para revisar la documentacion de cada API. Por ejemplo https://restlet.com/modules/studio/

Para consumir las API se puede utilizar un cliente de APIs Rest como https://restlet.com/modules/client/ 
basta con importar el archivo de especificación en el cliente y agregar en el header **Ocp-Apim-Subscription-Key** nuestra llave de suscripción.


> **Nota:**
> - Hay ejemplos de uso en el wiki de este repositorio https://github.com/formiiklabs/apis/wiki
> - Todas las APIs son asíncronas, y constan de 2 métodos uno para indicar el recurso a ser procesado y otro para revisar el estatus de la operacion y/o resultado.

