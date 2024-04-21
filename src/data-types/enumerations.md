# Enumeraciones

Las enumeraciones son un tipo de dato que permite definir un conjunto de constantes con un nombre asociado. Por ejemplo, si se desea definir un conjunto de días de la semana, se puede hacer de la siguiente manera:

```csharp
enum Dias {
	Lunes,
	Martes,
	Miercoles,
	Jueves,
	Viernes,
	Sabado,
	Domingo
}
```

Por defecto, las enumeraciones se numeran automáticamente de cero en adelante cuando se declaran, el lenguaje termina con un código como este:

```csharp
enum Dias {
	Lunes = 0,
	Martes = 1,
	Miercoles = 2,
	Jueves = 3,
	Viernes = 4,
	Sabado = 5,
	Domingo = 6
}
```

Sin embargo, es posible modificar el valor que se le asigna a cada constante de la enumeración.

```csharp
enum Dias {
	Lunes = 7,
	Martes = 6,
	Miercoles = 5,
	Jueves = 4,
	Viernes = 3,
	Sabado = 2,
	Domingo = 1
}
```

Las enumeraciones son útiles para definir un conjunto de valores que no cambian y que se pueden utilizar en diferentes partes del código.