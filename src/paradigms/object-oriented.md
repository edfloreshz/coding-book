# Paradigma orientado a objetos

![banner](https://images.unsplash.com/photo-1481349518771-20055b2a7b24?ixlib=rb-4.0.3&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=3600)

El paradigma orientado a objetos es un estilo de programación que se basa en el concepto de "objetos", que pueden contener datos en forma de campos (también conocidos como atributos) y código en forma de procedimientos (también conocidos como métodos). En este paradigma, los objetos son instancias de clases, que definen la estructura y el comportamiento de los objetos.

## Clases y objetos

Una clase es una plantilla que define la estructura y el comportamiento de los objetos. Contiene campos para almacenar datos y métodos para realizar operaciones. Por otro lado, un objeto es una instancia de una clase, que contiene datos específicos y puede realizar operaciones definidas por la clase.

```csharp
class Persona
{
    // Campos
    public string Nombre;
    public int Edad;

    // Métodos
    public void Presentarse()
    {
        Console.WriteLine($"Hola, mi nombre es {Nombre} y tengo {Edad} años");
    }
}

// Crear un objeto de la clase Persona

Persona persona = new Persona();
persona.Nombre = "Juan";
persona.Edad = 30;
persona.Presentarse();
```

En este ejemplo, se define una clase `Persona` con campos para el nombre y la edad, y un método `Presentarse` que imprime un mensaje con el nombre y la edad de la persona. Luego, se crea un objeto de la clase `Persona` llamado `persona` y se asignan valores a sus campos. Finalmente, se llama al método `Presentarse` para mostrar el mensaje.


## Encapsulamiento

El encapsulamiento es un principio de la programación orientada a objetos que consiste en ocultar los detalles de implementación de un objeto y exponer una interfaz pública para interactuar con él. Esto se logra definiendo campos como privados y proporcionando métodos públicos para acceder y modificar esos campos.

```csharp
class CuentaBancaria
{
    private double saldo;

    public void Depositar(double monto)
    {
        saldo += monto;
    }

    public void Retirar(double monto)
    {
        saldo -= monto;
    }

    public double ObtenerSaldo()
    {
        return saldo;
    }
}

CuentaBancaria cuenta = new CuentaBancaria();
cuenta.Depositar(1000);
cuenta.Retirar(500);
Console.WriteLine($"Saldo actual: {cuenta.ObtenerSaldo()}");
```

En este ejemplo, se define una clase `CuentaBancaria` con un campo privado `saldo` y métodos públicos para depositar, retirar y obtener el saldo de la cuenta. El campo `saldo` se mantiene privado para ocultar su implementación interna, y los métodos públicos proporcionan una interfaz para interactuar con la cuenta.


## Herencia

La herencia es un mecanismo que permite que una clase herede campos y métodos de otra clase. La clase que hereda se conoce como "clase derivada" o "subclase", y la clase de la que hereda se conoce como "clase base" o "superclase". La herencia permite reutilizar código y definir relaciones entre clases.

```csharp
class Empleado
{
    public string Nombre;
    public double Salario;

    public void Trabajar()
    {
        Console.WriteLine($"{Nombre} está trabajando");
    }
}

class Gerente : Empleado
{
    public void Gestionar()
    {
        Console.WriteLine($"{Nombre} está gestionando");
    }
}

Gerente gerente = new Gerente();
gerente.Nombre = "Ana";
gerente.Salario = 50000;
gerente.Trabajar();
gerente.Gestionar();
```

En este ejemplo, se define una clase `Empleado` con campos para el nombre y el salario, y un método `Trabajar`. Luego, se define una clase `Gerente` que hereda de `Empleado` y agrega un método `Gestionar`. Se crea un objeto de la clase `Gerente` llamado `gerente` y se accede a los campos y métodos de la clase base.


## Polimorfismo

El polimorfismo es un concepto que permite que un objeto se comporte de diferentes maneras según el contexto en el que se utilice. En la programación orientada a objetos, el polimorfismo se puede lograr mediante la definición de métodos con el mismo nombre pero diferentes implementaciones en clases diferentes.

```csharp
class Figura
{
    public virtual void Dibujar()
    {
        Console.WriteLine("Dibujando figura");
    }
}

class Circulo : Figura
{
    public override void Dibujar()
    {
        Console.WriteLine("Dibujando círculo");
    }
}

class Cuadrado : Figura
{
    public override void Dibujar()
    {
        Console.WriteLine("Dibujando cuadrado");
    }
}

Figura figura = new Circulo();
figura.Dibujar();

figura = new Cuadrado();
figura.Dibujar();
```

En este ejemplo, se define una clase base `Figura` con un método `Dibujar` que se sobrescribe en las clases derivadas `Circulo` y `Cuadrado`. Se crea un objeto de tipo `Figura` que se asigna a instancias de `Circulo` y `Cuadrado`, y se llama al método `Dibujar` para cada objeto, lo que produce resultados diferentes según la implementación.


## Ventajas del paradigma orientado a objetos

Algunas de las ventajas del paradigma orientado a objetos son:

- **Reutilización de código**: La herencia y el polimorfismo permiten reutilizar y extender el código de manera eficiente.
- **Abstracción**: Las clases y objetos permiten modelar entidades del mundo real de manera más precisa y abstracta.
- **Encapsulamiento**: El encapsulamiento ayuda a ocultar la implementación interna de un objeto y proteger sus datos.
- **Mantenibilidad**: La estructura modular y jerárquica de las clases facilita la modificación y mantenimiento del código.
- **Seguridad**: El encapsulamiento y la herencia controlada ayudan a garantizar la integridad y seguridad de los datos.
- **Escalabilidad**: La estructura orientada a objetos facilita la escalabilidad y extensibilidad del código.

El paradigma orientado a objetos es ampliamente utilizado en la programación moderna debido a sus ventajas en términos de reutilización, abstracción, encapsulamiento y mantenibilidad. Al comprender los conceptos fundamentales del paradigma orientado a objetos, puedes mejorar tu habilidad para diseñar y desarrollar programas eficientes y fáciles de mantener.
