# Objetos

Los objetos son una de las características más importantes de la programación orientada a objetos (OOP, por sus siglas en inglés). Un objeto es una entidad que combina datos y comportamientos, y se puede considerar como una representación realista de algún elemento en el mundo real.

Por ejemplo, podemos tener un objeto `Auto` que represente un automóvil real, con atributos como la marca, el modelo, el color y la velocidad, así como también con métodos como acelerar, frenar y apagar el motor.

Para crear un objeto, primero debemos definir una clase que represente a ese objeto. La clase define las propiedades y los métodos que tendrá el objeto, y cada vez que creamos una nueva instancia de la clase, estamos creando un nuevo objeto.

Por ejemplo, podemos tener la siguiente clase Auto en C#:

```csharp
public class Auto
{
    public string Marca { get; set; }
    public string Modelo { get; set; }
    public string Color { get; set; }
    public int Velocidad { get; set; }

    public void Acelerar(int kmh)
    {
        Velocidad += kmh;
    }

    public void Frenar(int kmh)
    {
        Velocidad -= kmh;
    }

    public void ApagarMotor()
    {
        Velocidad = 0;
    }
}
```

Luego, podemos crear una nueva instancia de la clase Auto y acceder a sus propiedades y métodos de la siguiente manera:

```csharp
Auto miAuto = new Auto();
miAuto.Marca = "Toyota";
miAuto.Modelo = "Corolla";
miAuto.Color = "Rojo";

miAuto.Acelerar(20);

Console.WriteLine("Mi auto es un " + miAuto.Marca + " " + miAuto.Modelo + " de color " + miAuto.Color + " y va a una velocidad de " + miAuto.Velocidad + " km/h.");
```

En este ejemplo, creamos una nueva instancia de la clase `Auto` llamada `miAuto`, asignamos valores a sus propiedades y llamamos al método `Acelerar`. Finalmente, imprimimos en la consola los valores de las propiedades del objeto `miAuto`.