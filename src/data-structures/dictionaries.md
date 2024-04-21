# Diccionarios

Los diccionarios o `Dictionary` son una estructura de datos que permite asociar claves a valores. Cada clave es única y se utiliza para acceder al valor correspondiente. Es similar a una lista, pero en lugar de acceder a los elementos por un índice numérico, se accede a ellos a través de la clave.

## Declaración

Para importar este tipo de dato, es necesario utilizar este namespace:

```csharp
using System.Collections.Generic;
```

Después, podemos crear un diccionario de la siguiente forma:

```csharp
Dictionary<string, int> dic = new Dictionary<string, int>();
```

También se puede declarar utilizando `var`:

```csharp
var dic = new Dictionary<string, int>();
```

### Agregar datos

Podemos agregar una nueva clave y su valor utilizando el siguiente código:

```csharp
dic.Add("Clave", 1);
```

### Acceder a los datos

Podemos acceder a un valor a través de su clave con el siguiente código:

```csharp
var valor = dic["Clave"];
```

### Eliminar datos

Podemos eliminar una clave y su valor utilizando el siguiente código:

```csharp
dic.Remove("Clave");
```

### Revisar existencia de un elemento

Podemos verificar si una clave existe en el diccionario con el siguiente código:

```csharp
var claveExiste = dic.ContainsKey("Clave");
```

### Eliminar todos los elementos

Podemos eliminar todas las claves y valores del diccionario con el siguiente código:

```csharp
dic.Clear();
```