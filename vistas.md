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

