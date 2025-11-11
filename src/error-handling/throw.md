# Throw (Lanzar excepciones)

La cláusula `lanzar` se utiliza para lanzar una excepción en un programa. Una excepción es un objeto que representa un error o una condición inesperada. Al lanzar una excepción, se interrumpe el flujo normal del programa y se transfiere el control a un bloque `capturar` que maneja la excepción.

## Sintaxis básica

```/dev/null/pseudocode.txt#L1-3
lanzar nuevo Error("Mensaje de error")
```

## Ejemplo

```/dev/null/pseudocode.txt#L1-25
función dividir(a : Entero, b : Entero) -> Entero
    si b = 0 entonces
        lanzar nuevo Error("No se puede dividir por cero")
    fin si

    retornar a / b
fin función

función validarEdad(edad : Entero)
    si edad < 0 entonces
        lanzar nuevo Error("La edad no puede ser negativa")
    fin si

    si edad > 150 entonces
        lanzar nuevo Error("La edad no es válida")
    fin si
fin función

// Uso
intentar
    resultado : Entero ← dividir(10, 0)
    mostrar("Resultado: ", resultado)
capturar error como excepción
    mostrar("Error: ", excepción.mensaje)
fin intentar
```

## Relanzar excepciones

A veces es necesario capturar una excepción, realizar alguna acción, y luego relanzarla:

```/dev/null/pseudocode.txt#L1-14
función procesarArchivo(nombreArchivo : Texto)
    intentar
        archivo : Archivo ← abrirArchivo(nombreArchivo)
        // Procesar archivo...
    capturar error como excepción
        registrarEnLog("Error al procesar: " + nombreArchivo)
        lanzar excepción  // Relanzar la misma excepción
    fin intentar
fin función

intentar
    procesarArchivo("datos.txt")
capturar error
    mostrar("No se pudo procesar el archivo")
fin intentar
```

## Notas importantes

- Usar excepciones para condiciones **excepcionales**, no para flujo de control normal
- Siempre proporcionar mensajes de error informativos
- Las excepciones deben representar errores, no resultados normales
- Lanzar excepciones tiene un costo de rendimiento, úselas apropiadamente
