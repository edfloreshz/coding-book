# Booleanos

Los valores booleanos son aquellos que pueden ser verdaderos o falsos. En la mayoría de los lenguajes de programación, estos valores son representados por las palabras `true` y `false`.

## Operadores lógicos

Los operadores lógicos se utilizan para realizar operaciones lógicas sobre valores booleanos. Algunos de los operadores lógicos más comunes son:
- `&&` (AND): Devuelve `true` si ambos operandos son `true`.
- `||` (OR): Devuelve `true` si al menos uno de los operandos es `true`.
- `!` (NOT): Devuelve `true` si el operando es `false`.
- `^` (XOR): Devuelve `true` si uno de los operandos es `true` y el otro es `false`.

### Ejemplos

```java
boolean a = true;
boolean b = false;

boolean and = a && b; // and = false
boolean or = a || b; // or = true
boolean not = !a; // not = false
boolean xor = a ^ b; // xor = true
```

## Operadores de comparación

Los operadores de comparación se utilizan para comparar dos valores y devolver un resultado booleano. Algunos de los operadores de comparación más comunes son:
- `<`: Devuelve `true` si el primer valor es menor que el segundo valor.
- `<=`: Devuelve `true` si el primer valor es menor o igual que el segundo valor.
- `>`: Devuelve `true` si el primer valor es mayor que el segundo valor.
- `>=`: Devuelve `true` si el primer valor es mayor o igual que el segundo valor.
- `==`: Devuelve `true` si el primer valor es igual al segundo valor.
- `!=`: Devuelve `true` si el primer valor no es igual al segundo valor.
- `===`: Devuelve `true` si el primer valor es igual al segundo valor y son del mismo tipo.
- `!==`: Devuelve `true` si el primer valor no es igual al segundo valor o no son del mismo tipo.
- `<>`: Devuelve `true` si los valores son diferentes.
- `<=>`: Devuelve `-1` si el primer valor es menor que el segundo, `0` si son iguales y `1` si el primer valor es mayor que el segundo.


### Ejemplos

```java
int x = 10;
int y = 5;

boolean lessThan = x < y; // lessThan = false
boolean greaterThan = x > y; // greaterThan = true
boolean equalTo = x == y; // equalTo = false
boolean notEqualTo = x != y; // notEqualTo = true
```
