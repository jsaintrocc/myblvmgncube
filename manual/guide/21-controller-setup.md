# My BLV MGN Cube - Assembly Instructions

## Step 19 Build Bowden Extruder and Hotend Cable Manager

[Reference guide NOT PERFECT](https://www.makenprint.uk/3d-printing/3d-printing-guides/skr-v1-4-setup-guide/#pwrconnections)

[SKR 1.4 Manual](https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3/raw/master/BTT%20SKR%20V1.4/BTT%20SKR%20V1.4%20Instruction%20Manual.pdf)

[TFT support](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware)

[TFT wiring up](https://www.youtube.com/watch?v=v0PCzHGXTgk)

[Dual Lead screws](https://www.youtube.com/watch?v=3jAFQdTk8iw&t=117s)

[BLTouch manual](https://5020dafe-17d8-4c4c-bf3b-914a8fdd5140.filesusr.com/ugd/f5a1c8_d40d077cf5c24918bd25b6524f649f11.pdf)


### Step 19 BoM

#### Hardware
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|


| Extruder Stepper Motor | 1 | STEPPERONLINE 17HS16-2004S1 | [STEPPERONLINE](https://www.omc-stepperonline.com/nema-17-bipolar-45ncm-64oz-in-2a-42x42x40mm-4-wires-w-1m-cable-and-connector.html?search=17HS16-2004S1) |
| BMG Extruder | 1 | A good quality clone is fine | [Aliexpress](https://www.aliexpress.com/item/32917029058.html?spm=a2g0s.9042311.0.0.27424c4d85bUyI) |
| M3 35mm Socket Head Cap Screws | 3 | DIN912 (Should be included with the BMG Extruder Kit)| |
| M3 8mm Socket Head Cap Screws | 1 | DIN912 | |
| M5 T-Nuts | 4 | Hammer Head/Drop In Style | |
| M5 10mm Socket Button Head Screws | 2 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M5 8mm Socket Button Head Screws | 2 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M3 Thin Square Nuts | 1 | DIN562 | |
| 1/2" Flex Tubing | 62cm | Also called split wire loom | [Home Depot](https://www.homedepot.com/p/Gardner-Bender-3-8-in-and-1-2-in-Flex-Tubing-7-ft-and-10-ft-Combo-Pack-FLX-538C10/205588197#product-overview) [Amazon](https://www.amazon.com/Gardner-Bender-FLX-538C10-Assorted-Corrugated/dp/B01MSN7D25/ref=sr_1_10?dchild=1&keywords=split%2Bflex%2Btubing%2B1%2F2%22&qid=1628354523&s=hi&sr=1-10&th=1) [Aliexpress](https://www.aliexpress.com/item/32855974110.html?spm=a2g0o.productlist.0.0.112a72eas6e75a&algo_pvid=6370ddcb-8c94-4862-98e7-a1bb0f65fe20&algo_exp_id=6370ddcb-8c94-4862-98e7-a1bb0f65fe20-28) |
| 3mm x 10.16cm zip ties (4in)  | 3 | ~2.5mm x ~120mm | [Amazon](https://amzn.to/3p2nDaE) |
| 24 inch Nylon zip ties | 1 | ~9mm wide at least 60cm long | [Amazon](https://www.lowes.com/pd/Utilitech-15-Pack-24-in-Cable-Ties/50005756) |

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|
| [skr14-dinrailmount.stl](../../extra/din-rail-mount-skr-board/files/skr14-dinrailmount.stl) | 2 | [Printed Parts Settings](../partsSettings.md) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|

| 1.5mm Allen Wrench | 1 | For extruder gear | [Amazon](https://amzn.to/3qNmEgs) |
| M3 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| M5 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |

### TFT Wiring
Kit came with 24 AWG
Using 24 AWG ethernet cable
Use the keyed RS232 connector on the Touch screen board See Pict
Here is a useful table for getting the wiring right https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware#connect-the-tft-to-the-mainboard

For SKR-V1.4 From left to right (With stepper drivers on top)
RST Rx0 Tx0 Gnd NPWR

You should have one pair for Rx (Rx0 + Gnd) and one pair for Tx (Tx0 + Gnd). RS232 isn't differential I.E. Rx and Tx don't have corresponding Rx+ and Rx- so you pair with ground to cut down on cross talk.

So for color coding
Rx0 Orange
Gnd Orange/White
Tx0 Green
Gnd Green/White
NPWR Blue Blue/White
Rst Brown

TFT connector on SKR is to the right of the SD card and is labelled.

Cable Clip
https://github.com/gregsaun/prusa_i3_bear_upgrade/blob/master/printed_parts/common_to_all_versions/stl/cable_clip_vertical.stl

or 

https://github.com/gregsaun/prusa_i3_bear_upgrade/blob/master/printed_parts/common_to_all_versions/stl/cable_clip_horizontal.stl

### TFT Firmware Update
1. Download latest tarball from
2. https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware
   Note: Or do "git clone git@github.com:bigtreetech/BIGTREETECH-TouchScreenFirmware.git
3. Go through TFT menus and get BOARD Model
   Settings/Info
   Board: BIGTREETECH_TFT35_V2.0
   Firmware TFT35_V2.0.23

4. Insert a SD card with at least 256MB of space on it
4. From 'Copy to SD Card root directory to update' folder copy the relevant bin.
   BIQU_TFT35_APP1_V2.0.27.x.bin  
   NOTE: If you're unsure of the names just copy several. The updater will pick the one it needs.
6. Copy the config.ini
7. From the 'THEME_Hybrid Red Menu Material theme' folder copy the 'TFT35' folder
   Note: This is how you change themes (Copy the same folder from another theme)
8. When done here is what the root of your SD card should look like

       BIQU_TFT35_APP1_V2.0.27.x.bin
       config.ini
       TFT35

   Note: It get's your printer name from marlin not the config.ini
   Speeds for xyz s=slow n=normal f=fast

9. There are other options such as languages etc.. Use this reference:  
   https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/blob/master/README.md#update-tft-firmware

10. Insert the SD card into the side of the TFT screen (until it clicks) and then hit the reset/panic button.
11. It should display that it's updating.
12. Fix the baud rate (On a update it seems to default back to 115K).
13. Settings/Connection/UART Speed (top left)/Printer and select 250000
14. Should now connect to the printer
15. 


### BL-Touch Wiring
Using Servio and probe connector from left to right
Brown/Red/Orange Black/White Note check the wiring harnes extension cable to make sure they didn't switch some of the wires. I had this problem!! (Take picture of Bl-Touch to wiring harness extension.

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
