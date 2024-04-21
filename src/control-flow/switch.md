# Switch

La declaración `switch` es una estructura de control de flujo que permite ejecutar diferentes bloques de código basados en una variable o expresión específica. Es útil cuando se tienen múltiples opciones y se desea elegir una de ellas para ejecutar en función de su valor.

```csharp
Console.WriteLine("Introduce una opción (1, 2 o 3):");
int option = int.Parse(Console.ReadLine());

switch (option)
{
    case 1:
        Console.WriteLine("Has elegido la opción 1");
        break;
    case 2:
        Console.WriteLine("Has elegido la opción 2");
        break;
    case 3:
        Console.WriteLine("Has elegido la opción 3");
        break;
    default:
        Console.WriteLine("Opción inválida");
        break;
}
```

> En este ejemplo, se solicita al usuario que introduzca una opción y se almacena en la variable `option`. Luego, se utiliza la declaración `switch` para elegir qué bloque de código ejecutar en función del valor de `option`. Si `option` es `1`, se imprime en la consola "Has elegido la opción 1". Si `option` es `2`, se imprime en la consola "Has elegido la opción 2". Y así sucesivamente. Si `option` no coincide con ninguno de los casos, se ejecuta el bloque de código dentro de la declaración `default` y se imprime en la consola "Opción inválida".
> 

La declaración `switch` puede ser más eficiente que la anidación de declaraciones `if` en algunos casos, y también puede hacer que el código sea más legible y fácil de mantener. Sin embargo, es importante tener en cuenta que la declaración `switch` solo funciona con valores de tipo `int`, `short`, `long`, `byte`, `sbyte`, `char`, `string` y `enum`.