# Fan-Controller

A quad port wifi powered fan controller

  

This is the official repository for the Fan-Controller.

**Reach goals:**

 - [ ] Variable PWM port with 5 - 12V supply (Supporting 5V, 9V and 12V fans)
 - [ ] Power output of 250mA (each port, total: 1A) 
 - [ ] Small display to show important values (like: flowing current, case temperature, fan voltage, active fan) 
 - [ ] WiFi enabled to controll over smart home app and showing stats
- [ ] Fans could be connected directly (PC-Fan connector)
- [ ] Lowpower consumtion on MCU side
- [ ] Automatic fan control dependend on case temperature

# Challenge

 
 # Version 2.0 Fan-Controller
 The new version of the Fan-Controller is not only a new hardware revision. It will also fix the following bugs: 
 

 - [ ] Powersupply is to hard to solder correct
 - [ ] Powersupply can not supply enought power
 - [ ] only 5V output
 - [ ] No Display or Serial output to controll
 - [ ] Firmware is to complicated so that a newbie could understand it
 - [ ] The controll circuit consums too much current
 - [ ] Could only connect Fans over male headers

with the new version I want to solve this problems. I also adding the following features as I already need to redesign the whole thing: 

**MCU**
In the first version I used a Microchip ATMega328P microcontroller. This one did the job well but it's an old chip and it does not fit many pins and functions. A long time ago I ordered some of these ESP32 Modules and wanted to use them in a project. Now finally the time is comming. They feature WiFi & Bluetooth, a fast core and many I/O (enought for this project). 