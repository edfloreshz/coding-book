# Arreglos

Un arreglo es una estructura de datos que permite almacenar un conjunto de elementos del mismo tipo. Al declarar un arreglo, se debe indicar su tamaño, y en ese momento se reserva la memoria necesaria para almacenar los datos solicitados por el programador.

## Indices

Cuando un arreglo almacena algo, le otorga un indice numérico. Por ejemplo, un arreglo de nombres con 6 elementos se vería así: 

| 0 | 1 | 2 | 3 | 4 | 5 |
| --- | --- | --- | --- | --- | --- |
| Javier | Rodrigo | Luisa | Andrea | Patricio | Maria |

Note como los indices solo llegan hasta `5`, aun que el arreglo tiene `6` elementos, esto es debido a que los indices de un arreglo comienzan desde `0` e incrementan conforme el arreglo crece.

# Tipos de arreglos

## Unidimensionales

Podemos visualizar a un arreglo unidimensional como una lista de objetos.

| 0 | 1 | 2 | 3 | 4 | 5 |
| --- | --- | --- | --- | --- | --- |
| Javier | Rodrigo | Luisa | Andrea | Patricio | Maria |

## Bidimensionales

Un arreglo bidimensional consta de un arreglo que contiene arreglos dentro del mismo, algo así como una lista de listas.

| Indices | 0 | 1 | 2 | 3 | 4 |
| --- | --- | --- | --- | --- | --- |
| 0 | Javier | Rodrigo | Luisa | Andrea | Patricio |
| 1 | Pedro | Juanita | Eduardo | Claudia | Clara |
| 2 | Ángel | Alberto | Andrés | Alonso | Francisco |
| 3 | Fernando | Gabriel | Héctor | Oliver | León |
| 4 | Lucas | Joel | Gael | Dylan | Dante |

Para comprender mejor como funciona, establezcamos que la primera fila de números son los indices del primer arreglo, después, la columna de indices equivaldrían a los indices de los arreglos contenidos en cada una de las posiciones del primer arreglo, por lo tanto si tenemos un arreglo de 5 posiciones, contendría 5 arreglos dentro del mismo, cada uno con 5 posiciones.