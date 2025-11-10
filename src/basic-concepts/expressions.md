# Expresiones

Una expresión es una combinación de valores, variables, operadores y llamadas a funciones que se evalúan para producir un resultado. Las expresiones son fundamentales en la programación, ya que permiten realizar cálculos y manipular datos.

## Tipos de expresiones

### Expresiones aritméticas

Las expresiones aritméticas utilizan operadores matemáticos para realizar cálculos con números.

```pseudocode
variable a : entero ← 5
variable b : entero ← 3
variable suma : entero ← a + b              // suma = 8
variable resta : entero ← a - b             // resta = 2
variable multiplicacion : entero ← a * b    // multiplicacion = 15
variable division : entero ← a / b          // division = 1
variable modulo : entero ← a % b            // modulo = 2
```

### Expresiones relacionales

Las expresiones relacionales comparan dos valores y producen un resultado booleano (verdadero o falso).

```pseudocode
variable x : entero ← 10
variable y : entero ← 5
variable igual : booleano ← (x = y)         // igual = falso
variable diferente : booleano ← (x ≠ y)     // diferente = verdadero
variable mayor : booleano ← (x > y)         // mayor = verdadero
variable menor : booleano ← (x < y)         // menor = falso
variable mayorIgual : booleano ← (x ≥ y)    // mayorIgual = verdadero
variable menorIgual : booleano ← (x ≤ y)    // menorIgual = falso
```

### Expresiones lógicas

Las expresiones lógicas combinan valores booleanos utilizando operadores lógicos.

```pseudocode
variable p : booleano ← verdadero
variable q : booleano ← falso
variable andLogico : booleano ← p y q       // andLogico = falso
variable orLogico : booleano ← p o q        // orLogico = verdadero
variable notLogico : booleano ← no p        // notLogico = falso
```

### Expresiones de asignación

Las expresiones de asignación almacenan un valor en una variable.

```pseudocode
variable edad : entero ← 25
variable nombre : texto ← "Juan"
variable activo : booleano ← verdadero
```

## Operador ternario

El operador ternario es una forma abreviada de escribir una expresión condicional simple. Evalúa una condición y devuelve un valor u otro dependiendo del resultado.

```pseudocode
variable temperatura : entero ← 30
variable mensaje : texto ← si (temperatura > 25) entonces "Hace calor" sino "No hace calor"
mostrar(mensaje)  // "Hace calor"
```

Esto es equivalente a:

```pseudocode
variable temperatura : entero ← 30
variable mensaje : texto

si (temperatura > 25) entonces
    mensaje ← "Hace calor"
sino
    mensaje ← "No hace calor"
fin si
```

## Expresiones combinadas

Las expresiones pueden combinarse para crear expresiones más complejas:

```pseudocode
variable a : entero ← 10
variable b : entero ← 5
variable c : entero ← 3

// Expresión aritmética compleja
variable resultado : entero ← (a + b) * c - (a / b)
// resultado = (10 + 5) * 3 - (10 / 5) = 15 * 3 - 2 = 45 - 2 = 43

// Expresión lógica compleja
variable x : booleano ← (a > b) y (c < b) o (a = 10)
// x = (verdadero) y (verdadero) o (verdadero) = verdadero
```

## Precedencia de operadores

Los operadores tienen diferentes niveles de precedencia, que determinan el orden en que se evalúan las expresiones:

1. Paréntesis `()`
2. Negación lógica `no`
3. Multiplicación, división, módulo `*`, `/`, `%`
4. Suma, resta `+`, `-`
5. Operadores relacionales `<`, `>`, `≤`, `≥`
6. Igualdad y desigualdad `=`, `≠`
7. AND lógico `y`
8. OR lógico `o`

```pseudocode
variable resultado : entero ← 2 + 3 * 4
// Se evalúa primero 3 * 4 = 12, luego 2 + 12 = 14
mostrar(resultado)  // 14

variable conParentesis : entero ← (2 + 3) * 4
// Se evalúa primero (2 + 3) = 5, luego 5 * 4 = 20
mostrar(conParentesis)  // 20
```

## Buenas prácticas

- Usa paréntesis para hacer explícito el orden de evaluación, incluso cuando no sean estrictamente necesarios
- Divide expresiones complejas en expresiones más simples para mejorar la legibilidad
- Asigna resultados intermedios a variables con nombres descriptivos

```pseudocode
// Menos legible
variable total : decimal ← (precio * cantidad * (1 + iva)) - descuento + envio

// Más legible
variable subtotal : decimal ← precio * cantidad
variable conIva : decimal ← subtotal * (1 + iva)
variable conDescuento : decimal ← conIva - descuento
variable total : decimal ← conDescuento + envio
```
