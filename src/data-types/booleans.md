# Booleanos

Los valores booleanos son uno de los tipos de datos más fundamentales en programación. Representan valores de verdad y solo pueden tener dos estados: verdadero o falso.

## ¿Qué son los booleanos?

Un booleano es un tipo de dato que puede almacenar únicamente dos valores posibles: `verdadero` o `falso`. Son esenciales para tomar decisiones, controlar el flujo del programa, validar condiciones y representar estados binarios (encendido/apagado, sí/no, activo/inactivo).

## Operadores lógicos

Los operadores lógicos principales son:

- **AND (y)** - verdadero solo si ambos operandos son verdaderos
- **OR (o)** - verdadero si al menos uno es verdadero
- **NOT (no)** - invierte el valor booleano
- **XOR (xor)** - verdadero si los operandos son diferentes

## Operadores de comparación

Los operadores de comparación evalúan expresiones y devuelven valores booleanos:

- `=` - igual a
- `≠` - diferente de
- `>` - mayor que
- `<` - menor que
- `≥` - mayor o igual que
- `≤` - menor o igual que

## Ejemplo

```pseudocode
// Declarar variables booleanas
variable esMayorDeEdad : booleano ← verdadero
variable tieneLicencia : booleano ← falso

// Comparar números
variable edad : entero ← 20
variable puedeVotar : booleano ← edad ≥ 18
mostrar(puedeVotar)  // verdadero

// Operador AND (y) - ambos deben ser verdaderos
variable puedeConducir : booleano ← esMayorDeEdad y tieneLicencia
mostrar(puedeConducir)  // falso (porque no tiene licencia)

// Operador OR (o) - al menos uno debe ser verdadero
variable tieneAcceso : booleano ← esMayorDeEdad o tieneLicencia
mostrar(tieneAcceso)  // verdadero (porque es mayor de edad)

// Operador NOT (no) - invierte el valor
variable esMenorDeEdad : booleano ← no esMayorDeEdad
mostrar(esMenorDeEdad)  // falso

// Usar en decisiones
si (puedeVotar) entonces
    mostrar("Puede votar en las elecciones")
sino
    mostrar("No puede votar todavía")
fin si
```

## Tablas de verdad

### AND (y)
| A | B | A y B |
|---|---|-------|
| verdadero | verdadero | verdadero |
| verdadero | falso | falso |
| falso | verdadero | falso |
| falso | falso | falso |

### OR (o)
| A | B | A o B |
|---|---|-------|
| verdadero | verdadero | verdadero |
| verdadero | falso | verdadero |
| falso | verdadero | verdadero |
| falso | falso | falso |

### NOT (no)
| A | no A |
|---|------|
| verdadero | falso |
| falso | verdadero |

### XOR (xor)
| A | B | A xor B |
|---|---|---------|
| verdadero | verdadero | falso |
| verdadero | falso | verdadero |
| falso | verdadero | verdadero |
| falso | falso | falso |

## Precedencia de operadores

El orden de evaluación (de mayor a menor precedencia):

1. `no` (NOT)
2. `y` (AND)
3. `o` (OR)
4. `xor` (XOR)

Usa paréntesis para aclarar o cambiar el orden de evaluación.

## Buenas prácticas

1. **Usa nombres descriptivos** - `esMayorDeEdad` en lugar de `b1`
2. **Evita comparaciones redundantes** - usa `esActivo` en lugar de `esActivo = verdadero`
3. **Simplifica negaciones dobles** - `no (no x)` es equivalente a `x`
4. **Usa paréntesis para claridad** - especialmente en expresiones complejas
5. **Aprovecha el cortocircuito** - el orden de operandos puede prevenir errores

## Usos comunes

- **Validación de datos** - verificar que la entrada cumple requisitos
- **Control de flujo** - decidir qué código ejecutar
- **Banderas de estado** - rastrear el estado de un proceso
- **Condiciones de ciclos** - controlar la repetición
- **Permisos y autorizaciones** - verificar acceso a recursos

Los booleanos son fundamentales para la lógica de programación y se utilizan en casi todos los programas para tomar decisiones y controlar el flujo de ejecución.