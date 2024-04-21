# Constantes

Una constante es un valor que no cambia durante la ejecución de un programa. En la mayoría de los lenguajes de programación, las constantes se declaran con una palabra clave especial, como `const` o `final`, y se les asigna un valor que no puede ser modificado posteriormente.

Las constantes son útiles para almacenar valores que no deben cambiar durante la ejecución de un programa, como el valor de Pi o la dirección de memoria de un dispositivo de hardware.

## Declaración

```java
final double PI = 3.14159;
```

En el ejemplo anterior, se declara una constante de tipo `double` llamada `PI` con un valor de `3.14159`. La palabra clave `final` se utiliza en Java para indicar que la variable es una constante y su valor no puede ser modificado.

En algunos lenguajes de programación, como JavaScript, las constantes se declaran con la palabra clave `const` en lugar de `final`.

```javascript
const PI = 3.14159;
```

En este caso, se declara una constante llamada `PI` con un valor de `3.14159`. La palabra clave `const` se utiliza en JavaScript para indicar que la variable es una constante y su valor no puede ser modificado.

## Ventajas
- **Claridad**: Al utilizar constantes, se facilita la comprensión del código y se evitan errores causados por la modificación accidental de valores.
- **Reutilización**: Las constantes pueden ser utilizadas en múltiples partes de un programa sin necesidad de redefinirlas.
- **Optimización**: Al declarar una constante, el compilador puede realizar optimizaciones que mejoren el rendimiento del programa.
- **Mantenimiento**: Al centralizar los valores constantes en un solo lugar, se facilita el mantenimiento y la actualización de los mismos.
- **Seguridad**: Las constantes garantizan que ciertos valores críticos no sean modificados accidentalmente, lo que puede provocar errores en el programa.