# Pilas

Las pilas (stacks) son estructuras de datos que siguen el principio **LIFO** (Last In, First Out - Último en Entrar, Primero en Salir). Son como una pila de platos: solo puedes agregar o quitar platos desde arriba.

## ¿Qué son las pilas?

Una pila es una colección donde:
- Los elementos se agregan arriba
- Los elementos se sacan desde arriba
- El último en entrar es el primero en salir

## Visualización

```
    ┌─────┐
    │  C  │ ← Tope (se saca primero)
    ├─────┤
    │  B  │
    ├─────┤
    │  A  │ ← Base (se saca último)
    └─────┘
```

## Ejemplo

```pseudocode
// Crear una pila vacía
pila libros : texto

// Apilar libros (agregar arriba)
libros.apilar("Don Quijote")
libros.apilar("Cien años de soledad")
libros.apilar("El Principito")

// Ahora la pila es (de abajo a arriba):
// Don Quijote → Cien años de soledad → El Principito (arriba)

// Ver qué libro está arriba (sin sacarlo)
variable arriba : texto ← libros.tope()
mostrar(arriba)  // "El Principito"

// Sacar el libro de arriba (desapilar)
variable sacado : texto ← libros.desapilar()
mostrar(sacado)  // "El Principito"

// Ahora la pila es:
// Don Quijote → Cien años de soledad (arriba)

// Sacar el siguiente
sacado ← libros.desapilar()
mostrar(sacado)  // "Cien años de soledad"

// Ver cuántos libros quedan
variable cantidad : entero ← libros.tamaño()
mostrar(cantidad)  // 1

// Verificar si la pila está vacía
variable vacia : booleano ← libros.estaVacia()
mostrar(vacia)  // falso
```

## Operaciones principales

- **`apilar(elemento)`** - Agregar un elemento arriba
- **`desapilar()`** - Sacar y retornar el elemento de arriba
- **`tope()`** - Ver el elemento de arriba sin sacarlo
- **`tamaño()`** - Ver cuántos elementos hay
- **`estaVacia()`** - Verificar si la pila está vacía

## Usos comunes

Las pilas se usan para:
- **Deshacer/Rehacer** - En editores de texto (Ctrl+Z)
- **Navegación** - Botón "atrás" del navegador
- **Validar paréntesis** - Verificar que ( ) [ ] { } estén balanceados
- **Llamadas a funciones** - El sistema guarda dónde volver

## Diferencia con colas

| Característica | Pila (LIFO) | Cola (FIFO) |
|----------------|-------------|-------------|
| Orden | Último en entrar, primero en salir | Primero en entrar, primero en salir |
| Analogía | Pila de platos | Fila de personas |
| Agregar | Arriba | Al final |
| Sacar | De arriba | Del frente |

## Buenas prácticas

1. **Verifica si está vacía antes de desapilar** - evita errores
2. **Usa nombres descriptivos** - `pilaHistorial` en lugar de `s`
3. **Respeta el orden LIFO** - no accedas a elementos del medio
4. **Usa pilas para deshacer acciones** - guarda el historial de cambios

## Cuándo usar pilas

**Usa pilas cuando:**
- El último elemento debe procesarse primero
- Necesitas deshacer acciones
- Implementas recursión manualmente
- Validas estructuras anidadas (paréntesis, etiquetas HTML)

**No uses pilas cuando:**
- El primer elemento debe procesarse primero (usa colas)
- Necesitas acceso aleatorio a elementos
- No importa el orden de procesamiento

Las pilas son fundamentales en programación y el sistema las usa internamente para manejar llamadas a funciones.