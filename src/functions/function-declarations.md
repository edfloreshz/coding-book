# Declaración de funciones

Las funciones son bloques de código reutilizables que realizan una tarea específica. Son como recetas: defines cómo hacer algo una vez, y luego puedes usarlo muchas veces.

## ¿Qué es una función?

Una función tiene:
- **Nombre** - Cómo la llamas
- **Parámetros** (opcional) - Información que recibe
- **Código** - Lo que hace
- **Retorno** (opcional) - Lo que devuelve

## Estructura básica

```pseudocode
función nombreFuncion(parámetro : tipo) : tipoRetorno
    // Código que ejecuta
    retornar valor
fin función
```

## Ejemplo

```pseudocode
// Función simple que suma dos números
función sumar(a : entero, b : entero) : entero
    variable resultado : entero ← a + b
    retornar resultado
fin función

// Usar la función
variable total : entero ← sumar(5, 3)
mostrar(total)  // 8

// Función que saluda
función saludar(nombre : texto) : nulo
    mostrar("¡Hola, " + nombre + "!")
fin función

// Usar la función
saludar("María")  // ¡Hola, María!

// Función sin parámetros
función obtenerPi() : decimal
    retornar 3.14159
fin función

variable pi : decimal ← obtenerPi()
mostrar(pi)  // 3.14159

// Función que calcula el área de un rectángulo
función calcularArea(base : decimal, altura : decimal) : decimal
    variable area : decimal ← base * altura
    retornar area
fin función

variable miArea : decimal ← calcularArea(5.0, 3.0)
mostrar("El área es: " + convertirATexto(miArea))  // 15.0

// Función que verifica si un número es par
función esPar(numero : entero) : booleano
    retornar (numero % 2 = 0)
fin función

si (esPar(10)) entonces
    mostrar("Es par")
sino
    mostrar("Es impar")
fin si

// Función sin retorno (solo hace algo)
función imprimirMensaje(mensaje : texto, veces : entero) : nulo
    para i desde 1 hasta veces hacer
        mostrar(mensaje)
    fin para
fin función

imprimirMensaje("Hola", 3)
// Muestra "Hola" tres veces
```

## Parámetros

Los parámetros son valores que la función necesita para trabajar:

```pseudocode
// Un parámetro
función cuadrado(numero : entero) : entero
    retornar numero * numero
fin función

// Dos parámetros
función mayorDe(a : entero, b : entero) : entero
    si (a > b) entonces
        retornar a
    sino
        retornar b
    fin si
fin función

// Sin parámetros
función obtenerSaludo() : texto
    retornar "Buenos días"
fin función
```

## Retorno

El `retornar` devuelve un valor al código que llamó la función:

```pseudocode
función multiplicar(x : entero, y : entero) : entero
    retornar x * y
fin función

variable resultado : entero ← multiplicar(4, 5)
// resultado ahora vale 20
```

Si la función no retorna nada, usa `: nulo`:

```pseudocode
función mostrarBienvenida() : nulo
    mostrar("Bienvenido al programa")
    mostrar("Presiona ENTER para continuar")
fin función
```

## ¿Por qué usar funciones?

1. **Reutilización** - Escribe el código una vez, úsalo muchas veces
2. **Organización** - Divide el código en partes manejables
3. **Claridad** - El código es más fácil de leer
4. **Mantenimiento** - Si algo cambia, solo editas en un lugar

```pseudocode
// Sin funciones (repetitivo)
mostrar("=== Menú ===")
mostrar("1. Opción 1")
mostrar("2. Opción 2")
mostrar("============")

// ... más código ...

mostrar("=== Menú ===")
mostrar("1. Opción 1")
mostrar("2. Opción 2")
mostrar("============")

// Con funciones (mejor)
función mostrarMenu() : nulo
    mostrar("=== Menú ===")
    mostrar("1. Opción 1")
    mostrar("2. Opción 2")
    mostrar("============")
fin función

mostrarMenu()
// ... más código ...
mostrarMenu()
```

## Buenas prácticas

1. **Nombres descriptivos** - `calcularPromedio` en lugar de `calc`
2. **Una tarea por función** - Cada función hace una cosa bien
3. **No muy larga** - Si es muy larga, divídela en funciones más pequeñas
4. **Usa parámetros** - En lugar de variables globales

```pseudocode
// ✅ BIEN: nombre claro, hace una cosa
función convertirCelsiusAFahrenheit(celsius : decimal) : decimal
    retornar (celsius * 9.0 / 5.0) + 32.0
fin función

// ❌ MAL: nombre poco claro
función conv(c : decimal) : decimal
    retornar (c * 9.0 / 5.0) + 32.0
fin función
```

## Cuándo crear una función

Crea una función cuando:
- Repites el mismo código en varios lugares
- Una parte del código hace una tarea específica
- Quieres que el código sea más fácil de entender
- Necesitas probar una parte del código por separado

Las funciones son la base de la programación organizada y son esenciales para escribir código limpio y mantenible.