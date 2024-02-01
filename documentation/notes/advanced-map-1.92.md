# ADVANCE-MAP 1.92

A-Map es la herramienta principal para modificar una ROM. Nos permite cambiar los mapeados, los tiles o los eventos del juego.
La versión con la que voy a trabajar es la 1.92, así que los ejemplos y las explicaciones están enfocadas a esta versión concreta. Además,  trabajaremos con A-Map en ingles, ya que la versión en español puede darnos problemas.
Quiero aclarar que la versión más nueva de A-Map es la 1.95. Como podéis ver en la foto posterior ambas versiones son muy antiguas, pero la más nueva vendría a ser la versión developer que nos puede dar problemas por estar menos pulida.

![](advancedmap-versions.png)
Aquí os dejo su web:
http://ampage.no-ip.info/

![](advancedmap-mainframe.png)
Una vez abrimos A-Map el primer pasa que siempre hemos de realizar es abrir la ROM que queramos modificar (File > Load ROM) o podemos clicar sobre el botón marcado en rojo en la imagen anterior que nos abrirá una ventana de exploración desde donde buscaremos la ROM.
Una vez cargada la ROM ya podemos empezar a trabajar. Los mapas los abriremos por “From Header”, la carpeta Map files no la tocaremos. Dentro de esta encontraremos todos los mapas ordenados por carpetas o “banks”.

![](advancedmap-mapfolder.png)

Para acabar, si seleccionamos el botón rodeado en rojo podremos guardar los cambios que vamos realizando. Es recomendable hacerlo constantemente e ir haciendo copias de seguridad de la ROM modificada regularmente.

Pulsando sobre cualquier mapa lo abrimos y lo podemos visualizar:
![](advancedmap-mapopened.png)
## TILESET
Son los recuadros que nos permiten “pintar” el mapa.
MAP
Para modificar el mapa tenemos que seleccionar un bloque del tileset y posteriormente clicamos sobre el bloque del mapa que queramos modificar.
Podemos seleccionar más de un bloque del tileset con 
“CONTROL” + ”CLIC DERECHO DEL RATÓN” 
Guardad este atajo de teclado por que os ahorrará horas de mapeo si tuvieseis que modificar bloque a bloque de manera individual. Lo remarco por que hay muchos videos en internet que te enseñan a mapear que desconocen por completo que esto es posible.
El atajo nos generará una pequeña ventana flotante (Grosser block) donde podremos ver lo que tenemos seleccionado. Esto nos permitirá poner decenas de arboles con un solo clic o mover un edificio entero de lugar.
Tened en cuenta que allí donde hagas el clic deberá ser el extremo de arriba y de la izquierda de donde quieras colocar aquello seleccionado.

![](advancedmap-grosserblock.png)
## BORDER BLOCK
Es un bloque que es reproducirá indefinidamente para que el jugador no pueda ver que el mapa tiene un fin. Permitiéndonos conseguir un juego más profesional pero sin aumentar casi nada el peso del juego teniendo que hacer mapas enormes innecesariamente.
Hemos de vigilar si juntamos dos mapas que tienen un border block diferente, pues se sobrepondrán el uno al otro:

![](advancedmap-borderblock.png)

Esto lo podemos solucionar de dos maneras:
    1. Haciendo pasar lejos al jugador del borde del mapa,impidiendo que pueda ver los dos border blocks.
    2. Poniendo warps que nos transporten de un mapa a otro.


### MOVEMENT PERMISSIONS

Indican por que bloques puede pasar el jugador y por cuales no. Cada permiso esta representado por un numero hexadecimal sobre cada bloque.

Habitualmente apenas se utilizan de forma recurrente 2 de ellos, la C por donde el jugador puede pasar y el 1, por donde el jugador no puede pasar. Además del 4 que se utiliza para el agua.

Obviamente los permisos se pueden enriquecer mucho más, especialmente cuando en un mapa encontramos distintas elevaciones, sobretodo si no podemos colocar un bloque rojo entre los dos niveles a distintas alturas.

Es por ello que la inmensa mayoría de los permisos consisten en permitir o no permitir pasar al jugador, pero en distintos niveles de elevación, existiendo hasta 13 de ellos.

Solo existen 2 excepciones a esta regla:
- 4: solo se puede transitar con el haciendo Surf.
- 3C: permite que el personaje pase tanto por encima como por debajo del mismo.

**CONSEJO: HACIENDO CLIC EN LA BOLA DE RATÓN PODEMOS SUBSTITUIR UN CONJUNTO DE BLOQUES POR OTRO.**

Aquí tenéis la tabla con todos los permisos explicados:
 
