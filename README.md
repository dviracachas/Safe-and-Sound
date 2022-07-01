# Intercomunicador Safe & Sound 🏍
En este repositorio se encuentra el desarrollo de la propuesta de proyecto realizada para la asignatura de Sistemas Embebidos de la Universidad Nacional de Colombia, la cual consiste en un intercomunicador para motocicletas que cuente con funcionalidades orientadas a la seguridad de sus usuarios.

## Equipo de trabajo
* Juan Gabriel Barrera Barrera
* Juan José Forero Bernal
* Camilo Andrés Jaimes Reyes
* David Santiago Viracachá Suárez

## Descripción general
El intercomunicador Safe & Sound es un producto para motociclistas que buscan comunicarse con sus pasajeros o hacer uso de funciones de audio por medio de su teléfono celular, como lo puede ser recibir indicaciones de alguna aplicación de mapas. Además, es un producto que busca la seguridad del usuario, emitiendo alertas de velocidad e implementando detección de accidentes para realizar llamadas de emergencia haciendo uso del teléfono.

## Requerimientos funcionales
* Conectarse a otro dispositivo igual o un teléfono mediante Bluetooth
* Transmitir y/o recibir audio con los dispositivos conectados
* Procesamiento de señales dadas por sensores
* Emitir alertas de velocidad al usuario
* Detectar cambios repentinos de velocidad
* Comunicación con emergencias por medio de conexión con celular

## Requerimientos no funcionales
* Dispositivo pequeño adaptable a cascos para motocicletas
* Amigable al usuario
* Duración de la batería
* Cumplir con estándares de audio Bluetooth y compatibilidad electromagnética
* Cumplir con normas establecidas para circuitos impresos

## Diagrama de bloques
![Screenshot](/Imagenes/DiagramaBloques.png)

## Diagrama de funcionamiento
[Diagrama de funcionamiento](Imagenes/Funcionamiento_safe_and_sound.pdf)


### Descripción del Hardware
Una vez identificadas las funciones y los requerimientos del intercomunicador a realizar se escogen los compontes básicos, estos son:

Componentes Básicos:
* ESP32-WROOM-32
* Acelerómetro ADXL335.
* Batería de litio de 3.7V y 280mAh.
* Amplificador de Audio MAX98357 I2S 3W clase D
* Módulo Micrófono Mems I2s Inmp441
* Mini Altavoces.
* Conectores de diversos tipos.
* Resistores.
* Capacitores
* Potenciómetro.
* Pulsadores.
* Leds.
* Conector Micro-USB hembra.
* Switch Deslizante.




