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


## Descripción del Hardware
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

# Esp32-WROOM-32:

Se selecciona esta tarjeta chip teniendo en cuenta que esta permite una variedad de aplicaciones gracias a que mediante sus pines es posible la conexión de diferentes periféricos, cuenta con Wi-Fi, Bluetooth y Bluetooth LE MCU, permite el procesamiento de datos y es común en aplicaciones electrónicas portátiles alimentadas por batería. La tarjeta mencionada se ve a continuación:
 
Para este caso en específico se usará el Bluetooth para conectar el intercomunicador con un teléfono móvil, de este modo se transmitirán y recibirán señales de voz y de audio entre estos dos dispositivos. El procesamiento de datos se realizará una vez se reciban señales del acelerometro que se describirá posteriormente.
La tarjeta Esp32-WROOM-32 tiene las siguientes especificaciones según su fabricante: 
* Tensión de operación/Fuente de alimentación: 3.0V – 3.6V.
* Corriente de operación: 80mA promedio.
* Corriente mínima que debe ser entregad por la fuente de alimentación:  500mA.
* Rango de temperatura ambiente para su óptima operación: -40°C ~ + 85°C 
* Tamaño: 18mm x 25.5mm x 3.10mm.
* Interfaces del módulo: Tarjeta SD, UART, SPI, SDIO, I2C, LED PWM, Motor PWM, I2S, IR, GPIO, entre otros.
* Certificación Bluetooth: BQB.
* Protocolos Bluetooth: Bluetooth v4.2 BR/EDR and Bluetooth LE specification.
* Audio Bluetooth: CVSD y SBC.
* Microprocesador: Xtensa® single-/dual-core 32-bit LX6.
* ROM: 448KB.
* SRAM: 520KB.

# Acelerómetro ADXL335:
Con el fin de identificar cambios repentinos de la velocidad e inclinación del usuario (posibles accidentes) se usará el acelerómetro ADXL335 de 3 ejes mediante el cual es posible medir aceleraciones. Este módulo es ideal para aplicaciones de detección de inclinación gracias a que con este es posible medir la aceleracion estática de la gravedad así como la aceleración dinámica resultante de movimientos, choques o vibraciones. Las mediciones ejecutadas por este acelerómetro serán procesadas por medio de la Esp32 con el fin de interpretarlas de modo que se identifiquen posibles accidentes para la emisión de alertas. El acelerómetro se observa en la siguiente imagen: 
 
Especificaciones básicas de operación:
* Rando de de tensión para su funcionamiento: 1.8V – 3.6V.
* Corriente de alimentación: 350uA.
* Rango de temperatura para su funcionamiento: -40°C ~ + 85°C
* Rango de medición: +/-3g.
* Salida: Análoga.

# Amplificador de Audio MAX98357 I2S 3W clase D
Ampificador clase D (amplificador de switcheo de alta eficiencia) con entrada de modulación de código de pulso digital mediante el cual se realizará la amplificación de las señales de audio que se deseen transmitir por medio de los altavoces. Este módulo emplea el protocolo de transmision de señales de audio digital I2S y es frecuente en dispositivos portatiles por su eficiencia.
 
Especificaciones: 
* Tensión de alimentación: 2.5V – 5.5V.
* Corriente nominal: 2.4mA.
* Potencia de salida: 3.2W con una carga de 4Ohms a 5V, 1.8W con una carga de 8 Ohms a 5V.
* Entrada de audio: I2S.
* Ganancia de amplificación predeterminada: 9dB.
* Posibles ganancias de amplificación: 3, 6, 9, 12 y 15 dB.
* Frecuencia de muestreo: 8kHz – 96kHz.
* Salidas de audio: izquierda, derecha o (derecha+izquierda)/2.

