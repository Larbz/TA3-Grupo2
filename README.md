# TA3-Grupo2
## Integrantes
. Luis Roberto Arroyo Bonifaz - u201716094

. Roberto Carlos Basauri Quispe - u20181C074

## Link del video

https://www.youtube.com/watch?v=rURYc4T7ZrM

## Introduccion

El trabajo pide desarrollar el juego Hoop Hop Showdown – Rock Paper Scissors Hula Hoop, en el lenguaje Go y de forma concurrente, para la siguiente tarea se presenta el programa funcionando a través de la consola.

## Resumen del Código
Se crean dos estructuras, una para el equipo y otra para los jugadores. El juego funciona con un canal que controla los movimientos de los jugadores y una goroutine que se crea para cada jugador. Para esta ocasión los movimientos son aleatorios, de encontrarse los jugadores tendrán que jugar RPS, el perdedor volverá a comenzar y el ganador seguirá su camino hasta encontrar el cono y obtener los tokens. El equipo que se quede con 0 tokens es eliminado del juego y solo quedan los equipos restantes que seguiran jugando hasta que solo resulte un ganador. 

## Conclusiones y puntos de mejora
. Se puede mejorar esta primera versión del código omitiendno la clase jugador, ya que según las reglas del juego solo un jugador por cada equipo está interactuando en el "mapa". Por ende, solo es necesario almacenar un identificador dentro de la clase "equipo". Que contenga el jugador actual en juego.

. También, se puede cambiar la lógica de armado del juego, ya que según la distribución del juego, son M aros equitativos hasta un centro por cada equipo. Si son N equipos, se podría interpretar como una matriz NxM, en el que los encuentros se den en el borde derecho de la matriz o en la misma fila.

. Asimismo, se debe considerar cambiar la contención de los goroutines. Tomando en cuenta que el único momento donde se debe parar y ver el juego son el Piedra papel y tijeras, entonces es ahí donde se debería agregar un semáforo o mutex para evitar fallos, asimismo, todo movimiento adicional como saltos en aros, debería darse concurrentemente ya que no es necesario pararlos.

