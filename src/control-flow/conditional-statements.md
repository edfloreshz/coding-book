# Declaraciones condicionales

Las declaraciones condicionales permiten ejecutar bloques de código basados en condiciones específicas. Son fundamentales para controlar el flujo de ejecución de un programa y tomar decisiones basadas en diferentes situaciones.

## Estructura básica

La estructura básica de una declaración condicional es:

```pseudocode
si (condición) entonces
    // Bloque de código si la condición es verdadera
sino
    // Bloque de código si la condición es falsa
fin si
```

En este caso, si la condición es verdadera, se ejecutará el primer bloque de código. Si la condición es falsa, se ejecutará el bloque de código dentro del `sino`.

## Ejemplo simple

```pseudocode
variable numero : entero ← -5

si (numero ≥ 0) entonces
    mostrar("El número es positivo")
sino
    mostrar("El número es negativo")
fin si
```

En este ejemplo, si el número es mayor o igual a cero, se imprimirá "El número es positivo". De lo contrario, se imprimirá "El número es negativo".

## Condiciones múltiples (else if)

Las declaraciones condicionales también se pueden encadenar para evaluar múltiples condiciones:

```pseudocode
variable numero : entero ← 10

si (numero > 0) entonces
    mostrar("El número es positivo")
sino si (numero < 0) entonces
    mostrar("El número es negativo")
sino
    mostrar("El número es cero")
fin si
```

En este caso:
- Si el número es mayor que cero, se imprime "El número es positivo"
- Si no, se evalúa si es menor que cero, y se imprime "El número es negativo"
- Si ninguna de las condiciones anteriores se cumple, se imprime "El número es cero"

## Condiciones anidadas

Las declaraciones condicionales pueden anidarse unas dentro de otras:

```pseudocode
variable edad : entero ← 25
variable tieneLicencia : booleano ← verdadero

si (edad ≥ 18) entonces
    si (tieneLicencia) entonces
        mostrar("Puede conducir")
    sino
        mostrar("Es mayor de edad pero no tiene licencia")
    fin si
sino
    mostrar("Es menor de edad, no puede conducir")
fin si
```

## Condiciones compuestas

Puedes combinar múltiples condiciones usando operadores lógicos:

```pseudocode
variable temperatura : entero ← 28
variable esSoleado : booleano ← verdadero

si (temperatura > 25 y esSoleado) entonces
    mostrar("¡Perfecto para ir a la playa!")
fin si

variable hora : entero ← 14
si (hora < 12 o hora > 20) entonces
    mostrar("El restaurante está cerrado")
sino
    mostrar("El restaurante está abierto")
fin si
```

## Condicional simple (sin else)

No siempre es necesario incluir un bloque `sino`:

```pseudocode
variable saldo : decimal ← 100.0
variable retiro : decimal ← 50.0

si (retiro ≤ saldo) entonces
    saldo ← saldo - retiro
    mostrar("Retiro exitoso. Saldo actual: " + saldo)
fin si
```

## Ejemplo

```pseudocode
variable nota : decimal ← 8.5

si (nota ≥ 9.0) entonces
    mostrar("Calificación: Sobresaliente")
sino si (nota ≥ 7.0) entonces
    mostrar("Calificación: Notable")
sino si (nota ≥ 5.0) entonces
    mostrar("Calificación: Aprobado")
sino
    mostrar("Calificación: Reprobado")
fin si
```

## Buenas prácticas

1. **Mantén las condiciones simples y legibles**
   ```pseudocode
   // Menos legible
   si (no(edad < 18 o no(tieneLicencia))) entonces

   // Más legible
   si (edad ≥ 18 y tieneLicencia) entonces
   ```

2. **Evita anidaciones profundas**: Si tienes muchas condiciones anidadas, considera usar múltiples `sino si` o reestructurar tu código.

3. **Usa nombres descriptivos para variables booleanas**
   ```pseudocode
   variable esValido : booleano ← verdadero
   variable puedeAcceder : booleano ← falso
   ```

4. **Ordena las condiciones de más específica a más general**
   ```pseudocode
   si (edad < 2) entonces
       mostrar("Bebé")
   sino si (edad < 13) entonces
       mostrar("Niño")
   sino si (edad < 18) entonces
       mostrar("Adolescente")
   sino
       mostrar("Adulto")
   fin si
   ```
