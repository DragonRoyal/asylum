# dari // alexren's super cool weather station submission

Here's my submission for my weather station! Under the asylum "raincloud"

## Features:
- Displays:
    - Moon phases
    - Temperature 
    - Icons
- 8 WS2812Bs for dynamic LED effects
- A switch to swap between Freedom units and regular human units
- Breakout pins to add an indoor temp sensor + UART breakouts

## PCB
Here's a picture of my schematic! I wired a Wemos ESP32-C3* module to a TFT display, 8 WS2812B LEDs, a switch for Farenheit vs Celsius, and broken out headers for a DHT22 Sensor!

Schematic            |  PCB
:-------------------------:|:-------------------------:
![](assets/schematic.png)  |  ![](assets/pcb.png)

*For my actual build, I'm using a WeMos ESP32-S3 module instead since it's cheaper and I don't need the bluetooth functionality! As a bonus theres 2x the amount of GPIO to work with if I ned to in the future.

[ x ] I ran DRC in KiCad and have made sure there are 0 errors!

## CAD Model:
Everything fits together using 4 M3 Heatset inserts and 4 M3x16mm screws. Here's how it looks:

![Screenshot 2025-01-27 211719](https://github.com/user-attachments/assets/c8eca3a7-d0ad-49ec-87fa-2eafcd7997ae)
![Screenshot 2025-01-27 211705](https://github.com/user-attachments/assets/61288338-cd65-4beb-baaf-4ae4430ad419)

Made in solidworks
## Firmware overview
The firmware for this is written in Arduino. It grabs the weather info using an api request to mateoweather. Then, it uses the Adafruit_GFX library to push the data to the screen


[ x ] I remembered to exclude any personal information, including API Keys, WiFi passwords, etc


## BOM
All prices must be in USD.

Provided by dari // alex:
- 1x WeMos S2 Mini (as a cheaper replacement for the S2) WITHOUT FEMALE HEADERS
- 1x ST7735 1.8" LCD display WITHOUT FEMALE HEADERS. Male headers soldered!
- 1x 3D printed case

Purchasing from HQ:
- 8x WS2812Bs at $0.20/per. I will be losing $1.6 from my grant as a result.

I will be sourcing the following parts with my grant:
- 1x PCB from JLCPCB
    - $2 for 5x + $1.50 shipping
- 1x SPDT slide switch [(ADAFRUIT)](https://www.adafruit.com/product/4219) $2.95


Total before tax: $6.5

I'll also be source the following parts myself since I already have them and would like to help Hack Club:
- Some solid-core wire to wire the slide switch together
- 3d PRINT
