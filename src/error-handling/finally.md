# Finally

La cláusula `finally` es utilizada en conjunto con `intentar` y `capturar` para manejar excepciones en un programa. El bloque de código dentro de la cláusula `finally` se ejecutará siempre, sin importar si se lanzó una excepción o no.

## Concepto

El bloque `finally` garantiza que cierto código se ejecute sin importar qué suceda en los bloques `intentar` y `capturar`. Esto es especialmente útil para liberar recursos, cerrar archivos, o limpiar conexiones.

## Sintaxis básica

```/dev/null/pseudocode.txt#L1-11
intentar
    // Código que puede lanzar una excepción
capturar excepción
    // Código que maneja la excepción
finalmente
    // Código que se ejecuta SIEMPRE
fin intentar
```

## Ejemplo

```/dev/null/pseudocode.txt#L1-22
archivo : Archivo ← nulo

intentar
    archivo ← abrirArchivo("datos.txt", ModoLectura)
    contenido : Texto ← archivo.leerTodo()
    mostrar("Contenido: ", contenido)

    // Procesar el archivo...

capturar ArchivoNoEncontradoError como error
    mostrar("Error: El archivo no existe")

capturar ErrorDeEntradaSalida como error
    mostrar("Error al leer el archivo: ", error.mensaje)

finalmente
    si archivo ≠ nulo entonces
        archivo.cerrar()
        mostrar("Archivo cerrado correctamente")
    fin si
fin intentar

// El archivo SIEMPRE se cierra, haya o no error
```

## Orden de ejecución

El orden de ejecución es siempre:

1. Bloque `intentar`
2. Si hay error: bloque `capturar` correspondiente
3. Bloque `finalmente` (SIEMPRE)

```/dev/null/pseudocode.txt#L1-14
intentar
    mostrar("1. Ejecutando intentar")
    resultado : Entero ← 10 / 2
    mostrar("2. Resultado: ", resultado)

capturar error
    mostrar("Este no se ejecuta (no hay error)")

finalmente
    mostrar("3. Ejecutando finalmente")
fin intentar

// Salida: 1, 2, 3
```

## Notas importantes

- El bloque `finalmente` se ejecuta **siempre**, haya o no excepción
- Ideal para liberar recursos y limpieza
- Se ejecuta antes de retornar de una función
- No usar para alterar el flujo de control (return, throw)
