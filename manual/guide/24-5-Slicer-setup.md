PrusaSlicer Setup

import the BLV's SuperSlicer config
Change gcode to Marlin 2
Change START_GCODE to
```
START_PRINT EXTRUDER_TEMP=[first_layer_temperature] BED_TEMP=[first_layer_bed_temperature]
PRIME_LINE
```

End G-Code
```
END_PRINT
PLAY_MUSIC
```