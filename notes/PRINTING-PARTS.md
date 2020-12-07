# Instructions for printing the parts

## General Notes
Generally Ben has recommended 90% infill and 3 shells.  That seems excessive to me.  I'm going with the trusty Prusa recommended 20% infill and 3 shells.  5 tops layers 4 bottom layers

If you print all the stl's in the source directory you will have all the printed parts requred. Duplicate parts have renamed/duplicated stl's

## Hotend
Note: It useful to look at `BLV_Cube_mgn_Project_Drawing_-Hotend.pdf` to see the how the parts will be used

### `X_carriage_-_V6_Locker_BL-touch.stl`
* Orientation is upside down so reorient with largest surface on build plate
* Probably need supports for this one.
  Extra perimiters/detect bridging perimiters
* If supports needed do 40% overhang thresh and just from build plate?
* I printed in ABS
  I used a enclosed build environment to prevent warping.

### `X_carriage_-_V6_locker_IR_mini.stl`
* Orientation is upside down so reorient with largest surface on build plate
* Needs supports only from the build plate.
  Extra perimiters/detect bridging perimiters/40% overhang thresh
* I printed in ABS/Black would probably consider PETG
  I used a enclosed build environment to prevent warping.

### `X_carriage_-_Rear_plate.stl`
* Flip this part over so the ramps don't require support
  Add supports for hex hole

### `X_carriage_-_Block_shield.stl`
* Flip fins against build plate
* Must use supports for ABS at least (Make a slab enforcer around just the grill)
* Have fan at 50% past 3rd layer
* Must have good contact with the bed
* THIS ONE IS TOUGH print separately 
* THIS ONE COULD DEFINITELY USE A REDESIGN

### `X_carriage_-_Block_shield_for_Bltouch-8mm-12mm_sensors.stl` (Optional)
* Flip fins against build plate
* Must use supports for ABS at least (Make a slab enforcer around just the grill)
* Have fan at 50% past 3rd layer
* Must have good contact with the bed
* THIS ONE IS TOUGH print separately 
* THIS ONE COULD DEFINITELY USE A REDESIGN
* `X_carriage_-_Block_shield_for_Bltouch-8mm-12mm_sensors.3mf`

### `X_carriage_-_modified_MK3_fan_blower.stl`
* duct should be on bottom
* print with supports
* Orient cooling duct on bottom with fan opening on top
* Supports from build plate
* for ABS w/enclosure 50% cooling after 3rd layer

### `X_carriage_-_Fan_mount.stl`
* Works fine with no support
* Print in ABS

## Rear Corners and Bed
### `Bed_frame_cover_-_front_left.stl` (front\_right/rear\_left/rear\_right)
* These are all the same part you need Qty 4
* Orient rectanguar side, without hole, on bottom 
* Note: bevel on bottom curled a lot so try running fan at 50% past 3rd layer next time
* `Bed_frame_cover_-_all.3mf`

### `Z_mount_-_Left_mgn_mount.stl (Left/Right)`
* These are the same part you need Qty 2
* Orient with 20x20 on top and 2 through holes horizontal
* `Z_mount_-_mgn_and_block_mount.3mf`

### `Z_mount_-_Left_block.stl (Left/Right)`
* These are similar (accept they are labelled right and left
* orient with flattest side on bottom
* Need supports for the counter sunk holes but not the writing on the side use an support bocker for that.

## FRAME??
### `Jig_main.stl`
* orient flat on the build plate text facing up..duh
* Rotate 45% about the Z axis if it's too big to fit on the build plate (Too big for my Prusa Mk3s
* Qty: 1
