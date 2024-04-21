# Numeros de punto flotante

Los numeros de punto flotante representan numeros reales con signo. La representación de un número real con signo incluye una parte entera, una parte fraccionaria y un exponente.

```csharp
float num = -10.2;
double num = -10.2;
decimal num = -10.2;
```

Al igual que los numeros enteros, los numeros flotantes tambien se representan con `bits` de diferente tamaño.

| Tipo | Tamaño | Desde | Hasta | Precicion |
| --- | --- | --- | --- | --- |
| float | 32 bits | ±1.5 x 10^−45 | ±3.4 x 10^38 | ~6-9 digitos |
| double | 64 bits | ±5.0 × 10^−324 | ±1.7 × 10^308 | ~15-17 digitos |
| decimal | 128 bits | ±1.0 x 10^-28 | ±7.9228 x 10^28 | 28-29 digitos |