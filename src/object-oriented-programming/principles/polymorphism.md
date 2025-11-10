# Polimorfismo

El polimorfismo permite que objetos de diferentes clases sean tratados de manera uniforme a través de una interfaz común. La palabra "polimorfismo" significa "muchas formas".

## Concepto

El polimorfismo permite que diferentes objetos respondan de manera diferente al mismo mensaje o método, facilitando escribir código que funcione con diferentes tipos de objetos sin necesidad de conocer sus tipos específicos.

## Ejemplo

```/dev/null/pseudocode.txt#L1-45
clase Animal
    nombre : Cadena
    
    función constructor(nombre : Cadena)
        este.nombre ← nombre
    fin función
    
    función hacerSonido()
        mostrar("El animal hace un sonido")
    fin función
fin clase

clase Perro hereda de Animal
    función constructor(nombre : Cadena)
        super(nombre)
    fin función
    
    función hacerSonido()
        mostrar(nombre, " dice: ¡Guau!")
    fin función
fin clase

clase Gato hereda de Animal
    función constructor(nombre : Cadena)
        super(nombre)
    fin función
    
    función hacerSonido()
        mostrar(nombre, " dice: ¡Miau!")
    fin función
fin clase

// Polimorfismo: la misma variable puede contener diferentes tipos
animales : Lista<Animal> ← nueva Lista<Animal>()
animales.agregar(nuevo Perro("Rex"))
animales.agregar(nuevo Gato("Misi"))
animales.agregar(nuevo Perro("Max"))

// El método correcto se llama según el tipo real del objeto
para cada animal en animales hacer
    animal.hacerSonido()
fin para

// Salida:
// Rex dice: ¡Guau!
// Misi dice: ¡Miau!
// Max dice: ¡Guau!
```

## Ventajas del polimorfismo

1. **Código más flexible**: Funciona con diferentes tipos sin modificar el código
2. **Extensibilidad**: Fácil agregar nuevos tipos sin cambiar código existente
3. **Abstracción**: Trabajar con conceptos generales sin preocuparse por detalles
4. **Reutilización**: El mismo código funciona con múltiples tipos

## Notas importantes

- El polimorfismo permite tratar objetos de diferentes clases de forma uniforme
- El tipo en tiempo de ejecución determina qué método se ejecuta
- Facilita agregar nuevos tipos sin modificar código existente
- Se basa en herencia o interfaces