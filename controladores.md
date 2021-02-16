[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 

# Controladores

## ¿Qué son los controladores?
En lugar de definir toda la lógica de manejo de solicitudes como cierres en archivos de ruta, es posible que desee organizar este comportamiento utilizando clases de controlador. Los controladores pueden agrupar la lógica de manejo de solicitudes relacionadas en una sola clase. Los controladores se almacenan en el directorio app/Http/Controllers.

## Crear controlador
Para crear un controlador vamos a la consola y luego a la carpeta del proyecto y ejecutamos el siguiente comando 

````
php artisan make:controller HomeController
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

## Resource Controller
Los controladores de recursos son solo controladores de Laravel con todos los métodos para crear, leer, actualizar y eliminar un recurso (o un modelo). Puede crear un controlador de recursos con este comando artisan:

````
php artisan make:controller UserController --resource
````

Este comando creará una clase llamada UserController.php en su directorio de controladores y tendrá que crear automáticamente 7 métodos, index, show, create, store, edit, update, destroy. Todos estos métodos estarán vacíos; deberá completarlos con la lógica de cada acción. 

### Ruta de recursos de Laravel
Laravel también proporciona una manera fácil de hacer rutas para los controladores de recursos usando:


Route::resource('users', 'UserController');

//  GET   /user     
UserController@index 

//  GET    /user/create     
UserController@create 

//  POST   /user            
UserController@store 

//  GET    /user/{id}       
UserController@show 

//  GET    /user/{id}/edit  
UserController@edit 

//  PUT    /user/{id}       
UserController@update 

//  DELETE /user/{id}       
UserController@destory


Una clase controladora con los metodos se verà asì:

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class UserController extends Controller
{
    /**
     * Display a listing of the resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function index()
    {

}

    /**
     * Show the form for creating a new resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function create()
    {
        return view("tarea.create");
    }

    /**
     * Store a newly created resource in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return \Illuminate\Http\Response
     */
    public function store(Request $request)
    {
        //
    }

    /**
     * Display the specified resource.
     *
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function show($id)
    {
        //
    }

    /**
     * Show the form for editing the specified resource.
     *
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function edit($id)
    {
        //
    }

    /**
     * Update the specified resource in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function update(Request $request, $id)
    {
        //
    }

    /**
     * Remove the specified resource from storage.
     *
     * @param  int  $id
     * @return \Illuminate\Http\Response
     */
    public function destroy($id)
    {
        //
    }
}
```

Este método creará las 7 rutas necesarias para acceder a cada acción desde el navegador. Puede personalizar esto para crear solo ciertas rutas que necesita o dejar las que no necesita así.

````
Route::resource('user', 'UserController')->only(['index', 'show']); 
Route::resource('user', 'UserController')->except(['create', 'store', 'update', 'destroy']);
````

[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 
