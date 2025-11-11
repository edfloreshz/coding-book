# Enumeraciones

Las enumeraciones son un tipo de dato que permite definir un conjunto de constantes con nombres asociados. Son útiles cuando se tiene un conjunto fijo de valores relacionados que una variable puede tomar.

## Concepto

Una enumeración define un tipo que puede tener solo un conjunto limitado de valores nombrados. Por ejemplo, los días de la semana, los meses del año, o los estados de un proceso.

```/dev/null/pseudocode.txt#L1-9
enumeración Dias
    Lunes,
    Martes,
    Miércoles,
    Jueves,
    Viernes,
    Sábado,
    Domingo
fin enumeración
```

## Valores numéricos

Por defecto, las enumeraciones se numeran automáticamente comenzando desde 0:

```/dev/null/pseudocode.txt#L1-11
enumeración Dias
    Lunes,      // 0
    Martes,     // 1
    Miércoles,  // 2
    Jueves,     // 3
    Viernes,    // 4
    Sábado,     // 5
    Domingo     // 6
fin enumeración
```

## Valores personalizados

Es posible asignar valores específicos a cada elemento de la enumeración:

```/dev/null/pseudocode.txt#L1-11
enumeración Dias
    Lunes = 7,
    Martes = 6,
    Miércoles = 5,
    Jueves = 4,
    Viernes = 3,
    Sábado = 2,
    Domingo = 1
fin enumeración
```

También se puede comenzar desde un valor específico y el resto se incrementa automáticamente:

```/dev/null/pseudocode.txt#L1-9
enumeración Prioridad
    Baja = 1,
    Media,      // 2
    Alta,       // 3
    Crítica,    // 4
    Urgente     // 5
fin enumeración
```

## Uso de enumeraciones

```/dev/null/pseudocode.txt#L1-13
enumeración EstadoPedido
    Pendiente,
    EnProceso,
    Enviado,
    Entregado,
    Cancelado
fin enumeración

diaActual : Dias ← Dias.Lunes
estadoPedido : EstadoPedido ← EstadoPedido.Pendiente

mostrar("Hoy es: ", diaActual)
mostrar("Estado del pedido: ", estadoPedido)
```

## Comparación de enumeraciones

```/dev/null/pseudocode.txt#L1-12
enumeración Semáforo
    Rojo,
    Amarillo,
    Verde
fin enumeración

luz : Semáforo ← Semáforo.Rojo

si luz = Semáforo.Rojo entonces
    mostrar("¡Detenerse!")
sino si luz = Semáforo.Verde entonces
    mostrar("Puede avanzar")
fin si
```

## Ejemplos prácticos

### Sistema de calificaciones

```/dev/null/pseudocode.txt#L1-23
enumeración Calificación
    Excelente = 5,
    Notable = 4,
    Aprobado = 3,
    Insuficiente = 2,
    Deficiente = 1
fin enumeración

función obtenerCalificación(nota : Decimal) -> Calificación
    si nota >= 9.0 entonces
        retornar Calificación.Excelente
    sino si nota >= 7.0 entonces
        retornar Calificación.Notable
    sino si nota >= 5.0 entonces
        retornar Calificación.Aprobado
    sino si nota >= 3.0 entonces
        retornar Calificación.Insuficiente
    sino
        retornar Calificación.Deficiente
    fin si
fin función

notaEstudiante : Decimal ← 8.5
resultado : Calificación ← obtenerCalificación(notaEstudiante)
```

### Estados de una aplicación

```/dev/null/pseudocode.txt#L1-26
enumeración EstadoAplicación
    Iniciando,
    Ejecutando,
    Pausado,
    Deteniendo,
    Detenido,
    Error
fin enumeración

clase Aplicación
    estado : EstadoAplicación

    función iniciar()
        estado ← EstadoAplicación.Iniciando
        // Lógica de inicialización
        estado ← EstadoAplicación.Ejecutando
    fin función

    función pausar()
        si estado = EstadoAplicación.Ejecutando entonces
            estado ← EstadoAplicación.Pausado
        fin si
    fin función

    función detener()
        estado ← EstadoAplicación.Deteniendo
        // Lógica de limpieza
        estado ← EstadoAplicación.Detenido
    fin función
fin clase
```

### Direcciones

