# Identificadores

Un identificador es un nombre que se le asigna a una variable, constante, función, clase, módulo, paquete, etc. en un programa de computadora. Los identificadores son utilizados para referenciar a estos elementos en el código fuente.

## Reglas para identificadores
- Los identificadores pueden contener letras, dígitos y guiones bajos (`_`).
- Los identificadores deben comenzar con una letra o un guion bajo (`_`).
- Los identificadores no pueden contener espacios en blanco ni caracteres especiales, como signos de puntuación.
- Los identificadores distinguen entre mayúsculas y minúsculas.
- Los identificadores no pueden ser palabras reservadas del lenguaje de programación que se esté utilizando.

## Ejemplo

```pseudocode
variable miVariable : entero ← 10
constante MI_CONSTANTE : entero ← 20

función miFuncion()
    mostrar(miVariable)
fin función

clase MiClase
    atributo miAtributo : entero
fin clase
```

En este ejemplo:
- `miVariable` es un identificador para una variable
- `MI_CONSTANTE` es un identificador para una constante (normalmente en mayúsculas)
- `miFuncion` es un identificador para una función
- `MiClase` es un identificador para una clase
- `miAtributo` es un identificador para un atributo de clase

## Convenciones comunes

Aunque los lenguajes varían, estas convenciones son ampliamente aceptadas:

- **Variables y funciones**: `camelCase` o `snake_case` (ejemplos: `miVariable`, `mi_variable`)
- **Constantes**: `MAYÚSCULAS_CON_GUIONES` (ejemplo: `MI_CONSTANTE`)
- **Clases**: `PascalCase` (ejemplo: `MiClase`)
- **Descriptivos**: Usa nombres que describan el propósito (`edad` en lugar de `e`)

Los identificadores son una parte fundamental de la programación y se utilizan para nombrar y referenciar elementos en un programa de computadora.
