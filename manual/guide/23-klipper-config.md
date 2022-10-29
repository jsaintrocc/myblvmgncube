# Setup Steppers

## Calculate Rotational Distance

[Klipper Howto](https://www.klipper3d.org/Rotation_Distance.html)

X & Y
Microstepping is 16
X and Y steppers are 0.9 Degree Steppers so 400 steps for 360 17HM19-2004S1
Z is 1.8 Degree stepper so 200 steps for 360 17HS19-2004S1
From Marlin I have: #define DEFAULT_AXIS_STEPS_PER_UNIT   { 200, 200, 400, 917.444 }

Calc X
rotation_distance = <full_steps_per_rotation> * <microsteps> / <steps_per_mm>
rotation_distance = 400 * 16/200
rotation_distance = 32 # Gotta set steps for rotation below if you are using a 0.9 motor

full_steps_per_rotation: 400    # The number of full steps for one rotation of the stepper motor. 200 for 1.8 motor or 400 for 0.9 motor.


Calc Z 200 * 16/200 = 8

## Extruder Steps
### Rough Calculation
1. For BMG and clones set a gear ratio of 50:17 It's advertized at 3:1 but in reality it's this

        gear_ratio: 50:17

2. Measure the diameter of the hobbed bolt (down in the groove of the teeth)

        rotation_distance = <diameter> * 3.1415
        rotation_distance = 7.5mm * 3.1415
        rotation_distance = 23.56

### Fine Calculation
Then use the following procedure to "measure and trim":

1. Make sure the extruder has filament in it, the hotend is heated to
   an appropriate temperature, and the printer is ready to extrude.

2. Use a marker to place a mark on the filament around 70mm from the
   intake of the extruder body. Then use a digital calipers to measure
   the actual distance of that mark as precisely as one can. Note this
   as `<initial_mark_distance>`. 70

3. Extrude 50mm of filament with the following command sequence:

        G91
        G1 E50 F60

    Note 50mm as `<requested_extrude_distance>`. Wait for the extruder to finish the
   move (it will take about 50 seconds). It is important to use the
   slow extrusion rate for this test as a faster rate can cause high
   pressure in the extruder which will skew the results. (Do not use
   the "extrude button" on graphical front-ends for this test as they
   extrude at a fast rate.)

4. Use the digital calipers to measure the new distance between the
   extruder body and the mark on the filament. Note this as
   `<subsequent_mark_distance>` 22. Then calculate:
   `actual_extrude_distance = <initial_mark_distance> - <subsequent_mark_distance>` 48

5. Calculate rotation_distance as:
   `rotation_distance = <previous_rotation_distance> * <actual_extrude_distance> / <requested_extrude_distance>`
   Round the new rotation_distance to three decimal places.

If the actual_extrude_distance differs from requested_extrude_distance
by more than about 2mm then it is a good idea to perform the steps
above a second time.

Note: Do not use a "measure and trim" type of method to calibrate x, y, or z type axes. The "measure and trim" method is not accurate enough for those axes and will likely lead to a worse configuration. Instead, if needed, those axes can be determined by measuring the belts, pulleys, and lead screw hardware.

## Miscellaneous
Sense_resistor default of 0.110 Ohm is correct for BTT 2208 V3.0
Current: Max continuous current is 1.2A with 2A burst.

## Blowden tube load unload calculation
1. load blowden tube by hand
2. mark at entry to extruder
3. unload bowden tupe and measure filament to mark
4. mine was 85cm
5. Configure load macros 

## Add section on configuring the beeper Maybe create a specific LCD section.

## Probe offsets
### Get X Y Proble offsets
Center toolhead G28 assuming your bed dim are right
Put painters tape under probe
in terminal "PROBE" and mark the location of the probe
RUN GET_POSITION to get current post of toolhead
Proble position = X:150.000000 Y:150.000000 Z:1.497500
Move nozzle to be exactly on top of mark
Use LCD jog controls
RUN GET_POSITION again
Nozzle position = X:177.300000 Y:144.900000 Z:0.497500

X = nozzle_x_position - probe_x_position = 27.3
Y = nozzle_y_position - probe_y_position = -5.1

Continue here https://www.klipper3d.org/Probe_Calibrate.html

### Z probe offset
1. Start Klipper calibration routine (And heat bed for PLA)

       M190 S65
       G28
       PROBE_CALIBRATE
2. Place paper under nozzle
3. Slowly adjust probe height

       TESTZ z=-.1

4. Test with paper (Should feel a little grab but not stuck)

   NOTE: you seem to have to add .1 to the saved value to get the proper offset.
         Maybe more grab or less grab? Whatever adds .1mm

6. Accept and save values

       ACCEPT
       SAVE_CONFIG

Note: SAVE_CONFIG doesn't work if BLTouch config is in it's own file. Known issue and don't know why it isn't fixed. Just manually update the z_offset value in the bltouch config
Note:

## Configure Thermistors
1. Heatbed
   2. Uses an epcos 100K thermistor whcihc is:

      sensor_type:  "EPCOS 100K B57560G104F

2. Hotend
   2. For a genuine e3d thermistor use:
      sensor_type: "ATC Semitec 104GT-2"
## Z Tilt
Z_TILT_ADJUST

Put section in on how to set stepper_z position_min for max tilt allowed.

## Troubleshooting
### Restarting Klipper
#### From ssh

    sudo service klipper restart

#### From Terminal

    RESTART
### Octoprint config
Cancel print
G91; Set to Relative position
G1 E-1 F300; retract the filament a bit before lifting the nozzle
G0 Z15; move z axis up 15
G28 X; home X axis
G1 Y150 F5000; move part out for inspection
G90; Set to Absolute position
M104 S0 ; turn off extruder heat
M140 S0 ; turn off heated bed
M106 S0 ; Turn off fan
M18; Move Freely


### DISABLE M108 support in octoprint

### Add the bed screws adjust secton
G28
SCREWS_TILT_CALCULATE

1 turn = 60 minutes
CW turn to left
CCW turn to right

## Machine Limits
Klipper ignores any machine limits from the slicer
So emit for time estimate only and set according to klipper config
machine_usage_limits: Use for time estimate 
