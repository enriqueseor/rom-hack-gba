# ADVANCE-MAP 1.92

A-Map es la herramienta principal para modificar una ROM. Nos permite cambiar los mapeados, los tiles o los eventos del juego.
La versión con la que voy a trabajar es la 1.92, así que los ejemplos y las explicaciones están enfocadas a esta versión concreta. Además,  trabajaremos con A-Map en ingles, ya que la versión en español puede darnos problemas.
Quiero aclarar que la versión más nueva de A-Map es la 1.95. Como podéis ver en la foto posterior ambas versiones son muy antiguas, pero la más nueva vendría a ser la versión developer que nos puede dar problemas por estar menos pulida.

![](amap-versions.png)
Aquí os dejo su web:
http://ampage.no-ip.info/

![](amap-mainframe.png)
Una vez abrimos A-Map el primer pasa que siempre hemos de realizar es abrir la ROM que queramos modificar (File > Load ROM) o podemos clicar sobre el botón marcado en rojo en la imagen anterior que nos abrirá una ventana de exploración desde donde buscaremos la ROM.
Una vez cargada la ROM ya podemos empezar a trabajar. Los mapas los abriremos por “From Header”, la carpeta Map files no la tocaremos. Dentro de esta encontraremos todos los mapas ordenados por carpetas o “banks”.

![](amap-mapfolder.png)

Para acabar, si seleccionamos el botón rodeado en rojo podremos guardar los cambios que vamos realizando. Es recomendable hacerlo constantemente e ir haciendo copias de seguridad de la ROM modificada regularmente.

Pulsando sobre cualquier mapa lo abrimos y lo podemos visualizar:
![](amap-mapopened.png)
## TILESET
Son los recuadros que nos permiten “pintar” el mapa.
MAP
Para modificar el mapa tenemos que seleccionar un bloque del tileset y posteriormente clicamos sobre el bloque del mapa que queramos modificar.
Podemos seleccionar más de un bloque del tileset con 
“CONTROL” + ”CLIC DERECHO DEL RATÓN” 
Guardad este atajo de teclado por que os ahorrará horas de mapeo si tuvieseis que modificar bloque a bloque de manera individual. Lo remarco por que hay muchos videos en internet que te enseñan a mapear que desconocen por completo que esto es posible.
El atajo nos generará una pequeña ventana flotante (Grosser block) donde podremos ver lo que tenemos seleccionado. Esto nos permitirá poner decenas de arboles con un solo clic o mover un edificio entero de lugar.
Tened en cuenta que allí donde hagas el clic deberá ser el extremo de arriba y de la izquierda de donde quieras colocar aquello seleccionado.

![](amap-grosserblock.png)
## BORDER BLOCK
Es un bloque que es reproducirá indefinidamente para que el jugador no pueda ver que el mapa tiene un fin. Permitiéndonos conseguir un juego más profesional pero sin aumentar casi nada el peso del juego teniendo que hacer mapas enormes innecesariamente.
Hemos de vigilar si juntamos dos mapas que tienen un border block diferente, pues se sobrepondrán el uno al otro:

![](amap-borderblock.png)

Esto lo podemos solucionar de dos maneras:
    1. Haciendo pasar lejos al jugador del borde del mapa,impidiendo que pueda ver los dos border blocks.
    2. Poniendo warps que nos transporten de un mapa a otro.


## MOVEMENT PERMISSIONS

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

![](amap-movpermission1.png)
![](amap-movpermission2.png)


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

### WILD POKÉMON

Cuando estamos dentro de un mapa podemos encontrar Pokémons salvajes. Estos se pueden encontrar en 4 sitios diferentes:

![](wildpokemon-site.png) 
"GRASS” (hierba alta)
“WATER” (haciendo surf)
“TREE” (utilizando miel)
“FISHING ROD” (caña de pescar).

![](wildpokemon-encounterratio.png)

Debajo tenemos el “_Encounter ratio_” que un numero que determina el % de probabilidad hay cada vez que nos ubicamos sobre un bloque con hierba alta (en este caso).

Si cliqueamos en “_Expand_” podemos añadir cualquiera de estos 4 modos para encontrar Pokémons salvajes en nuestro mapa o quitarlos:

![](wildpokemon-expand.png)

