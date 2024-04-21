# Break y Continue

Las sentencias `break` y `continue` son utilizadas en conjunto con los ciclos para controlar el flujo de ejecución.

## `break`

La sentencia `break` interrumpe la ejecución del ciclo actual y hace que el control se transfiera fuera del ciclo. Por lo tanto, detiene la ejecución del ciclo y continúa con la siguiente sentencia después del ciclo.

Aquí hay un ejemplo de código:

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
    {
        break;
    }
    Console.WriteLine(i);
}
```

> En este ejemplo, el ciclo `for` se ejecuta diez veces, pero cuando la variable `i` alcanza el valor de `5`, la sentencia `break` interrumpe la ejecución del ciclo. Por lo tanto, el ciclo se detiene y el control se transfiere fuera del ciclo, mostrando en pantalla los números del 0 al 4.
> 

## `continue`

La sentencia `continue` interrumpe la ejecución de la iteración actual del ciclo y continúa con la siguiente iteración. Por lo tanto, detiene la ejecución de la iteración actual, pero no detiene la ejecución del ciclo en sí.

Aquí hay un ejemplo de código:

```csharp
for (int i = 0; i < 10; i++)
{
    if (i % 2 == 0)
    {
        continue;
    }
    Console.WriteLine(i);
}
```

> En este ejemplo, el ciclo `for` se ejecuta diez veces, pero cuando la variable `i` es un número par, la sentencia `continue` interrumpe la ejecución de la iteración actual y continúa con la siguiente iteración. Por lo tanto, los números pares no se muestran en pantalla, solo los números impares.
>