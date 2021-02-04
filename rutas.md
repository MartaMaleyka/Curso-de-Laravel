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
Route::get('contacto', function () {
         return 'Hola desde la pagina de contacto';
});
````

### Tipos de peticiones

Las mas comunes
```php
Route::get();              
Route::post();
``` 

```php
Route:::put();
Route::patch();       
Route::delete();  
```
Estas ultimas tres no son soportadas por los navegadores hoy dia, mas adelante veremos como Laravel maneja este tipo de peticiones

## Rutas con parametro

PARAMETRO OBLIGATORIO
```php
Route::get('saludo/{nombre}', function ($nombre) {
         return  'Hola ' .$nombre;
});
```

PARAMETRO NO OBLIGATORIO
```php
Route::get('saludo/{nombre?}', function ($nombre) {
         return  'Hola ' .$nombre;
});
```

