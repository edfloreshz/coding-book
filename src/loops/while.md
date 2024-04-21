# While

El ciclo `while` es una estructura de control de flujo que permite ejecutar un bloque de código repetidamente mientras se cumpla una condición específica. La condición se evalúa antes de cada iteración del ciclo y, si es verdadera, el cuerpo del ciclo se ejecuta; de lo contrario, el ciclo se detiene.

Aquí hay un ejemplo de código:

```csharp
int counter = 0;
while (counter < 10)
{
    Console.WriteLine(counter);
    counter++;
}
```

> En este ejemplo, la variable `counter` se inicializa con un valor de `0`. La condición `counter < 10` se evalúa antes de cada iteración del ciclo y, si es verdadera, el cuerpo del ciclo se ejecuta. La actualización `counter++` se ejecuta después de cada iteración del ciclo y aumenta el valor de `counter` en uno. Por lo tanto, el ciclo se ejecutará diez veces y mostrará en pantalla los números del 0 al 9.
> 

Es importante tener en cuenta que los ciclos `while` también pueden ser infinitos si la condición siempre es verdadera o no se actualiza dentro del cuerpo del ciclo. Por lo tanto, es importante tener cuidado al usar ciclos `while` y asegurarse de que se cumplan las condiciones adecuadas para detener su ejecución.