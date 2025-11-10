# Asignación

La asignación de valores a las variables es fundamental en la programación. Permite almacenar y modificar datos durante la ejecución del programa.

## Asignación básica

```pseudocode
variable x : entero
x ← 10
mostrar(x)  // 10
```

En este ejemplo, primero declaramos una variable `x` de tipo entero, luego le asignamos el valor `10` usando el operador de asignación `←`.

## Declaración e inicialización

```pseudocode
variable y : entero ← 20
mostrar(y)  // 20
```

En este caso, se declara la variable `y` y se le asigna el valor `20` en la misma línea.

La asignación es un concepto fundamental en la programación y se utiliza para almacenar y manipular datos en las variables de un programa.

## Operadores de asignación compuestos

Además del operador de asignación básico `=`, la mayoría de los lenguajes de programación también admiten operadores de asignación compuestos que combinan una operación aritmética con la asignación. Estos operadores son útiles para abreviar la escritura de expresiones comunes.

Por ejemplo, en lugar de escribir:

```pseudocode
x ← x + 5
```

Puedes usar la notación abreviada en algunos lenguajes:

```pseudocode
// Forma larga
x ← x + 5

// Forma abreviada (en muchos lenguajes)
x += 5
```

Esto es equivalente a la expresión anterior y realiza la misma operación de suma y asignación.

## Operadores compuestos comunes

Aquí hay una lista de algunos operadores de asignación compuestos comunes disponibles en la mayoría de lenguajes:

| Operador | Significado | Equivalente a |
|----------|-------------|---------------|
| `x += 5` | Suma y asignación | `x ← x + 5` |
| `x -= 5` | Resta y asignación | `x ← x - 5` |
| `x *= 5` | Multiplicación y asignación | `x ← x * 5` |
| `x /= 5` | División y asignación | `x ← x / 5` |
| `x %= 5` | Módulo y asignación | `x ← x % 5` |

## Ejemplo

```pseudocode
variable contador : entero ← 0
contador ← contador + 1  // contador ahora es 1
contador += 1             // contador ahora es 2 (notación abreviada)

variable total : decimal ← 100.0
total ← total * 1.5      // total ahora es 150.0
total *= 2               // total ahora es 300.0 (notación abreviada)
```

La asignación es un concepto fundamental en la programación que se utiliza para almacenar valores en variables. Los operadores de asignación compuestos son una forma conveniente de abreviar la escritura de expresiones comunes que involucran operaciones aritméticas y asignaciones.
