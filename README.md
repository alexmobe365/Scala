# 3. Ejercicios

## Ejercicio 1 — Variables, tipos e inferencia

Crea variables que representen la información de una partida de cartas:

- Nombre del jugador.
- Número de partidas jugadas.
- Puntuación actual.
- Porcentaje de victorias.
- Indicación de si el jugador continúa activo.

Realiza dos versiones:

### Versión A

Declara explícitamente el tipo de cada variable.

Ejemplo de estructura:

```scala
val nombre: String = ...
val partidas: Int = ...
```

### Versión B

Declara las mismas variables permitiendo que Scala infiera los tipos.

Finalmente, muestra los valores por pantalla.
## Ejercicio 2 — `val`, `var` y reasignación

Crea las siguientes variables:

```scala
val jugador = "Marta"
var puntuacion = 10
```

Realiza las siguientes operaciones:

1. Incrementa la puntuación en 5 puntos.
2. Vuelve a incrementarla en 3 puntos.
3. Muestra el resultado final.
4. Intenta reasignar el valor de `jugador`.

La última operación deberá producir un error.

### Documentación

Incluye una celda Markdown explicando:

- Por qué `puntuacion` puede modificarse.
- Por qué `jugador` no puede reasignarse.
- Qué mensaje genera Scala al intentar modificar un `val`.

No elimines la celda que contiene el error. Debe quedar documentada en el Notebook.

---

## Ejercicio 3 — Tipos numéricos y precisión

Declara un mismo valor decimal utilizando:

```scala
Double
Float
```

Utiliza un número con muchos decimales, por ejemplo:

```
3.14159265358979323846264338327
```

Muestra ambos valores.

Después:

1. Crea una variable de tipo `Int`.
2. Crea una variable de tipo `Boolean`.
3. Crea una variable de tipo `String`.

### Documentación

Explica:

- Qué diferencia observas entre `Double` y `Float`.
- Qué tipo utilizarías para representar el número de estudiantes de una clase.
- Qué tipo utilizarías para representar si un estudiante ha aprobado.

---

## Ejercicio 4 — Función para determinar si una mano se pasa de 21

Define una función llamada:

```scala
bust
```

que reciba la puntuación de una mano como `Int` y devuelva un `Boolean`.

La función deberá devolver:

- `true` si la puntuación es mayor que 21.
- `false` en caso contrario.

Prueba la función con los siguientes valores:

```
18
21
22
30
```

### Resultado esperado

Los resultados deberán corresponder conceptualmente a:

```
false
false
true
true
```

### Requisito

La función deberá devolver el resultado de la comparación y no deberá modificar variables externas.

---

## Ejercicio 5 — Comparación de dos manos

Define una función:

```scala
maxHand
```

que reciba dos valores enteros y devuelva el mayor de los dos utilizando `if` y `else`.

Prueba la función al menos con:

```
17 y 19
20 y 18
21 y 21
```

### Después

Explica qué sucede cuando ambas manos tienen el mismo valor.

Modifica la función si consideras necesario mejorar el comportamiento para ese caso y documenta tu decisión.

---

## Ejercicio 6 — Decidir el ganador de una partida

Utiliza la función `bust` del ejercicio 4.

Crea una función:

```scala
ganador
```

que reciba dos manos:

```scala
handA: Int
handB: Int
```

y aplique las siguientes reglas:

1. Si ambas manos superan 21, devuelve `0`.
2. Si solamente `handA` supera 21, devuelve `handB`.
3. Si solamente `handB` supera 21, devuelve `handA`.
4. Si ninguna supera 21, devuelve la mano con mayor puntuación.

Prueba como mínimo los siguientes casos:

```
26 y 20
18 y 22
24 y 25
17 y 19
21 y 20
```

### Documentación

Para cada prueba indica qué condición del bloque `if / else if / else` se ha cumplido.

---

## Ejercicio 7 — Arrays y mutabilidad

Crea el siguiente array:

```scala
val jugadores = Array("Alex", "Chen", "Marta")
```

Realiza las siguientes operaciones:

1. Muestra el array original.
2. Sustituye `"Alex"` por `"Sindhu"`.
3. Muestra nuevamente el array.
4. Intenta asignar el número `500` a una de sus posiciones.

### Documentación

Explica:

- Por qué los elementos del array pueden cambiar aunque la variable se haya declarado con `val`.
- Por qué Scala no permite introducir el valor `500` en un `Array[String]`.
- La diferencia entre reasignar la variable y modificar un elemento del array.

Mantén en el Notebook la prueba que genera el error de tipos.

---

## Ejercicio 8 — Creación e inicialización de Arrays

Crea un array para almacenar las puntuaciones de cuatro jugadores utilizando:

```scala
new ArrayInt
```

Realiza las siguientes tareas:

1. Muestra el array inmediatamente después de crearlo.
2. Asigna manualmente una puntuación a cada posición.
3. Muestra el array completo.
4. Muestra su longitud utilizando:

```scala
.length
```

Utiliza las puntuaciones:

```
17, 24, 21, 19
```

### Pregunta

¿Qué valores contiene un `Array[Int]` recién creado antes de que asignes manualmente sus elementos?

---

