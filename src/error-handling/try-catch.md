# Try-Catch

El manejo de errores con `try-catch` (intentar-capturar) permite ejecutar código que puede fallar y manejar los errores de manera controlada.

## ¿Qué es try-catch?

Try-catch es una estructura que permite:
- **Intentar** ejecutar código que puede generar errores
- **Capturar** el error cuando ocurre
- **Manejar** el error sin que el programa se detenga

## Estructura básica

```pseudocode
intentar
    // Código que puede fallar
capturar (error)
    // Qué hacer si falla
fin intentar
```

## Ejemplo

```pseudocode
// Pedir un número al usuario y dividir
intentar
    variable numero : entero
    mostrar("Ingresa un número:")
    leer(numero)
    
    variable resultado : entero ← 100 / numero
    mostrar("100 dividido entre " + convertirATexto(numero) + " = " + convertirATexto(resultado))
    
capturar (error)
    mostrar("Error: No se pudo realizar la operación")
    mostrar("Verifica que ingresaste un número válido y diferente de cero")
fin intentar

mostrar("El programa continúa funcionando")
```

## ¿Qué pasa sin try-catch?

**Sin try-catch:**
- Si el usuario ingresa 0, el programa se detiene con error
- El programa termina abruptamente

**Con try-catch:**
- Si el usuario ingresa 0, se captura el error
- Se muestra un mensaje amigable
- El programa continúa ejecutándose

## Bloque finally

Opcionalmente, puedes usar `finalmente` para código que siempre se ejecuta:

```pseudocode
intentar
    variable archivo : Archivo ← abrirArchivo("datos.txt")
    variable contenido : texto ← archivo.leer()
    mostrar(contenido)
    
capturar (error)
    mostrar("No se pudo leer el archivo")
    
finalmente
    // Esto SIEMPRE se ejecuta, haya error o no
    cerrarArchivo(archivo)
fin intentar
```

## Usos comunes

Try-catch se usa para:
- **Leer archivos** - El archivo puede no existir
- **Convertir texto a números** - El texto puede no ser válido
- **Conectar a internet** - La conexión puede fallar
- **Acceder a bases de datos** - Puede haber problemas de conexión
- **Dividir números** - El divisor puede ser cero

## Buenas prácticas

1. **Usa try-catch solo cuando sea necesario** - No envuelvas todo el código
2. **Muestra mensajes claros** - Explica qué salió mal y qué hacer
3. **No captures errores y los ignores** - Siempre haz algo con el error
4. **Usa finally para limpieza** - Cierra archivos, conexiones, etc.

## Cuándo usar try-catch

**Usa try-catch cuando:**
- El código puede fallar por razones fuera de tu control
- Trabajas con archivos, red, o entrada de usuario
- Quieres que el programa continúe aunque algo falle
- Necesitas mostrar mensajes amigables al usuario

**No uses try-catch cuando:**
- Puedes validar los datos antes de usarlos
- El error se puede prevenir con una simple verificación
- Estás aprendiendo y quieres ver dónde están los errores

Try-catch es una herramienta importante para hacer programas robustos que no se detengan ante errores inesperados.