# Break y Continue

Las palabras clave `break` (salir) y `continue` (continuar) permiten controlar el flujo dentro de los ciclos.

## Break (Salir)

`break` se usa para **salir completamente** de un ciclo antes de que termine naturalmente.

### Estructura

```pseudocode
mientras (condición) hacer
    // código
    si (alguna_condición) entonces
        salir  // break
    fin si
    // más código
fin mientras
```

### Ejemplo

```pseudocode
// Buscar un número en una lista
lista numeros : entero ← [5, 8, 12, 3, 9, 15]
variable buscando : entero ← 12
variable encontrado : booleano ← falso

para cada numero en numeros hacer
    si (numero = buscando) entonces
        mostrar("¡Encontrado!")
        encontrado ← verdadero
        salir  // Ya lo encontramos, salir del ciclo
    fin si
fin para

si (no encontrado) entonces
    mostrar("No se encontró el número")
fin si

// Limitar intentos
variable intentos : entero ← 0
variable correcto : booleano ← falso

mientras (verdadero) hacer
    mostrar("Ingresa la contraseña:")
    variable password : texto
    leer(password)
    
    si (password = "secreto") entonces
        mostrar("¡Contraseña correcta!")
        correcto ← verdadero
        salir  // Salir del ciclo
    fin si
    
    intentos ← intentos + 1
    
    si (intentos ≥ 3) entonces
        mostrar("Demasiados intentos")
        salir  // Salir del ciclo
    fin si
fin mientras

// Contar hasta encontrar un número par
para i desde 1 hasta 100 hacer
    mostrar(i)
    
    si (i % 2 = 0) entonces
        mostrar("Encontré un número par, deteniendo...")
        salir
    fin si
fin para
```

## Continue (Continuar)

`continue` se usa para **saltar** el resto de la iteración actual y pasar a la siguiente.

### Estructura

```pseudocode
para i desde 1 hasta 10 hacer
    si (alguna_condición) entonces
        continuar  // Salta a la siguiente iteración
    fin si
    // Este código se omite cuando se ejecuta continue
fin para
```

### Ejemplo

```pseudocode
// Mostrar solo números impares
para i desde 1 hasta 10 hacer
    si (i % 2 = 0) entonces
        continuar  // Saltar números pares
    fin si
    
    mostrar(i)  // Solo se ejecuta para impares
fin para
// Muestra: 1, 3, 5, 7, 9

// Procesar solo valores positivos
lista numeros : entero ← [5, -3, 8, -1, 12, -7, 4]

para cada numero en numeros hacer
    si (numero < 0) entonces
        continuar  // Saltar negativos
    fin si
    
    mostrar("Procesando: " + convertirATexto(numero))
fin para
// Procesa solo: 5, 8, 12, 4

// Saltar elementos vacíos
lista nombres : texto ← ["Ana", "", "Carlos", "", "María"]

para cada nombre en nombres hacer
    si (longitud(nombre) = 0) entonces
        continuar  // Saltar nombres vacíos
    fin si
    
    mostrar("Hola, " + nombre)
fin para
// Saluda a: Ana, Carlos, María
```

## Diferencia entre break y continue

| Break | Continue |
|-------|----------|
| Sale completamente del ciclo | Salta al siguiente elemento |
| El ciclo termina | El ciclo continúa |
| Código después del ciclo se ejecuta | Código después del continue NO se ejecuta |

```pseudocode
// Ejemplo que muestra la diferencia
para i desde 1 hasta 5 hacer
    si (i = 3) entonces
        mostrar("Usando break")
        salir
    fin si
    mostrar(i)
fin para
// Muestra: 1, 2, "Usando break"

para i desde 1 hasta 5 hacer
    si (i = 3) entonces
        mostrar("Usando continue")
        continuar
    fin si
    mostrar(i)
fin para
// Muestra: 1, 2, "Usando continue", 4, 5
```

## Usos comunes

### Break se usa para:
- **Búsquedas** - Detener cuando encuentras lo que buscas
- **Validaciones** - Salir cuando encuentras un error
- **Límites** - Detener después de cierto número de intentos
- **Menús** - Salir cuando el usuario elige "salir"

### Continue se usa para:
- **Filtrar** - Saltar elementos que no cumplen condiciones
- **Validación** - Ignorar datos inválidos
- **Procesamiento selectivo** - Procesar solo ciertos elementos

## Buenas prácticas

1. **Usa break para búsquedas** - No sigas buscando después de encontrar
2. **Usa continue para filtros** - Más claro que anidar muchos `si`
3. **No abuses de ellos** - Pueden hacer el código difícil de seguir
4. **Comenta por qué los usas** - Ayuda a entender la lógica

## Cuándo NO usarlos

```pseudocode
// ❌ MAL: break innecesario
para i desde 1 hasta 10 hacer
    mostrar(i)
    si (i = 10) entonces
        salir  // No es necesario, el ciclo ya termina
    fin si
fin para

// ✅ BIEN: sin break
para i desde 1 hasta 10 hacer
    mostrar(i)
fin para

// ❌ MAL: continue complica la lógica
para i desde 1 hasta 10 hacer
    si (i % 2 ≠ 0) entonces
        continuar
    fin si
    mostrar(i)
fin para

// ✅ MEJOR: usa una condición clara
para i desde 1 hasta 10 hacer
    si (i % 2 = 0) entonces
        mostrar(i)
    fin si
fin para
```

Break y continue son herramientas útiles para controlar el flujo de los ciclos, pero úsalas con moderación para mantener el código claro y fácil de entender.