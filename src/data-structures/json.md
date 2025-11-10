# JSON

JSON (JavaScript Object Notation) es un formato ligero de intercambio de datos que es fácil de leer y escribir para los humanos, y fácil de analizar y generar para las máquinas.

## Concepto

JSON es una forma de representar información estructurada como texto. Se utiliza ampliamente en la web para transferir datos entre un servidor y una aplicación cliente, y también para almacenar configuraciones y datos en archivos.

## Estructura básica

JSON se compone de dos estructuras principales:

1. **Objetos**: Colecciones de pares clave-valor entre llaves `{}`
2. **Arreglos**: Listas ordenadas de valores entre corchetes `[]`

## Tipos de datos en JSON

```/dev/null/json.txt#L1-9
{
  "cadena": "Hola Mundo",
  "número": 42,
  "decimal": 3.14,
  "booleano": true,
  "nulo": null,
  "arreglo": [1, 2, 3],
  "objeto": {"clave": "valor"}
}
```

## Ejemplo

```/dev/null/pseudocode.txt#L1-45
clase Estudiante
    nombre : Cadena
    edad : Entero
    materias : Lista<Cadena>
    activo : Booleano
fin clase

// Crear un estudiante
estudiante : Estudiante ← nuevo Estudiante()
estudiante.nombre ← "María López"
estudiante.edad ← 22
estudiante.activo ← verdadero
estudiante.materias ← ["Programación", "Bases de Datos", "Algoritmos"]

// Serializar a JSON (convertir objeto a texto)
json : Cadena ← serializarAJSON(estudiante)
mostrar(json)

// El JSON resultante:
// {
//   "nombre": "María López",
//   "edad": 22,
//   "materias": [
//     "Programación",
//     "Bases de Datos",
//     "Algoritmos"
//   ],
//   "activo": true
// }

// Deserializar desde JSON (convertir texto a objeto)
textoJSON : Cadena ← '{
  "nombre": "Juan Pérez",
  "edad": 25,
  "materias": ["Matemáticas", "Física"],
  "activo": true
}'

estudianteRecuperado : Estudiante ← deserializarJSON<Estudiante>(textoJSON)

mostrar(estudianteRecuperado.nombre)   // "Juan Pérez"
mostrar(estudianteRecuperado.edad)     // 25
mostrar(estudianteRecuperado.materias) // ["Matemáticas", "Física"]
```

## Trabajar con archivos JSON

```/dev/null/pseudocode.txt#L1-14
// Guardar datos en archivo JSON
función guardarEnJSON(ruta : Cadena, objeto : Objeto)
    json : Cadena ← serializarAJSON(objeto)
    escribirArchivo(ruta, json)
fin función

// Leer datos desde archivo JSON
función leerDesdeJSON<T>(ruta : Cadena) -> T
    json : Cadena ← leerArchivo(ruta)
    objeto : T ← deserializarJSON<T>(json)
    retornar objeto
fin función

guardarEnJSON("estudiante.json", estudiante)
estudianteCargado : Estudiante ← leerDesdeJSON<Estudiante>("estudiante.json")
```

## Notas importantes

- JSON no soporta comentarios en el formato estándar
- Las claves deben estar entre comillas dobles
- Los valores de cadena deben estar entre comillas dobles
- Los números no necesitan comillas
- JSON es sensible a la sintaxis: comas, llaves y corchetes deben estar correctamente balanceados
