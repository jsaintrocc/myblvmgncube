# My BLV MGN Cube - Step 11 Finish Building Hotend Carriage

## [Step 11 BoM Spreadsheet Link](https://docs.google.com/spreadsheets/d/e/2PACX-1vTVx7BvB3V7CozF2l4eWkNntWrHSjOawmrsi_bRSVxQLIGVlfZTYEGp8a6fHpENV6hV2cn9PrDLHHl0/pubhtml?gid=750497263&single=true)

### Prep

1. Solder 15cm lengths of black and green wires onto the limit switch. The black wire should attach to the Common (COM) terminal and the green wire should attach to the Normally Closed (NC) terminal. *It's important to use NC instead of NO. If a wire breaks it will automatically trigger the endstop*

    ![](img/11-SolderSWWires.jpeg)\
    *fig 11.1*

2. Test the limit switch and wiring using the continuity tester on your Multimeter. It should be a closed circuit until you press the switch.

    ![](img/11-ContTest.jpeg)\
    *fig 11.2*

3. Make sure the heater cartridge and thermistor wires come out this side of the heater block.

    ![](img/11-V6BlockWiring.jpeg)\
    *fig 11.3*

### Assembly
1. Remove the 2 lower M3 40mm Socket Head Cap Screws/Nuts from the X carrage and remove the bottom of the carriage. *Belts should be a little loose so it doesn't stress the rest of the carriage*

    ![](img/11-RemoveBottomXCarriage.jpeg)\
    *fig 11.4*

2. Dip the ends of the 2 M2 15mm Philips Pan Head Screws in threadlocker.

    ![](img/11-threadlocker.jpeg)\
    *fig 11.5*

3. Insert the 2 M2 15mm screws in to the lower X carrage as shown. You'll notice that I snapped off the bridge on this piece and I'm using M2's instead of M2.5s. This works much better, in reality, than what's described in BLV's hotend assembly video.

    ![](img/11-M2ScrewsCarriage.jpeg)\
    *fig 11.6*

4. Attach the limit switch to the lower X carrage using the M2 screws and nuts. You may need to file down the sides of the carraige to get the switch to fit. Don't overtighted the screws as the switch is delicate and you can crush the hollow casing. Note how I routed the wires.

    ![](img/11-AttachSwitch.jpeg)\
    *fig 11.7*

5.  Insert an M3 nuts into the fan blower as shown. *Don't worry about the other hole*

    ![](img/11-M3inFanDuct.jpeg)\
    *fig 11.8*

6. Using the M3 14mm Socket Head Cap Screw, attach the fan blower to the lower X carriage.

    ![](img/11-AttachDuct.jpeg)\
    *fig 11.9*

7. Put 10mm of heat shrink tubing over both wires and then solder the wires as shown. Then slide the tubing over the exposed terminals of the male JST connector and apply heat to the shrink the tubing with the Mini Butane Torch. **NOTE: Take a look at the soldering procedure in [Build Bowden Extruder and Hotend Wiring Harness](16-extruder-hotend-harness.md) it's much better**


    ![](img/11-AttachSWConnector.jpeg)\
    *fig 11.10*

    ![](img/11-JSTWired.jpeg)\
    *fig 11.11*

    ![](img/11-JSTHeatShrink.jpeg)\
    *fig 11.12*

8. Reattach the lower X carriage to the rest of the X carriage using the M3 40mm screws/nuts. *I used some threadlocker on the nuts for good measure*

    ![](img/11-ReattachLowerXcarriage.jpeg)\
    *fig 11.13*

9. Zip tie the limit switch wiring to the back X carriage.

    ![](img/11-SecureSWWiring.jpeg)\
    *fig 11.14*

10. Cleanup and trim the belts. Now is a good time to trim your belts and verify the limit switch can trigger without the belts catching in the idlers. *I also had to redo some of my zip ties so I could trim the belts closer*

    ![](img/11-TrimBelts.jpeg)\
    *fig 11.15*

11. Insert the 2 M3 25mm Socket Head Cap Screws, with washers, into the 5015 blower fan.

    ![](img/11-screwsInBlower.jpeg)\
    *fig 11.16*

12. Put the Fan mount over the screw ends.

    ![](img/11-addFanMount.jpeg)\
    *fig 11.17*

13. Secure the screw closest to the blower opening with a lock nut. *Don't overtighten or you will damage the fan*

    ![](img/11-lockNutFanMount.jpeg)\
    *fig 11.18*

14. Attach the blower fan to the X carraige and blower duct. Make sure the mouth of the blower is inserted into the duct correctly. *Don't overtighten or you will damage the fan*

    ![](img/11-attachBlowerFan.jpeg)\
    *fig 11.19*

15. Secure the blower fan wores and limit switch wires with a zip tie to the mount point on the back x carrage plate. Leave a little slack on the blower wire but make sure it doesn't run into the linear rail mount when the carriage is all the way to the left. *You should have a little more slack for the limit switch connecter than what you see in this pic. I updated the directions after realizing it was too short*

    ![](img/11-FanCableCleanup.jpeg)\
    *fig 11.20*

16. Attach the Hotend to the X Carrage.

    ![](img/11-AddV6toCarriage.jpeg)\
    *fig 11.21*

17. Attach the PTFE tubing to the hotend and then secure the hotend using the BLTouch Locker and 2 M3 30mm Socket Head Cap Screws. *To insert the tubing into the hotend, remove the orange clip and press down on the fitting then reattach the clip to secure it.*

    ![](img/11-AttachBLTLocker.jpeg)\
    *fig 11.22*

18. Connect the cable locker using the M3 14mm Socket Head Cap Screw. Make sure it grabs the nut embedded in the X carriage. If the screw bottoms out before it's tight use some M3 washers. The orientation of the cable locker is important. The bumps/lower offset should point towards the front.

    ![](img/11-AttachCableLocker.JPG)\
    *fig 11.23*

19. Using the 2 M3 10mm Socket Head Cap Screws and nuts and washers. Secure the BLTouch to the locker mount. Make sure the BLTouch probe is secure but don't overtighten or you might damage it.

    ![](img/11-AttachBLT.jpeg)\
    *fig 11.24*

20. Route the BLTouch and 4010 fan wires through the bottom opening in the cable locker.

    ![](img/11-RouteCableLockerWires.JPG)\
    *fig 11.25*

21. Using the 4x M3 18mm Socket Head Cap Screws attach the Block Sheild to the front of the X carriage. Make sure the 4010 fan is oriented so it will blow air across the heat sink. Also route the BLTouch probe wires inside the Block Sheild making sure not to pinch them.

    ![](img/11-4010FanDirection.jpeg)\
    *fig 11.26*

    ![](img/11-4010FanOnScrews.jpeg)\
    *fig 11.27*

    ![](img/11-AttachBlockShield.JPG)\
    *fig 11.28*

    ![](img/11-BLVWireRouting.jpeg)\
    *fig 11.29*

    ![](img/11-WireLockerRouting.JPG)\
    *fig 11.30*

21. Now route and zip tie the heater cartridge and thermistor wires so they are out of the way.

    ![](img/11-HotEndWireRouting.jpeg)\
    *fig 11.31*

22. Here's what it should look like when everything is done.

    ![](img/11-FinishedHotend.JPG)\
    *fig 11.32*