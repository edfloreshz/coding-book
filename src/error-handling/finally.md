# Finally

La cláusula `finally` es utilizada en conjunto con `try` y `catch` para manejar excepciones en un programa. El bloque de código dentro de la cláusula `finally` se ejecutará siempre, sin importar si se lanzó una excepción o no.

```csharp
try
{
    // Código que puede lanzar una excepción
}
catch (Exception ex)
{
    // Código que maneja la excepción
}
finally
{
    // Código que se ejecuta siempre
}
```

En este ejemplo, el bloque `try` contiene el código que puede lanzar una excepción. Si se produce una excepción, el control se transfiere al bloque `catch`, que maneja la excepción. El bloque `finally` contiene el código que se ejecutará siempre, independientemente de si se lanzó una excepción o no.

## Ejemplo

En el siguiente ejemplo, se intenta abrir un archivo y se cierra el archivo en el bloque `finally` para garantizar que los recursos se liberen correctamente:

```csharp
FileStream file = null;
try
{
    file = File.Open("archivo.txt", FileMode.Open);
    // Operaciones con el archivo
}
catch (IOException ex)
{
    Console.WriteLine("Error al abrir el archivo");
}
finally
{
    if (file != null)
    {
        file.Close();
    }
}
```

En este ejemplo, se intenta abrir el archivo "archivo.txt" y se realizan operaciones con él. Si se produce una excepción de tipo `IOException`, se maneja en el bloque `catch`. En el bloque `finally`, se verifica si el archivo se ha abierto correctamente y se cierra para liberar los recursos utilizados.

Al utilizar la cláusula `finally`, podemos garantizar que los recursos se liberen correctamente, incluso en caso de que se produzca una excepción durante la ejecución del programa.
