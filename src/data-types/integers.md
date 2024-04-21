# Numeros enteros

La mayoria de los lenguajes de programacion proveen tipos de dato para representar numeros enteros de diferentes tamaños. Entre ellos se incluyen los numeros firmados y no firmados.

> Los enteros **firmados** (signed integers) son numeros cuyo rango de valores se extiende hacia los numeros negativos.

> Los enteros **no firmados** (unsigned integers) son numeros cuyo rango de valores es siempre mayor o igual a cero, nunca negativo.

Cada representacion de numeros alcanza cierto rango de valores.

| Representacion | Tipo | Tamaño | Desde | Hasta |
| --- | --- | --- | --- | --- |
| sbyte | Firmado | 8 bits | -128 | 127 |
| byte | No firmado | 8 bits | 0 | 255 |
| short | Firmado | 16 bits | -32,768 | 32,767 |
| ushort | No firmado | 16 bits | 0 | 65,535 |
| int | Firmado | 32 bits | -2,147,483,648 | 2,147,483,647 |
| uint | No firmado | 32 bits | 0 | 4,294,967,295 |
| long | Firmado | 64 bits | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 |
| ulong | No firmado | 64 bits | 0 | 18,446,744,073,709,551,615 |

Si declaramos una variable entera de 8 bits y almacenamos un numero mayor a 127, el programa dejara de funcionar y nos reportara que encontro un error.

De igual forma, si la declaramos con un numero menor a 127 y le sumamos un numero cuyo resultado sea mayor a 127, terminaremos con un error.

```csharp
sbyte sbyteNum = 127;
byte byteNum = -128;
short shortNum = -32_768;
ushort ushortNum = 65_535;
int intNum = -2_147_483_648;
uint uintNum = 4_294_967_295;
long longNum = -9_223_372_036_854_775,808;
ulong ulongNum = 18_446_744_073_709_551_615;

var f = 0f; // float
var d = 0d; // double
var m = 0m; // decimal (money)
var u = 0u; // unsigned int
var l = 0l; // long
var ul = 0ul; // unsigned long
```