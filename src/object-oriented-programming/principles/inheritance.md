# Herencia

La herencia es un principio fundamental de la programación orientada a objetos que permite crear una nueva clase basada en una clase existente, reutilizando su código y extendiendo su funcionalidad.

## Concepto

La herencia permite que una clase (clase derivada o hija) adquiera las propiedades y métodos de otra clase (clase base o padre). Esto crea una relación "es un" entre las clases.

## Ejemplo

```/dev/null/pseudocode.txt#L1-35
clase Animal
    nombre : Texto
    edad : Entero

    función constructor(nombre : Texto, edad : Entero)
        este.nombre ← nombre
        este.edad ← edad
    fin función

    función hacerSonido()
        mostrar("El animal hace un sonido")
    fin función

    función dormir()
        mostrar(nombre, " está durmiendo")
    fin función
fin clase

clase Perro hereda de Animal
    raza : Texto

    función constructor(nombre : Texto, edad : Entero, raza : Texto)
        super(nombre, edad)
        este.raza ← raza
    fin función

    función hacerSonido()
        mostrar(nombre, " dice: ¡Guau! ¡Guau!")
    fin función

    función perseguirPelota()
        mostrar(nombre, " está persiguiendo la pelota")
    fin función
fin clase

// Uso
perro : Perro ← nuevo Perro("Max", 3, "Labrador")
perro.hacerSonido()      // "Max dice: ¡Guau! ¡Guau!" (sobreescrito)
perro.dormir()           // "Max está durmiendo" (heredado)
perro.perseguirPelota()  // "Max está persiguiendo la pelota" (propio)
```

## Ventajas de la herencia

1. **Reutilización de código**: Evita duplicar código al compartir funcionalidad común
2. **Jerarquías de clases**: Organiza conceptos en relaciones lógicas
3. **Extensibilidad**: Fácil añadir nuevas clases derivadas
4. **Polimorfismo**: Permite tratamiento uniforme de objetos relacionados

## Notas importantes

- La clase derivada hereda atributos y métodos de la clase base
- Usar `super()` para llamar al constructor de la clase padre
- Los métodos pueden ser sobreescritos para proporcionar comportamiento específico
- La herencia crea una dependencia fuerte entre clases
- Usar herencia solo cuando hay una clara relación "es un"
