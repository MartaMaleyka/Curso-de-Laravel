[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 

# Blade: Motor de plantillas de Laravel
Laravel 5.1 introduce el concepto de usar Blade , un motor de plantillas para diseñar un diseño único. El diseño así diseñado puede ser utilizado por otras vistas e incluye un diseño y una estructura consistentes.

En comparación con otros motores de plantillas, Blade es único en las siguientes formas:

- No restringe al desarrollador el uso de código PHP simple en las vistas.

- Las vistas así diseñadas se compilan y almacenan en caché hasta que se modifican.

La estructura de directorio completa de Laravel se muestra en la captura de pantalla que se proporciona aquí

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/blade.jpg)

Puede observar que todas las vistas se almacenan en el directorio resources / views y la vista predeterminada para el marco de Laravel es welcome.blade.php .

Tenga en cuenta que otras plantillas también se crean de manera similar.


## Pasos para crear un diseño de plantilla de hoja
Deberá seguir los siguientes pasos para crear un diseño de plantilla de hoja:

### Paso 1
- Cree una carpeta de diseño dentro de la carpeta de resources/vistas . Usaremos esta carpeta para almacenar todos los diseños juntos.

- Cree un nombre de archivo master.blade.php que tendrá el siguiente código asociado:

```html
<html>
   <head>
      <title>DemoLaravel - @yield('title')</title>
   </head>
   <body>
      @yield('content')
   </body>
</html>
```
### Paso 2
En este paso, debe ampliar el diseño. Ampliar un diseño implica definir los elementos secundarios. Laravel usa la directiva Blade @extends para definir los elementos secundarios.

Cuando amplíe un diseño, tenga en cuenta los siguientes puntos:

- Las vistas definidas en Blade Layout inyectan el contenedor de una manera única.

- Se crean varias secciones de vista como elementos secundarios.

- Los elementos secundarios se almacenan en la carpeta de diseños como child.blade.php

Aquí se muestra un ejemplo que muestra la extensión del diseño creado anteriormente:

```laravel
@extends('layouts.app')
@section('title', 'Page Title')
@section('sidebar')
   @parent
<p>This refers to the master sidebar.</p>
@endsection
@section('content')
<p>This is my body content.</p>
@endsection
````

