# Instructions for printing the parts

## THIS IS THE OLD FILE ## You should be editing manual/partsSettings.md instead 

## General Notes
Generally Ben has recommended 90% infill and 3 shells.  That seems excessive to me.  I'm going with the trusty Prusa recommended 20% infill and 3 shells.  5 tops layers 4 bottom layers. I'm starting to come around to something a little stronger than the default prusa settings and starting to follow the [Greg Saun's Prusa Bear Settings](https://github.com/gregsaun/prusa_i3_bear_upgrade/blob/master/doc/print_settings.md)

If you print all the stl's in the source directory you will have all the printed parts required. Duplicate parts have renamed/duplicated stl's

### ABS Parts
| STL File | Infill % | Shells | top layers | bottom layers | Build Plate Supports | Everywhere Supports | Custom Support |
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
| Main_Cable_Tube_Holder.stl | 20 | 4 | 5 | 5 | Yes | | |

## OLD STUFF
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
* For ABS need to print with automatic supports from build plate (To prevent currling at rounded edges
* This could benefit from a rework
* `Bed_frame_cover_-_all.3mf`

### `Z_mount_-_Left_mgn_mount.stl (Left/Right)`
* These are the same part you need Qty 2
* Orient with 20x20 on top and 2 through holes horizontal
* `Z_mount_-_mgn_and_block_mount.3mf`

### `Z_mount_-_Left_block.stl (Left/Right)`
* These are similar (accept they are labelled right and left
* orient with flattest side on bottom
* Need supports for the counter sunk holes but not the writing on the side use an support bocker for that.

### `Z_rail_stopper_-_Top_Left.stl (Left/Right)`
* These are the same part you need Qty 2
* orient flat rectangular side on bottom
* Need supports from build plate for those slightly rouded bevels
* Using 45 degee bevels would eliminate need for supports
* `Z_rail_stopper_-_All.3mf`

### `Z_rail_stopper_-_Bottom_Left.stl (Left/Right)`
* These are the same part you need Qty 2
* orient flat rectangular side on bottom (Side with countersunk holes)
* Need supports from build plate for those slightly rouded bevels and unsupported countersunk holes
* Using 45 degee bevels and sacrificial layer would eliminate need for supports
* `Z_rail_stopper_-_All.3mf`

### `Bed_Holder_-_Front_left_For_CR-10_bed_M4_screw.stl`
* My bed used M4 screws so I used this vs the M3 one. Notes should be the same for the M3 one
* Orient flat side down
* `Bed_Holder_-_All_For_CR-10_bed_M4_screw.3mf`

### `Left_Z_motor_mount.stl (Left/Right)`
* These are the same part you need Qty 2
* Orient with face with large hole on bottom
* Print with supports for those oh so annoying rounded edges
* Run the bed at 110 for all layers
* Do not let encloser get hotter than 36C
* I printed one at a time
* `Left_Z_motor_mount.3mf`
* `Right_Z_motor_mount.3mf`

### `Left_corner_-_Top.stl and Right_corner_-_Top.stl
* These parts are similar but not the same
* Orient with flat face down
* Print with supports from base plate because there are lots of holes
* Run the bed at 110 for all layers
* Optimal enclosure temp is ~33C 36C and you're X will start skipping
* If your enclosure is in the 20's you'll see too much shrinkage
* `Left_corner_-_Top.3mf`

### `Left_corner_-_Block.stl and Right_corner_-_Block.stl`
* These parts are similar but not the same
* Orient with flat face down
* only put supports from build plate under the *

### `Left_corner_-_cap.stl`, `Right_Corner_-_cap.stl`, `Right_motor_40mm_fan_mount.stl`, `Left_motor_40mm_fan_mount.stl`, `Right_corner_-_bottom_aux.stl`
* Orient with largest flat side on bottom
* Print with supports of build plate only (For counter sunk holes)
* Heatbed at 110C deg and max 35C enclosure temp
* `Right_corner_-_bottom_aux.3mf`

## Tensioner and X axis mounts
### `Left_Tensioner_-_mount.stl`, `Right_Tensioner_-_mount.stl`
* Orient mount with wheel countersink side down
* mount needs multiple support enforcers to print correctly see 3mf file
* `Left_tensioner_-_mount.3mf`
* `Right_tensioner_-_mount.3mf`

### `Left_Tensioner_-_idler_holder.stl`, `Right_Tensioner_-_idler_holder.stl`
* These are the same part Qty: 2
* Orient idler holder with square flat surface on bottom.
* `Left_tensioner_-_mount.3mf`
* `Right_tensioner_-_mount.3mf`

### `Left_Tensioner_-_tension_wheel.stl`, `Right_Tensioner_-_tension_wheel.stl`
* Orient tensioner wheel with hex face down
* tensioner wheel needs support enforcer cyliner only for coutersunk hole
* `Left_tensioner_-_mount.3mf`
* `Right_tensioner_-_mount.3mf`

## FRAME??
### `Jig_main.stl`
* orient flat on the build plate text facing up..duh
* Rotate 45% about the Z axis if it's too big to fit on the build plate (Too big for my Prusa Mk3s
* Qty: 1