Cabe decir que la cantidad de Pokémons que podemos encontrarnos en cada sección de estas tiene un número predeterminado que no se puede modificar.

La probabilidad de que nos aparezca un Pokémon u otro viene determinado implícitamente por su posición en la tabla, no pudiendo ser modificadas dichas probabilidades.

Probabilidades con Pokémons encontrados en la hierba alta:
![](wildpokemon-grassprob.png)

Probabilidades con Pokémons pescados:
![](wildpokemon-rodprob.png)

Probabilidades con Pokémons encontrados haciendo surf:
![](wildpokemon-surfprob.png)

Probabilidades con Pokémons usando miel en un árbol:
![](wildpokemon-treeprob.png)

## HEADER

![](amap-header.png)

**Name**: Podemos ponerle o cambiarle el nombre al mapa dentro de todos los nombres que tenemos. No podemos tener más nombres del numero predeterminado que lleva la ROM.
**Show name on entering**: si queremos que se muestre el nombre del mapa cada vez que entremos.
**Weather**: indica el clima del mapa.
**Type**: indica el tipo de mapa (Village o pueblo en este caso).
**Cave**: es para definir si se puede usar la “MO Destello”.

**USED TILESETS:**
Tileset1 o principal
Tileset 2 o secundario
MAP DIMENSIONS

Nos permite cambiar las dimensiones del mapa cambiando su ancho y alto.
El tamaño del mapa es limitado y la superficie total es variable, aunque suele rondar los 7.000 bloques. Cabe decir que este tamaño es enorme, por lo que no lo consideraría una limitación como tal, sino un límite.

![](dim100x75.png)
7.500 bloques

![](dim40x172.png)
6.880 bloques

![](dim60x122.png)
7.320 bloques

EL mapa **CUADRADO** más grande que puede existir es de **86x86**. Esto es importante por ejemplo por si nos planteamos hacer un mundo abierto.
![](profheaderview.png)

Si hacemos “**CONTROL + H**” en el HEADER podemos ver la “_Professional Header View_”.


## INSERTANDO MAPAS

### CREANDO NUEVOS MAPAS

Es frecuente que en el nuestro juego queramos más mapas de los que ya tenemos. Para ello podemos necesitar más mapas.

![](new-map.png)

Con el juego abierto cliqueamos sobre el botón marcado arriba.

(**“Create new Map”**)

![](create-new-map.png)

