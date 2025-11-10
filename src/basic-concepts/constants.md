# Constantes

Una constante es un valor que no cambia durante la ejecución de un programa. En la mayoría de los lenguajes de programación, las constantes se declaran con una palabra clave especial y se les asigna un valor que no puede ser modificado posteriormente.

Las constantes son útiles para almacenar valores que no deben cambiar durante la ejecución de un programa, como el valor de Pi, la velocidad de la luz, o configuraciones que permanecen fijas.

## Declaración

```pseudocode
constante PI : decimal ← 3.14159
constante VELOCIDAD_LUZ : entero ← 299792458
constante NOMBRE_APLICACION : texto ← "Mi Programa"
```

En los ejemplos anteriores, declaramos constantes de diferentes tipos. Una vez asignado su valor, este no puede ser modificado durante la ejecución del programa.

## Diferencia entre variables y constantes

```pseudocode
// Variable - su valor puede cambiar
variable edad : entero ← 25
edad ← 26  // Esto es válido

// Constante - su valor NO puede cambiar
constante MAX_INTENTOS : entero ← 3
MAX_INTENTOS ← 5  // Error: no se puede modificar una constante
```

## Ejemplos de uso

```pseudocode
constante IVA : decimal ← 0.16
constante MAX_USUARIOS : entero ← 100
constante MENSAJE_BIENVENIDA : texto ← "Bienvenido al sistema"

variable precio : decimal ← 100.0
variable precioConIVA : decimal ← precio * (1 + IVA)

mostrar(MENSAJE_BIENVENIDA)
mostrar("Precio final: " + precioConIVA)
```

## Ventajas

- **Claridad**: Al utilizar constantes, se facilita la comprensión del código y se evitan errores causados por la modificación accidental de valores.
- **Reutilización**: Las constantes pueden ser utilizadas en múltiples partes de un programa sin necesidad de redefinirlas.
- **Optimización**: Al declarar una constante, el compilador puede realizar optimizaciones que mejoren el rendimiento del programa.
- **Mantenimiento**: Al centralizar los valores constantes en un solo lugar, se facilita el mantenimiento y la actualización de los mismos.
- **Seguridad**: Las constantes garantizan que ciertos valores críticos no sean modificados accidentalmente, lo que puede provocar errores en el programa.

## Convenciones de nombres

Por convención, los nombres de constantes suelen escribirse en MAYÚSCULAS con guiones bajos separando las palabras:

```pseudocode
constante DIAS_POR_SEMANA : entero ← 7
constante HORAS_POR_DIA : entero ← 24
constante TEMPERATURA_EBULLICION : decimal ← 100.0
```

Esto hace que sean fácilmente identificables en el código y diferenciables de las variables normales.