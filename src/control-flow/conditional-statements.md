# Declaraciones condicionales

Las declaraciones condicionales permiten ejecutar bloques de código basados en condiciones específicas. En la mayoría de los lenguajes de programación, las declaraciones condicionales se realizan utilizando la estructura `if-else`.

## Estructura básica


La estructura básica de una declaración condicional `if-else` es la siguiente:

```java
if (condición) {
    // Bloque de código si la condición es verdadera
} else {
    // Bloque de código si la condición es falsa
}
```

En este caso, si la condición es verdadera, se ejecutará el bloque de código dentro del primer par de llaves `{}`. Si la condición es falsa, se ejecutará el bloque de código dentro del segundo par de llaves `{}`.

## Ejemplo

En el siguiente ejemplo, se muestra una declaración condicional `if-else` que verifica si un número es positivo o negativo:

```java
int numero = -5;

if (numero >= 0) {
    System.out.println("El número es positivo");
} else {
    System.out.println("El número es negativo");
}
```

En este caso, si el número es mayor o igual a cero, se imprimirá "El número es positivo". De lo contrario, se imprimirá "El número es negativo".

## Anidamiento

Las declaraciones condicionales también se pueden anidar, es decir, colocar una declaración condicional dentro de otra. Esto permite realizar múltiples comprobaciones en un solo bloque de código.

```java
int numero = 10;

if (numero > 0) {
    System.out.println("El número es positivo");
} else if (numero < 0) {
    System.out.println("El número es negativo");
} else {
    System.out.println("El número es cero");
}
```

En este caso, si el número es mayor que cero, se imprimirá "El número es positivo". Si el número es menor que cero, se imprimirá "El número es negativo". De lo contrario, se imprimirá "El número es cero".

