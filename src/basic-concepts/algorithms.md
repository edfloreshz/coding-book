# Algoritmos

Un algoritmo es una secuencia finita y ordenada de pasos que resuelve un problema o ejecuta una tarea. Cada paso debe ser claro, no ambiguo y ejecutable en un tiempo finito.

## Propiedades clave

- Corrección: produce resultados esperados para entradas válidas.
- Finitud: siempre termina tras un número finito de pasos.
- Determinismo: cada paso está definido sin ambigüedad.
- Eficiencia: usa razonablemente tiempo y memoria.

## Representaciones comunes

- Pseudocódigo
- Diagramas de flujo
- Lenguajes de programación

## Ejemplo en pseudocódigo: encontrar el máximo en una lista

```
entrada: lista de números L no vacía
maximo ← L[0]
para i desde 1 hasta longitud(L) - 1 hacer
    si L[i] > maximo entonces
        maximo ← L[i]
    fin si
fin para
salida: maximo
```

## Complejidad

La eficiencia de un algoritmo suele analizarse con notación O grande:

- Tiempo: cómo crece el número de operaciones con el tamaño de entrada n.
- Espacio: memoria adicional necesaria además de la entrada.

Ejemplo: el algoritmo anterior recorre la lista una vez → tiempo O(n) y espacio O(1).


