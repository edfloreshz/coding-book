# Declaración de tipos

Es posible declarar tipos de datos personalizados, comúnmente conocidos como _alias_, en la mayoría de los lenguajes de programación. Estos tipos de datos personalizados pueden ser útiles para simplificar la escritura de código y hacerlo más legible.

## Concepto

Un alias de tipo es un nombre alternativo para un tipo de dato existente. Esto puede ser útil cuando se trabaja con tipos complejos o cuando se desea dar un nombre más descriptivo a un tipo.

```/dev/null/pseudocode.txt#L1-15
// Definir alias para tipos complejos
tipo ListaDeNombres = Lista<Cadena>
tipo Coordenadas = Par<Decimal, Decimal>
tipo DiccionarioEdades = Mapa<Cadena, Entero>

// Usar los alias
nombres : ListaDeNombres ← ["Ana", "Juan", "María"]
ubicación : Coordenadas ← (10.5, 20.3)
edades : DiccionarioEdades ← nuevo DiccionarioEdades()

edades["Ana"] ← 25
edades["Juan"] ← 30

mostrar("Nombres: ", nombres)
mostrar("Ubicación: ", ubicación)
mostrar("Edad de Ana: ", edades["Ana"])
```

## Recomendaciones

- Usar alias para tipos complejos que se repiten frecuentemente
- Evitar alias para tipos primitivos (Entero, Cadena, Booleano)
- Usar nombres descriptivos que indiquen el propósito del tipo
- Los alias no crean nuevos tipos, solo nombres alternativos