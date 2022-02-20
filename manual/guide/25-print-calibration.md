# My BLV MGN Cube - Assembly Instructions

## Step 25 Printer Calibration

## Gotcha about the bowden clip being loose and letting the tube slip in and out 1-2mm

### Belt Adjustment
See your note about getting the getting X square 
Use the iphone app and this guide on getting belt tension right
https://docs.vorondesign.com/tuning/secondary_printer_tuning.html

1. set belt length
   You want a 150mm length which is 140 bearing to bearing edge
   I cut a chop stick to the 140mm length
   Pace in betweend adjuster bearing and x block which lines up to bearing
   Go from bearing to bearing edge bearings are 10mm dia
2. Bring up the iphone app select the Select Middle button to show frequency chart
   Adjust chart to look between 0 and 150Hz
   hit play and start plucking You want the lowest frequency to be 110Hz
3. To tighten move both adjusters CCW and equal distance (Otherwise you could bring x axis out of square)
   Count clicks on each side
4. When done move x axis to front and make minor tenson adjustments to each belt to make sure you aren't racking it.
Tips: Make sure to hold the iphone mic as close as possible to the belt


### PID Tune
1. Turn off all heaters and let everything cooldown to room temp
   TURN_OFF_HEATERS
2. PID tune the extruder
   PID_CALIBRATE HEATER=extruder TARGET=200
3. Comment out the control: pid_Kp pid_Ki pid_Kd sections of the config
   Need to do this for SAVE_CONFIG to not be blocked.
3. Save the config
   SAVE_CONFIG

PID_CALIBRATE HEATER=heater_bed TARGET=65
SAVE_CONFIG

### Bed Leveling

