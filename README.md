# 🚀 Starpet Project
This repository holds the open-source hardware and firmware design files for my **Hack Club Half-Life** project submission.
Starpet is basically a desktop pet tamagotchi which I made by referring the starbie guide provided by half-life.This project was done because i wanted to try building projects like these and hopefully learn something from them

I used Kicad to build the schematics and then finally build the pcb as per shown in the guide and made some changes in the way my pcb layout looks.I added a silkscreen of my sprite and made a few small customizations. I used the XIAO ESP32-C3 as my microcontoller and Arduino IDE was used for the firmware. The guide had provided a firmware in which I made some changes in the "beginner settings" block of code. I added my own sprite which I wanted to look like a cat and also added some functions for the buttons.


## 📁 Repository Structure
* `/pcb` - KiCad schematics, layouts, and manufacturing outputs.
* `/firmware` - Arduino IDE configuration code files.

<img width="1235" height="811" alt="image" src="https://github.com/user-attachments/assets/8870e8b2-a8c8-4afc-8df3-2125c81455b8" />

# **Schematic of PCB**
<img width="1272" height="905" alt="schematic" src="https://github.com/user-attachments/assets/8d71b067-54da-447f-9a4b-6263770de069" />


# **3D View**
<img width="825" height="537" alt="3dpcb" src="https://github.com/user-attachments/assets/e63fdbe1-e7ec-44ee-906f-1ba65406e65c" />


## CONTROLS

**Button 1**: Opens radial menu

**Button 2**: Shows stats

### When the device boots up, the pet hatches with these starting attribute baselines:

    Joy: 80/100
    Energy: 80/100
    Fullness: 70/100

### The Radial Action Menu

Tilting the board in the four directions helps to select their options with the help of MPU6050 gyroscope. The menu maps four custom options:

    TOP: NAP — Triggers a sleeping animation with floating 'Z' particles.
    RIGHT: RUN — Triggers two high-speed laps across the display.
    BOTTOM: JUMP — Triggers a happy jump.
    LEFT: PET — Triggers hearts floating above the cat.


# BOM(Bill of Materials)

|Item|Qty|Supplier|Cost/item|Total Cost|
|---|---|---|---|---|
|XIAO ESP32 C3|1|[Sharvi](https://sharvielectronics.com/product/seeed-studio-xiao-esp32c3-tiny-mcu-board-with-wifi-and-ble-battery-charge-supported-module/)|$6.70|$6.70|
|0.96 OLED|1|[Sharvi](https://sharvielectronics.com/product/0-96-inch-i2c-4pin-oled-display-module-white/)|$2.20|$2.20|
|MPU6050|1|[Sharvi](https://sharvielectronics.com/product/mpu-6050-3-axis-accelerometer-and-gyro-sensor/)|$1.98|$1.98|
|DHT11|1|[Sharvi](https://sharvielectronics.com/product/dht11-temperature-and-humidity-sensor-module/)|$0.72|$0.72|
|10k Resistor|1|[Sharvi](https://sharvielectronics.com/product/10k-ohm-1-4-watt-resistor-1-tolerance/)|$0.18|$0.18|
|PCB|1|[Seeed Studio](https://www.seeedstudio.com/fusion_pcb.html)|$9.90|$9.90|
|Estimated total shipping||||$10.54|

