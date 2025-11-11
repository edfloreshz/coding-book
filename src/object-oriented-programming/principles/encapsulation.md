# Encapsulamiento

El encapsulamiento es un principio fundamental de la programación orientada a objetos que oculta los detalles internos de un objeto y expone solo la interfaz pública necesaria.

## Concepto

El encapsulamiento agrupa datos (atributos) y métodos en una clase, controlando el acceso a ellos. Los atributos privados solo se pueden modificar a través de métodos públicos.

## Ejemplo

```/dev/null/pseudocode.txt#L1-35
clase CuentaBancaria
    // Atributos privados (ocultos del exterior)
    privado saldo : Decimal
    privado titular : Texto

    función constructor(titular : Texto)
        este.titular ← titular
        este.saldo ← 0.0
    fin función

    // Métodos públicos (interfaz pública)
    público función depositar(monto : Decimal)
        si monto > 0 entonces
            saldo ← saldo + monto
            mostrar("Depósito exitoso. Saldo: $", saldo)
        sino
            mostrar("Error: Monto debe ser positivo")
        fin si
    fin función

    público función retirar(monto : Decimal) -> Booleano
        si monto > saldo entonces
            mostrar("Error: Saldo insuficiente")
            retornar falso
        sino si monto <= 0 entonces
            mostrar("Error: Monto inválido")
            retornar falso
        sino
            saldo ← saldo - monto
            mostrar("Retiro exitoso. Saldo: $", saldo)
            retornar verdadero
        fin si
    fin función

    público función obtenerSaldo() -> Decimal
        retornar saldo
    fin función
fin clase

// Uso
cuenta : CuentaBancaria ← nueva CuentaBancaria("María García")

// No se puede hacer: cuenta.saldo ← 1000000  (saldo es privado)
// Se debe usar los métodos públicos:
cuenta.depositar(1000.0)
cuenta.retirar(500.0)
mostrar("Saldo actual: $", cuenta.obtenerSaldo())
```

## Ventajas del encapsulamiento

1. **Seguridad**: Evita modificaciones incorrectas de los datos
2. **Validación**: Los métodos públicos pueden validar los datos antes de modificarlos
3. **Flexibilidad**: Permite cambiar la implementación interna sin afectar el código externo
4. **Control**: Define claramente cómo se debe interactuar con el objeto

## Notas importantes

- Los atributos privados solo son accesibles dentro de la clase
- Los métodos públicos proporcionan una interfaz controlada para acceder a los datos
- El encapsulamiento ayuda a mantener la integridad de los datos
- Es una buena práctica hacer atributos privados por defecto
