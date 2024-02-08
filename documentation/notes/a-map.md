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
- **Arrow (Direction) => Warp “X” of Block**: Permite que funcionen os warps sobre el bloque en una dirección específica.
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