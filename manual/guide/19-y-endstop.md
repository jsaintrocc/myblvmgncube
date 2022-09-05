# My BLV MGN Cube - Step 19 Mount Y Endstop

## [Step 19 BoM Spreadsheet Link](https://docs.google.com/spreadsheets/d/e/2PACX-1vTVx7BvB3V7CozF2l4eWkNntWrHSjOawmrsi_bRSVxQLIGVlfZTYEGp8a6fHpENV6hV2cn9PrDLHHl0/pubhtml?gid=1290624575&single=true)

### Prep

1. Solder 45cm lengths of black and green wires onto the limit switch. The black wire should attach to the Common (COM) terminal and the green wire should attach to the Normally Closed (NC) terminal. *It's important to use NC instead of NO. If a wire breaks it will automatically trigger the endstop*

    ![](img/19-SolderSWWires.JPG)\
    *fig 19.1*

2. Test the limit switch and wiring using the continuity tester on your Multimeter. It should be a closed circuit until you press the switch.

    ![](img/19-ContTest.JPG)\
    *fig 19.2*

### Assembly
1. Attach the Limit switch to 3d printed Y-Endstop-for-kw11-3p mount using the 2x M2 12mm screws. *Pretend these are socket head screws instead of star/phillips heads. It's just what I had handy*

    ![](img/19-AttachYSwitchToMount.JPG)\
    *fig 19.3*

2. Attach the Y endstop mount to the frame as shown using 2x M5 10mm Screws and T-nuts (Fig 19.3). Positon it so that the switch is triggered just at the nozzle reaches the end of the bed and before it hits the bed power connector (Fig 19.4).

    ![](img/19-MountYStopToFrame.JPG)\
    *fig 19.3*

    ![](img/19-YstopNozzlePos.JPG)\
    *fig 19.4*