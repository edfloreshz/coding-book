# Listas enlazadas

Las listas enlazadas son una estructura de datos lineal en la que cada elemento (nodo) contiene un valor y una referencia (enlace) al siguiente elemento en la secuencia. A diferencia de los arreglos, los elementos no están almacenados en posiciones contiguas de memoria.

## Concepto

Una lista enlazada consiste en nodos conectados, donde cada nodo tiene:
- **Dato**: El valor almacenado
- **Siguiente**: Referencia al siguiente nodo

```/dev/null/pseudocode.txt#L1-7
clase Nodo
    dato : TipoDato
    siguiente : Nodo
    
    función constructor(valor : TipoDato)
        este.dato ← valor
        este.siguiente ← nulo
    fin función
fin clase
```

## Implementación básica

```/dev/null/pseudocode.txt#L1-47
clase ListaEnlazada
    cabeza : Nodo
    tamaño : Entero
    
    función constructor()
        cabeza ← nulo
        tamaño ← 0
    fin función
    
    // Agregar al inicio
    función agregarAlInicio(valor : TipoDato)
        nuevoNodo : Nodo ← nuevo Nodo(valor)
        nuevoNodo.siguiente ← cabeza
        cabeza ← nuevoNodo
        tamaño ← tamaño + 1
    fin función
    
    // Agregar al final
    función agregarAlFinal(valor : TipoDato)
        nuevoNodo : Nodo ← nuevo Nodo(valor)
        
        si cabeza = nulo entonces
            cabeza ← nuevoNodo
        sino
            actual : Nodo ← cabeza
            mientras actual.siguiente ≠ nulo hacer
                actual ← actual.siguiente
            fin mientras
            actual.siguiente ← nuevoNodo
        fin si
        
        tamaño ← tamaño + 1
    fin función
    
    // Eliminar elemento
    función eliminar(valor : TipoDato) -> Booleano
        si cabeza = nulo entonces
            retornar falso
        fin si
        
        si cabeza.dato = valor entonces
            cabeza ← cabeza.siguiente
            tamaño ← tamaño - 1
            retornar verdadero
        fin si
        
        actual : Nodo ← cabeza
        mientras actual.siguiente ≠ nulo hacer
            si actual.siguiente.dato = valor entonces
                actual.siguiente ← actual.siguiente.siguiente
                tamaño ← tamaño - 1
                retornar verdadero
            fin si
            actual ← actual.siguiente
        fin mientras
        
        retornar falso
    fin función
    
    // Mostrar todos los elementos
    función mostrarLista()
        actual : Nodo ← cabeza
        mientras actual ≠ nulo hacer
            mostrar(actual.dato, " -> ")
            actual ← actual.siguiente
        fin mientras
        mostrar("nulo")
    fin función
fin clase
```

## Ejemplo de uso

```/dev/null/pseudocode.txt#L1-13
lista : ListaEnlazada ← nueva ListaEnlazada()

lista.agregarAlInicio(3)  // [3] -> nulo
lista.agregarAlInicio(2)  // [2] -> [3] -> nulo
lista.agregarAlInicio(1)  // [1] -> [2] -> [3] -> nulo
lista.agregarAlFinal(4)   // [1] -> [2] -> [3] -> [4] -> nulo

lista.mostrarLista()  // 1 -> 2 -> 3 -> 4 -> nulo

lista.eliminar(2)     // [1] -> [3] -> [4] -> nulo

lista.mostrarLista()  // 1 -> 3 -> 4 -> nulo
```

## Ventajas y desventajas

**Ventajas:**
- Tamaño dinámico
- Inserción/eliminación eficiente al inicio: O(1)
- No requiere memoria contigua

**Desventajas:**
- Acceso secuencial: O(n) para acceder a un elemento
- Memoria extra para almacenar referencias
- No permite acceso directo por índice

## Notas importantes

- Ideal cuando se requieren muchas inserciones/eliminaciones
- No eficiente para acceso aleatorio frecuente
- Siempre validar que los punteros no sean nulos
- El primer nodo se llama "cabeza" de la lista