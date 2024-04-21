# JSON

JSON es una forma de representar información en internet. 

Se parece mucho a un diccionario o una lista de valores en un programa de computadora. La diferencia es que JSON es un formato que se utiliza en la web para transferir datos entre un servidor y una aplicación cliente, y también para almacenar datos en un archivo que puede leerse por humanos.

Por ejemplo, supongamos que quieres guardar información sobre una persona en un archivo. En JSON, podrías escribir algo como esto:

```json
{
  "nombre": "Juan",
  "edad": 30,
  "ciudad": "Madrid"
}
```

Como puedes ver, el formato de JSON es similar a un diccionario. Hay un par de claves y valores, entre comillas y separados por dos puntos.

En C#, puedes trabajar con JSON utilizando la biblioteca `System.Text.Json` o `Newtonsoft.Json`. Estas bibliotecas te permiten parsear (leer) una cadena de texto JSON y convertirla en un objeto de C#, o tomar un objeto de C# y convertirlo en una cadena de texto JSON.

Esto significa que puedes enviar y recibir información en formato JSON desde y hacia un servidor web, y trabajar con ella fácilmente en tu aplicación de C#.

## Uso

Aquí hay algunos ejemplos de código en C# que muestran cómo interactuar con JSON.

Tenemos el mismo objeto JSON representado en C# como una clase:

```csharp
class Persona
{
    public string Nombre { get; set; }
    public int Edad { get; set; }
    public string Ciudad { get; set; }
}
```

## Convirtiendo un objeto C# a JSON

```csharp
using System;
using System.Text.Json;

// Crea un objeto de ejemplo
var persona = new Persona
{
    Nombre = "Juan",
    Edad = 30,
    Ciudad = "Madrid"
};

// Convierte el objeto a JSON
string json = JsonSerializer.Serialize(persona);
Console.WriteLine(json);
```

## Convirtiendo JSON a un objeto C#

```csharp
// JSON de ejemplo
string json = @"{
  ""nombre"": ""Juan"",
  ""edad"": 30,
  ""ciudad"": ""Madrid""
}";

// Convierte el JSON a un objeto C#
Persona persona = JsonSerializer.Deserialize<Persona>(json);
Console.WriteLine(persona.Nombre);
Console.WriteLine(persona.Edad);
Console.WriteLine(persona.Ciudad);
```

Estos son solo algunos ejemplos básicos, pero puedes encontrar muchas más funcionalidades en la documentación de `System.Text.Json` o `Newtonsoft.Json`.