# Documentation for MelbPC 3D Printer

Printer resembles a Geeetech Prusa I3 Pro B 

http://www.geeetech.com/wiki/index.php/Acrylic_Prusa_I3_build_instruction%288mm%29

Uses a GT2560 electronics board

http://www.geeetech.com/wiki/index.php/GT2560

In addition, we have purchased a webcam and a raspberry pi.

## Files in the Repository
slic3r.ini: These Slic3r settings work well for simple prints. In Slic3r, File->Load Config

cura_experimental.ini: These settings produce good results for printing with Octoprint. Created using cura 15.04 . Must use this version because cura changed format from INI to json on later versions of cura.

Configuration.h: The main configuration file for Marlin.


## Firmware on GT2650
Tested with Marlin version 1.1.0-RC3 (https://github.com/MarlinFirmware/Marlin/releases)


NB: Must use Arduino IDE version 1.0.1 (Available from http://www.geeetech.com/wiki/index.php/Download#Arduino_IDE). Later versions won't work on the GT2560.





## Software 

### Steps involved in printing
- Need to produce an STL file for your print. Can source it from thingiverse.com, or make it yourself using tools such as Sketchup,Freecad, Solidworks, 123d, tinkercad etc.
- need to use a slicer program (Slic3r, Cura) to convert the STL file to a GCODE file.
- Then use another program to operate printer and send print jobs

### Option 1
- Use Pronterface to operate the printer
  https://github.com/kliment/Printrun
- Pronterface uses Slic3r for slicing. You will first need to configure Slic3r settings. Use the settings from this repository. Then simply load an STL file, then click Print.
- Requires directly connecting to controlled board using USB to PC.

### Option 2
There is a Raspberry Pi 2 running Octpi.Octoprint has advanced functionality like taking timelapse video and automatically uploading it to youtube. It has a web interface which can be accessed on the local network. For this to work, ensure Pi is powered, Ethernet and USB from controller board is connected.

Octoprint uses Cura to do the slicing. You can find the Cura settings here https://github.com/microcontrollersig/melbpc3DPrinter/blob/master/cura_experimental.ini

You can use Advanced IP Scanner (http://filehippo.com/download_angry_ip_scanner/) to determine IP address of Pi. Alternatively, you can install Bonjour Print Services (https://support.apple.com/kb/DL999?locale=en_US), then access Pi with http://octopi.local (zeroconf)

## Tips and Tricks for Octopi/octoprint

From downstairs:

http://192.168.0.105 (provided there is an ethernet connection to pi. Remember to plug the USB cable from GT2560 board to one of the 4 USB ports on the Pi.)

http://192.168.0.105:8080 (webcam)



From upstairs:

Port forwarding has been enabled on the router attached to the Pi.


https://192.168.81.39 (or whatever the IP address of the router attached to the Pi is, again use Advanced IP Scanner and look for the link below, which shows up on port 8080 mjpg-streamer)


http://192.168.81.39:8080 (webcam)

 
SSH available also with user/passwd pi/raspberry

#Youtube Channel
https://www.youtube.com/channel/UClFt878ZUMr_Nmuxnf45obg
