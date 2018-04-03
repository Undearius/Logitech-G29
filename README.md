# Logitech-G29

This script is used to quickly change the turning range and alternate modes for the Logitech G29 Driving Force Wheel. It is meant for utter simplicity.

# Usage
This works best if placed in a directory that's in of your $PATH.

`g29 [-s|G27|G29] [1-900]`

The script accepts 3 arguements:
- `-s` to switch between G29 and G27 mode
- an explicit `G27` or `G29` to switch to the specified mode (reduntant with `-s`)
- a number between `1` and `900` to set the turning range

Currently, switching modes is not supported, so really this is basically just an alias for `echo 540 > /sys/bus/hid/drivers/logitech/$ID/range` to `g29 540`
