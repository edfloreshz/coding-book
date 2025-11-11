# Paradigma orientado a objetos

![banner](https://images.unsplash.com/photo-1481349518771-20055b2a7b24?ixlib=rb-4.0.3&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=3600)

El paradigma orientado a objetos (POO) es un estilo de programación que organiza el código alrededor de "objetos" que combinan datos (atributos) y comportamiento (métodos) en una única unidad.

## Concepto fundamental

La programación orientada a objetos modela conceptos del mundo real como objetos. Cada objeto tiene un estado (datos) y comportamiento (métodos) que operan sobre esos datos.

## Los cuatro pilares de la POO

1. **Encapsulamiento**: Ocultar los detalles internos de un objeto
2. **Abstracción**: Mostrar solo lo esencial, ocultar la complejidad
3. **Herencia**: Crear nuevas clases basadas en clases existentes
4. **Polimorfismo**: Objetos de diferentes tipos tratados de manera uniforme

## Ejemplo

```/dev/null/pseudocode.txt#L1-65
// Clase base
clase Empleado
    privado nombre : Texto
    privado salario : Decimal

    función constructor(nombre : Texto, salario : Decimal)
        este.nombre ← nombre
        este.salario ← salario
    fin función

    función trabajar()
        mostrar(nombre, " está trabajando")
    fin función

    función calcularSalario() -> Decimal
        retornar salario
    fin función

    función obtenerNombre() -> Texto
        retornar nombre
    fin función
fin clase

// Clase derivada (Herencia)
clase Gerente hereda de Empleado
    privado bonificación : Decimal

    función constructor(nombre : Texto, salario : Decimal, bono : Decimal)
        super(nombre, salario)
        este.bonificación ← bono
    fin función

    // Polimorfismo: sobreescribir método
    función calcularSalario() -> Decimal
        retornar super.calcularSalario() + bonificación
    fin función

    función dirigir()
        mostrar(obtenerNombre(), " está dirigiendo el equipo")
    fin función
fin clase

// Uso
empleados : Lista<Empleado> ← nueva Lista<Empleado>()
empleados.agregar(nuevo Empleado("Ana", 3000.0))
empleados.agregar(nuevo Gerente("Carlos", 5000.0, 2000.0))
empleados.agregar(nuevo Empleado("María", 3500.0))

// Polimorfismo: procesar todos de forma uniforme
totalNómina : Decimal ← 0.0
para cada emp en empleados hacer
    emp.trabajar()
    salario : Decimal ← emp.calcularSalario()
    mostrar("Salario: $", salario)
    totalNómina ← totalNómina + salario
    mostrar("---")
fin para

mostrar("Total nómina: $", totalNómina)

// Salida:
// Ana está trabajando
// Salario: $3000.0
// ---
// Carlos está trabajando
// Salario: $7000.0
// ---
// María está trabajando
// Salario: $3500.0
// ---
// Total nómina: $13500.0
```

## Ventajas del paradigma orientado a objetos

1. **Reutilización de código**: La herencia permite reutilizar código existente
2. **Modularidad**: El código está organizado en unidades lógicas (clases)
3. **Mantenibilidad**: Más fácil de modificar y extender
4. **Modelado natural**: Los objetos representan conceptos del mundo real
5. **Encapsulamiento**: Protege los datos de modificaciones incorrectas
6. **Flexibilidad**: El polimorfismo permite código genérico y extensible

## Principios de diseño

**Principios SOLID:**
- **S**ingle Responsibility: Una clase debe tener una sola responsabilidad
- **O**pen/Closed: Abierto para extensión, cerrado para modificación
- **L**iskov Substitution: Los objetos derivados deben poder reemplazar a los base
- **I**nterface Segregation: Interfaces específicas mejor que generales
- **D**ependency Inversion: Depender de abstracciones, no de implementaciones

## Cuándo usar POO

La POO es especialmente útil para:
- Sistemas empresariales con entidades de negocio
- Aplicaciones con interfaces gráficas
- Videojuegos con personajes y objetos
- Simulaciones del mundo real
- Sistemas que requieren extensibilidad

## Notas importantes

- POO organiza el código en objetos con estado y comportamiento
- Los cuatro pilares (encapsulamiento, abstracción, herencia, polimorfismo) trabajan juntos
- No es la solución para todo; cada paradigma tiene sus casos de uso
- Diseñar jerarquías de clases pensando en la extensibilidad
- Preferir composición sobre herencia cuando sea apropiado
