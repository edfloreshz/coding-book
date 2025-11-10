# Listas

Las listas son estructuras de datos dinámicas que permiten almacenar colecciones de elementos del mismo tipo. A diferencia de los arreglos, las listas pueden crecer o reducirse según sea necesario durante la ejecución del programa.

## ¿Qué son las listas?

Una lista es una colección ordenada de elementos que permite:
- Agregar elementos en cualquier momento
- Eliminar elementos
- Acceder a elementos por su posición
- Modificar elementos existentes
- Crecer o reducirse dinámicamente

## Diferencias entre listas y arreglos

| Característica | Arreglos | Listas |
|----------------|----------|--------|
| Tamaño | Fijo al crearse | Dinámico |
| Memoria | Más eficiente | Usa más memoria |
| Flexibilidad | Limitada | Alta |
| Velocidad de acceso | Muy rápida | Rápida |
| Agregar elementos | No permite | Sí permite |

## Operaciones con listas

Las listas permiten almacenar varios elementos y modificarlos fácilmente.

### Ejemplo

```pseudocode
// Crear una lista vacía
lista frutas : texto

// Agregar elementos
frutas.agregar("manzana")
frutas.agregar("naranja")
frutas.agregar("plátano")

// Ver cuántos elementos hay
variable cantidad : entero ← frutas.tamaño()
mostrar("Tengo " + convertirATexto(cantidad) + " frutas")  // 3

// Acceder a un elemento por su posición (empieza en 0)
variable primera : texto ← frutas[0]
mostrar(primera)  // "manzana"

// Cambiar un elemento
frutas[1] ← "uva"
mostrar(frutas[1])  // "uva"

// Recorrer la lista
para cada fruta en frutas hacer
    mostrar(fruta)
fin para

// Eliminar un elemento
frutas.eliminar("plátano")
mostrar("Frutas restantes: " + convertirATexto(frutas.tamaño()))  // 2
```

## Buenas prácticas

1. **Verifica el tamaño antes de acceder por índice** - evita errores de índice fuera de rango
2. **Usa nombres descriptivos** - `nombresEstudiantes` en lugar de `lista1`
3. **Inicializa listas cuando sea posible** - si conoces los valores iniciales
4. **Ten cuidado con listas grandes** - agregar al final es más eficiente que insertar al inicio
5. **Verifica si está vacía antes de operar** - previene errores en listas sin elementos

## Cuándo usar listas

**Usa listas cuando:**
- No conoces el número de elementos de antemano
- Necesitas agregar o eliminar elementos frecuentemente
- El tamaño de la colección cambia dinámicamente
- Necesitas flexibilidad en el manejo de datos

**Usa arreglos cuando:**
- Conoces el tamaño exacto de antemano
- El tamaño no cambiará
- Necesitas máxima eficiencia en memoria
- Solo necesitas acceso por índice

Las listas son una de las estructuras de datos más versátiles y utilizadas en programación, perfectas para manejar colecciones dinámicas de elementos.
