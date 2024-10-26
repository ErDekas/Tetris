# README

## Descripción del Proyecto

Este código implementa un juego de tipo Tetris utilizando JavaScript y la biblioteca p5.js. En el juego, los jugadores controlan piezas que caen desde la parte superior de la pantalla, las cuales deben ser movidas y rotadas para formar líneas completas en un grid. Cuando se forma una línea completa, se elimina y el jugador gana puntos. El objetivo es evitar que las piezas acumulen hasta la parte superior de la pantalla.

## Estructura del Código

### Variables Principales

- **gridSpace**: Define el tamaño de cada espacio en el grid.
- **fallingPiece**: Representa la pieza que está cayendo actualmente.
- **gridPieces**: Arreglo que almacena todas las piezas que han sido colocadas en el grid.
- **currentScore**: Mantiene el puntaje actual del jugador.
- **currentLevel**: Indica el nivel actual del juego.
- **linesCleared**: Cuenta cuántas líneas han sido eliminadas.
- **pauseGame** y **gameOver**: Controlan el estado del juego.

### Funciones Clave

- **setup()**: Inicializa el canvas y la primera pieza que caerá.
- **draw()**: Se ejecuta en un bucle para actualizar y dibujar el estado del juego. Maneja la lógica de colisiones, la caída de las piezas y la visualización de la interfaz de usuario.
- **keyPressed()**: Maneja la entrada del teclado para mover y rotar las piezas, así como reiniciar el juego.

### Clases

1. **PlayPiece**: Representa la pieza que cae, maneja su posición, rotación y las colisiones con otras piezas y los límites del juego.
2. **Square**: Representa cada cuadrado de una pieza y su visualización.
3. **Worker**: Realiza el trabajo de mover las piezas cuando se eliminan líneas.

### Mecanismos de Juego

- **Colisiones**: Se verifica si la pieza puede moverse o rotar sin chocar con otras piezas o los bordes del área de juego.
- **Eliminación de Líneas**: Cuando se forma una línea completa, se elimina y las piezas por encima se mueven hacia abajo.
- **Puntaje y Niveles**: Se acumula puntaje a medida que se eliminan líneas, y cada 10 líneas eliminadas se aumenta la dificultad al acelerar la caída de las piezas.

### Controles

- **Flecha Izquierda**: Mover la pieza hacia la izquierda.
- **Flecha Derecha**: Mover la pieza hacia la derecha.
- **Flecha Arriba**: Rotar la pieza.
- **Flecha Abajo**: Acelerar la caída de la pieza.
- **Tecla R**: Reiniciar el juego.

## Cómo Ejecutar el Juego

1. Asegúrate de tener la biblioteca p5.js incluida en tu proyecto.
2. Copia y pega el código en un archivo HTML o en un entorno compatible con p5.js.
3. Abre el archivo en un navegador web para jugar.
