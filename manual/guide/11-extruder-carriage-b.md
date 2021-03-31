# My BLV MGN Cube - Assembly Instructions

## Step 11 Finish Building Extruder Carriage

### Step 11 BoM

#### Hardware
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Black Wire | ~12cm | 22 AWG Stranded Silicone | [Amazon](https://amzn.to/3ruTli7) |
| Green Wire | ~12cm | 22 AWG Stranded Silicone | [Amazon](https://amzn.to/3ruTli7) |
| Limit Switch | 1 | 3P with handle | [Aliexpress](https://s.click.aliexpress.com/e/_A4VObA) |
| M2 15mm Philips Pan Head Screws | 2 | DIN7985 | |
| M2 Nuts | 2 | DIN934 | |
| M3 14mm Socket Head Cap Screws | 1 | DIN912 | |
| M3 25mm Socket Head Cap Screws | 2 | DIN912 | |
| Heat Shrink Tubing | 10mm | Enough to cover 3 Pins <BR>of a JST-XH Male Connector | |
| M3 Nuts | 1 | DIN934 | |
| M3 Lock Nut | 1 | DIN934 | |
| M3 Washers | 2 | | |
| Male 3 Pin JST-XH Connector | 1 | Your controller uses these and you should too | [Aliexpress](https://s.click.aliexpress.com/e/_AWPLkY) [Amazon](https://amzn.to/3u0TiMD) |
| 3mm x 10.16cm zip ties (4in)  | 1-9 | ~2.5mm x ~120mm | [Amazon](https://amzn.to/3p2nDaE) |
| 5015 Blower fan | 1 | 24V Ball Bearings | [Aliexpress](https://s.click.aliexpress.com/e/_A9XEXg) |


 

#### Printed Parts
| Parts     | Quantity | Details |
|-----------|:--------:|---------|
| X_carriage_-_modified_MK3_fan_blower.stl | 1 | [Printed Parts Settings](../partsSettings) |
| X_carriage_-_Fan_mount.stl | 1 | [Printed Parts Settings](../partsSettings) |

#### Tools
| Parts     | Quantity | Details | Example Links |
|-----------|:--------:|---------|---------------|
| Soldering Iron and Solder | 1 | For small electronics | [Amazon](https://amzn.to/3rvsgLI) |
| Multimeter W/continuity tester | 1 | This multimeter has a temp probe too! | [Amazon](https://amzn.to/3sxUjeT) |
| Threadlocker | 0.2 Fl. Oz | Blue (removable) formula | [Amazon](https://amzn.to/3w539Tr) |
| M3 screwdriver | 1 | | |
| Small Philips screwdriver |1 | | |
| M3 Nut Wrench | 1 | Or small Needle Nose Pliers | |

### Prep

1. Solder 12cm lengths of black and green wires onto the limit switch. The black wire should attach to the Common (COM) terminal and the green wire should attach to the Normally Closed (NC) terminal. *It's important to use NC instead of NO. If the wire to the switch breaks it will automatically trigger the endstop*

    ![](img/11-SolderSWWires.jpeg)\
    *fig 11.1*

2. Test the limit switch and wiring using a continuity tester. It should be a closed circuit until you press the switch. *Throughout the wiring of the switch you should check this*

    ![](img/11-ContTest.jpeg)\
    *fig 11.2*

### Assembly
1. Remove the 2 lower M3 40mm screws/nuts from the X carrage and remove the bottom of the carriage. *Belts should be a little loose so it doesn't stress the rest of the carriage*

    ![](img/11-RemoveBottomXCarriage.jpeg)\
    *fig 11.3*

2. Dip the ends of the 2 M2 15mm Philips Pan Head Screws in threadlocker.

    ![](img/11-threadlocker.jpeg)\
    *fig 11.4*

3. Insert the 2 M2 15mm screws in to the lower X carrage as shown. You'll notice that I snapped off the bridge on this piece and I'm using M2's instead of M2.5s. This works much better, in reality, than what's described in BLV's extruder assembly video. I really really want to redesign this part.

    ![](img/11-M2ScrewsCarriage.jpeg)\
    *fig 11.5*

4. Attach the limit switch to the lower X carrage using the M2 screws and nuts. You may need to file down the sides of the carraige to get the switch to fit. Don't overtighted the screws as the switch is delicate and you can crush the hollow casing. Note how I routed the wires.

    ![](img/11-AttachSwitch.jpeg)\
    *fig 11.6*

5.  Insert an M3 nuts into the fan blower as shown. *Don't worry about the other hole*

    ![](img/11-M3inFanDuct.jpeg)\
    *fig 11.7*

6. Using the M3 14mm socket head cap screw, attach the fan blower to the lower X carriage.

    ![](img/11-AttachDuct.jpeg)\
    *fig 11.8*

7. Put the 10mm of heat shrink tubing over both wires and then solder the wires as shown. Then slide the tubing over the exposed terminals of the male JST connector and apply heat to the shrink the tubing. *I just use a cigarette ligher for this. Just be careful not to leave it in one spot for too long*

    ![](img/11-AttachSWConnector.jpeg)\
    *fig 11.9*


    ![](img/11-JSTWired.jpeg)\
    *fig 11.10*

    ![](img/11-JSTHeatShrink.jpeg)\
    *fig 11.11*

8. Reattach the lower X carriage to the rest of the X carriage using the M3 40mm screws/nuts. *I used some threadlocker on the nuts for good measure*

    ![](img/11-ReattachLowerXcarriage.jpeg)\
    *fig 11.12*

9. Zip tie the limit switch wiring to the back X carriage.

    ![](img/11-SecureSWWiring.jpeg)\
    *fig 11.13*

9. Cleanup and trim the belts. Now is a good time to trim your belts and verify the limit switch can trigger without the belts catching in the idlers. *I also had to redo some of my zip ties so I could trim the belts closer*

    ![](img/11-TrimBelts.jpeg)\
    *fig 11.14*

10. Insert the 2xM3 25mm Socket Head Cap Screws, with washers, into the 5015 blower fan.

    ![](img/11-screwsInBlower.jpeg)\
    *fig 11.15*

11. Put the Fan mount over the screw ends.

    ![](img/11-addFanMount.jpeg)\
    *fig 11.16*

12. Secure the screw closest to the blower opening with a lock nut. *Don't overtighten or you will damage the fan*

    ![](img/11-lockNutFanMount.jpeg)\
    *fig 11.17*

13. Attach the blower fan to the X carraige and blower duct. Make sure the mouth of the blower is inserted into the duct correctly. *Don't overtighten or you will damage the fan*

    ![](img/11-attachBlowerFan.jpeg)\
    *fig 11.18*

14. Secure the blower fan and limit switch wire with a zip tie and the mount point on the back x carrage plate. Leave a little slack on the blower wire but make sure it doesn't run into the linear rail mount when the carriage is all the way to the left.

    ![](img/11-FanCableCleanup.jpeg)\
    *fig 11.19*




