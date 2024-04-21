# Clases

Las clases son plantillas que definen la estructura de un objeto. En ellas se definen los atributos y métodos que tendrán los objetos que se creen a partir de ellas, comunmente se utilizan para modelar objetos reales en el código.

## Definición

Para definir una clase en C#, se utiliza la palabra clave `class`, seguida del nombre de la clase y el cuerpo de la clase entre llaves `{}`. Dentro del cuerpo de la clase, se pueden definir atributos y métodos que describen el comportamiento y las propiedades de los objetos de esa clase.

Aquí hay un ejemplo de cómo se ve la definición de una clase `Car` en C#:

```csharp
public class Product
{
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

## Instancias de clases

Una vez que se define una clase, se pueden crear objetos o "instancias" de ella. Cada instancia tendrá sus propios valores para los atributos y podrá ejecutar los métodos de la clase. Para crear una instancia de una clase en C#, se utiliza la palabra clave `new`, seguida del nombre de la clase y paréntesis `()`.


```csharp
Product apple = new Product();
product1.Name = "Apple";
product1.Price = 10.0;
```


## Propiedades

Las propiedades en programación son una forma de acceder y modificar valores de una clase de manera controlada. Se comportan como atributos, pero proporcionan un mayor nivel de control y seguridad, ya que se pueden establecer reglas y validaciones para el acceso y la asignación de valores.

El acceso a los valores de una propiedad se hace mediante la sintaxis de una variable, pero el código real detrás de una propiedad puede realizar cualquier tarea que se requiera, como validar un valor o calcular un valor basado en otras propiedades de la clase.

Este es un ejemplo de código en C# para una clase con una propiedad llamada `Name`:

```csharp
class Product
{
    public decimal Price { get; set; }
    private string name;

    public string Name
    {
        get
        {
            return name;
        }
        set
        {
            if (!string.IsNullOrEmpty(value))
            {
                name = value;
            }
        }
    }
}
```

## Metodos

Los métodos en programación son bloques de código que realizan una tarea específica. En el contexto de las clases, los métodos son funciones que se definen dentro de una clase y pueden acceder a los atributos y propiedades de la clase.

Los métodos pueden tener parámetros de entrada y pueden devolver un valor como resultado de su ejecución. También pueden ser públicos o privados, lo que determina si pueden ser accedidos desde fuera de la clase.

Este es un ejemplo de código en C# para una clase con un método llamado `PrintPrice`:

```csharp
class Product
{
    public string Name { get; set; }
    public decimal Price { get; set; }

    void PrintPrice()
    {
        Console.WriteLine("The price of " + Name + " is " + Price);
    }
}
```

## Constructores

Los constructores son métodos especiales que se utilizan para inicializar una nueva instancia de una clase. Al crear una instancia de una clase, se invoca automáticamente su constructor. Por ejemplo, podemos crear un constructor en la clase `Car` que asigne valores iniciales a los atributos cuando se crea una nueva instancia.

```csharp
class Product
{
    public string Name { get; set; }
    public decimal Price { get; set; }

    public Product(string name, decimal price)
    {
        Name = name;
        Price = price;
    }
}
```

## Destructores

Los destructores son métodos especiales que se invocan automáticamente cuando un objeto se elimina. Los destructores se utilizan para liberar recursos asociados con un objeto antes de que se destruya.

```csharp
class Product
{
    public string Name { get; set; }
    public decimal Price { get; set; }

    ~Product()
    {
        // Código para liberar recursos aquí
    }
}
```

## Sobrecarga de constructores

La sobrecarga de constructores es una técnica que permite tener varios constructores con diferentes argumentos en una misma clase. Esto se hace para que sea más fácil crear objetos con diferentes conjuntos de valores iniciales.

```csharp
class Product
{
    public string Name { get; set; }
    public decimal Price { get; set; }

    // Constructor sin argumentos
    public Product()
    {
        Name = "Product";
        Price = 0;
    }

    // Constructor con argumentos
    public Product(string name, decimal price)
    {
        Name = name;
        Price = price;
    }
}
```
