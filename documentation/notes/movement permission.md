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
