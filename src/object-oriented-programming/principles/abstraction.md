# Abstracción

La abstracción es un principio fundamental de la programación orientada a objetos que consiste en identificar las características esenciales de un objeto y ocultar los detalles de implementación innecesarios.

## Concepto

La abstracción permite enfocarse en **qué hace** un objeto en lugar de **cómo lo hace**. Se logra a través de clases abstractas e interfaces que definen contratos sin especificar todos los detalles de implementación.

## Ejemplo

```/dev/null/pseudocode.txt#L1-45
clase abstracta Figura
    color : Cadena
    
    función constructor(color : Cadena)
        este.color ← color
    fin función
    
    // Métodos abstractos: deben ser implementados por clases derivadas
    abstracto función calcularÁrea() -> Decimal
    abstracto función calcularPerímetro() -> Decimal
    
    // Método concreto: tiene implementación
    función mostrarInfo()
        mostrar("Figura de color: ", color)
        mostrar("Área: ", calcularÁrea())
        mostrar("Perímetro: ", calcularPerímetro())
    fin función
fin clase

clase Rectángulo hereda de Figura
    base : Decimal
    altura : Decimal
    
    función constructor(color : Cadena, base : Decimal, altura : Decimal)
        super(color)
        este.base ← base
        este.altura ← altura
    fin función
    
    función calcularÁrea() -> Decimal
        retornar base * altura
    fin función
    
    función calcularPerímetro() -> Decimal
        retornar 2 * (base + altura)
    fin función
fin clase

// Uso
rect : Rectángulo ← nuevo Rectángulo("Rojo", 5.0, 3.0)
rect.mostrarInfo()

// No se puede hacer: figura ← nuevo Figura("Azul")  (clase abstracta)
```

## Interfaces

Una interfaz define un contrato que una clase debe implementar, sin proporcionar implementación:

```/dev/null/pseudocode.txt#L1-30
interfaz Volador
    función volar()
    función aterrizar()
fin interfaz

clase Avión implementa Volador
    modelo : Cadena
    
    función constructor(modelo : Cadena)
        este.modelo ← modelo
    fin función
    
    función volar()
        mostrar("El avión ", modelo, " está volando")
    fin función
    
    función aterrizar()
        mostrar("El avión ", modelo, " está aterrizando")
    fin función
fin clase

// Uso
función hacerVolar(volador : Volador)
    volador.volar()
    volador.aterrizar()
fin función

avión : Avión ← nuevo Avión("Boeing 747")
hacerVolar(avión)
```

## Ventajas de la abstracción

1. **Simplicidad**: Oculta la complejidad innecesaria
2. **Flexibilidad**: Permite cambiar implementaciones sin afectar el código que las usa
3. **Reutilización**: Código genérico que funciona con múltiples implementaciones
4. **Mantenibilidad**: Cambios aislados en implementaciones específicas

## Diferencia entre clase abstracta e interfaz

**Clase abstracta:**
- Puede tener métodos concretos y abstractos
- Puede tener atributos
- Puede tener constructor
- Representa una relación "es un"

**Interfaz:**
- Solo define firmas de métodos (sin implementación)
- No puede tener atributos
- No tiene constructor
- Representa un contrato o capacidad "puede hacer"

## Notas importantes

- No se pueden crear instancias de clases abstractas directamente
- Toda clase que hereda de una clase abstracta debe implementar sus métodos abstractos
- Las interfaces permiten definir capacidades sin especificar la implementación
- La abstracción ayuda a crear código desacoplado y fácil de probar