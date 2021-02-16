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
1. insertaremos una clase en uno de las etiquetas <li>

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
````

