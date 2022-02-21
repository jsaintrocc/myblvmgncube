# My BLV MGN Cube - Assembly Instructions

## Step 21 Wire Electronics Panel

### Step 21 BoM

#### Hardware
| Parts                    | Quantity | Details                                                                          | Example Links                                                       |
|--------------------------|:--------:|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Controller Board         |    1     | BIGTREETECH SKR V1.4 Turbo W/TMC 2208 UART                                       | [AliExpress](https://s.click.aliexpress.com/e/_AYaAOG)              |
| Raspberry Pi             |    1     | rPi 4 w/2GB of Ram (Anything 3B or above is probably fine)                       | [Canakit](https://www.canakit.com/raspberry-pi-4-2gb.html)          |
| rPI Power Supply         |    1     | Don't skimp here!!                                                               | [Canakit](https://www.canakit.com/raspberry-pi-4-power-supply.html) |
| Lerdge High Power Module |    1     | External MOSFET that Protects/Isolates your Controller Board from the Heated Bed | [AliExpress](https://s.click.aliexpress.com/e/_9AROv5)              |

#### Printed Parts
| Parts                                                                                                                                                                                                 | Quantity | Details |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------:|---------|
| [Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Bottom_1_Body1_Bottom.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Bottom_1_Body1_Bottom.stl)                 |    1     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Left_Side_1_Body20_Left_Side.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Left_Side_1_Body20_Left_Side.stl)                      |    1     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Right_Side_1_Body1_Right_Side.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Right_Side_1_Body1_Right_Side.stl) |    1     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Top_1_Body1_Top.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct200mm_Slotted_Wire_Duct_v17_Top_1_Body1_Top.stl)                                                |    1     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Bottom_1_Body1_Bottom.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Bottom_1_Body1_Bottom.stl)                 |    9     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Left_Side_1_Body20_Left_Side.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Left_Side_1_Body20_Left_Side.stl)                      |    9     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Right_Side_1_Body1_Right_Side.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Right_Side_1_Body1_Right_Side.stl) |    9     | [Printed Parts Settings](../partsSettings.md) |
| [Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Top_1_Body1_Top.stl](../../parts/extra/slotted-wire-ducts/Slotted_Wire_Duct150mm_Slotted_Wire_Duct_v17_Top_1_Body1_Top.stl)                                                |    9     | [Printed Parts Settings](../partsSettings.md) |

#### Tools

| Parts          | Qunatity | Details | Example Links |
|----------------|:--------:|----|---------|
| Flat Head Nail |    1     | Used to melt the rivet heads | |
| Candle         |    1     | | |
| M3 Screwdriver |    1     | | [Amazon](https://amzn.to/3qNmEgs) |

### Prep
1. Assemble the Slotted Wire Ducts
   1. Sides should click onto pegs on bottom. 
   2. Heat the nail head, using the candle, and heat weld all the pegs.
   3. I used a twisting motion, with the nail, on top of each peg.
   
      ![](img/21-makeDucts.jpeg)\
      *fig 21.1*

2. Add JST-XH connectors
   1. Bltouch/Thermistors 
      1. Replace the 3 pin servo connector with a JST-XH 3 pin
      2. Replace the 2 pin probe switch connector with a JST-XH 2 pin

             Using Servo and probe connector from left to right
             Brown (GND)/Red (+5V)/Orange (Control Signal) Black(GND)/White (Zmin) 

         Note check the wiring harnes extension cable to make sure they didn't switch the wires. I had this problem!! (Take picture of Bl-Touch to wiring harness extension.

      3. Attach JST connectors to stepper motors
          Maybe do a bit on how to verify wiring for board

      4. On Thermistor Replace the 2 pin dupont connectors with a 2 pin JST-XH connector

### Assembly
1. Mount Slotted Wiring Ducts


3. Attach power wires to board in correct spot
4. Label all positive and or negative terminals (Neg is probably easier)
   5.   Did this with a marker
6. Verify power jumper has USB power disabled
7. Verify drivers have uart enabled pad soddered
8. Stick the heatsinks onto the drivers
9. Verify board is in UART mode
   Note: I think the default jumpers work for this (2208's only have UART and not SPI) so spi config probably winds up with uart.
10. Add drivers to board red pins match red pins
11. Attach power to board
12. Plug up all the steppers
13. Using the provided sd card boot up and carefully test each stepper. Directions aren't important and corexy will be messed up but just make sure each stepper is working (Wire test and validates your board is working with baseline config).
