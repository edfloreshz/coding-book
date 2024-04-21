# Expresiones aritmeticas

Una expresión aritmética es una combinación de valores, variables y operadores que se evalúa para producir un resultado numérico. Los operadores aritméticos se utilizan para realizar operaciones matemáticas básicas, como suma, resta, multiplicación y división.

### Operador de incremento `++`

El operador de incremento unario `++` incrementa su operando en 1.

El operador de incremento se admite en dos formas: el operador de incremento posfijo (`x++`) y el operador de incremento prefijo (`++x`).

### Operador de incremento de postfijo

El resultado de `x++` es el valor de `x` *antes* de la operación, tal y como se muestra en el ejemplo siguiente:

```csharp
int i = 3;
Console.WriteLine(i);   // output: 3
Console.WriteLine(i++); // output: 3
Console.WriteLine(i);   // output: 4
```

### Operador de incremento prefijo

El resultado de `++x` es el valor de `x` *después* de la operación, tal y como se muestra en el ejemplo siguiente:

```csharp
double a = 1.5;
Console.WriteLine(a);   // output: 1.5
Console.WriteLine(++a); // output: 2.5
Console.WriteLine(a);   // output: 2.5
```

# Operador de decremento `--`

El operador de decremento unario `--` disminuye su operando en 1. El operando debe ser una variable, un acceso de [propiedad](https://learn.microsoft.com/es-es/dotnet/csharp/programming-guide/classes-and-structs/properties) o un acceso de [indexador](https://learn.microsoft.com/es-es/dotnet/csharp/programming-guide/indexers/).

El operador de decremento se admite en dos formas: el operador de decremento posfijo (`x--`) y el operador de decremento prefijo (`--x`).

### Operador de decremento de postfijo

El resultado de `x--` es el valor de `x` *antes* de la operación, como se muestra en el ejemplo siguiente:

```csharp
int i = 3;
Console.WriteLine(i);   // output: 3
Console.WriteLine(i--); // output: 3
Console.WriteLine(i);   // output: 2
```

### Operador de decremento de prefijo

El resultado de `--x` es el valor de `x` *después* de la operación, tal y como se muestra en el ejemplo siguiente:

```csharp
double a = 1.5;
Console.WriteLine(a);   // output: 1.5
Console.WriteLine(--a); // output: 0.5
Console.WriteLine(a);   // output: 0.5
```

## Operadores unarios más y menos

El operador `+` unario devuelve el valor de su operando. El operador unario `-` calcula la negación numérica del operando.

```csharp
Console.WriteLine(+4);     // output: 4

Console.WriteLine(-4);     // output: -4
Console.WriteLine(-(-4));  // output: 4

int a = 5;
var b = -a;
Console.WriteLine(b);            // output: -5
Console.WriteLine(b.GetType());  // output: System.Int64

Console.WriteLine(-double.NaN);  // output: NaN
```

# Operador de suma `+`

El operador de suma `+` calcula la suma de sus operandos:

```csharp
Console.WriteLine(5 + 4);       // output: 9
Console.WriteLine(5 + 4.3);     // output: 9.3
Console.WriteLine(5.1m + 4.2m); // output: 9.3
```

También puede usar el operador `+` para la concatenación de cadenas.

# Operador de resta `-`

El operador de resta `-` resta el operando derecho del izquierdo:

```csharp
Console.WriteLine(47 - 3);      // output: 44
Console.WriteLine(5 - 4.3);     // output: 0.7
Console.WriteLine(7.5m - 2.3m); // output: 5.2
```

# Operador de multiplicación `*`

El operador de multiplicación `*` calcula el producto de sus operandos:

```csharp
Console.WriteLine(5 * 2);         // output: 10
Console.WriteLine(0.5 * 2.5);     // output: 1.25
Console.WriteLine(0.1m * 23.4m);  // output: 2.34
```

# Operador de división `/`

El operador de división `/` divide el operando izquierdo entre el derecho.

## División de enteros

Para los operandos de tipos enteros, el resultado del operador `/` es de un tipo entero y equivale al cociente de los dos operandos redondeados hacia cero:

```csharp
Console.WriteLine(13 / 5);    // output: 2
Console.WriteLine(-13 / 5);   // output: -2
Console.WriteLine(13 / -5);   // output: -2
Console.WriteLine(-13 / -5);  // output: 2
```

## División de punto flotante

Para los tipos `float`, `double` y `decimal`, el resultado del operador `/` es el cociente de los dos operandos:

```csharp
Console.WriteLine(16.8f / 4.1f);   // output: 4.097561
Console.WriteLine(16.8d / 4.1d);   // output: 4.09756097560976
Console.WriteLine(16.8m / 4.1m);   // output: 4.0975609756097560975609756098
```

Si uno de los operandos es `decimal`, otro operando no puede ser `float` ni `double`, ya que ni `float` ni `double` se convierte de forma implícita a `decimal`. Debe convertir explícitamente el operando `float` o `double` al tipo `decimal`.

# Operador de resto `%`

El operador de resto `%` calcula el resto después de dividir el operando izquierdo entre el derecho.

## Resto entero

En el caso de los operandos de tipos enteros, el resultado de `a % b` es el valor producido por `a - (a / b) * b`. El signo de resto distinto de cero es el mismo que el del operando izquierdo, como se muestra en el ejemplo siguiente:

```csharp
Console.WriteLine(5 % 4);   // output: 1
Console.WriteLine(5 % -4);  // output: 1
Console.WriteLine(-5 % 4);  // output: -1
Console.WriteLine(-5 % -4); // output: -1
```

## Resto de punto flotante

En el caso de los operandos `float` y `double`, el resultado de `x % y` para `x` e `y` finitos es el valor `z`, de modo que

- el signo de `z`, si no es cero, es el mismo que el signo de `x`;
- el valor absoluto de `z` es el valor producido por `|x| - n * |y|`, donde `n` es el entero más grande posible que sea menor o igual que `|x| / |y|`, y `|x|` e `|y|` son los valores absolutos de `x` e `y`, respectivamente.

En el ejemplo siguiente se muestra el comportamiento del operador de resto con operandos de punto flotante:

```csharp
Console.WriteLine(-5.2f % 2.0f); // output: -1.2
Console.WriteLine(5.9 % 3.1);    // output: 2.8
Console.WriteLine(5.9m % 3.1m);  // output: 2.8
```