| 0  | Cambio elevación            |
|----| --------------------------- |
| 1  | <div style="background:red">Intransitable</div>|
| 2  | ambiguo                     |
| 3  | ambiguo                     |
| 4  | <div style="background:pink">Surfeable (MO surf, agua)</div>|
| 5  | Intransitable (elevación 0) |
| 6  | ambiguo                     |
| 7  | ambiguo                     |
| 8  | Transitable (elevación 1)   |
| 9  | Intransitable (elevación 1) |
| A  | ambiguo                     |
| B  | ambiguo                     |
| C  | <div style="background:purple">Transitable (elevación 2)</div>|
| D  | Intransitable (elevación 2) |
| E  | ambiguo                     |
| F  | ambiguo                     |
| 10 | <div style="background:green">Transitable (elevación 3)</div>|
| 11 | Intransitable (elevación 3) |
| 12 | ambiguo                     |
| 13 | ambiguo                     |
| 14 | Transitable (elevación 4)   |
| 15 | Intransitable (elevación 4) |
| 16 | ambiguo                     |
| 17 | ambiguo                     |
| 18 | Transitable (elevación 5)   |
| 19 | Intransitable (elevación 5) |
| 1A | ambiguo                     |
| 1B | ambiguo                     |
| 1C | Transitable (elevación 6)   |
| 1D | Intransitable (elevación 6) |
| 1E | ambiguo                     |
| 1F | ambiguo                     |
| 20 | Transitable (elevación 7)   |
| 21 | Intransitable (elevación 7) |
| 22 | ambiguo                     |
| 23 | ambiguo                     |
| 24 | Transitable (elevación 8)   |
| 25 | Intransitable (elevación 8) |
| 26 | ambiguo                     |
| 27 | ambiguo                     |
| 28 | Transitable (elevación 9)   |
| 29 | Intransitable (elevación 9) |
| 2A | ambiguo                     |
| 2B | ambiguo                     |
| 2C | Transitable (elevación 10)  |
| 2D | Intransitable (elevación 10)|
| 2E | ambiguo                     |
| 2F | ambiguo                     |
| 30 | Transitable (elevación 11)  |
| 31 | Intransitable (elevación 11)|
| 32 | ambiguo                     |
| 33 | ambiguo                     |
| 34 | Transitable (elevación 12)  |
| 35 | Intransitable (elevación 12)|
| 36 | ambiguo                     |
| 37 | ambiguo                     |
| 38 | Transitable (elevación 13)  |
| 39 | Intransitable (elevación 13)|
| 3A | ambiguo                     |
| 3B | ambiguo                     |
| 3C | <div style="background:blue">Transitable por encima y por debajo (puentes) </div>|
| 3D | ambiguo                     |
| 3E | ambiguo                     |
| 3F | ambiguo                     |

En la siguiente página tenéis un ejemplo con la puesta en práctica de lo que hemos aprendido, llevando al límite los permisos jugando con las distintas elevaciones:

![](advancedmap-movpermission1.png)
![](advancedmap-movpermission2.png)


## EVENTS
### PERSON EVENT
Nos permite añadir personas en el mapa, conocidos como minisprites o minis. Los cuales podemos situar en cualquier punto del mapa y elegir dentro de los minis que tenemos en el juego el que queramos.
Si no le asociamos un script al mini y hablamos con él, el juego quedará congelado.
OPCIONES DE EDICIÓN
Person event no
id asociado dentro de el mapa
Picture no
id del minisprite dentro del listado de minis
Pos(X/Y)
Posición en el mapa
Movement type
El movimiento que hará el mini
Trainer
Si esta seleccionado es un entrenador
View radius
Distancia a la que nos puede ver un mini (entrenador)

### SIGNPOST EVENT
Se utilizan en carteles de ciudades y rutas o para objetos ocultos.
OPCIONES DE EDICIÓN
Talking level
Tiene relación con los niveles de altura, en “always” nos  ahorramos problemas.
Signpost type
0-4 son scripts para carteles y del 5-7 objectos ocultos.
Script offset
El lugar de memoria donde esta guardado el script asociado al signpost.

### WARP EVENT
Son los que nos llevan de un mapa a otro que no esta conectado.
Se ponen en la entrada de casas, cuevas, escaleras, etc. Configurar los es muy fácil,
 solo necesitamos poner dos warps que se apunten mutuamente.
Haciendo doble clic sobre cualquiera nos abrirá automáticamente el mapa al que nos lleva.
OPCIONES DE EDICIÓN
No
Id del warp seleccionado en el mapa en el que estamos
Pos(X/Y)
Posición en el mapa
To Warp no
Id del warp al que nos dirigirá dentro de su mapa.
Map bank
Id del bank en donde se encuentra el otro warp
Map
Id del mapa al que nos llevará el warp

En el ejemplo anterior podemos ver que el warp que tenemos seleccionado nos llevará a un mapa en el bank 1, dentro de ese bank hay un mapa que es el numero 88 y dentro de este mapa hay un warp que tiene de id 1. Esto ultimo es importante para aparecer justo en el warp del mapa que querais y no en cualquier otro.