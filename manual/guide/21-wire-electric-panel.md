# My BLV MGN Cube - Assembly Instructions

## Step 21 Wire Electronics Panel

### Step 21 BoM

#### Hardware
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|
| [skr14-dinrailmount.stl](../../extra/din-rail-mount-skr-board/files/skr14-dinrailmount.stl) | 2 | [Printed Parts Settings](../partsSettings.md) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| M3 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |

### BL-Touch Wiring
1. Replace the 3 pin servo connector with a JST-XH 3 pin
2. Replace the 2 pin probe switch connector with a JST-XH 2 pin

Using Servo and probe connector from left to right
Brown (GND)/Red (+5V)/Orange (Control Signal) Black(GND)/White (Zmin) 

Note check the wiring harnes extension cable to make sure they didn't switch some of the wires. I had this problem!! (Take picture of Bl-Touch to wiring harness extension.

### Thermistors
1. Replace the 2 pin dupont connectors with a 2 pin JST-XH connector

### Prep
1. Crimp ferrules to 14AWG wires.

    ![](img/19-CrimpWires.JPG)\
    *fig 19.1*

2. Attach JST connectors to stepper motors
   Maybe do a bit on how to verify wiring for board
2. Attach power wires to board in correct spot
3. Label all positive and or negative terminals (Neg is probably easier)
4. Verify power jumper has USB power disabled
2. Verify drivers have uart enabled pad soddered
3. Stick the heatsinks onto the drivers
4. Verify board is in UART mode
   Note: I think the default jumpers work for this (2208's only have UART and not SPI) so spi config probably winds up with uart.
3. Add drivers to board red pins match red pins
4. Attach power to board
5. Plug up all the steppers
6. Using the provided sd card boot up and carefully test each stepper. Directions aren't important and corexy will be messed up but just make sure each stepper is working (Wire test and validates your board is working with baseline config).

### FW config
Setup VSCode See your stackedit dir for this
1. Configure platformio.ini for skr board
   
        default_envs = LPC1768  
        *for SKR 1.4 non Turbo*
        default_envs = LPC1769

       [BTT Source for Turbo](https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3/blob/master/BTT%20SKR%20V1.4/Firmware/Marlin-2.0.x-SKR-V1.4-Turbo/platformio.ini)

2. Pick the closest config from 
https://github.com/MarlinFirmware/Configurations/archive/release-2.0.9.1.zip

3. Install the tft
4. See the marlin config changes
5. update the firmware
6. BLTtouch
7.  Check if you can enable 5v mode
  


SD emulation for eeprom

### Assembly
1. Attach power wires to SKR.

    ![](img/19-PowerWires.JPG)\
    *fig 19.2*
