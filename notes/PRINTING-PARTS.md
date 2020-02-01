# Instructing for printing the parts

## Extruder
Generally Ben has recommended 90% infill and 3 shells.  That seems excessive to me.  I'm going with the trusty Prusa recommended 20% infill and 3 shells.  5 tops layers 4 bottom layers

## Specific Parts Notes
### X_carriage_-_V6_locker_IR_mini.stl
* Orientation is upside down so reorient with largest surface on build plate
* Probably need supports for this one.
  Extra perimiters/detect briding perimiters/40% overhang thresh
* I printed in ABS/Black would probably consider PETG
  I used a enclosed build environment to prevent warping.

### X_carriage_-_Rear_plate.stl
* Flip this part over so the ramps don't require support
  Add supports for hex hole

### X_carriage_-_Block_shield.stl
* Flip fins against build plate
* Must use supports for ABS at least (Make an enforcer around just the grill)
  Note: Try this again with all the other fixes and without supports
* Have fan at 50% past 3rd layer
* Must have good contact with the bed
* THIS ONE IS TOUGH print separately 
* THIS ONE COULD DEFINITELY USE A REDESIGN

### X_carriage_-_modified_MK3_fan_blower.stl
* duct should be on bottom
* print with supports
* Orient as naturally colling duct on bottom
* Supports from build plate
* for ABS w/enclosure 50% cooling after 3rd layer

