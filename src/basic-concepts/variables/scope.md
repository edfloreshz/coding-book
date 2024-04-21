# Alcance

El alcance de una variable es la región del programa en la que la variable es accesible. En la mayoría de los lenguajes de programación, el alcance de una variable está determinado por el bloque de código en el que se declara la variable.

Por ejemplo, en el siguiente código, la variable `x` solo es accesible dentro del bloque de código que comienza con `{` y termina con `}`:

```csharp
{
    int x = 10;
    Console.WriteLine(x); // 10
}
Console.WriteLine(x); // Error: 'x' no existe en el contexto actual
```

En este caso, la variable `x` tiene un alcance local, lo que significa que solo es accesible dentro del bloque de código en el que se declara.

## Alcance global

En contraste, una variable con alcance global es accesible desde cualquier parte del programa. Por ejemplo, en el siguiente código, la variable `y` se declara fuera de cualquier bloque de código y, por lo tanto, tiene un alcance global:

```csharp
int y = 20;

{
    Console.WriteLine(y); // 20
}
Console.WriteLine(y); // 20
```

En este caso, la variable `y` tiene un alcance global, lo que significa que es accesible desde cualquier parte del programa.