Nos aparecerá un panel que nos pedirá los parámetros básicos del mapa:
- Nombre del mapa (Map name)
- anchura (Width
- altura (Height)
- Tileset principal (Tileset 1)
- Tileset secundario (Tileset 2)

![[blank-map.png]]

Una vez creado nos aparecerá un mapa así con los tilesets seleccionados. Ahora nos tocará “pintar”.
![[new-map-done.png]](.png)

Una vez hayamos acabado nos hemos acordar de establecer las “_Movement Permissions_”:

![[default-permissions.png]]

Como podéis ver si insertamos así el mapa en el juego el personaje podrá caminar por todos los bloques. Por eso hemos de establecer las prohibiciones.(1).

![](permissions-set.png)

![](insert-map.png)

Ahora debemos clicar el botón de insertar (_I__nsert map_).

Se nos abrirá una pestaña como la siguiente:
![](bank.png)  
Dentro de la opción “_Create_ _new_ _space_” seleccionamos el “_Bank_” donde queremos que es coloque nuestro mapa. En mi caso le diré que en cree uno nuevo.

### CREANDO NUEVAS CONEXIONES

Una vez hemos creado un nuevo mapa lo tenemos que conectar con otros para que el jugador pueda acceder a él. Para ello creamos “conexiones”.

**NOTA: hemos de tener en cuenta que este tipo de conexiones son directas, no usando un WARP. Por tanto, los tilesets 2 de ambos mapas tendrán que ser los mismos, sino el resultado no sera óptimo. Siempre que no impidamos que el jugador pueda ver el border block allí donde se unen ambos.**
![[connection-button.png]]

Si seleccionamos el botón que tiene 4 flechas se nos abrira un menú como el siguiente:
![[connections.png]]

Aquí tendremos las siguientes opciones:
- Número de conexiones que tiene el mapa
- Dirección de cada conexión
- El “_Bank_” del mapa
- El nº del mapa

Si seleccionamos “_Add_” nos agregara una nueva conexión. Después hemos de cambiar la “_Direction_” de “_Nothing_” a la dirección que queramos, en mi caso por ejemplo a “_Right_”.

![[connections-options.png]]

Además hemos de indicar el número de mapa que queremos agregar (en el nuestro caso 0) y el su “_B__ank_”, en este caso el 34.

Este proceso lo hemos de repetir en ambos mapas. Un vez hecho esto podemos ver el resultado final:
![[connection-result.png]]

Ahora vamos atratar el offset, que antes no lo hemos tenido en cuenta. Este nos será de utilidad cuando queramos conectar dos mapas que tengas dos lados diferentes y que necesitamos que encajen de una manera determinada.

Un ejemplo de ello sería por ejemplo las 3 conexiones que tiene ciudad verde en Pokémon Rojo Fuego, en donde las 3 rutas que convergen en la ciudad son más estrechas que la misma.
  
Si no modificáramos en offset los mapas se unirían tal que así:
![[connection-offset-exp.png]]
Lo normal es que quisiésemos centrar las rutes que confluyen en nuestra ciudad, y para ello hemos de modificar el offset.

Para saber que valor le hemos de dar contamos el número de bloque desde la parte izquierda o superior de cada mapa, teniendo en cuenta por que lado estará nuestra conexión.

Ciudad verde peor ejemplo con su ruta inferior (ruta 1) tiene el punto de la conexión por la izquierda en el bloque 22, i la ruta 1 en el bloque 10.

Si restamos 10 a 22 nos da 12, es por eso que vemos el valor 12 en el offset de ciudad verde. Por el otro lado si restemos 22 a 10 tendremos como a resultado -12 siendo el valor que vemos en el offset de la ruta.

Como podéis ver el valor del offset siempre será el mismo numero pero en vez de positivo en negativo en el mapa pequeño.

### BLOCK EDITOR

El editor de bloques nos permitirá editar el tileset de cada uno de los mapas, bien por que queramos renovar completa o parcialmente loa gráficos de la ROM original o por motivos de guion nos veamos obligados a insertar elementos que no existen en la ROM original.

En los mapas hay un tileset principal (Tileset 0) y uno secundario (Tileset 1). En el principal encontramos los gráficos que se utilizan constantemente. Es por eso que el Tileset exterior principal siempre sera el mismo (el numero 0, lo podéis comprobar en el “_H__eader_”), y el que cambiará normalmente sera el secundario.

![[blockeditor-btn.png]]

El Block Editor es una opción del A-MAP que nos cambiar o editar nuestro tiles. Para acceder a el clicamos el icono con forma de pieza de puzzle. Obviamente hemos de tener abierto algún mapa para acceder a él.

#### BLOCK EDITOR WORKAREA
![[blockeditor-workarea.png]]

**TILESET**
Hi tenim tots els blocs que podem utilitzar actualment a l’hora de mapejar. Aquests blocs es poden editar amb elements del tileset

**PALETA**
Esta compuesta por bloques de 8x8 que nos permites crear los bloques del tileset en la pestaña down/up. Estas paletas las descargaremos, modificaremos y volveremos a cargar en la ROM para insertar bloques nuevos.

**DOWN/UP**
Carga la composición del bloque en dos cuadrados diferentes. Los bloques están compuestos por una parte inferior y una superior. Permitiéndonos crear bloques que sean la combinación de otros, como por ejemplo la copa de un árbol con yerba alta detrás, como podéis ver en el tileset.

**X-FLIP i Y-FLIP**
Sirven para voltear las tiles de 8x8 de manera que cuando creemos bloques simétricos o diferentes bloques simétricos entre ellos solo necesitaremos insertar un bloque de 8x8 y voltear-lo, ahorrando espacio.

**PALETTE0**
Nos permite seleccionar cualquiera de las 12 paletas que podemos tener en el juego. Cada una de ellas puede tener como máximo 15 colores, más 1 color que actúa como transparencia.

LAS PALETES 0-6 CORRESPONDEN AL TILESET 0 Y LAS 7-12 AL TILESET 1

En Pokémon Rojo Fuego cada paleta se usa para lo siguiente:

|Palette0|Arboles, hierba, arbustos, etc.|
|--------|-------------------------------|
|Palette1|Montaña|
|Palette2|Centro Pokémon|
|Palette3|Tienda Pokémon|

**BEHAVIOR-BYTE**
![[behavior-byte.png]]
- **Use warp/use door warp**: Para que sobre el bloque funcionen los warps
- **Grass animation (Pokémon):** Al pisar el bloque se ejecuta la animación de hierba alta.
- **Arrow (Direction) => Warp **“X” of Block**: Permite que funcionen os warps sobre el bloque en una dirección específica.
- **00**: Sin comportamiento

**BACKGROUND-BYTE**
![[background-byte.png]]
- **00**: el bloque cubre al jugador.
- **Block is covered by hero**: Cuando creamos un bloque con una parte superior y otra inferior, nuestro héroe por defecto estará en la capa de en medio, si queremos que la parte superior este detrás del héroe cuando pasa sobre el debemos debemos seleccionar esta opción.

#### BLOCK EDITOR TOOLBAR
![[blockeditor-picture.png]]

**PICTURE**
- **Save tileset** **1**: Exporta la imagen del tileset principal
- **Load tileset** **1**: Importa la imagen del tileset principal
- **Save tileset 2**: Exporta la imagen del tileset secundari
- **Load tileset 2**: Importa la imatge del tileset secundari
- **Load new blocks**: refresca los bloques que han sido modificados en los tilesets.

![[blockeditor-blocks.png]]
**BLOCKS**
- **Save tileset 1**: Exporta l’orde dels blocs del tileset principal
- **Load tileset 1**: Importa l’orde dels blocs del tileset principal
- **Save tileset 2**: Exporta l’orde dels blocs del tileset secundari
- **Load tileset 2**: Importa l’orde dels blocs del tileset secundari
- **Change amount**: Cambia la cantidad de bloques del tileset secundario.

![[blockeditor-palettes.png]]
#### PALETTES
- **Show palette editor**: Muestra el editor de paletas.

![[palette-form.png]]

Podemos ver los 16 colores que conforman la paleta. El primero es el color transparente.
- **Write palette changes to ROM**: Guarda los cambios que hayamos hecho en las paletas en la ROM
- **Write current palette to file**: Exporta la paleta en forma de archivo
- **Load current palette from file**: Carga una paleta desde un archivo externo.
- **Change palette definition of block data**: Cambia todos los tiles de una determinada paleta a otra definida por el usuario.

### INSERTAR TILES

En primer lugar necesitamos descargar-nos los tiles de internet:
![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_fbe8d2ca.png)

Pongamos que queremos insertar estos tiles. Os tenéis que asegurar que los tiles no contengan más de 15 colores diferentes, así que buscad tiles específicos para ROM hacking si os queréis ahorrar trabajo.

Abriremos la herramienta tileHelperAvance.

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_c4b1b7d.png)

