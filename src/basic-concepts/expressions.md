# Expresiones

Una expresión es una combinación de valores, variables, operadores y funciones que se evalúa para producir un resultado. En la mayoría de los lenguajes de programación, las expresiones se utilizan para realizar cálculos y tomar decisiones.

## Tipos de expresiones

Las expresiones se pueden clasificar en varios tipos según su función y los operadores que contienen. Algunos de los tipos más comunes son:
    
### Aritméticas
Realizan operaciones matemáticas, como suma, resta, multiplicación y división.

```java
int a = 5;
int b = 3;
int suma = a + b; // suma = 8
int resta = a - b; // resta = 2
int multiplicacion = a * b; // multiplicacion = 15
int division = a / b; // division = 1
```

### Relacionales
Comparan dos valores y devuelven un resultado booleano (verdadero o falso).

```java
int x = 10;
int y = 5;
boolean igual = x == y; // igual = false
boolean mayor = x > y; // mayor = true
boolean menor = x < y; // menor = false
```

### Lógicas
Realizan operaciones lógicas, como AND, OR y NOT, sobre valores booleanos.

```java
boolean p = true;
boolean q = false;
boolean and = p && q; // and = false
boolean or = p || q; // or = true
boolean not = !p; // not = false
```

### Asignación
Asignan un valor a una variable.

```java
int edad = 25;
String nombre = "Juan";
boolean activo = true;
```

### Condicionales
Evalúan una condición y devuelven un valor en función de si la condición es verdadera o falsa.

```java
int temperatura = 30;
String mensaje = (temperatura > 25) ? "Hace calor" : "No hace calor";
```
