# Listas

Las listas son estructuras de datos basadas en arreglos, existen algunas diferencias entre ambos, especialmente en la manera de acceder y modificar la información. Para declarar una lista, se le debe especificar el tipo de dato que va a almacenar, igual que a un arreglo, pero su tamaño no necesita ser especificado. 

> Algo a tener en cuenta con las listas es que estas consumen mas memoria que los arreglos, esto es dado a que cuando un arreglo se declara, se debe especificar explícitamente su tamaño, por tanto se puede almacenar en el ***stack***, una lista crece conforme se necesite, por tanto necesita estar almacenada en el ***heap***.
> 

Las listas son útiles cuando se requiere una manera de almacenar datos menos restrictiva que un arreglo, existen varios métodos que nos ayudan a manipular los datos dentro de la lista.

## Declaración

Para importar este tipo de dato, es necesario utilizar este namespace:

```csharp
using System.Collections.Generic;
```

Después, podemos crear una lista de la siguiente forma: 

```csharp
List<string> list = new();
```

También se puede declarar utilizando `var`:

```csharp
var list = new List<string>();
```

También podemos declarar una lista con datos:

```csharp
List<string> list = new() { "Prueba" };
```

### Agregar datos

```csharp
list.Add("Prueba");
```

### Acceder a los datos

```csharp
var elemento = list[0];
```

### Eliminar datos

```csharp
list.Remove(0);
```

### Revisar existencia de un elemento

```csharp
var pruebaExiste = list.Contains("Prueba");
```