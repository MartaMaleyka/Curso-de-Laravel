# Rutas

## ¿Qué son las rutas?

Las rutas son una capa muy importante en Laravel, es por ello que el Framework destina un directorio en la carpeta raíz, llamado routes, para ubicar todas las rutas de la aplicación.  Por defecto, tiene 2 archivos de rutas web.php y api.php. Como sus nombres lo expresan en web.php se definen las rutas para la web y en api.php las rutas para crear APIs para la aplicación.
En este capitulo nos enfocaremos en las rutas web.

##  Definiendo rutas
````php
Route::get('/esta-es-la-url', function () {
         return 'Hola mundo';
});
````

### Ejemplos

Ruta de inicio 

````php
Route::get('/', function () {
         return 'Hola desde la pagina de inicio';
});

````

Ruta contacto

````php

Route::get(‘contacto', function () {
         return 'Hola desde la pagina de contacto';
});

````
