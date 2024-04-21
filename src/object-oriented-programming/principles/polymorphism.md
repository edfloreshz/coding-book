# Polimorfismo

El polimorfismo se refiere a la capacidad de un objeto de comportarse de diferentes maneras en función del contexto en el que se encuentra. Esto permite que un objeto de una clase derivada se comporte como un objeto de la clase base, lo que facilita la creación de código genérico y flexible.

## Tipos de polimorfismo

En programación orientada a objetos, existen dos tipos principales de polimorfismo: polimorfismo de subtipos y polimorfismo paramétrico.

### Polimorfismo de subtipos

El polimorfismo de subtipos se refiere a la capacidad de un objeto de una clase derivada de comportarse como un objeto de la clase base. Esto significa que un objeto de la clase derivada puede ser tratado como un objeto de la clase base en el código, lo que facilita la creación de código genérico y flexible.

Por ejemplo, considera las clases `Animal` y `Dog`:

```csharp
class Animal
{
    public virtual void Eat()
    {
        Console.WriteLine("The animal is eating");
    }
}

class Dog : Animal
{
    public override void Eat()
    {
        Console.WriteLine("The dog is eating");
    }
}
```

En este ejemplo, la clase `Dog` hereda de la clase `Animal` y sobrescribe el método `Eat`. Esto significa que un objeto de la clase `Dog` puede ser tratado como un objeto de la clase `Animal` en el código, lo que facilita la creación de código genérico y flexible.


### Polimorfismo paramétrico

El polimorfismo paramétrico se refiere a la capacidad de un objeto de comportarse de diferentes maneras en función de los parámetros de entrada que recibe. Esto permite que un método o función pueda aceptar diferentes tipos de datos como entrada y producir diferentes resultados en función de esos datos.

Por ejemplo, considera una función `Add` que puede sumar dos números enteros o concatenar dos cadenas de texto:

```csharp

public int Add(int a, int b)
{
    return a + b;
}

public string Add(string a, string b)
{
    return a + b;
}
```

En este ejemplo, la función `Add` puede aceptar diferentes tipos de datos como entrada y producir diferentes resultados en función de esos datos. Esto es un ejemplo de polimorfismo paramétrico, ya que el comportamiento de la función varía en función de los parámetros de entrada que recibe.
