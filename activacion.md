# Activación de links de navegación

Regresaremos al archivo master.blade.php 

```html
<html>
   <head>
      <title>DemoLaravel - @yield('title')</title>
   </head>
   <body>
     <nav>
      <ul>
        <li><a href="/">Home </a></li>
        <li><a href="/about">About </a></li>
        <li><a href="/portfolio">Portafolio </a></li>
        <li><a href="/contact">Contact </a></li>
       </ul>
     </nav>
      @yield('content')
   </body>
</html>
````

Ahora para activar el link haremos lo siguiente:
1. Insertaremos una clase en uno de las etiquetas < li >
2. Haremos una inserción de codigo css en una etiqueta <style>
   
```html
<html>
   <head>
      <style> 
         .active a{
         color:red;
         text-decoration:none;
         }
     </style>
      <title>DemoLaravel - @yield('title')</title>
   </head>
   <body>
     <nav>
      <ul>
        <li class="active"><a href="/">Home </a></li>
        <li><a href="/about">About </a></li>
        <li><a href="/portfolio">Portafolio </a></li>
        <li><a href="/contact">Contact </a></li>
       </ul>
     </nav>
      @yield('content')
   </body>
</html>
```

La salida:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/CSS1.PNG)

Ahora haremos uso de la función request() de la clase Illuminate\Http\Request que proporciona una clase orientada a objetos para interactuar con la solicitud HTTP actual que está manejando su aplicación, así como para recuperar la entrada, las cookies y los archivos que se enviaron con la solicitud.

```html
<html>
   <head>
      <style> 
         .active a{
         color:red;
         text-decoration:none;
         }
     </style>
      <title>DemoLaravel - @yield('title')</title>
   </head>
   <body>
      <pre>
      {
      {
      request() 
      }
      }
      </pre>
     <nav>
      <ul>
        <li class="active"><a href="/">Home </a></li>
        <li><a href="/about">About </a></li>
        <li><a href="/portfolio">Portafolio </a></li>
        <li><a href="/contact">Contact </a></li>
       </ul>
     </nav>
      @yield('content')
   </body>
</html>
```

La salida:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/CSS2.PNG)

Para hacer la salida en formato JSON usaremos la funcion dump()

````html
{{ 
dump(request())
}}
````

La salida:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/CSS3.PNG)

Ahora usaremos el metodo path, que devuelve la información de la ruta de la solicitud. Entonces, si la solicitud entrante está dirigida a http://example.com/foo/bar, el pathmétodo devolverá foo/bar:

````html
{{ request()->path() }}
````

SALIDA

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/CSS4.PNG)


Haremos uso del metodo routeIs(), que puede determinar si la solicitud entrante coincide con una ruta con nombre, y devuekve un valor booleano :

````
{{ request()->routeIs("home") }}
````
![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/CSS5.PNG)

Usaremos este metodo para identificar las rutas de la siguiente manera
````
        <li class="{
        {request()->routeIs('home') ? 'active': '' }
        }"><a href="/">Home </a></li>
````
Haciendo uso del identificador ternario "?" que es una forma abreviada de la sentencia if else que usamos para las decisiones en PHP (y en otros lenguajes de programación), usarla nos ayuda a crear código más limpio y fácil de entender y además nos ayuda a escribir código más rápido por que hay menos caracteres que escribir.
<code>
<!DOCTYPE html>
<html lang="en">
<head>
<style>
.active a{
  color:red;
  text-decoration:none;
}
</style>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>@yield("title")</title>
</head>
<body>
<nav>
      <ul>
        <li class="{{request()->routeIs('home') ? 'active': '' }}"><a href="/">Home </a></li>
        <li class="{{request()->routeIs('about') ? 'active': '' }}"> <a href="/about">About </a></li>
        <li class="{{request()->routeIs('portfolio') ? 'active': '' }}"><a href="/portfolio">Portafolio </a></li>
        <li class="{{request()->routeIs('contact') ? 'active': '' }}"><a href="/contact">Contact </a></li>
       </ul>
     </nav>
      @yield('content')
</body>
</html>

</code>

