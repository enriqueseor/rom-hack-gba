# ADVANCE-MAP 1.92

A-Map es la herramienta principal para modificar una ROM. Nos permite cambiar los mapeados, los tiles o los eventos del juego.
La versión con la que voy a trabajar es la 1.92, así que los ejemplos y las explicaciones están enfocadas a esta versión concreta. Además,  trabajaremos con A-Map en ingles, ya que la versión en español puede darnos problemas.
Quiero aclarar que la versión más nueva de A-Map es la 1.95. Como podéis ver en la foto posterior ambas versiones son muy antiguas, pero la más nueva vendría a ser la versión developer que nos puede dar problemas por estar menos pulida.

Aquí os dejo su web:
http://ampage.no-ip.info/

Una vez abrimos A-Map el primer pasa que siempre hemos de realizar es abrir la ROM que queramos modificar (File > Load ROM) o podemos clicar sobre el botón marcado en rojo en la imagen anterior que nos abrirá una ventana de exploración desde donde buscaremos la ROM.
Una vez cargada la ROM ya podemos empezar a trabajar. Los mapas los abriremos por “From Header”, la carpeta Map files no la tocaremos. Dentro de esta encontraremos todos los mapas ordenados por carpetas o “banks”.

Para acabar, si seleccionamos el botón rodeado en rojo podremos guardar los cambios que vamos realizando. Es recomendable hacerlo constantemente e ir haciendo copias de seguridad de la ROM modificada regularmente.
Pulsando sobre cualquier mapa lo abrimos y lo podemos visualizar:


## TILESET
Son los recuadros que nos permiten “pintar” el mapa.
MAP
Para modificar el mapa tenemos que seleccionar un bloque del tileset y posteriormente clicamos sobre el bloque del mapa que queramos modificar.
Podemos seleccionar más de un bloque del tileset con 
“CONTROL” + ”CLIC DERECHO DEL RATÓN” 
Guardad este atajo de teclado por que os ahorrará horas de mapeo si tuvieseis que modificar bloque a bloque de manera individual. Lo remarco por que hay muchos videos en internet que te enseñan a mapear que desconocen por completo que esto es posible.
El atajo nos generará una pequeña ventana flotante (Grosser block) donde podremos ver lo que tenemos seleccionado. Esto nos permitirá poner decenas de arboles con un solo clic o mover un edificio entero de lugar.
Tened en cuenta que allí donde hagas el clic deberá ser el extremo de arriba y de la izquierda de donde quieras colocar aquello seleccionado.

## BORDER BLOCK
Es un bloque que es reproducirá indefinidamente para que el jugador no pueda ver que el mapa tiene un fin. Permitiéndonos conseguir un juego más profesional pero sin aumentar casi nada el peso del juego teniendo que hacer mapas enormes innecesariamente.
Hemos de vigilar si juntamos dos mapas que tienen un border block diferente, pues se sobrepondrán el uno al otro:

Esto lo podemos solucionar de dos maneras:
    1. Haciendo pasar lejos al jugador del borde del mapa,impidiendo que pueda ver los dos border blocks.
    2. Poniendo warps que nos transporten de un mapa a otro.

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