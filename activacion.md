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
      {{ request() }}
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

````
{{ dump(request()) }}
````

La salida:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/CSS3.PNG)
