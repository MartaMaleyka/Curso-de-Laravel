# Controladores

## ¿Qué son los controladores?
En lugar de definir toda la lógica de manejo de solicitudes como cierres en archivos de ruta, es posible que desee organizar este comportamiento utilizando clases de controlador. Los controladores pueden agrupar la lógica de manejo de solicitudes relacionadas en una sola clase. Los controladores se almacenan en el directorio app/Http/Controllers.

## Controladores basicos
A continuación, se muestra un ejemplo de una clase de controlador básica:

```php
<?php namespace App\Http\Controllers;

use App\Http\Controllers\Controller;

class UserController extends Controller {

    /**
     * Show the profile for the given user.
     *
     * @param  int  $id
     * @return Response
     */
    public function show()
    {
        return view('home');
    }

}
````

