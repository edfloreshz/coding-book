# For

El ciclo `for` (o `para`) se usa para repetir código un número específico de veces.

## Estructura básica

```pseudocode
para variable desde inicio hasta fin hacer
    // Código que se repite
fin para
```

## Ejemplo

```pseudocode
// Contar del 1 al 5
para i desde 1 hasta 5 hacer
    mostrar(i)
fin para

// Esto muestra:
// 1
// 2
// 3
// 4
// 5

// Contar del 1 al 10
para numero desde 1 hasta 10 hacer
    mostrar("Número: " + convertirATexto(numero))
fin para

// Sumar números del 1 al 100
variable suma : entero ← 0
para i desde 1 hasta 100 hacer
    suma ← suma + i
fin para
mostrar("La suma es: " + convertirATexto(suma))  // 5050

// Recorrer una lista
lista frutas : texto ← ["manzana", "naranja", "plátano"]
para i desde 0 hasta frutas.tamaño() - 1 hacer
    mostrar(frutas[i])
fin para

// Tabla de multiplicar del 5
para i desde 1 hasta 10 hacer
    variable resultado : entero ← 5 * i
    mostrar("5 x " + convertirATexto(i) + " = " + convertirATexto(resultado))
fin para
```

## For-each (para cada)

Forma más simple para recorrer listas:

```pseudocode
lista colores : texto ← ["rojo", "verde", "azul"]

para cada color en colores hacer
    mostrar(color)
fin para
```

## Paso personalizado

```pseudocode
// Contar de 2 en 2
para i desde 0 hasta 10 paso 2 hacer
    mostrar(i)  // 0, 2, 4, 6, 8, 10
fin para

// Contar hacia atrás
para i desde 10 hasta 1 paso -1 hacer
    mostrar(i)  // 10, 9, 8, 7, 6, 5, 4, 3, 2, 1
fin para
```

## Usos comunes

El ciclo `for` se usa para:
- **Contar** - Del 1 al 10, del 0 al 100, etc.
- **Recorrer listas** - Procesar cada elemento
- **Repetir acciones** - Hacer algo N veces
- **Generar secuencias** - Tablas de multiplicar, patrones

## Diferencia con while

| For | While |
|-----|-------|
| Sabes cuántas veces se repetirá | No sabes cuántas veces se repetirá |
| Más corto y claro | Más flexible |
| Usa contador | Usa condición |

## Buenas prácticas

1. **Usa nombres claros** - `i` está bien para contadores simples, pero usa nombres descriptivos cuando sea necesario
2. **No modifiques el contador dentro del ciclo** - Puede causar confusión
3. **Usa for-each cuando sea posible** - Es más simple y claro
4. **Verifica los límites** - Asegúrate de no salir del rango de la lista

## Cuándo usar for

**Usa for cuando:**
- Sabes exactamente cuántas veces repetir
- Necesitas un contador
- Recorres una lista o arreglo
- Generas secuencias numéricas

**Usa while cuando:**
- No sabes cuántas veces repetir
- Dependes de una condición que puede cambiar
- Esperas entrada del usuario
- La repetición es condicional

El ciclo `for` es una de las estructuras más usadas en programación por su simplicidad y claridad.