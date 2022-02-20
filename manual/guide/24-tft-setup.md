# My BLV MGN Cube - Assembly Instructions

## Step 24 TFT Setup

### Step 24 BoM

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
