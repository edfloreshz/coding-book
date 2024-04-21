# Do-While

El ciclo `do-while` es similar al ciclo `while`, pero con una diferencia importante: el cuerpo del ciclo se ejecuta al menos una vez, independientemente de si la condición se cumplió o no. La condición se evalúa después de cada iteración del ciclo y, si es verdadera, el cuerpo del ciclo se ejecuta de nuevo; de lo contrario, el ciclo se detiene.

Aquí hay un ejemplo de código:

```csharp
int counter = 0;
do
{
    Console.WriteLine(counter);
    counter++;
}
while (counter < 10);
```

> En este ejemplo, la variable `counter` se inicializa con un valor de `0`. El cuerpo del ciclo se ejecuta al menos una vez antes de evaluar la condición `counter < 10`. La actualización `counter++` se ejecuta después de cada iteración del ciclo y aumenta el valor de `counter` en uno. La condición `counter < 10` se evalúa después de cada iteración del ciclo y, si es verdadera, el cuerpo del ciclo se ejecuta de nuevo. Por lo tanto, el ciclo se ejecutará diez veces y mostrará en pantalla los números del 0 al 9.
> 

Es importante tener en cuenta que los ciclos `do-while` también pueden ser infinitos si la condición siempre es verdadera o no se actualiza dentro del cuerpo del ciclo. Por lo tanto, es importante tener cuidado al usar ciclos `do-while` y asegurarse de que se cumplan las condiciones adecuadas para detener su ejecución.