# Registro de abatidos por día en el Call of Duty
![Portada](portadaCOD.png)

Se nos pide modelar un servicio para el famoso videojuego Call of Duty que permita registrar la cantidad de abatidos 
por día. 

Cada registro del registro de abatidos deberá contener la cantidad de abatidos y el día correspondiente. Analizar las 
posibles soluciones para resolver el problema. 
Para representar el valor de día, en este modelo, usaremos un entero del tipo AAAAMMDD. Por ejemplo para el 31/12/2022
 iría 20221231. Ya veremos que Wollok contempla la posibilidad de usar fechas, pero eso será más adelante. 
Considerar también la posibilidad de eliminar uno o todos los registros.

<br>

El registro debe ser capaz de responder las siguientes consultas:
- `cantidadDeDiasRegistrados()`: indica la cantidad de días de los que se tiene registro.
- `estaVacioElRegistro()`: indica si el registro está vacío o no.
- `algunDiaAbatio(cantidad)`: indica si el registro incluye al menos un día en el que se abatió, exactamente, la 
cantidad indicada.
- `primerValorDeAbatidos()`: indica la cantidad del primer registro.
- `ultimoValorDeAbatidos()`: el último valor registrado.  
- `maximoValorDeAbatidos()`: el valor más alto de abatidos.
- `totalAbatidos()`: el total de abatidos por el jugador.
- `cantidadDeAbatidosElDia(dia)`: la cantidad de abatidos por el jugador el día indicado.
- `ultimoValorDeAbatidosConSize()`: Demostrar que last() == size()-1.
- `diasConAbatidosSuperioresA(cuanto)`: los dias que abatió un valor superior al indicado.
- `valoresDeAbatidosPares()`: los valores de abatidos del registro que son valores pares.
- `abatidosSumando(cantidad)`: la lista de valores que resulta de sumar el valor indicado en 'cantidad' a cada valor
 de abatidos del registro. 
- `abatidosEsAcotada(n1,n2)`: indica si en el registro, la cantidad de abatidos se encuentra entre los valores 
indicados.
- `algunDiaAbatioMasDe(cantidad)`: indica si algún día de que se tiene registro, la cantidad de abatidos es mayor 
al valor indicado.
- `todosLosDiasAbatioMasDe(cantidad)`: indica si todos los días de que se tiene registro, la cantidad de abatidos 
es mayor al valor indicado.
- `cantidadAbatidosMayorALaPrimera()`: la cantidad de valores de abatidos diaria que superan a la cantidad indicada 
para el primer día del registro.
- `esCrack()`: indica verdadero si en todos los días de los que se tiene registro, el valor de abatidos siempre fue 
aumentando (mayor valor día a día).

A modo de ejemplo, se indica qué debe responder el registro de abatidos a varios mensajes, si incluye el juego de 
seis días con valores 43,18,49,62,33,39 y los días serían 20221231,20230101,20230105,20230106,20230107,20230108.
 
| mensaje | resultado esperado | 
| --- | --- |
| `registroAbatidos.algunDiaAbatio(49)` | `true` |
| `registroAbatidos.algunDiaAbatio(52)` | `false` |
| `registroAbatidos.maximoValorDeAbatidos()` | `62` |
| `registroAbatidos.valoresDeAbatidosPares()` | `18,62` |
| `registroAbatidos.abatidosEsAcotada(10,100)` | `true` |
| `registroAbatidos.abatidosEsAcotada(20,100)` | `false` (porque 18 no está en el rango) |
| `registroAbatidos.abatidosSuperioresA(35)` | `43,49,62,39` |
| `registroAbatidos.abatidosSumando(5)` | `48,23,54,67,38,44` |
| `registroAbatidos.totalAbatidos()` | `244` |
| `registroAbatidos.ultimoValorDeAbatidos()` | `39` |
| `registroAbatidos.cantidadAbatidosMayorALaPrimera()` | `2` (los valores 49 y 62) |
| `registroAbatidos.algunDiaAbatioMasDe(50)` | `true` |
| `registroAbatidos.todosLosDiasAbatioMasDe(30)` | `false` |
| `registroAbatidos.esCrack()` | `false` |

Realizar los test de los otros métodos que no fueron mencionados en este ejemplo, a fin de comprobar que todos 
funcionan correctamente.

## Puntos desafío

- modificar el método `agregarAbatidosDia(cantidad, dia)` para que contemple la posiblidad de sumar la cantidad 
indicada en caso que ya exista el día en el registro.
- hacer el método `ordenarRegistro()` que realiza el ordenamiento de todo el registro de abatidos por fecha. 
Modificar el método `esCrack()` para ordenar previamente el registro de abatidos por fecha antes de evaluar la 
condición. 
- agregar todas las validaciones que consideren necesarias para que el modelo sea consistente. 
