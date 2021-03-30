# Fan-Controller

  

A quad port wifi powered fan controller
This is the official repository for the Fan-Controller.

**Reach goals:**

- [ ] Variable PWM port with 5V supply (Supporting 5VDC fans)
- [ ] Power output of 250mA (each port, total: 1A)
- [ ] Small display to show important values (like: flowing current, case temperature, fan voltage, active fan)
- [ ] WiFi enabled to controll over smart home app and showing stats
- [ ] Fans could be connected directly (PC-Fan connector)
- [ ] Lowpower consumtion on MCU side
- [ ] Automatic fan control dependend on case temperature

## Challenge
- limited budget
- limited time (Should be done in less than a week of work)
- should fit all functions


## Version 2.0 Fan-Controller

The new version of the Fan-Controller is not only a new hardware revision. It will also fix the following bugs:

- [ ] Powersupply is to hard to solder correct
- [ ] Powersupply can not supply enought power
- [ ] No Display or Serial output to controll
- [ ] Firmware is to complicated so that a newbie could understand it
- [ ] The controll circuit consums too much current
- [ ] Could only connect Fans over male headers

with the new version I want to solve this problems. I also adding the following features as I already need to redesign the whole thing:

  
**MCU:**
In the first version I used a Microchip ATMega328P microcontroller.
This one did the job well but it's an old chip and it does not fit many pins and functions.
As WiFi is not the most important feature I will use an STM32 as main CPU. But as a second WiFi core I will add an ESP8266 to add WiFi to the project. This ESP is fully controlled by the STM32 and could be disconnnected completly by the IO of the STM32. 
  

**FAN Output:**
As a fan output driver I will use the IRF540 FET's. These one are a bit overpowered, but this is even better because they are not getting hot and I have plenty of them.


**Power Supply:**
As for power the whole pcb will be powered by +12VDC.
on the system we have two voltage regulators for the diffrent voltages (+3V3(MCU), +5V(Fan)).
To keep the whole circuit as simple and cheap as possible we will only use 5V fans. This also makes the first version of the PCB a bit easier to test the whole application.


**Display:**
In this project I'm using a small Monochrome TFT Display to display the most important data. This display which I use is not available any more but I have some laying around, so I will use them to display this data: 

- flowing current (each Fan)
- Server case Temperature
- which voltage is set for the fan
- which port is active

