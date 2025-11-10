# Colas

Las colas (queues) son estructuras de datos que siguen el principio **FIFO** (First In, First Out - Primero en Entrar, Primero en Salir). Son como una fila de personas: el primero que llega es el primero en ser atendido.

## ¿Qué son las colas?

Una cola es una colección donde:
- Los elementos se agregan al final
- Los elementos se sacan del frente
- El primero en entrar es el primero en salir

## Visualización

```
    ┌──────┬─────────┬────────┐
    │ Ana  │ Carlos  │ María  │
    └──────┴─────────┴────────┘
      ↑                    ↑
    Frente              Final
    (sale primero)   (entra último)
```

## Ejemplo

```pseudocode
// Crear una cola vacía
cola fila : texto

// Agregar personas a la fila (encolar)
fila.encolar("Ana")
fila.encolar("Carlos")
fila.encolar("María")

// Ahora la fila es: Ana → Carlos → María

// Ver quién está al frente (sin sacarlo)
variable siguiente : texto ← fila.frente()
mostrar(siguiente)  // "Ana"

// Atender a la primera persona (desencolar)
variable atendido : texto ← fila.desencolar()
mostrar(atendido)  // "Ana"

// Ahora la fila es: Carlos → María

// Atender al siguiente
atendido ← fila.desencolar()
mostrar(atendido)  // "Carlos"

// Ahora la fila es: María

// Ver cuántas personas quedan
variable cantidad : entero ← fila.tamaño()
mostrar(cantidad)  // 1

// Verificar si la cola está vacía
variable vacia : booleano ← fila.estaVacia()
mostrar(vacia)  // falso
```

## Operaciones principales

- **`encolar(elemento)`** - Agregar al final de la cola
- **`desencolar()`** - Sacar y retornar el elemento del frente
- **`frente()`** - Ver el elemento del frente sin sacarlo
- **`tamaño()`** - Ver cuántos elementos hay
- **`estaVacia()`** - Verificar si la cola está vacía

## Usos comunes

Las colas se usan para:
- **Filas de espera** - Turnos en un banco, cafetería, etc.
- **Impresión** - Cola de documentos para imprimir
- **Procesamiento de tareas** - Procesar trabajos en orden
- **Mensajes** - Enviar mensajes en el orden que llegan

## Diferencia con pilas

| Característica | Cola (FIFO) | Pila (LIFO) |
|----------------|-------------|-------------|
| Orden | Primero en entrar, primero en salir | Último en entrar, primero en salir |
| Analogía | Fila de personas | Pila de platos |
| Agregar | Al final | Arriba |
| Sacar | Del frente | De arriba |

## Buenas prácticas

1. **Verifica si está vacía antes de desencolar** - evita errores
2. **Usa nombres descriptivos** - `colaTareas` en lugar de `q`
3. **Respeta el orden FIFO** - no accedas a elementos del medio
4. **Usa colas para procesamiento ordenado** - cuando el orden importa

## Cuándo usar colas

**Usa colas cuando:**
- Necesitas procesar elementos en orden de llegada
- Implementas sistemas de turnos o espera
- Gestionas tareas que deben ejecutarse en secuencia
- El orden de procesamiento es importante

**No uses colas cuando:**
- Necesitas acceso aleatorio a elementos
- El último elemento debe procesarse primero (usa pilas)
- No importa el orden de procesamiento

Las colas son fundamentales en programación y se usan en muchos sistemas donde el orden de llegada debe respetarse.
