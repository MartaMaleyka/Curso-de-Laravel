[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 

# Vistas

En el marco MVC, la letra "V" significa Vistas . Separa la lógica de la aplicación y la lógica de presentación. Las vistas se almacenan en el directorio de resources/views . Generalmente, la vista contiene el HTML que será mostrado por la aplicación.

## Ejemplo
Observe el siguiente ejemplo para comprender mejor las vistas:

Paso 1 : copie el siguiente código y guárdelo en resources/views/test.blade.php

```html 
<html>
   <body>
      <h1>Hello, World</h1>
   </body>
</html>
````
Paso 2 : agregue la siguiente línea en el archivo routes/routes.php para establecer la ruta para la vista anterior.

```php
Route::get('/test', function() {
   return view('test');
});
````

Paso 3 : visite la siguiente URL para ver el resultado de la vista.

http://localhost:8000/test

Paso 4 : la salida aparecerá como se muestra en la siguiente imagen.

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/vistas.jpg)

## Pasar datos a vistas
Mientras se crea la aplicación, es posible que sea necesario pasar datos a las vistas. Pase una matriz para ver la función auxiliar. Después de pasar una matriz, podemos usar la clave para obtener el valor de esa clave en el archivo HTML.

### Ejemplo
Observe el siguiente ejemplo para comprender mejor cómo pasar datos a las vistas:

Paso 1 : copie el siguiente código y guárdelo en resources/views/test.php
```html 
<html>
   <body>
      <h1><?php echo $name; ?></h1>
   </body>
</html>
```
Paso 2 : agregue la siguiente línea en el archivo routes/web.php para establecer la ruta para la vista anterior.
routes/web.php

```php
Route::get('/test', function() {
   return view('test',["name"=>"Virat Gandhi"]);
});
```

Paso 3 : el valor del nombre de la clave se pasará al archivo test.php y $ name será reemplazado por ese valor.

Paso 4 : visite la siguiente URL para ver el resultado de la vista.

http://localhost:8000/test

Paso 5 : la salida aparecerá como se muestra en la siguiente imagen.

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/vistas1.jpg)

### Metodo with
También podemos usar el método with encadenándolo al llamado a la función view para pasar datos a la vista en formato de array asociativo:

```php
Route::get('/test', function() {
$users = [
'Joel',
'Ellie',
'Tess',
];

return view('users')->with([
    'users' => $users
]);  
});
```

### Metodo compact
Si los datos que queremos pasar a la vista se encuentran dentro de variables locales podemos utilizar la función compact,  la cual acepta como argumentos los nombres de las variables y las convierte en un array asociativo:


```php
Route::get('/test', function() {
$users = [
'Joel',
'Ellie',
'Tess',
];

$title = 'Listado de usuarios';

return view('users', compact('users', 'title'));

});
```
[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 

