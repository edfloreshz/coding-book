# Clases

Las clases son plantillas para crear objetos. Son como moldes que definen qué propiedades y acciones tendrán los objetos.

## ¿Qué es una clase?

Una clase tiene:
- **Atributos** - Las características (como nombre, edad, color)
- **Métodos** - Las acciones que puede hacer (como caminar, hablar)
- **Constructor** - Cómo se crea el objeto

## Estructura básica

```pseudocode
clase NombreClase
    atributo propiedad : tipo
    
    constructor(parámetro : tipo)
        este.propiedad ← parámetro
    fin constructor
    
    método hacerAlgo() : tipo
        // código
    fin método
fin clase
```

## Ejemplo

```pseudocode
// Definir la clase Perro
clase Perro
    // Atributos (características)
    atributo nombre : texto
    atributo edad : entero
    atributo raza : texto
    
    // Constructor (cómo crear un perro)
    constructor(nombre : texto, edad : entero, raza : texto)
        este.nombre ← nombre
        este.edad ← edad
        este.raza ← raza
    fin constructor
    
    // Métodos (acciones que puede hacer)
    método ladrar() : nulo
        mostrar(este.nombre + " dice: ¡Guau!")
    fin método
    
    método cumplirAños() : nulo
        este.edad ← este.edad + 1
        mostrar(este.nombre + " ahora tiene " + convertirATexto(este.edad) + " años")
    fin método
    
    método presentarse() : nulo
        mostrar("Hola, soy " + este.nombre)
        mostrar("Tengo " + convertirATexto(este.edad) + " años")
        mostrar("Soy un " + este.raza)
    fin método
fin clase

// Crear objetos (instancias) de la clase Perro
variable miPerro : Perro ← nuevo Perro("Max", 3, "Labrador")
variable otroPerro : Perro ← nuevo Perro("Luna", 5, "Beagle")

// Usar los métodos
miPerro.presentarse()
// Hola, soy Max
// Tengo 3 años
// Soy un Labrador

miPerro.ladrar()  // Max dice: ¡Guau!

otroPerro.ladrar()  // Luna dice: ¡Guau!

// Acceder a atributos
mostrar(miPerro.nombre)  // Max
mostrar(otroPerro.edad)  // 5

// Modificar atributos
miPerro.cumplirAños()  // Max ahora tiene 4 años

// Otro ejemplo: Clase Coche
clase Coche
    atributo marca : texto
    atributo modelo : texto
    atributo velocidad : entero
    
    constructor(marca : texto, modelo : texto)
        este.marca ← marca
        este.modelo ← modelo
        este.velocidad ← 0
    fin constructor
    
    método acelerar() : nulo
        este.velocidad ← este.velocidad + 10
        mostrar("Velocidad: " + convertirATexto(este.velocidad) + " km/h")
    fin método
    
    método frenar() : nulo
        este.velocidad ← 0
        mostrar("El coche se ha detenido")
    fin método
    
    método mostrarInfo() : nulo
        mostrar(este.marca + " " + este.modelo)
    fin método
fin clase

// Usar la clase Coche
variable miCoche : Coche ← nuevo Coche("Toyota", "Corolla")

miCoche.mostrarInfo()  // Toyota Corolla
miCoche.acelerar()     // Velocidad: 10 km/h
miCoche.acelerar()     // Velocidad: 20 km/h
miCoche.frenar()       // El coche se ha detenido
```

## La palabra `este`

`este` se refiere al objeto actual. Se usa para diferenciar entre:
- Atributos de la clase: `este.nombre`
- Parámetros del método: `nombre`

```pseudocode
clase Persona
    atributo nombre : texto
    
    constructor(nombre : texto)
        este.nombre ← nombre  // este.nombre es el atributo
                              // nombre es el parámetro
    fin constructor
fin clase
```

## ¿Por qué usar clases?

Las clases ayudan a:
- **Organizar el código** - Agrupar datos relacionados
- **Reutilizar código** - Crear muchos objetos del mismo tipo
- **Modelar el mundo real** - Representar cosas como personas, coches, productos
- **Mantener el código** - Cambios en un solo lugar

## Diferencia entre clase y objeto

| Clase | Objeto |
|-------|--------|
| La plantilla o molde | El resultado concreto |
| Se define una vez | Se pueden crear muchos |
| Como un plano de casa | Como una casa real |

```pseudocode
// La clase es la plantilla
clase Estudiante
    atributo nombre : texto
    atributo nota : decimal
fin clase

// Los objetos son instancias concretas
variable estudiante1 : Estudiante ← nuevo Estudiante()
variable estudiante2 : Estudiante ← nuevo Estudiante()
variable estudiante3 : Estudiante ← nuevo Estudiante()
// Cada uno es un estudiante diferente con sus propios datos
```

## Buenas prácticas

1. **Nombres en singular** - `Perro`, no `Perros`
2. **Nombres descriptivos** - `Coche` en lugar de `C`
3. **Un propósito claro** - Cada clase representa una cosa
4. **Atributos privados cuando sea posible** - Protege los datos

## Cuándo usar clases

Usa clases cuando:
- Necesitas representar entidades del mundo real (persona, coche, producto)
- Tienes datos y comportamientos relacionados
- Quieres crear múltiples objetos similares
- Necesitas organizar código complejo

No necesitas clases para:
- Scripts simples y pequeños
- Operaciones matemáticas básicas
- Código que se ejecuta una sola vez

Las clases son la base de la programación orientada a objetos y te permiten organizar tu código de manera clara y reutilizable.