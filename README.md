# PingPong2 - Juego en Lenguaje Jack (Arquitectura Hack)

Proyecto desarrollado para la asignatura Organización de Computadores (Universidad EAFIT, 2026-2). Consiste en una implementación del clásico juego Pong construido en lenguaje Jack en Nand2Tetris,
 enfocado en la optimización de memoria de video, captura de teclado y su movimiento dinámico.

 ## Integrantes

- Juan Daniel Martínez Fernández
- Jeronimo Estrada Arias

## Requisitos Técnicos Implementados

- **Interactividad por teclado:** Lectura en tiempo real mediante `Keyboard.keyPressed()`, evitando pausas bloqueantes para mantener la fluidez de la paleta y el entorno.
- **Entorno dinámico:** Actualización continua del fondo de pantalla durante la partida sin interferir con el renderizado de la pelota ni de la paleta.
- **Física y rebotes:** Cálculo de trayectoria y detección de colisiones contra los bordes de la pantalla y la paleta, incorporando variaciones de ángulo y aleatoriedad.
- **Visualización de puntaje:** Marcador en pantalla que se actualiza dinámicamente a medida que avanza el juego.

## Estructura del Proyecto

El código fuente está organizado de forma modular en las siguientes clases:

- `Main.jack`: Punto de entrada del programa. Inicializa la instancia principal del juego y libera la memoria al finalizar.
- `Juego.jack`: Controla el bucle principal (*game loop*), la lectura de entradas del usuario, la sincronización de cuadros y las colisiones generales.
- `Paleta.jack`: Gestiona el dibujo, borrado, posición y desplazamiento de la paleta controlada por el jugador.
- `Pelota.jack`: Encapsula las coordenadas, el tamaño, los vectores de movimiento y la lógica de rebote de la pelota.
- `Fondo.jack`: Administra el renderizado y el desplazamiento continuo de los elementos visuales del escenario.
- `Marcador.jack`: Se encarga de llevar el conteo de puntos y mostrarlo actualizado en la interfaz.
- `Azar.jack`: Implementa un generador pseudoaleatorio para variar el comportamiento inicial y los rebotes durante la partida.

## Cómo Compilar y Ejecutar

Para correr el proyecto en la suite de herramientas de Nand2Tetris, sigue estos pasos:

1. Descarga la carpeta del proyecto (`PingPong2`) y extrae los archivos en tu equipo.
2. Abre el *Jack Compiler* de Nand2Tetris y selecciona la carpeta extraída (`PingPong2`).
3. Haz clic en el botón *Compile*(o en el ícono de compilación) para generar todos los archivos `.vm` correspondientes a cada clase.
4. Abre el *VM Emulator* 
5. Carga la misma carpeta `PingPong2` dentro del emulador.
6. En la barra superior del emulador, cambia la velocidad de ejecucion a *Fast*.
7. Presiona el botón *Run* para iniciar el juego.

## Video Demostrativo

- https://youtu.be/qzvD_xUnfFY
