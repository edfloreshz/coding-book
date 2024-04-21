# Declaración de funciones

Las funciones son una de las herramientas más importantes en la programación. Una función es un bloque de código reutilizable que realiza una tarea específica y puede ser invocado (llamado) desde otras partes de su programa. 

Las funciones son esenciales para la programación eficiente y organizada, ya que permiten dividir un programa en pequeñas partes que pueden ser comprendidas y mantenidas de manera más fácil.

Cada función tiene un nombre **único** y puede aceptar argumentos (también conocidos como parámetros) que se pasan a la función cuando se invoca. La función realiza su tarea utilizando estos argumentos y, a menudo, devuelve un resultado o valor.

Aquí hay un ejemplo en C# de una función que acepta dos argumentos y devuelve su suma:

```csharp
static void Main(string[] args)
{
    int resultado = Sumar(3, 4);
    Console.WriteLine(resultado); // Imprime 7
}

static int Sumar(int a, int b)
{
    int resultado = a + b;
    return resultado;
}
```

> En este ejemplo, la función se llama `sumar` y acepta dos argumentos, `a` y `b`. La función realiza la operación de suma y devuelve el resultado asignándolo a la variable `resultado`. Luego, se invoca la función con los valores `3` y `4` y se imprime el resultado devuelto.
> 

Es importante tener en cuenta que las funciones pueden ser llamadas muchas veces en un programa sin necesidad de escribir el código de la función varias veces. Esto hace que sea más fácil de mantener y depurar su código, ya que solo necesita modificar la función en un solo lugar en lugar de en muchos lugares diferentes.

Además, las funciones también ayudan a mantener la claridad y la legibilidad de su código, ya que permiten darle un nombre descriptivo a un bloque de código en lugar de tener que leer y comprender una serie de líneas de código en su totalidad.