# My BLV MGN Cube - Assembly Instructions

## Step 18 Install Heated Bed

**Warning Experimental Work Ahead**

![](img/all-hardHat.png)

The heated bed is one of the most likely components on a 3d printer to catch fire. Probably like you I'm an amature and I'm accepting the risk for myself on what I'm doing here. If you aren't comfortable doing the same then please consult a professional. If you think I'm doing something unsafe and stupid please let me know by raising an issue for the github project.

### Step 18 BoM

#### Hardware
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Heated Bed | 1 | 24V ~220W Aluminum Heated 310mm x 310mm x 3mm | [AliExpress](https://s.click.aliexpress.com/e/_Aq7W5i) |
| 24 inch Nylon zip ties | 1 | ~9mm wide at least 60cm long | [Amazon](https://www.lowes.com/pd/Utilitech-15-Pack-24-in-Cable-Ties/50005756) |
| M5 8mm Socket Button Head Screws | 4 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M5 T-Nuts | 4 | Hammer Head/Drop In Style | |
| M3 Thin Square Nuts | 2 | DIN562 | |
| M3 10mm Socket Head Cap Screws | 2 | DIN912 | |
| M4 Nuts | 4 | DIN934 | |

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|
| [BLV_Thumbwheel_bed_leveling_knob.stl](extra/bedadjuster/BLV_Thumbwheel_bed_leveling_knob.stl) | 4 | [Printed Parts Settings](../partsSettings.md) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Multimeter W/Continuity Tester | 1 | This multimeter has a temp probe too! | [Amazon](https://amzn.to/3sxUjeT) |
| M3 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| M5 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |

### Prep
1. Test the heat bed to determine it's wattage and make sure it doesn't have a short. Using the multimeter set to read resistance, measure the restisance between the red and black wires. Use the formula Volts * (Volts/Resistance) = Watts to determine the Wattage. In my case, 24V * (24V/2.5 Ohms) = 230 Watts.

    ![](img/18-TestHeatedBed.JPG)\
    *fig 18.1*

    Note: Big Tree Tech recommends an external mosfet for anything over 144 Watts so I'll definitely be using a $10 external Mosfet to keep my board from catching on fire. Also it will probably increase the life on any controller board as they'll run a lot cooler.

2. Test the thermistor to make sure it isn't shorted or there isn't a loose wire. Using the multimeter set to read resistance, measure the restisance between the yellow thermistor wires. I get around 111 KOhms at room temperature which is good. As long as you get a reading KOhms you're probably good.

    ![](img/18-TestBedThermistor.JPG)\
    *fig 18.2*

1. Insert M4 nuts in each bed leveling knob. Regular nuts are fine because the tension with the bed leveling springs will keep everything tight.

    ![](img/18-M4NutInLevelKnob.JPG)\
    *fig 18.3*

2. Put M3 square nuts and M3 10mm screws into each wireguide mount. Also attach 2x M5 8mm and T-Nuts.

    ![](img/18-WireguidePrep.JPG)\
    *fig 18.4*

3. Cut the ratchet end off the 24" zip tie.

    ![](img/18-CutRatchetOffZiptie.JPG)\
    *fig 18.5*

### Assembly
1. Attach the wireguide mount to the bed frame at 120mm.

    ![](img/18-XXX.JPG)\
    *fig 18.3*

2. Attach the wireguide mount to the frame at 248mm (~.

    ![](img/18-XXX.JPG)\
    *fig 18.4*

3. Attach zip tie to the wireguide mount and titen the m3 screws to clamp in place. Manually move the bed up and down and make sure the wireguide doesn't run into anything. Trim the zip tie once you are happy with it's movement. Mine was 520mm long.

    ![](img/18-XXX.JPG)\
    *fig 18.5*

    ![](img/18-XXX.JPG)\
    *fig 18.6*

4. Attach the bed to the frame with using the a M4 ??mm flat head screw/2 washers/bed spring/bed leveling knob.

    ![](img/18-XXX.JPG)\
    *fig 18.2*

    ![](img/18-XXX.JPG)\
    *fig 18.3

    ![](img/18-XXX.JPG)\
    *fig 18.4

5. Thread the heated bed wires through the wire guide
