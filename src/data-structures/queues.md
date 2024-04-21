# Colas

Las colas o `Queue`  son similares a cuando uno quiere ir a comer un sandwich a la cafetería y se pone en una fila. Esta estructura es una estructura FIFO (*first in, first out*), el primero en entrar es el primero en salir.

El nuevo elemento se inserta debajo del elemento existente, de modo que el elemento más antiguo puede estar en la parte superior y sacarse primero.

| 0 |
| --- |
| 1 |
| 2 |
| 3 |
| 4 |
| 5 |

## Declaración

Para importar este tipo de dato, es necesario utilizar este namespace:

```csharp
using System.Collections.Generic;
```

Después, podemos crear una pila de la siguiente forma: 

```csharp
Queue<string> queue = new();
```

También se puede declarar utilizando `var`:

```csharp
var queue = new Queue<string>();
```

También podemos declarar una lista con datos:

```csharp
Queue<string> queue = new() { "Prueba" };
```

### Agregar datos

Utilizando `Enqueue()` se agrega un objeto al final de la fila.

```csharp
queue.Enqueue("Prueba");
```

### Acceder a los datos

Utilizando `Peek()` se devuelve el objeto situado al principio de la pila sin eliminarlo.

```csharp
var elemento = queue.Peek();
```

### Eliminar datos

Utilizando `Dequeue()` se elimina y devuelve el objeto al comienzo de la fila.

```csharp
var elemento = queue.Dequeue();
```

### Revisar existencia de un elemento

```csharp
var pruebaExiste = list.Contains("Prueba");
```

### Eliminar todos los elementos

```csharp
queue.Clear();
```