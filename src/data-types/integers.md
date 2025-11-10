# Números enteros

Los números enteros (integers) son uno de los tipos de datos más fundamentales en programación. Representan números completos sin parte decimal, tanto positivos como negativos, incluyendo el cero.

## ¿Qué son los números enteros?

Un número entero puede representar valores como: -100, -5, 0, 42, 1000, 999999

Los enteros se usan para contar, indexar, iterar y cualquier situación donde no se necesitan decimales.

## Características principales

- **Sin decimales**: Solo números completos
- **Rango limitado**: Depende del tamaño en memoria (8, 16, 32 o 64 bits)
- **Operaciones rápidas**: Más eficientes que los números de punto flotante
- **Precisión exacta**: No hay errores de redondeo

## Tipos según tamaño

| Tipo | Rango aproximado | Uso común |
|------|-----------------|-----------|
| Byte (8 bits) | -128 a 127 | Caracteres, flags |
| Corto (16 bits) | -32,768 a 32,767 | Contadores pequeños |
| Entero (32 bits) | -2 mil millones a 2 mil millones | Uso general |
| Largo (64 bits) | -9 trillones a 9 trillones | Grandes cantidades |

## Ejemplo

```pseudocode
// Declarar números enteros
variable edad : entero ← 25
variable temperatura : entero ← -5
variable puntos : entero ← 100

// Operaciones básicas
variable a : entero ← 10
variable b : entero ← 3

variable suma : entero ← a + b
variable resta : entero ← a - b
variable multiplicacion : entero ← a * b
variable division : entero ← a / b

mostrar(suma)            // 13
mostrar(resta)           // 7
mostrar(multiplicacion)  // 30
mostrar(division)        // 3 (¡sin decimales!)

// División entera: descarta los decimales
variable resultado : entero ← 10 / 3
mostrar(resultado)  // 3, no 3.333...

// Módulo: obtiene el residuo de la división
variable residuo : entero ← 10 % 3
mostrar(residuo)  // 1

// El módulo es útil para saber si un número es par
variable numero : entero ← 42
si (numero % 2 = 0) entonces
    mostrar("Es par")
sino
    mostrar("Es impar")
fin si

// Contar de 1 a 5
para i desde 1 hasta 5 hacer
    mostrar(i)
fin para
```

## Operaciones comunes

- **Suma**: `a + b`
- **Resta**: `a - b`
- **Multiplicación**: `a * b`
- **División entera**: `a / b` (trunca decimales)
- **Módulo**: `a % b` (residuo de la división)
- **Potenciación**: `a ^ b`
- **Valor absoluto**: `abs(a)`
- **Máximo/Mínimo**: `max(a, b)`, `min(a, b)`

## División entera vs módulo

- **División entera** (`/`): Retorna el cociente sin decimales (10 / 3 = 3)
- **Módulo** (`%`): Retorna el residuo de la división (10 % 3 = 1)

Estos operadores son útiles para:
- Verificar si un número es par/impar (`n % 2 = 0`)
- Extraer dígitos de un número
- Implementar ciclos circulares
- Distribuir elementos uniformemente

## Desbordamiento de enteros

⚠️ **Advertencia importante**: Los enteros tienen un rango limitado. Exceder este rango causa **desbordamiento** (overflow), donde el valor "se envuelve" al otro extremo del rango.

**Ejemplo conceptual**:
- Si el máximo es 2,147,483,647 (32 bits)
- `2,147,483,647 + 1` puede resultar en `-2,147,483,648`

**Prevención**:
- Valida los rangos antes de operaciones grandes
- Usa tipos más grandes si es necesario (64 bits)
- Verifica resultados en operaciones críticas

## Buenas prácticas

1. **Usa nombres descriptivos** - `edadUsuario` en lugar de `x`
2. **Valida divisiones por cero** - previene errores en tiempo de ejecución
3. **Ten cuidado con el desbordamiento** - especialmente en multiplicaciones y potencias
4. **Usa el tipo apropiado** - byte para valores pequeños, largo para grandes
5. **Recuerda que la división es entera** - `7 / 2` es `3`, no `3.5`
6. **Usa módulo para verificar divisibilidad** - más eficiente que divisiones

## Usos comunes

- **Contadores**: Iterar en ciclos
- **Índices**: Acceder a elementos de arreglos y listas
- **Identificadores**: IDs de usuarios, productos, transacciones
- **Cantidades**: Números de artículos, población, distancias enteras
- **Flags binarios**: Usar bits individuales para estados
- **Cálculos matemáticos**: Cuando no se necesitan decimales

## Cuándo usar enteros

**Usa enteros cuando:**
- Cuentas cosas que no pueden ser fraccionarias
- Necesitas precisión exacta sin errores de redondeo
- Trabajas con índices o posiciones
- La velocidad y eficiencia son importantes
- Los valores son siempre números completos

**Usa decimales cuando:**
- Necesitas representar fracciones
- Trabajas con mediciones continuas
- Realizas cálculos financieros con céntimos
- Los valores pueden tener parte decimal

Los números enteros son la base de la programación y se utilizan en casi todos los programas para contar, indexar y realizar cálculos exactos.