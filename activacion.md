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

