# Estructuras de control más comunes en Blade

## Imprimir variables

Si queremos imprimir una variable, podemos hacerlo utilizando la sintaxis de dobles llaves {{ }}

```
<li>{{ $user }}</li>
```

## Ciclos y estructuras

Si queremos utilizar ciclos y estructuras condicionales, podemos utilizar directivas. Las directivas de Blade van precedidas por un arroba (@) y luego el nombre de la directiva:

```
@foreach ($users as $user)
    <li>
    print ({{ $user }})
    </li>
@endforeach
```
