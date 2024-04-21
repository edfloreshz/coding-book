# Throw

La clausula `throw` se utiliza para lanzar una excepción en un programa. Una excepción es un objeto que representa un error o una condición inesperada que se produce durante la ejecución de un programa. Al lanzar una excepción, se interrumpe el flujo normal del programa y se transfiere el control a un bloque `catch` que maneja la excepción.

## Sintaxis

La sintaxis de la cláusula `throw` es la siguiente:

```csharp
throw new Exception("Mensaje de error");
```

En este ejemplo, se lanza una excepción de tipo `Exception` con un mensaje de error específico. El mensaje de error proporciona información adicional sobre la excepción que se ha producido y puede ser útil para identificar y depurar problemas en el programa.

## Ejemplo

En el siguiente ejemplo, se lanza una excepción si se intenta dividir por cero:

```csharp
try 
{
    int result = 10 / 0;
    Console.WriteLine($"El resultado de la división es: {result}");
}
catch (DivideByZeroException ex)
{
    Console.WriteLine("Error: No se puede dividir por cero");
    throw ex;
}
```

En este ejemplo, se intenta dividir `10` por `0`, lo cual resulta en una excepción `DivideByZeroException`. En el bloque `catch`, se imprime un mensaje de error en la consola y se lanza la excepción nuevamente utilizando la cláusula `throw`. Esto permite que la excepción se propague a bloques `catch` superiores o al sistema de tiempo de ejecución para su manejo.