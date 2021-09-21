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
| M4 Screws | 4 | Din7991 | [AliExpress](https://s.click.aliexpress.com/e/_A1aLOM) |
| Bed Leveling Springs | 4 | Length: 20mm OD: 8mm ID: 4mm | [AliExpress](https://www.amazon.com/gp/product/B07QCN4LB9/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) |
| Heated Bed Insulation | 1 | 300mm x 300mm x 10mm | [AliExpress](https://s.click.aliexpress.com/e/_AaR1YQ) |
| Heated Bed Magnetic Flex Plate | 1 | 310mm x 310mm Double Sided PEI Flex Plate and High Temp Magnetic Sheet | [Amazon (Fulament)](https://www.amazon.com/Fulament-Printing-Magnetic-Sticker-Adhesive/dp/B07ZVYPSSQ/ref=sr_1_1_sspa?crid=3LGKKARPDOG34&dchild=1&keywords=fulament%2Bflex%2Bbed&qid=1632181739&s=industrial&sprefix=fulament%2Cindustrial%2C162&sr=1-1-spons&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExUkMxNUdRNzRNSUpWJmVuY3J5cHRlZElkPUEwNjUwNTAyM0kzTDg1ME9FNUtTRSZlbmNyeXB0ZWRBZElkPUEwMTA5NzQ5OU1RM1NSWEs4UjI3JndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ&th=1) [AliExpress (Energetic)](https://s.click.aliexpress.com/e/_9jGuVk) |
| 3mm x 10.16cm zip ties (4in)  | 12 | ~2.5mm x ~120mm | [Amazon](https://amzn.to/3p2nDaE) |

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|
| [BLV_Thumbwheel_bed_leveling_knob.stl](../../parts/extra/bedadjuster/BLV_Thumbwheel_bed_leveling_knob.stl) | 4 | [Printed Parts Settings](../partsSettings.md) |
| [heatbed-wireguide-bedmount.stl](../../parts/extra/heated-bed-cable-manager/heatbed-wireguide-bedmount.stl) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [heatbed-wireguide-framemount.stl](../../parts/extra/heated-bed-cable-manager/heatbed-wireguide-framemount.stl) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [heatbed-wireguide-loop.stl](../../parts/extra/heated-bed-cable-manager/heatbed-wireguide-loop.stl) | 8 | [Printed Parts Settings](../partsSettings.md) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Multimeter W/Continuity Tester | 1 | This multimeter has a temp probe too! | [Amazon](https://amzn.to/3sxUjeT) |
| M3 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| M5 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| Plastic Spreader | 1 | Can use an old Credit Card instead | [Amazon](https://www.amazon.com/3M-357-Bondo-Spreader-Pack/dp/B000BOC9K4/ref=sr_1_7?crid=PC2YPFP1GXF4&dchild=1&keywords=spreader+body+filler&qid=1632181340&sprefix=spreader+body%2Caps%2C152&sr=8-7) |
| X-Acto Knife | 1 | | [Amazon](https://amzn.to/3gUPYPI) |

### Prep
1. Test the heat bed to determine it's wattage and make sure it doesn't have a short. Using the multimeter set to read resistance, measure the restisance between the red and black wires. Use the formula Volts * (Volts/Resistance) = Watts to determine the Wattage. In my case, 24V * (24V/2.5 Ohms) = 230 Watts.

    ![](img/18-TestHeatedBed.JPG)\
    *fig 18.1*

    Note: Big Tree Tech recommends an external mosfet for anything over 144 Watts so I'll definitely be using a $10 external Mosfet to keep my board from catching on fire. Also it will probably increase the life on any controller board as they'll run a lot cooler.

2. Test the thermistor to make sure it isn't shorted or there isn't a loose wire. Using the multimeter set to read resistance, measure the restisance between the yellow thermistor wires. I get around 111 KOhms at room temperature which is good. As long as you get a reading KOhms you're probably good.

    ![](img/18-TestBedThermistor.JPG)\
    *fig 18.2*

3. Attach the heated bed insulation
    1. Measure and cut holes for bed leveling springs.

        ![](img/18-HBInsulationHoles1.JPG)\
        *fig 18.3*

        ![](img/18-HBInsulationHoles2.JPG)\
        *fig 18.4*

    2. Clean the bottom of the heated bed with alcohol and then apply the insulation.

        ![](img/18-HBAlcoholPrep.JPG)\
        *fig 18.5*

        ![](img/18-HBwInsulation.JPG)\
        *fig 18.6*

    3. Make sure to trim the metal backing away from any power connectors.

        ![](img/18-HBInsulationTrimFromPower.JPG)\
        *fig 18.7*

5. Attach magnetic base for the flex plate.
    1. Remove the protective film on the top surface of the build plate.

        ![](img/18-HBRemoveFilm.JPG)\
        *fig 18.8*

    2. Clean the build plate with some alcohol and is free of dust/dirt/hair etc..

        ![](img/18-HBAluClean.JPG)\
        *fig 18.9*

    2. Peel back 4cm of the paper backing on one edge of the magnteic bed and carefully apply to back edge.

        ![](img/18-AttachHBMagSurface1.JPG)\
        *fig 18.10*

    3. Using a platic spreader (or old credit card) smooth down the exposed part of the magnetic sheet to prevent air bubbles from getting trapped underneath.

        ![](img/18-AttachHBMagSurface2.JPG)\
        *fig 18.11*

    4. Repeat the process by peeling back another section of the paper and using the spreader to make sure there are no air bubbles.

        ![](img/18-AttachHBMagSurface3.JPG)\
        *fig 18.12*

    4. Once fully attached flip over and use an X-acto knife to trim the excess material.

        ![](img/18-TrimHBMagSurface.JPG)\
        *fig 18.13*

    5. Also using your fingers feel for heated bed mouting holes and using the X-acto knife cut them out.

        ![](img/18-CutHolesHBMagSurface.JPG)\
        *fig 18.14*

4. Insert M4 nuts in each bed leveling knob. Regular nuts are fine because the tension with the bed leveling springs will keep everything tight.

    ![](img/18-M4NutInLevelKnob.JPG)\
    *fig 18.15*

5. Put M3 square nuts and M3 10mm screws into each wireguide mount. Also attach 2x M5 8mm and T-Nuts.

    ![](img/18-WireguidePrep.JPG)\
    *fig 18.16*

6. Cut the ratchet end off the 24" zip tie.

    ![](img/18-CutRatchetOffZiptie.JPG)\
    *fig 18.17*

### Assembly
1. Attach the heatbed wireguide bedmount (Long one) to the bed frame placing it ~120mm from the bed frame corner to the edge of the mount.

    ![](img/18-AttachBedframeMount.JPG)\
    *fig 18.18*

2. Attach the heatbed wireguide framemount to the top back 2020 extrusion so that it's centered on the frame (~248mm for me).

    ![](img/18-AttachFrameMount.JPG)\
    *fig 18.19*

3. Attach zip tie to the wireguide mounts. Manually move the bed up and down and make sure the wireguide doesn't run into anything. The zip tie should maintain a graceful arc at all points and should naturally stay level with the 2020 extrusion (See Fig 18.9 and 18.10). **The teeth should be on the outside of the loop.**

    ![](img/18-AttachZipTie.JPG)\
    *fig 18.20*

    ![](img/18-ZipTieTop.JPG)\
    *fig 18.21*

    ![](img/18-ZipTieBottom.JPG)\
    *fig 18.22*

4. Trim the zip tie, once your happy with it's movement, and tighten the m3 screws to clamp in place. *Mine was 520mm long when trimmed.*

    ![](img/18-TrimZipTie.JPG)\
    *fig 18.23*

5. Attach the 8x wireguide loops to the 24" zip tie. There are teeth on the loops that should grab the teeth on the zip tie.

    ![](img/18-AttachLoopsToZipTie.JPG)\
    *fig 18.24*

6. Attach the bed to the frame using 4x bed leveling assemblies. Each assembly is as follows: M4 40mm flat head screw->M4 washer->bed spring->M4 washer->bed mount->bed leveling knob. **It's much easier to do this if you lay the printer frame on its side**

    ![](img/18-AttachBedToFrame1.JPG)\
    *fig 18.25*

    ![](img/18-HoldNutWChopStick.JPG)\
    *fig 18.26*

    Note: I used a chopstick to keep the M4 Nut in place. 

    ![](img/18-AttachBedToFrame2.JPG)\
    *fig 18.27*

7. Attach the heated bed wiring harness and thread it through the wire guide.

    ![](img/18-RouteHBWiring.JPG)\
    *fig 18.28*

8. Using small zip ties attach the heated bed wiring harness to the mounts and the loops to the large zip tie.

    ![](img/18-ZipTieHBWiring.JPG)\
    *fig 18.28*

9. Here's what it should look like when it's done.

    ![](img/18-FinalHB.JPG)\
    *fig 18.29*

