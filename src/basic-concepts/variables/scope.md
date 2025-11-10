# Alcance

El alcance de una variable es la región del programa en la que la variable es accesible. En la mayoría de los lenguajes de programación, el alcance de una variable está determinado por el bloque de código en el que se declara la variable.

Por ejemplo, en el siguiente código, la variable `x` solo es accesible dentro del bloque de código que comienza con `{` y termina con `}`:

```pseudocode
inicio_bloque
    variable x : entero ← 10
    mostrar(x)  // 10
fin_bloque
mostrar(x)  // Error: 'x' no existe fuera de su alcance
```

En este caso, la variable `x` tiene un alcance local, lo que significa que solo es accesible dentro del bloque de código en el que se declara.

## Alcance global

En contraste, una variable con alcance global es accesible desde cualquier parte del programa. Por ejemplo, en el siguiente código, la variable `y` se declara fuera de cualquier bloque de código y, por lo tanto, tiene un alcance global:

```pseudocode
variable y : entero ← 20

inicio_bloque
    mostrar(y)  // 20 - y es accesible aquí
fin_bloque
mostrar(y)  // 20 - y sigue siendo accesible
```

En este caso, la variable `y` tiene un alcance global, lo que significa que es accesible desde cualquier parte del programa.
