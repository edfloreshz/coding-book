# Primeros algoritmos

Los primeros algoritmos fueron desarrollados por los matemáticos de la antigüedad, quienes los utilizaban para resolver problemas de matemáticas y astronomía. Uno de los primeros algoritmos conocidos es el algoritmo de Euclides, que se utiliza para encontrar el máximo común divisor de dos números enteros. Otro algoritmo famoso es el algoritmo de la criba de Eratóstenes, que se utiliza para encontrar todos los números primos menores que un número dado.

Con el tiempo, los algoritmos se han vuelto más complejos y se utilizan en una amplia variedad de campos, como la informática, la inteligencia artificial, la criptografía y la bioinformática. Los algoritmos son la base de la programación y son utilizados para resolver una amplia variedad de problemas en la vida cotidiana.

## Algoritmo de Euclides

El algoritmo de Euclides es un algoritmo que se utiliza para encontrar el máximo común divisor de dos números enteros. El máximo común divisor de dos números es el número más grande que divide a ambos números sin dejar un residuo.

El algoritmo de Euclides se basa en el principio de que el máximo común divisor de dos números es el mismo que el máximo común divisor del divisor y el residuo de la división de los dos números. El algoritmo se puede expresar de la siguiente manera:

1. Si `b` es igual a `0`, entonces el máximo común divisor es `a`.
2. De lo contrario, el máximo común divisor es el máximo común divisor de `b` y `a % b`.
3. Repetir el paso 2 hasta que `b` sea igual a `0`.
4. El máximo común divisor es el valor de `a`.
5. Fin.

## Algoritmo de la criba de Eratóstenes

El algoritmo de la criba de Eratóstenes es un algoritmo que se utiliza para encontrar todos los números primos menores que un número dado. Un número primo es un número entero mayor que `1` que solo es divisible por `1` y por sí mismo.

El algoritmo de la criba de Eratóstenes se basa en el principio de eliminar los múltiplos de los números primos conocidos para encontrar los números primos restantes. El algoritmo se puede expresar de la siguiente manera:

1. Crear una lista de números del `2` al número dado.
2. Inicializar un puntero en el primer número de la lista (`2`).
3. Eliminar todos los múltiplos del número apuntado por el puntero.
4. Mover el puntero al siguiente número de la lista.
5. Repetir los pasos 3 y 4 hasta que el cuadrado del número apuntado sea mayor que el número dado.
6. Los números restantes en la lista son los números primos menores que el número dado.
7. Fin.
