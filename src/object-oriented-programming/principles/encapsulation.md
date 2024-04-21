# Encapsulamiento

Se refiere al proceso de ocultar los detalles internos de un objeto y exponer solo la interfaz pública. Esto significa que los atributos de un objeto (variables de instancia) deben ser privados, y el acceso a ellos debe realizarse a través de métodos públicos (métodos de acceso).

El encapsulamiento tiene varios beneficios en el desarrollo de software:

- **Seguridad**: Al hacer que los atributos de un objeto sean privados, se evita que se modifiquen de manera incorrecta o inesperada. Esto ayuda a prevenir errores y garantiza la integridad de los datos.
- **Abstracción**: Al ocultar los detalles internos de un objeto, se facilita su uso y comprensión. Los usuarios de la clase solo necesitan conocer la interfaz pública para interactuar con el objeto, sin preocuparse por su implementación interna.
- **Flexibilidad**: Al exponer solo la interfaz pública de un objeto, se facilita la modificación de su implementación interna sin afectar a los usuarios de la clase. Esto permite realizar cambios en la implementación sin necesidad de modificar el código que utiliza la clase.
- **Segregación de responsabilidades**: Al definir una interfaz pública clara para un objeto, se establecen claramente las responsabilidades de la clase y se evita la dependencia de detalles internos. Esto facilita la creación de clases cohesivas y con una única responsabilidad.


## Ejemplo

En el siguiente ejemplo, se muestra cómo se puede aplicar el encapsulamiento en C# mediante la definición de atributos privados y métodos públicos para acceder y modificar esos atributos:

```csharp
class Person
{
    private string name;
    private int age;

    public string Name
    {
        get { return name; }
        set { name = value; }
    }

    public int Age
    {
        get { return age; }
        set { age = value; }
    }
}
```

En este ejemplo, la clase `Person` tiene dos atributos privados (`name` y `age`) y dos propiedades públicas (`Name` y `Age`) que permiten acceder y modificar esos atributos. Al hacer que los atributos sean privados y proporcionar métodos públicos para acceder a ellos, se garantiza que el acceso a los datos de la clase se realice de manera controlada y segura.

```csharp
Person person = new Person();
person.Name = "Alice";
person.Age = 30;

Console.WriteLine($"Name: {person.Name}, Age: {person.Age}");
```

Al utilizar la clase `Person`, los usuarios solo necesitan interactuar con las propiedades públicas `Name` y `Age`, sin necesidad de conocer los detalles internos de la clase. Esto facilita el uso de la clase y garantiza la integridad de los datos almacenados en ella.