```/dev/null/pseudocode.txt#L1-26
enumeración Dirección
    Norte,
    Sur,
    Este,
    Oeste
fin enumeración

función mover(direcciónActual : Dirección) -> Texto
    según direcciónActual hacer
        caso Dirección.Norte:
            retornar "Moviendo hacia el Norte"
        caso Dirección.Sur:
            retornar "Moviendo hacia el Sur"
        caso Dirección.Este:
            retornar "Moviendo hacia el Este"
        caso Dirección.Oeste:
            retornar "Moviendo hacia el Oeste"
        por defecto:
            retornar "Dirección desconocida"
    fin según
fin función

dirección : Dirección ← Dirección.Norte
mensaje : Texto ← mover(dirección)
mostrar(mensaje)
```

### Sistema de permisos

```/dev/null/pseudocode.txt#L1-33
enumeración Rol
    Invitado = 0,
    Usuario = 1,
    Moderador = 2,
    Administrador = 3
fin enumeración

función tienePermiso(rolUsuario : Rol, rolRequerido : Rol) -> Booleano
    retornar rolUsuario >= rolRequerido
fin función

función verificarAcceso(usuario : Rol, acción : Texto)
    si acción = "leer" entonces
        si tienePermiso(usuario, Rol.Invitado) entonces
            mostrar("Acceso concedido para leer")
        fin si
    sino si acción = "escribir" entonces
        si tienePermiso(usuario, Rol.Usuario) entonces
            mostrar("Acceso concedido para escribir")
        fin si
    sino si acción = "moderar" entonces
        si tienePermiso(usuario, Rol.Moderador) entonces
            mostrar("Acceso concedido para moderar")
        fin si
    sino si acción = "administrar" entonces
        si tienePermiso(usuario, Rol.Administrador) entonces
            mostrar("Acceso concedido para administrar")
        fin si
    fin si
fin función

rolActual : Rol ← Rol.Usuario
verificarAcceso(rolActual, "escribir")
```

## Ventajas de las enumeraciones

1. **Legibilidad**: Los nombres descriptivos hacen el código más fácil de entender que usar números mágicos
2. **Seguridad de tipos**: Previene el uso de valores inválidos
3. **Autocompletado**: Los editores pueden sugerir valores válidos
4. **Mantenibilidad**: Cambios en los valores se hacen en un solo lugar
5. **Documentación**: El código se auto-documenta con nombres significativos

## Buenas prácticas

### ✅ Usar nombres descriptivos

```/dev/null/pseudocode.txt#L1-7
// Bueno: Nombres claros y descriptivos
enumeración EstadoConexión
    Desconectado,
    Conectando,
    Conectado,
    Error
fin enumeración
```

### ✅ Agrupar valores relacionados

```/dev/null/pseudocode.txt#L1-8
// Bueno: Valores que pertenecen juntos
enumeración TipoDocumento
    DNI,
    Pasaporte,
    LicenciaConducir,
    TarjetaIdentidad
fin enumeración
```

### ❌ Evitar enumeraciones muy grandes

```/dev/null/pseudocode.txt#L1-8
// Malo: Demasiados valores, considere otra estructura
enumeración TodosLosPaísesDelMundo
    // 195+ países...
    // Mejor usar una base de datos o diccionario
fin enumeración
```

### ✅ Usar valores explícitos cuando importa el número

```/dev/null/pseudocode.txt#L1-7
// Bueno: Valores explícitos para códigos de estado HTTP
enumeración CódigoHTTP
    OK = 200,
    NoEncontrado = 404,
    ErrorServidor = 500
fin enumeración
```

## Conversión entre enumeraciones y números

```/dev/null/pseudocode.txt#L1-15
enumeración Mes
    Enero = 1,
    Febrero = 2,
    Marzo = 3,
    // ... resto de meses
    Diciembre = 12
fin enumeración

// Convertir número a enumeración
númeroMes : Entero ← 3
mesActual : Mes ← convertirAMes(númeroMes)  // Mes.Marzo

// Convertir enumeración a número
mes : Mes ← Mes.Febrero
valor : Entero ← convertirAEntero(mes)  // 2
```

## Iteración sobre enumeraciones

```/dev/null/pseudocode.txt#L1-16
enumeración DíaSemana
    Lunes,
    Martes,
    Miércoles,
    Jueves,
    Viernes,
    Sábado,
    Domingo
fin enumeración

// Procesar todos los días
para cada día en DíaSemana hacer
    si día = DíaSemana.Sábado o día = DíaSemana.Domingo entonces
        mostrar(día, " es fin de semana")
    sino
        mostrar(día, " es día laboral")
    fin si
fin para
```

## Notas importantes

- Las enumeraciones son útiles para conjuntos fijos de valores relacionados
- Proporcionan seguridad de tipos en tiempo de compilación
- Mejoran la legibilidad y mantenibilidad del código
- Son ideales para máquinas de estados,
