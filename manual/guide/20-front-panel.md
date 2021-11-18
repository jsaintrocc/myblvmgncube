# My BLV MGN Cube - Assembly Instructions

## Step 20 Build Front Panel

### Step 20 BoM

#### Hardware
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| BTT 3.5 in Touch Screen V3.0 | 1 | Dual mode, TFT mode (Marlin)/12864 mode (Klipper/RRF) | [Amazon](https://www.amazon.com/BIGTREETECH-Graphic-Display-Controller-Printer/dp/B07VWF4W3J) [Aliexpress](https://s.click.aliexpress.com/e/_9x9JTN) |
| IDC Ribbon Cables | 2 | These are the EXP1 and EXP2 cables (Included W/TFT) | |
| RS232 cable | 1 | Black Cable (Included W/TFT) | |
| 576mm (~22.7in) 2020 Extrusion | 1 | from standard 365mm Z frame | |
| Ethernet/RJ45 Keystone Jacks | 6 | | [Amazon](https://www.amazon.com/gp/product/B07JRD69V6/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&th=1)|
| 1 Meter Ethernet Cables | 3 | Whatever you have lying around is fine (AWG24 is ideal, stranded or solid) |[Amazon](https://www.amazon.com/Cable-Matters-5-Pack-Snagless-Ethernet/dp/B00C2CBBAM) |
| Female 5 Pin JST-XH Connector | 1 | Your controller uses these and you should too | [Aliexpress](https://s.click.aliexpress.com/e/_AWPLkY) [Amazon](https://amzn.to/3u0TiMD) |
[2020 M5 Angle Brackets](img/all-PlateVsBracket.jpeg) (Brackets) | 4 | | [Amazon](https://amzn.to/3rRVq7U) |
| M3 6mm Socket Head Cap Screws | 4 | DIN912 | |
| M3 12mm Socket Head Cap Screws | 4 | DIN912 | |
| M3 16mm Socket Head Cap Screws | 1 | DIN912 | |
| M3 Nuts | 1 | DIN934 | |
| M5 8mm Socket Button Head Screws | 8 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M5 10mm Socket Button Head Screws | 14 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M5 T-Nuts | 22 | Hammer Head/Drop In Style | |
| 3mm x 10.16cm zip ties (4in)  | 6 | ~2.5mm x ~120mm | [Amazon](https://amzn.to/3p2nDaE) |

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|
| [TFT35v3Mount-tweaked.stl](../../parts/extra/tft35v30-bezel-insert/files/FTFT35v3Mount-tweaked.stl) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [Front_Panel_-_Left_plate_for_TFT35_V2.STL](../../parts/extra/improved-bezel/files/Front_Panel_-_Left_plate_for_TFT35_V2.STL) | 1 | Works for TFT35 V3.0 as well [Printed Parts Settings](../partsSettings.md) |
| [Front_Panel_-_Center_plate.STL](../../parts/extra/improved-bezel/files/Front_Panel_-_Center_plate.STL) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [Front_Panel_-_Right_plate.STL](../../parts/extra/improved-bezel/files/Front_Panel_-_Right_plate.STL) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [Front_Panel_-_left_grill.STL](../../parts/extra/improved-bezel/files/Front_Panel_-_left_grill.STL) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [Front_Panel_-_right_grill.STL](../../parts/extra/improved-bezel/files/Front_Panel_-_right_grill.STL) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [Jig_Main.stl](../../parts/source/stl/Jig_Main.stl) | 2 | [Printed Parts Settings](../partsSettings.md) |
| [cable_clip_vertical.stl](../../parts/extra/bearCableClip/cable_clip_vertical.stl) | 5 | [Printed Parts Settings](../partsSettings.md) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| M2 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| M3 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| M5 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| Blue Tape | 1 roll | | [Amazon](https://amzn.to/3ujyctH) |
| Ethernet Stripper/Punch Down Tool | 1 | A plastic one is fine, if you have it | [Amazon](https://www.amazon.com/Weletric-Stripper-Crimping-Stripping-Telephone/dp/B078B5G4B2) [Aliexpress](https://s.click.aliexpress.com/e/_AOMa0o) |

### Prep

1. Adapt the EXP1 (10pin IDC) cable to use Ethernet extensions (For legacy LCD support)

    1. Cut the EXP1 ribbon cable about 60mm from each end and separate the ribbons into individual wires.

        ![](img/20-PrepExp1.JPG)\
        *fig 20.1*

    2. For the adapter that will attach to the TFT touch screen (Key on top of connector), splice with a keystone jack. Red wire is wire 1. Wires 6/7/8 are not used for EXP1 and can be trimmed.

        ![](img/20-Exp1LCDKeystone.JPG)\
        *fig 20.2*

        Note: I used a stripper/puch down tool to make sure each wire was spliced properly. One of those plastic puch down tools, that usually comes with keystone jacks, would be fine but the ones I bought didn't come with them (That's what you get for $1/each).

        <details><summary>EXP1 Pinout</summary>
        <p>

        ![](img/20-exp1pinout.JPG)

        [Pinout Reference](https://reprap.org/wiki/RepRapDiscount_Full_Graphic_Smart_Controller)

        </p>
        </details>


    3. For the adapter that will attach to the controller board (Key on bottom connector), flip the cable over so red wire is on the left. Wiring is exactly the same as the LCD end. Wires 6/7/8 are not used for EXP1 and can be trimmed.

        ![](img/20-Exp1BoardKeystone.JPG)\
        *fig 20.3*

    4. Make sure to attach the little caps on the keystones. These prevent the spliced wires from slipping out. Also it's a good idea to label the connectors with "EXP1". The Exp1 and Exp2 cables will **not** be interchangeable.

        ![](img/20-Exp1KeystonesFinal.JPG)\
        *fig 20.4*

1. Adapt the EXP2 (10pin IDC) cable to use Ethernet extensions (For legacy LCD support)

     2. Follow the same process you used for the EXP1 cable but with wires 7 and 10 not attached.

        ![](img/20-Exp2Keystones.JPG)\
        *fig 20.5*

        <details><summary>EXP2 Pinout</summary>
        <p>

        ![](img/20-exp2pinout.JPG)

        [Pinout Reference](https://reprap.org/wiki/RepRapDiscount_Full_Graphic_Smart_Controller)

        </p>
        </details>

1. Adapt RS232 (5pin JST-XH) cable to use Ethernet extensions (For TFT support)

    1. Using the RS232 (Black) cable provided with the TFT touch screen and 2 keystone jacks, make ethernet adapters (See picture for pinout). You will also need to replace the dupont connector with a 5 pin JST-XH connector (White). Note that the cable is a cross over cable with the pins reversed on each side.

	    ![](img/20-rs232keystone1.JPG)\
        *fig 20.6*

        <details><summary>RS232 Pinout</summary>
        <p>

        ![](img/20-rs232pinout.JPG)

        </p>
        </details>

    2. Make sure to attach the little caps on the keystones. These prevent the spliced wires from slipping out. Also it's a good idea to label the connectors.

	    ![](img/20-rs232labeledCaps.JPG)\
        *fig 20.7*


### Assembly
1. Using 2 Main jigs postion the 576mm 2020 extrusion 45mm above the lower front 4040 extrusion. Attach the extrusion to the front vertical extrusions using 4x angle brackets and 8x 8mm M5 screws/T-Nuts (2 brackets on each side).

    ![](img/20-AttachExtSupp1.JPG)\
    *fig 20.8*

    ![](img/20-AttachExtSupp2.JPG)\
    *fig 20.9*

2. Plug the EXP1, EXP2, and RS232 adapters into the back of the TFT touch screen.

    ![](img/20-TFTwAdapters.JPG)\
    *fig 20.10*

3. Using 4x M3 6mm screws attach the TFT touch screen to the TFT35 Mount.

    ![](img/20-AttachTFTtoMount.JPG)\
    *fig 20.11*

4. Using 4x M3 12mm screws attach the TFT35 Mount to the left panel.

    ![](img/20-AttachTFTMountToPanel.JPG)\
    *fig 20.12*

5. Attach the knob onto the TFT touch screen encoder.

    ![](img/20-AttachTFTKnob.JPG)\
    *fig 20.13*

6. Attach 2x M5 10mm screws/T-Nuts to the left panel and attach to the frame as shown.

    ![](img/20-AttachLTPanel1.JPG)\
    *fig 20.14*

7. Don't bother using the M5 attachment point inside the left panel. It's a pain to get to and you won't be able to adjust the panels later if you use it.

    ![](img/20-AttachLTPanel2.JPG)\
    *fig 20.15*

8. Secure the bottom of the left panel using a M5 10mm screw/T-nut. Be careful because this part of the print is delicate. I broke it and had to fix it with crazy glue gel. To help position the T-nut use a strip of blue tape.

    ![](img/20-AttachLTPanel3Tape.JPG)\
    *fig 20.16*

    ![](img/20-AttachLTPanel3.JPG)\
    *fig 20.17*

9. Attach 2x M5 10mm screws/T-Nuts to the center panel and attach to the frame as shown.

    ![](img/20-AttachCPanel1.JPG)\
    *fig 20.18*

    ![](img/20-AttachCPanel2.JPG)\
    *fig 20.19*

10. Using a M3 16mm screw and nut, tie the left and center panels together.

    ![](img/20-AttachLtToCPanel.JPG)\
    *fig 20.20*

11. Attach 4x M5 10mm screws/T-Nuts to the right panel.

    ![](img/20-AttachRTPanelM5s.JPG)\
    *fig 20.21*

12. Carefully flex the panel to get the top T-Nuts into the 2040 extrusion channel and tighten.

    ![](img/20-AttachRTPanel1.JPG)\
    *fig 20.22*

    ![](img/20-AttachRTPanel2.JPG)\
    *fig 20.23*

13. Adjust the panels to close any gaps. I had to shift the left and right panels together to minimize the gaps.

    ![](img/20-AdjustPanels.JPG)\
    *fig 20.24*

14. Attach the bottom of the right panel using a M5 10mm screw/T-Nut.

    ![](img/20-AttachRTPanel3.JPG)\
    *fig 20.25*

15. Useing 4x M5 10mm screws/T-Nuts to attach the left and right grills to the bottom extrusion.

    ![](img/20-AttachLTGrill.JPG)\
    *fig 20.26*

    ![](img/20-AttachRTGrill.JPG)\
    *fig 20.27*

16. Here's what the front panel should look like at this point.

    ![](img/20-FullFrontPanel.JPG)\
    *fig 20.28*

17. Now attach 5 vertical wire mounts to the lower left side extrusion as shown.

    ![](img/20-wireMounts.JPG)\
    *fig 20.29*

18. Connect the 3 Ethernet cables to the 3 Ethernet adapters in the panel and zip tie to the vertical wire mounts. *Attach the other end of each cable to their correspoinding adapters to avoid mixing them up.*

    ![](img/20-attachEthCables.JPG)\
    *fig 20.30*

19. Here's what it should look like when everything is done.

    ![](img/20-final.JPG)\
    *fig 20.31*
















