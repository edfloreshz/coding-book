# Números de punto flotante

Los números de punto flotante (también llamados números decimales o reales) son tipos de datos que permiten representar números con parte decimal. Son esenciales para cálculos científicos, financieros y cualquier situación donde se necesite precisión decimal.

## ¿Qué son los números de punto flotante?

Un número de punto flotante puede representar valores con parte decimal como: 3.14, -0.5, 1234.567, 0.0001, 2.718281828

## Tipos según precisión

| Tipo | Precisión | Uso común |
|------|-----------|-----------|
| Flotante simple | 6-9 dígitos | Gráficos, cálculos generales |
| Flotante doble | 15-17 dígitos | Científico, ingeniería |
| Decimal | 28-29 dígitos | Finanzas, dinero |

## Ejemplo

```pseudocode
// Declarar números decimales
variable precio : decimal ← 19.99
variable temperatura : decimal ← -3.5
variable pi : decimal ← 3.14

// Operaciones con decimales
variable a : decimal ← 10.5
variable b : decimal ← 2.0

variable suma : decimal ← a + b
variable resta : decimal ← a - b
variable multiplicacion : decimal ← a * b
variable division : decimal ← a / b

mostrar(suma)            // 12.5
mostrar(resta)           // 8.5
mostrar(multiplicacion)  // 21.0
mostrar(division)        // 5.25

// La división con decimales SÍ guarda los decimales
variable resultado : decimal ← 10.0 / 3.0
mostrar(resultado)  // 3.333333...

// Redondear números
variable numero : decimal ← 3.7
variable redondeado : decimal ← redondear(numero)
mostrar(redondeado)  // 4.0

// Calcular raíz cuadrada
variable raiz : decimal ← raizCuadrada(16.0)
mostrar(raiz)  // 4.0

// IMPORTANTE: Los decimales no siempre son exactos
variable x : decimal ← 0.1 + 0.2
mostrar(x)  // Puede mostrar 0.30000000000004 en lugar de 0.3

// Por eso NUNCA compares decimales con =
// ❌ MAL:
si (x = 0.3) entonces
    mostrar("Iguales")
fin si

// ✅ BIEN: Verifica si están "cerca"
variable diferencia : decimal ← abs(x - 0.3)
si (diferencia < 0.0001) entonces
    mostrar("Aproximadamente iguales")
fin si
```

## Problema de imprecisión

⚠️ **Advertencia importante**: Los números de punto flotante tienen limitaciones de precisión porque se representan en binario. Esto puede causar pequeños errores de redondeo.

**Ejemplos de imprecisión:**
- `0.1 + 0.2` puede dar `0.30000000000000004` en lugar de `0.3`
- Acumular errores en operaciones repetidas
- Comparaciones de igualdad pueden fallar

## Buenas prácticas

1. **Nunca compares flotantes con igualdad exacta** - usa una tolerancia (epsilon)
2. **Para dinero, usa tipos decimales de alta precisión** - o trabaja con centavos como enteros
3. **Redondea resultados para presentación** - especialmente en interfaces de usuario
4. **Ten cuidado con la acumulación de errores** - en cálculos iterativos largos
5. **Valida resultados especiales** - infinito y NaN pueden causar problemas
6. **Usa notación científica para números extremos** - facilita la lectura

## Funciones matemáticas comunes

- `raizCuadrada(x)` - raíz cuadrada
- `potencia(base, exp)` - potenciación
- `abs(x)` - valor absoluto
- `redondear(x)` - redondeo al entero más cercano
- `piso(x)` - redondeo hacia abajo
- `techo(x)` - redondeo hacia arriba
- `truncar(x)` - elimina la parte decimal
- `sen(x)`, `cos(x)`, `tan(x)` - funciones trigonométricas
- `log(x)`, `ln(x)` - logaritmos
- `max(a, b)`, `min(a, b)` - máximo y mínimo

## Casos especiales

- **Infinito positivo** - resultado de dividir número positivo entre cero
- **Infinito negativo** - resultado de dividir número negativo entre cero
- **NaN (Not a Number)** - resultado de operaciones inválidas como `0.0 / 0.0`
- **Cero negativo** - en algunos sistemas existe `-0.0` (diferente de `+0.0`)

## Cuándo usar flotantes

**Usa números de punto flotante cuando:**
- Necesitas representar valores con decimales
- Realizas cálculos científicos o de ingeniería
- Trabajas con mediciones físicas
- Necesitas un rango muy amplio de valores

**Evita flotantes cuando:**
- Necesitas precisión exacta (dinero, conteo)
- Comparas igualdad frecuentemente
- La precisión es crítica y no toleras errores de redondeo

Los números de punto flotante son herramientas poderosas pero requieren comprensión de sus limitaciones para usarlos correctamente.