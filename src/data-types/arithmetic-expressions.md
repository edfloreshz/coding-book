# Expresiones aritméticas

Una expresión aritmética es una combinación de valores, variables y operadores que se evalúa para producir un resultado numérico. Los operadores aritméticos se utilizan para realizar operaciones matemáticas básicas, como suma, resta, multiplicación y división.

## Operadores básicos

```/dev/null/pseudocode.txt#L1-8
a : Entero ← 10
b : Entero ← 3

suma : Entero ← a + b         // 13
resta : Entero ← a - b        // 7
multiplicación : Entero ← a * b  // 30
división : Entero ← a / b     // 3
resto : Entero ← a % b        // 1
```

## Operadores de incremento y decremento

El operador de incremento (`++`) aumenta el valor en 1, y el operador de decremento (`--`) lo disminuye en 1.

### Incremento/Decremento posfijo

El valor se usa primero, luego se incrementa o decrementa:

```/dev/null/pseudocode.txt#L1-6
i : Entero ← 3
mostrar(i++)    // muestra 3, luego i se convierte en 4
mostrar(i)      // muestra 4

j : Entero ← 5
mostrar(j--)    // muestra 5, luego j se convierte en 4
```

### Incremento/Decremento prefijo

El valor se incrementa o decrementa primero, luego se usa:

```/dev/null/pseudocode.txt#L1-6
i : Entero ← 3
mostrar(++i)    // i se convierte en 4, luego muestra 4
mostrar(i)      // muestra 4

j : Entero ← 5
mostrar(--j)    // j se convierte en 4, luego muestra 4
```

## Precedencia de operadores

Los operadores siguen un orden de evaluación:

1. Paréntesis `()`
2. Incremento/Decremento `++`, `--`
3. Multiplicación, División, Módulo `*`, `/`, `%`
4. Suma, Resta `+`, `-`

```/dev/null/pseudocode.txt#L1-4
resultado : Entero ← 2 + 3 * 4      // 14 (multiplicación primero)
resultado : Entero ← (2 + 3) * 4    // 20 (paréntesis primero)
resultado : Entero ← 10 / 2 * 3     // 15 (izquierda a derecha)
```

## Ejemplo práctico

```/dev/null/pseudocode.txt#L1-7
// Calcular el área de un rectángulo
base : Decimal ← 5.0
altura : Decimal ← 3.0
área : Decimal ← base * altura
perímetro : Decimal ← 2 * (base + altura)

mostrar("Área: ", área, ", Perímetro: ", perímetro)
```

## Notas importantes

- La división de enteros descarta la parte decimal
- El operador módulo (`%`) devuelve el resto de la división
- Usar paréntesis para clarificar el orden de las operaciones
- Los operadores de incremento/decremento modifican la variable directamente