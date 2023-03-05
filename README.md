# TelemetricOBD

###### This repo acts as the digital storage of all associated developments (e.g. firmware, pcb development, CAD) and related documentation (e.g. schematic captures, pictures, testing data) to the Telemetric OBD Breakout Unit. 

## Board Functionality
This board acts as a quick connect to the OBD diagnostic port on a Toyota Tacoma 2023 in order for me to check on vehicle performance over long work trips and to evaluate overall vehicle performance over its lifetime.

![image](https://user-images.githubusercontent.com/126422709/222989379-cd9871d0-ebbd-4954-b26f-62520ebde9a3.png)

Data collected VIA CAN (e.g. Diagnostic troublecodes, Engine RPM, Coolant Temperature, Intake Manifold Temperature, Fuel Pressure, et.c) is displayed on an OLED display which a user toggle to cycle through its data collection.
All Data is written to an SD card for hard data and is additionally streamed via bluetooth to an IOS app where all data is collected and plotted for a specific trip). 

An additional feature I wanted to implement was tying the data collected to the apple maps vehicle path menu for a physical overlay where certain value thresholds and extremes are met (especially in rugged environments) 

## Inspiration

https://www.autopi.io/blog/can-bus-explained/

A few years ago I saw the adoption of the ELM327 microcontroller unit that acted as a interface for vehicle diagnostic for a certain set of supported FSAE protocols. 
It had a UART interface to connect to other handheld diagnostic tools. I want to modernize this design and update its MCU to the STM32 family for higher performance and open source all
aspects of its development for my specific vehicle and set different configuration packets for a range of SAE CAN standards. 

![image](https://user-images.githubusercontent.com/126422709/222988891-c67becc6-91a3-4e95-818f-7bfca187253f.png)


## TODO: 
- Determine Toyota Tacoma 2023 CAN Protocal --> set in Documentation
- Select CAN chip for interfacing with STM32. Preferably with easy to read library docs. 
      - See if there's an individual breakout board w/ same chip with interfacing with the nucleoboard. Set a benchtop setup. 
      - See if basic CAN data can be read for a demo protocal standard. 
- Set basic peripherial circuitry for the STM32 device selected.