## Ejercicio 9 — Recorrer un Array con `while`

Utiliza el array:

```scala
val manos = Array(17, 24, 21, 19, 26)
```

Recórrelo utilizando un bucle `while`.

Para cada posición deberás mostrar:

- El valor de la mano.
- El resultado de aplicar la función `bust`.

El ejercicio deberá utilizar:

```scala
var i = 0
```

y la propiedad:

```scala
manos.length
```

para determinar cuándo termina el bucle.

### Documentación

Explica:

- Por qué el contador debe ser mutable.
- Qué ocurriría si no incrementaras `i`.
- Qué elementos del ejercicio corresponden al estilo imperativo.

---

## Ejercicio 10 — Listas e inmutabilidad

Crea la siguiente lista:

```scala
val jugadores = List("Alex", "Chen", "Marta")
```

Realiza las siguientes operaciones:

1. Muestra la lista original.
2. Crea una nueva lista añadiendo `"Sindhu"` al principio mediante `::`.
3. Muestra ambas listas.
4. Comprueba que la lista original no ha cambiado.
5. Muestra:
    - Su longitud.
    - La lista invertida mediante `reverse`.

### Documentación

Explica por qué la operación con `::` produce una lista nueva en lugar de modificar la lista original.

---

## Ejercicio 11 — Construcción y concatenación de listas

Construye una lista utilizando `Nil` y el operador `::`.

La lista deberá contener:

```
Ana
Luis
Marta
```

A continuación crea una segunda lista:

```
Pedro
Sofia
```

Concatena ambas listas utilizando:

```scala
:::
```

Finalmente muestra:

- Primera lista.
- Segunda lista.
- Lista resultante.

### Requisito

Demuestra mediante la salida que las dos listas originales permanecen sin cambios después de la concatenación.

---

## Ejercicio 12 — Operadores relacionales y lógicos

Considera las siguientes puntuaciones:

```scala
val handA = 18
val handB = 21
val handC = 25
```

Crea expresiones que respondan a las siguientes preguntas:

1. ¿Es `handA` mayor que `handB`?
2. ¿Es `handB` igual a 21?
3. ¿Es `handC` diferente de 21?
4. ¿Son `handA` y `handB` menores o iguales a 21?
5. ¿Alguna de las manos `handA` o `handC` supera 21?
6. ¿No se ha pasado `handB` de 21?

Utiliza según corresponda:

```
>
<
>=
<=
==
!=
&&
||
!
```

### Documentación

Incluye una tabla Markdown con tres columnas:

| Expresión | Resultado | Explicación |
| --- | --- | --- |
| … | … | … |

---

## Ejercicio 13 — `foreach` y funciones como valores

Utiliza:

```scala
val manos = Array(17, 24, 21, 26, 18)
```

y la función `bust`.

Recorre el array utilizando:

```scala
foreach
```

de forma que se evalúe cada mano.

Debes realizar dos versiones:

### Versión A

Utiliza un bucle `while`.

### Versión B

Utiliza `foreach` pasando una función que procese cada elemento.

### Documentación

Compara ambas versiones e identifica:

- Cuál necesita un contador.
- Cuál necesita una variable `var` para recorrer la colección.
- Cuál se aproxima más al estilo funcional presentado en el material del curso (Datacamp).

---

## Ejercicio 14 — Efectos secundarios y estilo de programación

Analiza el siguiente planteamiento:

```scala
var total = 0

def sumarAlTotal(valor: Int) = {
  total = total + valor
}
```

Realiza las siguientes tareas:

1. Ejecuta la función varias veces.
2. Muestra el valor de `total` después de cada llamada.
3. Explica por qué la función modifica una variable situada fuera de su ámbito local.
4. Identifica el efecto secundario.

Después crea una segunda versión:

```scala
def sumar(a: Int, b: Int): Int = {
  ...
}
```

que reciba valores y devuelva un nuevo resultado sin modificar variables externas.

### Documentación

Compara ambas funciones en una tabla:

| Característica | `sumarAlTotal` | `sumar` |
| --- | --- | --- |
| Modifica datos externos |  |  |
| Devuelve un resultado calculado |  |  |
| Utiliza efecto secundario |  |  |
| Estilo predominante |  |  |

---

## Ejercicio 15 — Programa integrado: torneo de Twenty-One

Desarrolla un pequeño programa que combine los principales conceptos trabajados en esta parte.

Dispones de los siguientes jugadores:

```scala
val jugadores = List("Alex", "Chen", "Marta", "Sindhu")
```

y de sus puntuaciones:

```scala
val manos = Array(18, 24, 21, 20)
```

El programa deberá:

1. Mantener los nombres de los jugadores en una `List`.
2. Mantener las puntuaciones en un `Array[Int]`.
3. Utilizar la función `bust` para determinar qué manos superan 21.
4. Recorrer todas las puntuaciones y mostrar si cada mano se ha pasado o no.
5. Determinar cuál es la mejor puntuación válida.
6. Utilizar `if`, `else if` y `else` cuando sea necesario.
7. Utilizar operadores relacionales o lógicos.
8. Utilizar al menos una función definida por ti.
9. Utilizar al menos una estructura `while` o `foreach`.
10. Evitar modificar las listas originales.
