# While

El ciclo `while` (o `mientras`) se usa para repetir código mientras una condición sea verdadera.

## Estructura básica

```pseudocode
mientras (condición) hacer
    // Código que se repite
fin mientras
```

## Ejemplo

```pseudocode
// Contar del 1 al 5
variable numero : entero ← 1

mientras (numero ≤ 5) hacer
    mostrar(numero)
    numero ← numero + 1
fin mientras

// Esto muestra:
// 1
// 2
// 3
// 4
// 5

// Pedir contraseña hasta que sea correcta
variable contraseña : texto
variable correcta : booleano ← falso

mientras (no correcta) hacer
    mostrar("Ingresa la contraseña:")
    leer(contraseña)
    
    si (contraseña = "secreto123") entonces
        correcta ← verdadero
        mostrar("¡Contraseña correcta!")
    sino
        mostrar("Contraseña incorrecta. Intenta de nuevo.")
    fin si
fin mientras

// Sumar números hasta que el usuario ingrese 0
variable suma : entero ← 0
variable numero : entero ← 1

mostrar("Ingresa números para sumar (0 para terminar):")

mientras (numero ≠ 0) hacer
    leer(numero)
    suma ← suma + numero
fin mientras

mostrar("La suma total es: " + convertirATexto(suma))

// Juego de adivinar número
variable numeroSecreto : entero ← 7
variable intento : entero ← 0
variable adivinado : booleano ← falso

mientras (no adivinado) hacer
    mostrar("Adivina el número (1-10):")
    leer(intento)
    
    si (intento = numeroSecreto) entonces
        mostrar("¡Correcto!")
        adivinado ← verdadero
    sino si (intento < numeroSecreto) entonces
        mostrar("Muy bajo")
    sino
        mostrar("Muy alto")
    fin si
fin mientras
```

## ¿Cuándo se detiene?

El ciclo `while` se detiene cuando la condición se vuelve falsa.

**Importante:** Asegúrate de que la condición eventualmente sea falsa, o tendrás un ciclo infinito.

```pseudocode
// ❌ MAL: Ciclo infinito (nunca se detiene)
variable x : entero ← 1
mientras (x > 0) hacer
    mostrar(x)
    // x siempre será mayor que 0
fin mientras

// ✅ BIEN: El ciclo eventualmente termina
variable x : entero ← 5
mientras (x > 0) hacer
    mostrar(x)
    x ← x - 1  // x eventualmente llegará a 0
fin mientras
```

## Diferencia con for

| While | For |
|-------|-----|
| No sabes cuántas veces se repetirá | Sabes cuántas veces se repetirá |
| Depende de una condición | Usa un contador |
| Más flexible | Más corto para contar |

## Usos comunes

El ciclo `while` se usa para:
- **Validar entrada** - Pedir datos hasta que sean válidos
- **Juegos** - Mientras el jugador tenga vidas
- **Menús** - Mientras el usuario no elija "salir"
- **Procesar datos** - Mientras haya datos por leer

## Buenas prácticas

1. **Asegúrate de que la condición cambie** - Para evitar ciclos infinitos
2. **Inicializa variables antes del ciclo** - La condición debe tener sentido desde el inicio
3. **Usa nombres claros** - La condición debe ser fácil de entender
4. **Ten cuidado con ciclos infinitos** - Siempre debe haber una forma de salir

## Cuándo usar while

**Usa while cuando:**
- No sabes cuántas veces repetir
- Dependes de la entrada del usuario
- Esperas que algo cambie (archivo se cargue, condición se cumpla)
- La condición de parada es compleja

**Usa for cuando:**
- Sabes exactamente cuántas veces repetir
- Estás contando o recorriendo una lista
- Tienes un inicio y fin claros

El ciclo `while` es esencial para situaciones donde no sabemos de antemano cuántas veces necesitamos repetir algo.