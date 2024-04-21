# Caracteres

Los caracteres son un tipo de dato que representa un solo carácter alfanumérico. En la mayoría de los lenguajes de programación, los caracteres se representan con comillas simples (`'`) y se pueden almacenar en variables de tipo `char`.

## Codificación de caracteres

Los caracteres se almacenan en la memoria de la computadora como números enteros. Cada carácter tiene un valor numérico asociado, que se determina mediante un sistema de codificación de caracteres. Uno de los sistemas de codificación de caracteres más comunes es ASCII (American Standard Code for Information Interchange), que asigna un número entero a cada carácter imprimible en inglés.

Por ejemplo, el carácter `'A'` se representa con el número entero `65` en ASCII. Los caracteres numéricos `'0'` al `'9'` se representan con los números enteros `48` al `57`, respectivamente.

## ASCII

[Tabla de caracteres](http://www.csc.villanova.edu/~tway/resources/ascii-table.html)

El ASCII es, básicamente, un código de caracteres que tiene su base en el alfabeto romano o latino. Esto quiere decir que el ASCII sirve para convertir, a través de una serie de reglas, un carácter que forma parte de un lenguaje natural (como una letra de un alfabeto) en un símbolo que pertenece a otra clase de sistema representativo.

Aunque no es la única manera, una de las representaciones mas utilizadas es `UTF-8`, dado a su flexibilidad y capacidad para mostrar mas caracteres que `ASCII`.

## UTF-8

[Tabla de caracteres](https://www.ssec.wisc.edu/~tomw/java/unicode.html)

UTF-8 es un formato de codificación de caracteres `Unicode` que ha revolucionado el mundo digital. Es el responsable de que tu navegador o tu cliente de correo te muestre el contenido del texto correctamente decodificado, sin errores ni caracteres extraños.

## Caracteres de escape

Algunos caracteres tienen un significado especial en los lenguajes de programación y no se pueden representar directamente en una cadena de texto. Estos caracteres se denominan "caracteres de escape" y se representan con una barra invertida (`\`) seguida de un carácter especial. Algunos de los caracteres de escape más comunes son:

- `\n`: Salto de línea.
- `\t`: Tabulación.
- `\'`: Comilla simple.
- `\"`: Comilla doble.
- `\\`: Barra invertida.
- `\0`: Carácter nulo.
- `\r`: Retorno de carro.

## Conclusión

Los caracteres son un tipo de dato fundamental en la programación que se utiliza para representar caracteres alfanuméricos y especiales. Los caracteres se almacenan en la memoria de la computadora como números enteros y se pueden representar en los lenguajes de programación mediante comillas simples. Los caracteres de escape y especiales permiten representar caracteres no imprimibles y Unicode en las cadenas de texto.