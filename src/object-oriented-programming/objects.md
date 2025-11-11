# Objetos

Los objetos son una de las características más importantes de la programación orientada a objetos (POO). Un objeto es una entidad que combina datos (atributos) y comportamientos (métodos), y se puede considerar como una representación de algún elemento del mundo real.

## Concepto

Un objeto es una instancia de una clase que encapsula datos y funcionalidad. Cada objeto tiene:
- **Estado**: Representado por sus atributos o propiedades
- **Comportamiento**: Definido por sus métodos o funciones
- **Identidad**: Cada objeto es único, incluso si tiene los mismos valores

## Clases y objetos

Una **clase** es como un molde o plantilla que define la estructura y el comportamiento de los objetos. Un **objeto** es una instancia específica de esa clase.

```/dev/null/pseudocode.txt#L1-22
clase Persona
    // Atributos (estado)
    nombre : Texto
    edad : Entero

    // Constructor
    función constructor(nombre : Texto, edad : Entero)
        este.nombre ← nombre
        este.edad ← edad
    fin función

    // Métodos (comportamiento)
    función presentarse()
        mostrar("Hola, mi nombre es ", nombre, " y tengo ", edad, " años")
    fin función

    función cumplirAños()
        edad ← edad + 1
        mostrar("¡Feliz cumpleaños! Ahora tengo ", edad, " años")
    fin función
fin clase
```

## Crear objetos

Para usar una clase, primero debemos crear un objeto (instanciar la clase):

```/dev/null/pseudocode.txt#L1-10
// Crear objetos de la clase Persona
persona1 : Persona ← nueva Persona("Juan", 30)
persona2 : Persona ← nueva Persona("María", 25)

// Usar los objetos
persona1.presentarse()  // "Hola, mi nombre es Juan y tengo 30 años"
persona2.presentarse()  // "Hola, mi nombre es María y tengo 25 años"

persona1.cumplirAños()  // "¡Feliz cumpleaños! Ahora tengo 31 años"
```

## Ejemplo

```/dev/null/pseudocode.txt#L1-32
clase CuentaBancaria
    privado saldo : Decimal
    titular : Texto

    función constructor(titular : Texto)
        este.titular ← titular
        este.saldo ← 0.0
    fin función

    función depositar(monto : Decimal)
        si monto > 0 entonces
            saldo ← saldo + monto
            mostrar("Depósito exitoso. Saldo: $", saldo)
        fin si
    fin función

    función retirar(monto : Decimal)
        si monto > saldo entonces
            mostrar("Error: Saldo insuficiente")
        sino
            saldo ← saldo - monto
            mostrar("Retiro exitoso. Saldo: $", saldo)
        fin si
    fin función

    función obtenerSaldo() -> Decimal
        retornar saldo
    fin función
fin clase

cuenta : CuentaBancaria ← nueva CuentaBancaria("Pedro García")
cuenta.depositar(1000.0)
cuenta.retirar(300.0)
mostrar("Saldo actual: $", cuenta.obtenerSaldo())
```

## Notas importantes

- Un objeto es una instancia específica de una clase
- Cada objeto tiene su propio estado (valores de atributos)
- Los métodos definen el comportamiento de los objetos
- Los constructores inicializan los objetos cuando se crean
- La palabra clave `este` se refiere al objeto actual dentro de los métodos
