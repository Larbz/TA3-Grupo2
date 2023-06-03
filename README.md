# TA3-Grupo2
## Integrantes
. Luis Roberto Arroyo Bonifaz

. Roberto Carlos Basauri Quispe

## Introduccion

El trabajo pide desarrollar el juego Hoop Hop Showdown – Rock Paper Scissors Hula Hoop, en el lenguaje Go y de forma concurrente, para la siguiente tarea se presenta el programa funcionando a través de la consola.

## Resumen del Código
Se crean dos estructuras, una para el equipo y otra para los jugadores. El juego funciona con un canal que controla los movimientos de los jugadores y una goroutine que se crea para cada jugador. Para esta ocasión los movimientos son aleatorios, de encontrarse los jugadores tendrán que jugar RPS, el perdedor volverá a comenzar y el ganador seguirá su camino hasta encontrar el cono y obtener los tokens. El equipo que se quede con 0 tokens es eliminado del juego y solo quedan los equipos restantes que seguiran jugando hasta que solo resulte un ganador. 
