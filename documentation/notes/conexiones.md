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