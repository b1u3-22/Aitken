
# What is Aitken
Aitken is small light, that was designed to help astronomers to see better during night sky observations without losing their night vision. 

## Name
The name **Aitken** was chosen after [Robert Grand Aitken](https://en.wikipedia.org/wiki/Robert_Grant_Aitken) who discovered the [Red Rectangle Nebula](https://en.wikipedia.org/wiki/Red_Rectangle_Nebula). The shape of the nebula was also inspiration when creating logo for this project

## Features
### USB-C
Used for two-way charging with USB-PD. It can also be used to program the ESP32-S3 microcontroller inside.

### Controls
Aitken features rotatory encoder that is used to either change the light intensity and to navigate the menu. Above that is small OLED screen. 

### Sensors
Featuring accelerometer and gyroscope enables Aitken to be controlled via gestures. It also has 3-axis magnetometer.

### Lights
The board has 30 LEDs with all of them being red in the 620 - 630nm range with luminous flux of around 4 lumens each. 

## Project status

| Status                     	| Action           	 | ETA       	 |
|----------------------------	|------------------	 |-----------	 |
| ✅ Done                       | Schematic design 	 | Done      	 |
| ❎ In progress 		        | PCB design         | 16.09.2024	 |
| ❎ Waiting for PCB            | PCB test         	 |           	 |
| ❎ Waiting for PCB 		    | Firmware         	 |           	 |

## Technical details
### MCU
The MCU used is [ESP32-S3FN8](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf) with integrated 8MB flash, 2.4GHz Wi-Fi and Bluetooth 5.0 LE.

### Sensors 
For accelerometer I decided to use [LSM6DSOTR](https://www.st.com/resource/en/datasheet/lsm6dso.pdf).
The magnetometer used is [LIS3MDLTR](https://www.st.com/content/ccc/resource/technical/document/datasheet/54/2a/85/76/e3/97/42/18/DM00075867.pdf/files/DM00075867.pdf/jcr:content/translations/en.DM00075867.pdf)

### Power
For USB-PD controller, battery charger and power bus manager I chose [MAX77972](https://www.analog.com/media/en/technical-documentation/data-sheets/max77972.pdf) mainly for the ability
to program the charge voltage and current using resistors and the integrated battery fuel gauge.
Power for lights is provided from [AP3031](https://www.diodes.com/assets/Datasheets/AP3031.pdf) and 3V3 power rail is powered from [NCP186](https://www.onsemi.com/pdf/datasheet/ncp186-d.pdf)

### PCB
Aitken is made out of 2 separate boards. The first one has 4 layer stack up with main circutry and battery holders. The second one is 1 layer aluminium board with just the LEDs and connector. 
