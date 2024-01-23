#ADVANCE-MAP 1.92
A-Map es la herramienta principal para modificar una ROM. Nos permite cambiar los mapeados, los tiles o los eventos del juego.
La versión con la que voy a trabajar es la 1.92, así que los ejemplos y las explicaciones están enfocadas a esta versión concreta. Además,  trabajaremos con A-Map en ingles, ya que la versión en español puede darnos problemas.
Quiero aclarar que la versión más nueva de A-Map es la 1.95. Como podéis ver en la foto posterior ambas versiones son muy antiguas, pero la más nueva vendría a ser la versión developer que nos puede dar problemas por estar menos pulida.

Aquí os dejo su web:
http://ampage.no-ip.info/

Una vez abrimos A-Map el primer pasa que siempre hemos de realizar es abrir la ROM que queramos modificar (File > Load ROM) o podemos clicar sobre el botón marcado en rojo en la imagen anterior que nos abrirá una ventana de exploración desde donde buscaremos la ROM.
Una vez cargada la ROM ya podemos empezar a trabajar. Los mapas los abriremos por “From Header”, la carpeta Map files no la tocaremos. Dentro de esta encontraremos todos los mapas ordenados por carpetas o “banks”.

Para acabar, si seleccionamos el botón rodeado en rojo podremos guardar los cambios que vamos realizando. Es recomendable hacerlo constantemente e ir haciendo copias de seguridad de la ROM modificada regularmente.
Pulsando sobre cualquier mapa lo abrimos y lo podemos visualizar:


##TILESET
Son los recuadros que nos permiten “pintar” el mapa.
MAP
Para modificar el mapa tenemos que seleccionar un bloque del tileset y posteriormente clicamos sobre el bloque del mapa que queramos modificar.
Podemos seleccionar más de un bloque del tileset con 
“CONTROL” + ”CLIC DERECHO DEL RATÓN” 
Guardad este atajo de teclado por que os ahorrará horas de mapeo si tuvieseis que modificar bloque a bloque de manera individual. Lo remarco por que hay muchos videos en internet que te enseñan a mapear que desconocen por completo que esto es posible.
El atajo nos generará una pequeña ventana flotante (Grosser block) donde podremos ver lo que tenemos seleccionado. Esto nos permitirá poner decenas de arboles con un solo clic o mover un edificio entero de lugar.
Tened en cuenta que allí donde hagas el clic deberá ser el extremo de arriba y de la izquierda de donde quieras colocar aquello seleccionado.

##BORDER BLOCK
Es un bloque que es reproducirá indefinidamente para que el jugador no pueda ver que el mapa tiene un fin. Permitiéndonos conseguir un juego más profesional pero sin aumentar casi nada el peso del juego teniendo que hacer mapas enormes innecesariamente.
Hemos de vigilar si juntamos dos mapas que tienen un border block diferente, pues se sobrepondrán el uno al otro:

Esto lo podemos solucionar de dos maneras:
    1. Haciendo pasar lejos al jugador del borde del mapa,impidiendo que pueda ver los dos border blocks.
    2. Poniendo warps que nos transporten de un mapa a otro.