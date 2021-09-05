# My BLV MGN Cube - Assembly Instructions

## Step 18 Install Heated Bed

**Warning Experimental Work Ahead**

![](img/all-hardHat.png)

I'm a big fan of right-sized engineering but this is an area where overengineering is much safer. The heated bed is easily one of the most likely components on a 3d printer to catch fire. That in mind I'm definitely going to overengineer here. Probably like you I'm an amature and I am accepting the risk for myself on what I'm doing here. If you aren't comfortable doing the same then please consult a professional. If you think I'm duing something unsafe and stupid please let me know by raising an issue for the github project.

### Step 18 BoM

#### Hardware
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Heated Bed | 1 | 300mmx300mm Prusa MK42 Style, Design...Yikes | [Aliexpress](https://s.click.aliexpress.com/e/_9wyXiW)|
| Ring Wire Connectors | 2 | 14AWG M3 | [Aliexpress](https://www.aliexpress.com/item/4000098059922.html?spm=a2g0o.productlist.0.0.67e035eehfxpOl&algo_pvid=fd22be4d-13ac-432a-b708-f58a578c09d2&algo_exp_id=fd22be4d-13ac-432a-b708-f58a578c09d2-10) |

| Extruder Stepper Motor | 1 | STEPPERONLINE 17HS16-2004S1 | [STEPPERONLINE](https://www.omc-stepperonline.com/nema-17-bipolar-45ncm-64oz-in-2a-42x42x40mm-4-wires-w-1m-cable-and-connector.html?search=17HS16-2004S1) |
| BMG Extruder | 1 | A good quality clone is fine | [Aliexpress](https://www.aliexpress.com/item/32917029058.html?spm=a2g0s.9042311.0.0.27424c4d85bUyI) |
| M3 35mm Socket Head Cap Screws | 3 | DIN912 (Should be included with the BMG Extruder Kit)| |
| M3 8mm Socket Head Cap Screws | 1 | DIN912 | |
| M5 T-Nuts | 4 | Hammer Head/Drop In Style | |
| M5 10mm Socket Button Head Screws | 2 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M5 8mm Socket Button Head Screws | 2 | DIN9427 | [Amazon](https://amzn.to/3txrazT) [AliExpress](https://s.click.AliExpress.com/e/_ASWaER) |
| M3 Thin Square Nuts | 1 | DIN562 | |
| 1/2" Flex Tubing | 62cm | Also called split wire loom | [Home Depot](https://www.homedepot.com/p/Gardner-Bender-3-8-in-and-1-2-in-Flex-Tubing-7-ft-and-10-ft-Combo-Pack-FLX-538C10/205588197#product-overview) [Amazon](https://www.amazon.com/Gardner-Bender-FLX-538C10-Assorted-Corrugated/dp/B01MSN7D25/ref=sr_1_10?dchild=1&keywords=split%2Bflex%2Btubing%2B1%2F2%22&qid=1628354523&s=hi&sr=1-10&th=1) [Aliexpress](https://www.aliexpress.com/item/32855974110.html?spm=a2g0o.productlist.0.0.112a72eas6e75a&algo_pvid=6370ddcb-8c94-4862-98e7-a1bb0f65fe20&algo_exp_id=6370ddcb-8c94-4862-98e7-a1bb0f65fe20-28) |
| 3mm x 10.16cm zip ties (4in)  | 11 | ~2.5mm x ~120mm | [Amazon](https://amzn.to/3p2nDaE) |
| 24 inch Nylon zip ties | 1 | ~9mm wide at least 60cm long | [Amazon](https://www.lowes.com/pd/Utilitech-15-Pack-24-in-Cable-Ties/50005756) |

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|

| [extruder-mount.stl](../../extra/hotend-cable-manager/files/extruder-mount.stl) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [frame-hotend-cable-locker.stl](../../extra/hotend-cable-manager/files/frame-hotend-cable-locker.stl) | 1 | [Printed Parts Settings](../partsSettings.md) |
| [flex-tube-reinforcer.stl](../../extra/hotend-cable-manager/files/flex-tube-reinforcer.stl) | 10 | [Printed Parts Settings](../partsSettings.md) |
| [hotend-cable-guide.stl](../../extra/hotend-cable-manager/files/hotend-cable-guide.stl) | 5 | [Printed Parts Settings](../partsSettings.md) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Multimeter W/Continuity Tester | 1 | This multimeter has a temp probe too! | [Amazon](https://amzn.to/3sxUjeT) |

| 1.5mm Allen Wrench | 1 | For extruder gear | [Amazon](https://amzn.to/3qNmEgs) |
| M3 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |
| M5 Screwdriver | 1 | | [Amazon](https://amzn.to/3qNmEgs) |

### Prep
1. Fix Bed wires. Bed wires soldered to a bed are a bad idea. I bent these wires about 10 times taking it in and out of the box. They're already breaking. Breaking decreases the guage and increases the heating of the wire which could cause them to catch fire.

    ![](img/18-FrayedBedWires.JPG)\
    *fig 18.1*

    Note: Factory wires didn't have gauge but they measured to be about 16 AWG. That is too small for ~400W at 24V. Also the insulation was stiff which also isn't good for a motion application.

2. Drill holes 7.3mm on each side of main hole.
   Drill bit should be 3mm or 1/8" for us which is about 3.2mm

The heated bed I have has multiple design flaws so I'm going to have to fix them.
    2. Bed wires soldered to bed instead of crimped. Take a look at the picture and you can see why this is a very bad idea. Note as the wire frays you will essentially decreate it's guague and this could lead to the bed wires heating up and possibly starting a fire!!

Test heated bed element using the multimeter set to read resistance. You're really just looking for a finite resistance, probably 1-2. If you are interested in the math V*V/R=W so in my case 24V*24V/1.5Ohms=384W.

    ![](img/18-HeaterTest.JPG)\
    *fig 18.1*

http://wiresizecalculator.net/calculators/advancedwireampacity.htm
https://www.powerstream.com/Wire_Size.htm


Remove any sharp edges on the inside of the flex tube reinforcers.

    ![](img/17-ReamReinforcer.JPG)\
    *fig 17.1*

### Assembly
1. Place the M3 Square nut in the frame cable locker and use an M3 8mm screw to secure itkl.

    ![](img/17-InstallclampOnCableLocker.JPG)\
    *fig 17.2*

2. Attach the frame cable locker with 2x M5 8mm screws and T-nuts centered on the top back extrusion.

    ![](img/17-AttachFrameCableLocker.JPG)\
    *fig 17.3*

3. Place the mounting plate on the stepper motor and measure a 2mm gap from the plate to the botton of the BMG extruder gear. Carefully tighten the set screw. **DON'T OVERTIGHTEN THE SET SCREW OR IT WILL STRIP**

    ![](img/17-SetBMGGear.JPG)\
    *fig 17.4*

4. Separate the BMG extruder and insert the bowden adapter.

    ![](img/17-BowdenAdapter.JPG)\
    *fig 17.5*

5. Make a BMG/Extruder Mount/Stepper sandwich. To help the stepper/gear insert into the BMG extruder try gently wobbling it. Note stepper wires are on the left.

    ![](img/17-InsertStepperGearBMG.JPG)\
    *fig 17.6*

6. Complete the extruder mount using 3x M3 35mm screws.

    ![](img/17-FinishExtruderMount.JPG)\
    *fig 17.7*

7. Using 2x M5 10mm and T-nuts attach the extruder to frame with the bowden hole on the printer centerline.

    ![](img/17-AttachExtruderMount.JPG)\
    *fig 17.8*

    ![](img/17-AttachExtruderMount2.JPG)\
    *fig 17.9*

7. Attach the BMG extruder tensioner.

    ![](img/17-ExtruderTensioner.JPG)\
    *fig 17.10*

8. Insert 10 of the flex tube reinforcers into the 62cm flex tube as indicated by the pictre. The reinforcers are spaced about 9cm apart (center to center). There are 2 reinforcers at one end, for the hotend locker, and 3 reinforcers at the other end, for the frame locker.

    ![](img/17-WireLoom.JPG)\
    *fig 17.11*

9. Carefully insert the cables into the flex tube and through the reinforcers. Try not to twist the cables around one another in the tube. Don't put connectors inside of the tube.

    ![](img/17-CablesInFlexTube.JPG)\
    *fig 17.12*

10. Using 3x small zip ties secure the end of the flex tube, that has 2 reinforcers, to the Hotend cable locker. The flex tube slit should be centered on the locker. Secure any loose wires using zip ties (Ugly, but it works for now). Again: Connecters inside the flex tube is bad.

    ![](img/17-SecureFlexToHELocker.JPG)\
    *fig 17.13*

    ![](img/17-FlexTubeAlignment.JPG)\
    *fig 17.14*

11. Thread the large zip tie into the hotend locker until the head of the zip tie clicks into place.

    ![](img/17-ZipTieIntoHELocker.JPG)\
    *fig 17.15*

12. Thread the PTFE tube and large zip tie onto the hotend cable guides and use the small zip ties to secure to the flex tube. The cable guide has a notch that should align with the reinforcer lips. The slit on the flex tube should be on top.

    ![](img/17-AssembleCableMgr1.JPG)\
    *fig 17.16*

    ![](img/17-AssembleCableMgr2.JPG)\
    *fig 17.17*

    ![](img/17-AssembleCableMgr3.JPG)\
    *fig 17.18*

13. Insert the large zip tie end and flex tube into the frame locker. Also cut the PTFE tube and insert into the extruder. Tighten the M3 to clamp the end of the zip tie. Around 79cm is what my PTFE tube mesured.

    ![](img/17-AttachToFrameLocker.JPG)\
    *fig 17.19*

14. Secure the frame locker using 3 small zip ties. *Note: I didn't use the top hole to allow the flex tube a little more play.*

    ![](img/17-SecureFrameLocker.JPG)\
    *fig 17.20*

14. Here is how the final cable guide should look.

    ![](img/17-CableMgr3.JPG)\
    *fig 17.21*

