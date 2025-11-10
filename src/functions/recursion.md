# Recursión

La recursión es una técnica de programación poderosa donde una función se llama a sí misma para resolver un problema. Es útil cuando un problema puede dividirse en subproblemas más pequeños que son similares al problema original.

## ¿Qué es la recursión?

Una función recursiva es aquella que se invoca a sí misma durante su ejecución. Cada llamada recursiva trabaja con una versión más simple del problema original hasta alcanzar un caso base.

## Componentes esenciales

Toda función recursiva debe tener:

1. **Caso base**: La condición que detiene la recursión (evita bucles infinitos)
2. **Caso recursivo**: La llamada a la función misma con un problema más simple
3. **Progreso hacia el caso base**: Cada llamada debe acercarse al caso base

## Ejemplo: Factorial

El factorial de un número es multiplicarlo por todos los números menores hasta llegar a 1.
Por ejemplo: 5! = 5 × 4 × 3 × 2 × 1 = 120

```pseudocode
// Función que se llama a sí misma (recursiva)
función factorial(n : entero) : entero
    // Caso base: cuando llega a 1, se detiene
    si (n = 1) entonces
        retornar 1
    sino
        // Caso recursivo: se llama a sí misma con un número menor
        retornar n * factorial(n - 1)
    fin si
fin función

// Calcular factorial de 5
variable resultado : entero ← factorial(5)
mostrar(resultado)  // 120

// ¿Cómo funciona?
// factorial(5) = 5 * factorial(4)
// factorial(4) = 4 * factorial(3)
// factorial(3) = 3 * factorial(2)
// factorial(2) = 2 * factorial(1)
// factorial(1) = 1 (se detiene aquí)
//
// Luego regresa multiplicando:
// 2 * 1 = 2
// 3 * 2 = 6
// 4 * 6 = 24
// 5 * 24 = 120
```

## Recursión vs Iteración

La mayoría de problemas recursivos pueden resolverse también con ciclos (iteración):

**Versión recursiva (factorial):**
- Más elegante y fácil de entender
- Usa la pila de llamadas
- Puede causar desbordamiento de pila con valores grandes

**Versión iterativa (factorial):**
- Más eficiente en memoria
- No tiene límite de pila
- Puede ser menos intuitiva para algunos problemas

## Cuándo usar recursión

**Usa recursión cuando:**
- El problema se puede dividir naturalmente en subproblemas similares
- Trabajas con estructuras de datos recursivas (árboles, listas enlazadas)
- El código recursivo es más claro que el iterativo
- El número de llamadas recursivas es razonable

**Evita recursión cuando:**
- El problema requiere muchas llamadas recursivas (riesgo de desbordamiento)
- La solución iterativa es más eficiente
- Hay muchas llamadas duplicadas (como Fibonacci sin optimizar)
- El rendimiento es crítico

## Ventajas de la recursión

1. **Código más limpio y elegante** - especialmente para problemas naturalmente recursivos
2. **Divide y vencerás** - descompone problemas complejos en casos simples
3. **Ideal para estructuras recursivas** - árboles, grafos, listas enlazadas
4. **Expresividad** - algunos algoritmos son más naturales en forma recursiva

## Desventajas de la recursión

1. **Uso de memoria** - cada llamada consume espacio en la pila
2. **Rendimiento** - overhead de llamadas a función
3. **Desbordamiento de pila** - demasiadas llamadas pueden causar errores
4. **Dificultad de depuración** - seguir el flujo puede ser complejo

## Buenas prácticas

1. **Siempre define un caso base claro** - evita recursión infinita
2. **Asegúrate de progresar hacia el caso base** - cada llamada debe simplificar el problema
3. **Valida las entradas** - previene errores con valores inesperados
4. **Considera límites** - ten en cuenta el tamaño del problema
5. **Documenta el funcionamiento** - explica el caso base y recursivo
6. **Compara con iteración** - a veces un ciclo es más apropiado

## Problemas comunes

1. **Recursión infinita** - olvidar el caso base o no progresar hacia él
2. **Desbordamiento de pila** - demasiadas llamadas recursivas anidadas
3. **Ineficiencia** - calcular los mismos valores múltiples veces
4. **Casos base incorrectos** - no cubrir todos los escenarios de terminación

La recursión es una herramienta poderosa que, cuando se usa correctamente, puede hacer que el código sea más elegante y fácil de entender, especialmente para problemas que tienen una estructura recursiva natural.