Y abrimos el archivo del tile:

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_e27b350e.png)

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_42927ce6.png)

Cliqueamos en “_C__onvert tileset_”:

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_4588944f.png)

Nos saldrá una especie de error, no sufráis, es normal.

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_193592c6.png)

Seleccionamos “_S__ave palette_” y guardemos el archivo como “_A__dvance__M__ap_ _1.92-P__alette_ _(__.__pal)_” en mi cas, si usais A-Map 1.95 ya sabeis...

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_e58294f3.png)

Ahora abrimos abrimos AdvanceMap y en el Block Editor seleccionamos lo siguiente:

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_64c6718f.png)

Seleccionamos el archivo .pal que hemos guardado hace un momento. Esto nos cargará la paleta que tenía nuestro tile. Ahora vamos a “_Picture_” y guardamos el tileset 2.

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_a03b752d.png)

Nos lo hará guardar en formato “_Device Intependent Bitmap o .dib_”

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_124fc0da.png)

Ahora abrimos este archivo con Paint o similares y pegamos en este archivo el tile que queríamos insertar.

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_fc103798.png)

Quedaría así insertado:

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_6a92c6f9.png)

Guardemos y vamos a Advanced Map de nuevo

Entonces hacemos lo siguiente:

![](file:///tmp/lu72631dwsm.tmp/lu72631dwsp_tmp_e9413a9a.png)

**EL RESULTADO FINAL NO FUE SATISFACTORIO**