# Declaración

La declaración de una variable es la acción de reservar un espacio en memoria para almacenar un valor. En la mayoría de los lenguajes de programación, la declaración de una variable se compone de dos partes: el tipo de dato y el nombre de la variable.

```pseudocode
variable edad : entero
```

En el ejemplo anterior, se declara una variable de tipo entero llamada `edad`. El tipo de dato `entero` indica que la variable almacenará un número entero.

## Declaración con inicialización

También podemos declarar una variable y asignarle un valor inicial al mismo tiempo:

```pseudocode
variable edad : entero ← 25
```

En este caso, la variable `edad` se declara e inicializa con el valor `25` en una sola línea.

## Ejemplos con diferentes tipos

```pseudocode
variable nombre : texto ← "María"
variable precio : decimal ← 19.99
variable activo : booleano ← verdadero
variable inicial : carácter ← 'A'
```

> **Nota:** En algunos lenguajes de programación, el tipo de dato se infiere automáticamente a partir del valor asignado, mientras que en otros es necesario especificarlo explícitamente. El pseudocódigo de este libro usa tipado explícito para mayor claridad.