# Guía de Pseudocódigo

A lo largo de este libro, utilizamos **pseudocódigo** para ilustrar conceptos de programación de manera independiente del lenguaje. El pseudocódigo es una forma de escribir algoritmos y lógica de programación usando un lenguaje simplificado que cualquier persona puede entender, sin estar atado a la sintaxis específica de un lenguaje de programación particular.

## ¿Por qué pseudocódigo?

El pseudocódigo te permite:
- **Enfocarte en la lógica** sin preocuparte por la sintaxis específica
- **Aplicar los conceptos** a cualquier lenguaje de programación
- **Entender mejor** los fundamentos antes de aprender un lenguaje específico
- **Traducir fácilmente** a tu lenguaje de programación preferido

## Convenciones utilizadas

### Declaración de variables

```pseudocode
variable nombre_variable : tipo
variable edad : entero
variable nombre : texto
variable precio : decimal
variable activo : booleano
```

### Asignación de valores

```pseudocode
nombre_variable ← valor
edad ← 25
nombre ← "María"
precio ← 19.99
activo ← verdadero
```

### Estructuras condicionales

```pseudocode
si (condición) entonces
    // código si la condición es verdadera
sino
    // código si la condición es falsa
fin si
```

### Ciclos

```pseudocode
// Ciclo mientras
mientras (condición) hacer
    // código a repetir
fin mientras

// Ciclo para
para i desde 0 hasta 10 hacer
    // código a repetir
fin para

// Ciclo hacer-mientras
hacer
    // código a repetir
mientras (condición)
```

### Funciones

```pseudocode
función nombre_función(parámetro1 : tipo, parámetro2 : tipo) : tipo_retorno
    // cuerpo de la función
    retornar valor
fin función
```

### Comentarios

```pseudocode
// Esto es un comentario de una línea

/* Esto es un comentario
   de múltiples líneas */
```

### Operadores

| Operador | Significado | Ejemplo |
|----------|-------------|---------|
| ← | Asignación | x ← 5 |
| = | Igualdad | x = 5 |
| ≠ | Diferente | x ≠ 5 |
| < | Menor que | x < 5 |
| > | Mayor que | x > 5 |
| ≤ | Menor o igual | x ≤ 5 |
| ≥ | Mayor o igual | x ≥ 5 |
| y | AND lógico | (x > 0) y (x < 10) |
| o | OR lógico | (x = 0) o (x = 10) |
| no | NOT lógico | no(x = 0) |

### Entrada y Salida

```pseudocode
// Mostrar en pantalla
mostrar("Hola mundo")
imprimir(variable)

// Leer entrada del usuario
leer(variable)
variable ← entrada()
```

### Arreglos

```pseudocode
// Declaración
arreglo números[5] : entero

// Acceso
números[0] ← 10
valor ← números[0]
```

### Objetos y Clases

```pseudocode
clase NombreClase
    // Atributos
    atributo nombre : texto
    atributo edad : entero

    // Constructor
    constructor(nombre : texto, edad : entero)
        este.nombre ← nombre
        este.edad ← edad
    fin constructor

    // Métodos
    método saludar()
        mostrar("Hola, soy " + este.nombre)
    fin método
fin clase
```

## Tipos de datos comunes

- **entero**: Números enteros (1, 2, 3, -5, 0)
- **decimal**: Números con punto decimal (3.14, 2.5, -0.5)
- **texto**: Cadenas de caracteres ("Hola", "Mundo")
- **carácter**: Un solo carácter ('a', 'Z', '1')
- **booleano**: Valores de verdad (verdadero, falso)
- **nulo**: Ausencia de valor (nulo)

## Ejemplo

```pseudocode
// Programa para calcular el promedio de calificaciones

función calcularPromedio(calificaciones : arreglo de decimal) : decimal
    variable suma : decimal ← 0
    variable cantidad : entero ← longitud(calificaciones)

    para cada calificacion en calificaciones hacer
        suma ← suma + calificacion
    fin para

    retornar suma / cantidad
fin función

// Programa principal
inicio
    arreglo calificaciones[5] : decimal
    calificaciones ← [8.5, 9.0, 7.5, 8.0, 9.5]

    variable promedio : decimal
    promedio ← calcularPromedio(calificaciones)

    mostrar("El promedio es: " + promedio)
fin
```

## Adaptando a tu lenguaje favorito

El pseudocódigo de este libro puede traducirse fácilmente a cualquier lenguaje:

| Pseudocódigo | Python | JavaScript | Java |
|--------------|--------|------------|------|
| `variable x : entero` | `x = 0` | `let x;` | `int x;` |
| `x ← 5` | `x = 5` | `x = 5;` | `x = 5;` |
| `si ... entonces` | `if ...:` | `if (...) {` | `if (...) {` |
| `mostrar(x)` | `print(x)` | `console.log(x)` | `System.out.println(x)` |

¡Recuerda que el objetivo es entender la lógica primero, y la sintaxis específica vendrá después!
