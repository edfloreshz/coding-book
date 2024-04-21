# Pilas

Las pilas o `Stack` son similares a una pila de platos, donde se puede agregar y sacar platos sólo por el extremo superior, son de tipo LIFO, que significa último en entrar primero en salir.

El elemento nuevo se inserta sobre el elemento existente, de modo que el elemento más nuevo se mantiene en la parte superior y puede sacarse primero.

| 5 |
| --- |
| 4 |
| 3 |
| 2 |
| 1 |
| 0 |

## Declaración

Para importar este tipo de dato, es necesario utilizar este namespace:

```csharp
using System.Collections.Generic;
```

Después, podemos crear una pila de la siguiente forma: 

```csharp
Stack<string> stack = new();
```

También se puede declarar utilizando `var`:

```csharp
var stack = new Stack<string>();
```

También podemos declarar una lista con datos:

```csharp
Stack<string> stack = new() { "Prueba" };
```

### Agregar datos

Utilizando `Push(T)` se Inserta un objeto al principio de la pila.

```csharp
stack.Push("Prueba");
```

### Acceder a los datos

Utilizando `Peek()` se devuelve el objeto situado al principio de la pila sin eliminarlo.

```csharp
var elemento = stack.Peek();
```

### Eliminar datos

Utilizando `Pop()` se elimina y devuelve el objeto situado al principio de la pila.

```csharp
var elemento = stack.Pop();
```

### Revisar existencia de un elemento

```csharp
var pruebaExiste = stack.Contains("Prueba");
```

### Eliminar todos los elementos

```csharp
stack.Clear();
```