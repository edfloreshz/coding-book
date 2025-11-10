# Do-While

El ciclo `do-while` (o `hacer-mientras`) es similar al `while`, pero con una diferencia importante: **siempre se ejecuta al menos una vez**.

## Diferencia con while

| While | Do-While |
|-------|----------|
| Verifica la condición primero | Ejecuta primero, luego verifica |
| Puede no ejecutarse nunca | Siempre se ejecuta al menos una vez |

## Estructura básica

```pseudocode
hacer
    // Código que se repite
mientras (condición)
```

## Ejemplo

```pseudocode
// Pedir un número positivo
variable numero : entero

hacer
    mostrar("Ingresa un número positivo:")
    leer(numero)
    
    si (numero ≤ 0) entonces
        mostrar("Error: debe ser positivo")
    fin si
mientras (numero ≤ 0)

mostrar("Número válido: " + convertirATexto(numero))

// Menú de opciones
variable opcion : entero

hacer
    mostrar("=== MENÚ ===")
    mostrar("1. Jugar")
    mostrar("2. Opciones")
    mostrar("3. Salir")
    mostrar("Elige una opción:")
    leer(opcion)
    
    según (opcion) hacer
        caso 1:
            mostrar("Iniciando juego...")
            salir
        caso 2:
            mostrar("Abriendo opciones...")
            salir
        caso 3:
            mostrar("¡Hasta luego!")
            salir
        por defecto:
            mostrar("Opción inválida. Intenta de nuevo.")
    fin según
mientras (opcion < 1 o opcion > 3)

// Contador que siempre muestra al menos un número
variable i : entero ← 10

hacer
    mostrar(i)
    i ← i + 1
mientras (i < 5)

// Esto muestra: 10
// Aunque la condición es falsa, se ejecuta una vez
```

## ¿Cuándo se usa?

El `do-while` es útil cuando:
- **Menús** - Siempre debes mostrar el menú al menos una vez
- **Validación** - Siempre debes pedir el dato al menos una vez
- **Confirmaciones** - "¿Deseas continuar? (s/n)"

## Comparación práctica

```pseudocode
// Con WHILE: puede no ejecutarse
variable numero : entero ← 10
mientras (numero < 5) hacer
    mostrar(numero)  // No se ejecuta
fin mientras

// Con DO-WHILE: siempre se ejecuta
variable numero : entero ← 10
hacer
    mostrar(numero)  // Se ejecuta una vez: muestra 10
mientras (numero < 5)
```

## Buenas prácticas

1. **Usa do-while cuando garantizas una ejecución** - Menús, validaciones
2. **Prefiere while si la condición puede ser falsa desde el inicio** - Más común y claro
3. **No abuses de do-while** - En la mayoría de casos, `while` es suficiente

## Cuándo usar do-while

**Usa do-while cuando:**
- Necesitas ejecutar el código al menos una vez
- Estás validando entrada del usuario
- Implementas menús interactivos
- Pides confirmación

**Usa while cuando:**
- La primera ejecución depende de la condición
- No estás seguro si debe ejecutarse
- Es el caso más común (úsalo por defecto)

El ciclo `do-while` es menos común que `while`, pero es perfecto para situaciones donde garantizas que el código debe ejecutarse al menos una vez.