# Abstracción

La abstracción es el proceso de identificar las características esenciales de un objeto y eliminar los detalles innecesarios. En programación orientada a objetos, la abstracción se logra a través de la creación de clases y la definición de sus propiedades y métodos.

Por ejemplo, considera la clase `Car`:

```csharp
class Car
{
    public string Brand { get; set; }
    public string Model { get; set; }
    public int Year { get; set; }

    public void Start()
    {
        Console.WriteLine("The car is starting");
    }

    public void Stop()
    {
        Console.WriteLine("The car is stopping");
    }
}
```

En este ejemplo, `Car` es una clase que define las propiedades `Brand`, `Model` y `Year`, así como los métodos `Start` y `Stop`. Para crear un objeto de la clase `Car`, podemos hacer lo siguiente:

```csharp
Car myCar = new Car();
myCar.Brand = "Toyota";
myCar.Model = "Corolla";
myCar.Year = 2020;

myCar.Start();
```

En este caso, `myCar` es un objeto de la clase `Car` con los valores específicos para sus propiedades `Brand`, `Model` y `Year`. Al llamar al método `Start`, se imprime el mensaje "The car is starting".
