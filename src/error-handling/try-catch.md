# Try-Catch

El manejo de errores es una parte fundamental de la programación. En JavaScript, puedes manejar errores utilizando bloques `try-catch`. Un bloque `try` contiene el código que puede lanzar una excepción, y un bloque `catch` contiene el código que maneja la excepción.

```csharp
try
{
    // Código que puede lanzar una excepción
}
catch (Exception ex)
{
    // Código que maneja la excepción
}
```

En este ejemplo, el bloque `try` contiene el código que puede lanzar una excepción. Si se produce una excepción, el control se transfiere al bloque `catch`, que maneja la excepción. El parámetro `ex` contiene información sobre la excepción que se ha producido, como su tipo y mensaje.

## Ejemplo

En el siguiente ejemplo, se intenta dividir dos números y se maneja la excepción si el divisor es cero:

```csharp
try
{
    int result = 10 / 0;
    Console.WriteLine($"El resultado de la división es: {result}");
}
catch (DivideByZeroException ex)
{
    Console.WriteLine("Error: No se puede dividir por cero");
}
```

En este ejemplo, se intenta dividir `dividendo` por `divisor`. Si `divisor` es cero, se lanza una excepción `DivideByZeroException`, que se maneja en el bloque `catch`. En este caso, se imprime un mensaje de error en la consola.

