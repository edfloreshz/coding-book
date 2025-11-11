# Cadenas de texto

Las cadenas de texto (strings) son uno de los tipos de datos más utilizados en programación. Representan secuencias de caracteres y se usan para almacenar y manipular texto.

## ¿Qué son las cadenas de texto?

Una cadena de texto es una secuencia de caracteres que puede incluir letras, números, símbolos y espacios. Ejemplos: "Hola", "123", "usuario@email.com", "¡Hola, mundo!"

## Características principales

- **Longitud variable**: Pueden contener desde cero caracteres (cadena vacía) hasta miles
- **Inmutables**: En muchos lenguajes, no se pueden modificar directamente (se crean nuevas cadenas)
- **Secuenciales**: Los caracteres tienen un orden y posición específica
- **Versátiles**: Pueden contener cualquier carácter Unicode

## Operaciones con cadenas

Las cadenas permiten almacenar y manipular texto.

### Ejemplo

```pseudocode
// Crear una cadena de texto
variable nombre : Texto ← "María"
variable apellido : Texto ← "López"

// Unir cadenas (concatenación)
variable nombreCompleto : Texto ← nombre + " " + apellido
mostrar(nombreCompleto)  // "María López"

// Ver cuántos caracteres tiene
variable cantidad : entero ← longitud(nombre)
mostrar(cantidad)  // 5

// Convertir a mayúsculas
variable enMayusculas : texto ← aMayusculas(nombre)
mostrar(enMayusculas)  // "MARÍA"

// Crear un mensaje
variable edad : entero ← 20
variable mensaje : texto ← nombre + " tiene " + convertirATexto(edad) + " años"
mostrar(mensaje)  // "María tiene 20 años"
```

## Caracteres especiales

Las cadenas pueden contener caracteres especiales usando secuencias de escape:

- `\n` - Nueva línea
- `\t` - Tabulación
- `\"` - Comillas dobles
- `\\` - Barra invertida

## Buenas prácticas

1. **Verifica valores nulos o vacíos antes de operar**
2. **Usa constantes para cadenas repetidas**
3. **Evita concatenación excesiva en ciclos** - usa arrays y únelos al final
4. **Normaliza entradas del usuario** - elimina espacios y convierte a minúsculas
5. **Usa nombres descriptivos** para variables de texto

## Limitaciones comunes

- Las cadenas pueden consumir mucha memoria si son muy largas
- Las operaciones de búsqueda y reemplazo pueden ser lentas en cadenas grandes
- En algunos lenguajes, las cadenas son inmutables (cada operación crea una nueva cadena)
- La comparación es sensible a mayúsculas por defecto

Las cadenas de texto son fundamentales en la programación y se utilizan para mostrar mensajes, procesar datos de usuario, manipular archivos de texto y mucho más.
