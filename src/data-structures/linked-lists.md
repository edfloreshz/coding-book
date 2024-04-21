# Listas enlazadas

Las listas enlazadas o `LinkedList` son una estructura de datos que permite almacenar una secuencia de elementos, donde cada elemento contiene una referencia al siguiente elemento en la lista. Esto permite una mayor flexibilidad en la inserción y eliminación de elementos en comparación con las listas estáticas.

## Declaración

Para importar este tipo de dato, es necesario utilizar este namespace:

```csharp
using System.Collections.Generic;
```

Después, podemos crear una lista enlazada de la siguiente forma:

```csharp
LinkedList<string> listaEnlazada = new LinkedList<string>();
```

También se puede declarar utilizando `var`:

```csharp
var listaEnlazada = new LinkedList<string>();
```

## Agregar datos

Podemos agregar un nuevo elemento al final de la lista enlazada con el siguiente código:

```csharp
listaEnlazada.AddLast("Elemento");
```

También se puede agregar un elemento al inicio de la lista enlazada con el siguiente código:

```csharp
listaEnlazada.AddFirst("Elemento");
```

## Acceder a los datos

Podemos acceder al primer elemento de la lista enlazada con el siguiente código:

```csharp
var primerElemento = listaEnlazada.First.Value;
```

Podemos acceder al último elemento de la lista enlazada con el siguiente código:

```csharp
var ultimoElemento = listaEnlazada.Last.Value;
```

## Eliminar datos

Podemos eliminar un elemento de la lista enlazada con el siguiente código:

```csharp
listaEnlazada.Remove("Elemento");
```

## Revisar existencia de un elemento

Podemos verificar si un elemento existe en la lista enlazada con el siguiente código:

```csharp
var elementoExiste = listaEnlazada.Contains("Elemento");
```

## Eliminar todos los elementos

Podemos eliminar todos los elementos de la lista enlazada con el siguiente código:

```csharp
listaEnlazada.Clear();
```