### Print 1st layer
[Teaching Tech Guide](https://teachingtechyt.github.io/calibration.html#firstlayer)

Use custom start and end gcode and add your macros

| Key                | Value  |
|--------------------|--------|
| Auto Bed Levelling | No ABL |
| Bed X Dimension    | 310    |
| Bed Y Dimension    | 310    |



Probably tell people to use 310 x 310 bed with 5 mm safety

### Print the sample cube

### Calibrate Flow
https://teachingtechyt.github.io/calibration.html#flow
Upped the PLA temp to 210 because of underextrusion
Also increased x/y scale by 150%
Don't forget to disable the slow down for quick layers 
filament Settings/cooling/Slow down if layer print time is below: 0


### Calibrate StepperCurrent
https://teachingtechyt.github.io/calibration.html#steppers

https://www.omc-stepperonline.com/nema-17-bipolar-0-9deg-46ncm-65-1oz-in-2a-2-8v-42x42x48mm-4-wires-full-d-cut-shaft.html?search=17HM19-2004S
https://www.omc-stepperonline.com/nema-17-bipolar-45ncm-64oz-in-2a-42x42x40mm-4-wires-w-1m-cable-and-connector.html?search=17HS16-2004S1
Note the Steppers you have are rated at 2A so 2/1.41 = 1.418439716
Now the Stepper drivers are capable of 1.2 Continuous with a 2A peak
https://github.com/bigtreetech/BIGTREETECH-TMC2208-V3.0/blob/master/TMC2208-V3.0%20manual.pdf
So max would be 1.2A. Although I've set at the following without issues  
X/Y 1A run_current
500ma hold
Z 0.650A run_current
450ma hold
E 1A run_current
500mz hold

NOTE if you have a bunch of skips on the initial move after homing and when hotend is heating probably need to increase X/Y

### Calibrate Temp
https://teachingtechyt.github.io/calibration.html#temp

Base feed rate set at 60 (Because of part cooling and the generated code). Temp range 195-215 1st layer 205
Use your own start and end code
Retract is 0.75 (Consider putting this back at 6)
Enable part cooling on layer3

205 For the Black PLA

### Retraction Tuning

1. Use this guide
   https://teachingtechyt.github.io/calibration.html#retraction
2. See appendix for settings

4.5-7.5
60mm feedrate as these test shouldn't be affected by speed Try 160 base rate.


### input shaping
https://www.youtube.com/watch?v=EJapxNsntsQ&t=928s

1. Download this model
  https://www.klipper3d.org/prints/ringing_tower.stl
2. Use these slicker settings
   *layer height is 0.2
   *Vase mode
   *Speed at least 100 mm/sec for external perimeters
   *disable any dynamic acelleration control in the slicer
3. In klipper config
   max_accel and max_accel_to_decel are 7000 (They are)
   square_corner_velocity =5 (it is)
   RESTART klipper if any of the above are changed

4. in the terminal
Disable Pressure Advance:
SET_PRESSURE_ADVANCE ADVANCE=0
SET_INPUT_SHAPER SHAPER_FREQ_X=0 SHAPER_FREQ_Y=0
TUNING_TOWER COMMAND=SET_VELOCITY_LIMIT PARAMETER=ACCEL START=2000 FACTOR=100 BAND=5
  Note: unknown is fine

TUNING_TOWER COMMAND=SET_VELOCITY_LIMIT PARAMETER=ACCEL START=1250 FACTOR=100 BAND=5
TUNING_TOWER COMMAND=SET_VELOCITY_LIMIT PARAMETER=ACCEL START=2000 FACTOR=100 BAND=5

Execute the command TUNING_TOWER COMMAND=SET_VELOCITY_LIMIT PARAMETER=ACCEL START=1250 FACTOR=100 BAND=5. Basically, we try to make ringing more pronounced by setting different large values for acceleration. This command will increase the acceleration every 5 mm starting from 1500 mm/sec^2: 1500 mm/sec^2, 2000 mm/sec^2, 2500 mm/sec^2 and so forth up until 7000 mm/sec^2 at the last band.

Do not turn the model. The model has X and Y marks at the back of the model. Note the unusual location of the marks vs. the axes of the printer - it is not a mistake. The marks can be used later in the tuning process as a reference, because they show which axis the measurements correspond to.

5.
SET_PRESSURE_ADVANCE ADVANCE=0
SET_INPUT_SHAPER SHAPER_TYPE=MZV

## Pressure Advance
1. Download the calibration STL  
https://raw.githubusercontent.com/Klipper3d/klipper/master/docs/prints/square_tower.stl
2. Use 0 infill .3 mm layer height disable any dynamic accelleration control 1 perimiter
3. 
3. Run the following gcode


        SET_VELOCITY_LIMIT SQUARE_CORNER_VELOCITY=1 ACCEL=500
        TUNING_TOWER COMMAND=SET_PRESSURE_ADVANCE PARAMETER=ADVANCE START=0 FACTOR=.005 ; for direct drive
        TUNING_TOWER COMMAND=SET_PRESSURE_ADVANCE PARAMETER=ADVANCE START=0 FACTOR=.020 ; for long bowden

4. Measure from very bottom to best spot

27.93mm X 0.020 = .559
20.45 x 0.020 = .409
24.00 x 0.020 = .48


## Appendix Retraction Settings  

Settings for retraction tuning form
_________________________________________________________________________

G-Code originally generated by Simplify3D(R) Version 4.1.2
This calibration test gcode modified by the Teaching Tech Calibration website: https://teachingtechyt.github.io/calibration.html
All changes are marked in the gcode with 'custom' at the end of each line. Open the gcode in a text editor and search for this to your check inputs if needed.


Nozzle diameter: 0.4 mm
Layer height: 0.2 mm
Custom start gcode:
M190 S0 ; Use this to suppress built in bed heatup
M104 S0 ; Use this to suppress built in hotend heatup
START_PRINT EXTRUDER_TEMP=205 BED_TEMP=55


Bed: 310 x 310 mm

Base feedrate: 160 mm/sec
Perimeters: 96 mm/sec
Solid infill: 128 mm/sec
Travel moves: 267 mm/sec
First layer: 80 mm/sec

Temperatures:
Bed: 55 deg C
Hot end: 205 deg C


Part Cooling: 100% from layer 3


ABL: No ABL

Segment | Retraction distance | Retraction speed | Extra restart distance | Unretract speed | Z hop
   F    |          3 mm       |     40 mm/sec    |        0       mm      | 40 mm/sec       |  0 mm
   E    |          2.5 mm       |     40 mm/sec    |        0       mm      | 40 mm/sec       |  0 mm
   D    |          2 mm       |     40 mm/sec    |        0       mm      | 40 mm/sec       |  0 mm
   C    |          1.5 mm       |     40 mm/sec    |        0       mm      | 40 mm/sec       |  0 mm
   B    |          1 mm       |     40 mm/sec    |        0       mm      | 40 mm/sec       |  0 mm
   A    |          .5 mm       |     40 mm/sec    |        0       mm      | 40 mm/sec       |  0 mm
