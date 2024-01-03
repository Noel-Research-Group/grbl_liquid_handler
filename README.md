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
