# Declaración de tipos

Es posible declarar tipos de datos personalizados, comunmente conocidos como _alias_, en la mayoría de los lenguajes de programación. Estos tipos de datos personalizados pueden ser útiles para simplificar la escritura de código y hacerlo más legible.

En C# es posible declarar un tipo de dato personalizado utilizando la palabra clave `using`. Por ejemplo, si se desea crear un tipo de dato personalizado para una lista de clientes, se puede hacer de la siguiente manera:

```csharp
using ListaDeClientes = System.Collections.Generic.List<Cliente>;

ListaDeClientes lista = new();
```

Sin embargo, se recomienda no crear tipos personalizados para tipos de datos primitivos:

```csharp
using IntegerType = int;
using StringType = string;
using BooleanType = bool;
```

Es preferible utilizar los tipos de datos primitivos directamente en el código dado que pueden causar confusión y dificultar la lectura del código.