# Switch

La declaración `switch` (o `según` en español) es una estructura de control de flujo que permite ejecutar diferentes bloques de código basados en el valor de una variable o expresión. Es especialmente útil cuando tienes múltiples opciones mutuamente excluyentes y deseas elegir una de ellas para ejecutar.

## Estructura básica

```pseudocode
según (variable) hacer
    caso valor1:
        // Código para valor1
        salir
    caso valor2:
        // Código para valor2
        salir
    caso valor3:
        // Código para valor3
        salir
    por defecto:
        // Código si ningún caso coincide
fin según
```

## Ejemplo básico

```pseudocode
variable opcion : entero
mostrar("Introduce una opción (1, 2 o 3):")
leer(opcion)

según (opcion) hacer
    caso 1:
        mostrar("Has elegido la opción 1")
        salir
    caso 2:
        mostrar("Has elegido la opción 2")
        salir
    caso 3:
        mostrar("Has elegido la opción 3")
        salir
    por defecto:
        mostrar("Opción inválida")
fin según
```

En este ejemplo, el programa evalúa el valor de `opcion` y ejecuta el bloque de código correspondiente. Si `opcion` es `1`, muestra "Has elegido la opción 1". Si es `2`, muestra "Has elegido la opción 2", y así sucesivamente. Si no coincide con ningún caso, ejecuta el bloque `por defecto`.

## Switch con texto

El `switch` también puede funcionar con valores de texto:

```pseudocode
variable diaSemana : texto ← "lunes"

según (diaSemana) hacer
    caso "lunes":
        mostrar("Inicio de semana")
        salir
    caso "viernes":
        mostrar("Fin de semana laboral")
        salir
    caso "sábado":
    caso "domingo":
        mostrar("Fin de semana")
        salir
    por defecto:
        mostrar("Día laboral normal")
fin según
```

## Múltiples valores para un mismo caso

Puedes agrupar múltiples valores que ejecuten el mismo código:

```pseudocode
variable mes : entero ← 3

según (mes) hacer
    caso 12:
    caso 1:
    caso 2:
        mostrar("Invierno")
        salir
    caso 3:
    caso 4:
    caso 5:
        mostrar("Primavera")
        salir
    caso 6:
    caso 7:
    caso 8:
        mostrar("Verano")
        salir
    caso 9:
    caso 10:
    caso 11:
        mostrar("Otoño")
        salir
    por defecto:
        mostrar("Mes inválido")
fin según
```

## Switch con rangos (en algunos lenguajes)

Algunos lenguajes permiten usar rangos en los casos:

```pseudocode
variable edad : entero ← 25

según (edad) hacer
    caso 0..12:
        mostrar("Niño")
        salir
    caso 13..17:
        mostrar("Adolescente")
        salir
    caso 18..64:
        mostrar("Adulto")
        salir
    caso 65..120:
        mostrar("Adulto mayor")
        salir
    por defecto:
        mostrar("Edad inválida")
fin según
```

## Ejemplo: Sistema de calificaciones

```pseudocode
variable calificacion : carácter
mostrar("Introduce tu calificación (A, B, C, D, F):")
leer(calificacion)

según (calificacion) hacer
    caso 'A':
        mostrar("Excelente - 90-100 puntos")
        mostrar("¡Felicidades!")
        salir
    caso 'B':
        mostrar("Muy bien - 80-89 puntos")
        mostrar("Buen trabajo")
        salir
    caso 'C':
        mostrar("Aceptable - 70-79 puntos")
        mostrar("Aprobado")
        salir
    caso 'D':
        mostrar("Suficiente - 60-69 puntos")
        mostrar("Necesitas mejorar")
        salir
    caso 'F':
        mostrar("Reprobado - Menos de 60 puntos")
        mostrar("Debes estudiar más")
        salir
    por defecto:
        mostrar("Calificación no reconocida")
fin según
```

## Switch vs If-Else

### Cuándo usar Switch:
- Cuando comparas una variable contra múltiples valores constantes
- Cuando los casos son mutuamente excluyentes
- Cuando quieres hacer el código más legible para múltiples opciones

### Cuándo usar If-Else:
- Cuando necesitas evaluar expresiones complejas o rangos
- Cuando las condiciones no son simples comparaciones de igualdad
- Cuando necesitas usar operadores lógicos (y, o)

```pseudocode
// Mejor con switch
según (opcionMenu) hacer
    caso 1: /* ... */ salir
    caso 2: /* ... */ salir
    caso 3: /* ... */ salir
fin según

// Mejor con if-else
si (temperatura > 30 y humedad > 70) entonces
    mostrar("Hace mucho calor y está húmedo")
sino si (temperatura < 10) entonces
    mostrar("Hace frío")
fin si
```

## Importancia del "salir" (break)

La instrucción `salir` (break) es crucial en un `switch`. Sin ella, la ejecución continuará hacia los siguientes casos (comportamiento llamado "fall-through"):

```pseudocode
// SIN salir (fall-through)
variable numero : entero ← 1

según (numero) hacer
    caso 1:
        mostrar("Uno")
        // No hay salir, continúa al siguiente caso
    caso 2:
        mostrar("Dos")
        salir
fin según

// Salida: "Uno" y "Dos"
```

## Buenas prácticas

1. **Siempre incluye un caso por defecto**: Maneja situaciones inesperadas
2. **Usa salir en cada caso**: Evita comportamientos inesperados
3. **Agrupa casos relacionados**: Cuando múltiples valores tienen la misma acción
4. **Mantén los casos simples**: Si un caso es muy complejo, considera usar una función
5. **Ordena los casos lógicamente**: Por frecuencia de uso o alfabéticamente

```pseudocode
// Buena práctica: casos ordenados y con por defecto
variable comando : texto
leer(comando)

según (comando) hacer
    caso "ayuda":
        mostrarAyuda()
        salir
    caso "guardar":
        guardarArchivo()
        salir
    caso "salir":
        cerrarPrograma()
        salir
    por defecto:
        mostrar("Comando no reconocido. Escribe 'ayuda' para ver opciones")
fin según
```

## Limitaciones

En la mayoría de los lenguajes, `switch` tiene algunas limitaciones:

- Solo funciona con valores constantes y específicos
- No permite condiciones complejas o comparaciones de rangos (excepto en lenguajes modernos)
- Los casos deben ser valores conocidos en tiempo de compilación

Para condiciones más complejas, es mejor usar declaraciones `if-else` encadenadas.
