# Liquid handler grbl

This is a fork of grbl pre-configured for the CNC-based liquid handler system.
The system uses the Arduino CNC shield from protoneer (V3) to drive a 3 axis CNC converted to liquid handler sampler.

# Installation Instructions

The grbl firmware must be written to an Arduino UNO board before this can be connected to the Arduino CNC shield and the rest of the components.
This can all be done via the Arduino IDE:

1. Clone this repository, or just download the grbl_liquid_handler > grbl folder.
2. Create a .zip archive of the grbl folder (not the main folder!).
3. Open the Arduino IDE and go to Sketch > Include Library > Add zip library... and select the .zip archive you just created.
4. Once installed, a 'grblUpload' sketch should become available from File > Examples > grbl. Open it.
5. Connect the Arduino UNO board, select it in the IDE and click on the sketch upload button.

That is it! You can check if everything is working correctly by opening the serial monitor in the Arduino IDE and check the messages from the board:
You should read this message: `Grbl 0.9j \['$' for help\]`

# Default parameters

These are the Grbl parameters for the liquid handler (first):

$0=10 (step pulse, usec)
$1=25 (step idle delay, msec)
$2=0 (step port invert mask:00000000)
$3=0 (dir port invert mask:00000000)
$4=0 (step enable invert, bool)
$5=0 (limit pins invert, bool)
$6=0 (probe pin invert, bool)
$10=3 (status report mask:00000011)
$11=0.010 (junction deviation, mm)
$12=0.002 (arc tolerance, mm)
$13=0 (report inches, bool)
$20=1 (soft limits, bool)
$21=1 (hard limits, bool)
$22=1 (homing cycle, bool)
$23=3 (homing dir invert mask:00000011)
$24=25.000 (homing feed, mm/min)
$25=2000.000 (homing seek, mm/min)
$26=250 (homing debounce, msec)
$27=1.000 (homing pull-off, mm)
$100=400.000 (x, step/mm)
$101=400.000 (y, step/mm)
$102=400.000 (z, step/mm)
$110=6000.000 (x max rate, mm/min)
$111=6000.000 (y max rate, mm/min)
$112=1000.000 (z max rate, mm/min)
$120=100.000 (x accel, mm/sec^2)
$121=100.000 (y accel, mm/sec^2)
$122=50.000 (z accel, mm/sec^2)
$130=173.000 (x max travel, mm)
$131=285.000 (y max travel, mm)
$132=77.500 (z max travel, mm)
