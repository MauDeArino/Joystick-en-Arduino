# Joystick en Arduino
Representación gráfica de valores máximos y mínimos de traslación de un joystick para implementarlo en un control.

## Información general
El proyecto consiste en obtener gráficamente los valores máximos y mínimos de traslación de un *joystick* para adaptarlo a un control, además de su valor promedio en reposo. Un joystick es un arreglo de 2 potenciómetros que permite conocer la posición de la palanca en un eje X y un eje Y. Para leer estos valores se conectaron los canales analógicos de los potenciómetros del joystick a un Arduino MEGA y se escribió un programa en el software de Arduino que recibe los valores X y Y y los traduce de un intervalo entre 0 y 1023 a un intervalo entre -1 y 1 para desplegarlos gráficamente.

## Recolección de datos
Para llevar a cabo la lectura correctamente se escribió un código que toma los valores del X y Y del joystick a traves de entradas analógicas (A0 y A1) y los despliega en una tabla y una gráfica. La conexión del joystick al Arduino se basó en el diagrama de la Imagen 1.

![Diagrama](https://github.com/fmonter11/Joystick-en-Arduino/blob/main/Imagenes/Diagrama.png)
*Imagen 1. Circuito con joystick analógico*

Después se realizó un experimento físico que consistió en mover la palanca del joystick en diversas direcciones para obtener los valores de los ejes de traslación deseados, como puede observarse en la Tabla 1.

|         |   Eje Y:  Mínimo: 0   |   |
| :-------------: |:-------------:| :-------------:|
| **Eje X: Mínimo: 0**   | ![Joystick](https://github.com/fmonter11/Joystick-en-Arduino/blob/main/Imagenes/JoyTable.png) |**Máximo: 1023** |
|     | **Máximo: 1023**       |   |
|     | **En reposo: X: 498, Y: 517**    |   |

*Tabla 1. Valores obtenidos con el joystick analógico*

Por último, se tradujeron los valores del joystick a un intervalo de -1 a 1 y se desplegó el movimiento de la palanca de forma gráfica a través de un intervalo de tiempo, como puede apreciarse en la Gráfica 1.

![Monitor serial](https://github.com/fmonter11/Joystick-en-Arduino/blob/main/Imagenes/Monitor.png)

*Gráfica 1. Captura del Serial Plotter con gráfica sinusoidal*

El archivo Practica-joystick.ino incluye el código utilizado. 

## Implementación
Un joystick puede ser implementado en múltiples sistemas electricos que necesiten integrar un componente mecánico que indique dirección en un plano x y. En este caso el enfoque fue un control, pero los joysticks también son utilizados en muchas industrias diferentes, dos usos comunes son la dirección de sillas de ruedas eléctricas y el movimiento de brazos de maquinaria pesada como grúas.

## Contacto
Fernanda Monter y Mauricio de Ariño
