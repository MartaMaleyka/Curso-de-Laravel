[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 

# Controladores

## ¿Qué son los controladores?
En lugar de definir toda la lógica de manejo de solicitudes como cierres en archivos de ruta, es posible que desee organizar este comportamiento utilizando clases de controlador. Los controladores pueden agrupar la lógica de manejo de solicitudes relacionadas en una sola clase. Los controladores se almacenan en el directorio app/Http/Controllers.

## Crear controlador
Para crear un controlador vamos a la consola y luego a la carpeta del proyecto y ejecutamos el siguiente comando 

````
php artisan make:controller PagesController
````
Esto se guardara en la carpeta App\Http\Controllers

## Controladores basicos
A continuación, se muestra un ejemplo de una clase de controlador básica:

Dentro de esta clase (en nuestro caso HomeController) agregamos nuestros métodos públicos (llamados acciones), que después podemos enlazar a una ruta:

```php
<?php namespace App\Http\Controllers;

use App\Http\Controllers\Controller;

class HomeController extends Controller {

    /**
     * Show the profile for the given user.
     *
     * @param  int  $id
     * @return Response
     */
    public function index()
    {
        return view('home');
    }

}
````

Luego vamos a la carpeta routes, al archivo web.php

Para enlazar una ruta a un controlador pasamos como argumento el nombre del controlador y del método que queremos enlazar, separados por un @. En este caso queremos enlazar la ruta /home al método index del controlador HomeController:



````
Route::get('/home', 'HomeController@index');
````

[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 
