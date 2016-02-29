# Documentation for MelbPC 3D Printer

Printer resembles a Geeetech Prusa I3 Pro B.
Uses a GT2560 electronics board.
In addition, we have purchased a webcam and a raspberry pi for advanced usage.

## Firmware
Tested with lastest Marlin version 1.1.0-RC3 (https://github.com/MarlinFirmware/Marlin/releases)

NB: Must use Arduino IDE version 1.0.1 (Available from http://www.geeetech.com/wiki/index.php/Download#Arduino_IDE). Later versions won't work on the GT2560.

## Software
Pronterface to operate printer
Slic3r or Cura to slice stl files to gcode

Alternatively, there is a Raspberry Pi running Octpi.
Octopi has advanced functionality like taking timelapse video, in addition to slicing STL files, printing gcode and operating 3D printer. 

If you have Bonjour Print Services installed, you can access the webpage from http://octopi.local, otherwise you will need to know the IP address of the pi (use something like Angry IP Scanner).
Remember to plug the USB cable from GT2560 board to one of the 4 USB ports on the Pi.

## Tips and Tricks
1. Latest version of Marlin has a feature called Mesh Bed Levelling. From the LCD, Prepare->Level Bed initiates a guide levelling/tramming procedure. Use  the knob to lower Z-Axis and the old paper routine, once you feel it's at the right level, single click on the knob, and it will proceed to next point.




