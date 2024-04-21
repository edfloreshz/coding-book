# Recursion

La recursión es un concepto importante en la programación que se refiere a la capacidad de una función de llamarse a sí misma. 

La recursión es útil cuando un problema puede ser dividido en subproblemas más pequeños que son similares o idénticos al problema original. En lugar de escribir un código iterativo para resolver el problema, se escribe una función recursiva que se llama a sí misma para resolver cada subproblema.

```csharp
static void Main(string[] args)
{
    int resultado = Factorial(5);
    Console.WriteLine(resultado); // Imprime 120
}

static int Factorial(int n)
{
    if (n == 0)
    {
        return 1;
    }
    else
    {
        return n * Factorial(n - 1);
    }
}
```

Es importante tener en cuenta que, para evitar que la recursión se convierta en un bucle infinito, debe haber un caso base que detenga la recursión. En este ejemplo, el caso base es cuando el número es `0`.

La recursión es una herramienta poderosa en la programación, pero también puede ser costosa en términos de memoria y rendimiento. Por lo tanto, es importante entender cuándo y cómo utilizar la recursión de manera efectiva en su código.