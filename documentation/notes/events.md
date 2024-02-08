## EVENTS

### PERSON EVENT
![](amap-personevent.png)
Nos permite añadir personas en el mapa, conocidos como minisprites o minis. Los cuales podemos situar en cualquier punto del mapa y elegir dentro de los minis que tenemos en el juego el que queramos.
Si no le asociamos un script al mini y hablamos con él, el juego quedará congelado.

|OPCIONES DE EDICIÓN|                                                 |
|---------------|-----------------------------------------------------|
|Person event no|id asociado dentro de el mapa                        |
|Picture no     |id del minisprite dentro del listado de minis        |
|Pos(X/Y)       |Posición en el mapa                                  |
|Movement type  |El movimiento que hará el mini                       |
|Trainer        |Si esta seleccionado es un entrenador                |
|View radius    |Distancia a la que nos puede ver un mini (entrenador)|

### SIGNPOST EVENT

![](amap-signpostevent.png)
Se utilizan en carteles de ciudades y rutas o para objetos ocultos.
 
|OPCIONES DE EDICIÓN|                                                                        |
|-------------|------------------------------------------------------------------------------|
|Talking level|Tiene relación con los niveles de altura, en “always” nos ahorramos problemas.|
|Signpost type|0-4 son scripts para carteles y del 5-7 objectos ocultos.                     |
|Script offset|El lugar de memoria donde esta guardado el script asociado al signpost.       |

### WARP EVENT

![](amap-warpevent.png)
Son los que nos llevan de un mapa a otro que no esta conectado.
Se ponen en la entrada de casas, cuevas, escaleras, etc. Configurar los es muy fácil, solo necesitamos poner dos warps que se apunten mutuamente.
Haciendo doble clic sobre cualquiera nos abrirá automáticamente el mapa al que nos lleva.
 
|OPCIONES DE EDICIÓN|                                            |
|----------|-----------------------------------------------------|
|No        |Id del warp seleccionado en el mapa en el que estamos|
|Pos(X/Y)  |Posición en el mapa                                  |
|To Warp no|Id del warp al que nos dirigirá dentro de su mapa.   |
|Map bank  |Id del bank en donde se encuentra el otro warp       |
|Map       |Id del mapa al que nos llevará el warp               |

En el ejemplo anterior podemos ver que el warp que tenemos seleccionado nos llevará a un mapa en el bank 1, dentro de ese bank hay un mapa que es el numero 88 y dentro de este mapa hay un warp que tiene de id 1. Esto ultimo es importante para aparecer justo en el warp del mapa que querais y no en cualquier otro.

### SCRIPT EVENT

En español se conocen como scripts de gatillo, pues “saltan” cuando el jugador se ubica sobre el bloque en donde están colocados.

![](amap-scriptevent.png)

Aquí podemos ver la primera ruta de Pokémon Esmeralda, donde nos encontraremos al profesor siendo atacado por un Pokémon salvaje. Todos elos scripts que vemos al lado del que esta seleccionado son iguales, no permitiendo que el personaje se pueda ir de la acción en mitad del evento.
Para verlo solo tenéis que cliquear sobre “_Open script_”

![](amap-scriptcode.png)

|#dynamic 0x900000|indica que el offset del script será de tipo dinámico y empezará a buscar un espacio libre en memoria a partir del offset 900000|
|---|---|
|#org @start|Start es el puntero que indica el inicio del script. Cada puntero tiene una dirección en memoria, nosotros tenemos que colocarle la de start al script offset|
|lockall|Bloquea todos los elementos en movimiento, jugador incluido.|
|Msgbox @string1<br><br>MSG_KEEPOPEN|Genera una caja con mensaje y la mantiene abierta|
|closeonkeypress|Cierra la caja con mensaje cuando el jugador pulsa un botón|
|Applymovement MOVE_PLAYER @move1|Aplica movimiento a un mini<br><br>Indica que el mini al que se le aplican los movimientos es el del jugador<br><br>Mueve un bloque a la derecha al jugador|
|realeaseall|Deshace el lockall inicial|
|end|Final del script|

Como es un tema extraordinariamente extenso lo veremos por separado mas adelante.