# Estructuras de control más comunes en Blade

## Imprimir variables

Si queremos imprimir una variable, podemos hacerlo utilizando la sintaxis de dobles llaves {{ }}

```html
<li>
    {
    { $user }
    }
</li>
```
Seria asi 

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/imprimir.PNG)

Pero para propositos de que se muestre, lo estaré haciendo como se muestra arriba.

## Ciclos y estructuras

Si queremos utilizar ciclos y estructuras condicionales, podemos utilizar directivas. Las directivas de Blade van precedidas por un arroba (@) y luego el nombre de la directiva:

```php
@foreach ($users as $user)
    <li>
    {
    { $user }
    }
    </li>
@endforeach

```

### Directiva if

También podemos utilizar la directiva @if:

```php
@if (! empty($users))
    ...
@endif
```

### Directiva if/else 

La directiva @if puede ser utilizada junto con un bloque else (utilizando @else):
```php
@if (! empty($users))
    ...
@else
    <p>No hay usuarios registrados.</p>
@endif
```


