
# What is Aitken
Aitken is small light, that was designed to help astronomers to see better during night sky observations without losing their night vision. 

## Name
The name **Aitken** was chosen after [Robert Grand Aitken](https://en.wikipedia.org/wiki/Robert_Grant_Aitken) who discovered the [Red Rectangle Nebula](https://en.wikipedia.org/wiki/Red_Rectangle_Nebula). The shape of the nebula was also inspiration when creating logo for this project

## Features
### USB-C
Used for two-way charging with USB-PD. It can also be used to program the microcontroller inside.

### Controls
Aitken features rotatory encoder that is used to either change the light intensity and to navigate the menu. Above that is small OLED screen. 

### Sensors
Featuring accelerometer and gyroscope enables Aitken to be controlled via gestures. It also has 3-axis magnetometer for finding north, but this feature has to be tested yet.

### Lights
The board has 30 LEDs with all of them being red in the 620 - 630nm range with luminous flux of 26 lumens each. 

## Project status

| Status                     	| Action           	 | ETA       	 |
|----------------------------	|------------------	 |-----------	 |
| ✅ Done                       | Schematic design 	| Done      	|
| ✅ Done                       | PCB design       	| Done      	|
| ❎ Waiting for parts          | PCB assembly     	| 25.1.2024 	|
| ❎ Waiting for PCB assembly   | PCB test         	|           	|
| ❎ Waiting for PCB assembly   | Firmware         	|           	|

## Technical details
### MCU
The MCU used is [ESP32-C3FH4](https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf) with integrated 4MB flash, 2.4GHz Wi-Fi and Bluetooth 5.0.

### Sensors 
For accelerometer I decided to use [LSM6DS3HTR](https://cz.mouser.com/datasheet/2/389/dm00229854-1798742.pdf) but with any future iteration I'm going to switch to [LSM6DSOTR](https://www.st.com/resource/en/datasheet/lsm6dso.pdf).
The magnetometer used is [LIS3MDLTR](https://www.st.com/content/ccc/resource/technical/document/datasheet/54/2a/85/76/e3/97/42/18/DM00075867.pdf/files/DM00075867.pdf/jcr:content/translations/en.DM00075867.pdf)

### Power
For USB-PD controller, battery charger and power bus manager I chose [MP2722](https://www.monolithicpower.com/en/documentview/productdocument/index/version/2/document_type/Datasheet/lang/en/sku/MP2722GRH/document_id/10035/)
Power for lights is provided from [KTD2801](https://www.kinet-ic.com/uploads/KTD2801-04b.pdf) and 3V3 power rail is powered from [NCP186](https://www.onsemi.com/pdf/datasheet/ncp186-d.pdf)

### PCB
It is 4 layer stack up with components mounted on both sides. One side is occupied by LEDs only while the other side hosts the other components.