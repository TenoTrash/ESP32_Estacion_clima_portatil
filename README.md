Monitoreo de clima portatil con ESP32 y BME280

Con una pantalla OLED y un par de pantallas con:

    Resumen de clima
    Temperatura
    Humedad
    Presion
    Altitud (relativa Buenos Aires con respecto a la presón atmosférica)
    Creditos

Se van ciclando las pantallas con un pulsador (con control anti rebote simple)

Las lecturas del BME280 se hacen cada minuto, en el menor sampleo posible, según lo indicado por el fabricante en la hoja de datos. Esto minimiza el diferencial de temperatura debido al consumo de energía y mejora notablemente la presición de la medición.

Faltan varias cosas y estoy pensando en apagar y prender tanto el sensor como la pantalla mediante un pin digital, acerca de mejorar el consumo de batería cuando no se necesitan.

Y armar los estados de deep sleep!

Conexiones:
============

Pantalla OLED SPI (7 pines):
----------------------------
GND -> GND
VCC -> 3V3
D0  -> D18 (gpio 18 )
D1  -> D23 (gpio 23 )
RES -> TX2 (gpio 17 )
DC  -> RX2 (gpio 16 )
CS  -> D5  (gpio 5 )

BME 280:
--------
VCC -> 3V3
GND -> GND
SCL -> D22 (gpio 22 )
SDA -> D21 (gpio 21 )
CSE -> n/a
SDO -> n/a


Pulsador -> (gpio 13 )
----------------------

Gracias!!!