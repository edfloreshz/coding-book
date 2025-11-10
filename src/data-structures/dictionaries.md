# Diccionarios

Los diccionarios (también llamados mapas o tablas hash) son estructuras de datos que almacenan pares clave-valor. Permiten acceder a los valores de manera eficiente usando claves únicas, similar a cómo usarías un diccionario real para buscar definiciones por palabras.

## ¿Qué son los diccionarios?

Un diccionario es una colección de pares clave-valor donde:
- Cada **clave** es única
- Cada clave está asociada a un **valor**
- El acceso a valores por clave es muy rápido
- Las claves pueden ser de cualquier tipo (texto, números, etc.)
- Los valores pueden ser de cualquier tipo

## Diferencias con otras estructuras

| Característica | Arreglo/Lista | Diccionario |
|----------------|---------------|-------------|
| Acceso | Por índice numérico | Por clave única |
| Orden | Secuencial | No garantizado |
| Búsqueda | Lenta (O(n)) | Rápida (O(1)) |
| Claves | Solo números | Cualquier tipo |

## Operaciones con diccionarios

Los diccionarios almacenan pares de clave-valor para buscar información rápidamente.

### Ejemplo

```pseudocode
// Crear un diccionario de edades
diccionario edades : texto -> entero

// Agregar elementos (clave → valor)
edades["Ana"] ← 25
edades["Carlos"] ← 30
edades["María"] ← 28

// Ver la edad de una persona
variable edadAna : entero ← edades["Ana"]
mostrar(edadAna)  // 25

// Cambiar un valor
edades["Ana"] ← 26
mostrar(edades["Ana"])  // 26

// Verificar si existe una clave
variable existeCarlos : booleano ← edades.contieneClave("Carlos")
mostrar(existeCarlos)  // verdadero

// Recorrer el diccionario
para cada nombre en edades.claves() hacer
    variable edad : entero ← edades[nombre]
    mostrar(nombre + " tiene " + convertirATexto(edad) + " años")
fin para

// Eliminar un elemento
edades.eliminar("Carlos")
mostrar("Personas: " + convertirATexto(edades.tamaño()))  // 2
```

## Operaciones comunes

- **Agregar/Modificar**: `diccionario[clave] ← valor`
- **Acceder**: `valor ← diccionario[clave]`
- **Eliminar**: `diccionario.eliminar(clave)`
- **Verificar existencia**: `diccionario.contieneClave(clave)`
- **Obtener claves**: `diccionario.claves()`
- **Obtener valores**: `diccionario.valores()`
- **Tamaño**: `diccionario.tamaño()`
- **Limpiar**: `diccionario.limpiar()`

## Buenas prácticas

1. **Verifica si la clave existe antes de acceder** - evita errores al buscar claves inexistentes
2. **Usa nombres descriptivos para claves** - facilita la comprensión del código
3. **Mantén tipos consistentes** - todas las claves del mismo tipo, todos los valores del mismo tipo
4. **Usa diccionarios para búsquedas rápidas** - mucho más eficiente que buscar en listas
5. **Considera el tamaño** - los diccionarios usan más memoria que las listas

## Cuándo usar diccionarios

**Usa diccionarios cuando:**
- Necesitas asociar datos (claves con valores)
- Requieres búsquedas rápidas por identificador
- Las claves tienen significado semántico (nombres, IDs, códigos)
- Necesitas mapear relaciones uno a uno

**Usa listas/arreglos cuando:**
- El orden de elementos es importante
- Accedes principalmente por posición numérica
- No necesitas claves únicas
- Quieres ahorrar memoria

Los diccionarios son extremadamente útiles para almacenar datos relacionados, implementar cachés, contar frecuencias y crear índices eficientes.