# Documentation for MelbPC 3D Printer

Printer resembles a Geeetech Prusa I3 Pro B.
Uses a GT2560 electronics board.
In addition, we have purchased a webcam and a raspberry pi(optional).

## Firmware
Tested with lastest Marlin version 1.1.0-RC3 (https://github.com/MarlinFirmware/Marlin/releases)


NB: Must use Arduino IDE version 1.0.1 (Available from http://www.geeetech.com/wiki/index.php/Download#Arduino_IDE). Later versions won't work on the GT2560.


The Configuration.h provided by this repo contains the correct parameters for the 3D Printer.


## Software 
- Pronterface to operate printer
- Slic3r or Cura to slice stl files to gcode

## Raspberry Pi
Alternatively, there is a Raspberry Pi running Octpi.
Octopi has advanced functionality like taking timelapse video, in addition to slicing STL files, printing gcode and operating 3D printer. 


You can use Angry IP Scanner to determine IP address of Pi. Alternatively, you can install Bonjour Print Services, then access Pi with http://octopi.local (zeroconf)

## Tips and Tricks
1. Latest version of Marlin has a feature called Mesh Bed Levelling. From the LCD, Prepare->Level Bed initiates a guided levelling/tramming procedure. Use  the knob to lower Z-Axis and the old paper routine, once you feel it's at the right level, single click on the knob, and it will proceed to next point. If you want to save the mesh, issue a M500 (save to EEPROM). Then to view the stored mesh values, issue a G29 (either from Pronterface or Octopi). 

2. From downstairs:

http://192.168.0.105 (provided there is an ethernet connection to pi, octoprint interface. Remember to plug the USB cable from GT2560 board to one of the 4 USB ports on the Pi.)

http://192.168.0.105:8080 (webcam)



From upstairs:

Port forwarding has been enabled on the router attached to the Pi.


https://192.168.81.39 (or whatever the IP address of the router attached to the Pi is, again use Angry IP Scanner and look for D-link )


http://192.168.81.39:8080 (webcam)

 
SSH available also with user/passwd octopi/octopi 


