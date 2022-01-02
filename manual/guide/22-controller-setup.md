# My BLV MGN Cube - Assembly Instructions

## Step 22 Controller Setup

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

### References
[Reference guide NOT PERFECT](https://www.makenprint.uk/3d-printing/3d-printing-guides/skr-v1-4-setup-guide/#pwrconnections)

[SKR 1.4 Manual](https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3/raw/master/BTT%20SKR%20V1.4/BTT%20SKR%20V1.4%20Instruction%20Manual.pdf)

[TFT support](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware)

[TFT wiring up](https://www.youtube.com/watch?v=v0PCzHGXTgk)

[Dual Lead screws](https://www.youtube.com/watch?v=3jAFQdTk8iw&t=117s)

[BLTouch manual](https://5020dafe-17d8-4c4c-bf3b-914a8fdd5140.filesusr.com/ugd/f5a1c8_d40d077cf5c24918bd25b6524f649f11.pdf)

