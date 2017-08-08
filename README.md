# Documentation for MelbPC 3D Printer

Printer is a CTC Prusa I3 Pro B.

It is a knockoff of Geeetech Prusa I3 Pro B. 

http://www.geeetech.com/wiki/index.php/Acrylic_Prusa_I3_build_instruction%288mm%29

Uses a GT2560 electronics board

http://www.geeetech.com/wiki/index.php/GT2560

In addition, we have purchased a webcam and a raspberry pi.

## Relevant Files in the Repository
### Marlin-1.1.4/Configuration.h and Marlin-1.1.4/Configuration_adv.h
To use these settings from fresh, download latest Arduino and Marlin 1.1.4 and then replace these two files.

## Software 

### Octoprint
Octorprint is running on a Raspberry Pi 2. It is used to operate the printer.

Octoprint uses Cura to do the slicing. You can find the Cura settings here https://github.com/microcontrollersig/melbpc3DPrinter/blob/master/cura_experimental.ini

UPDATE: Latest Cura can send print jobs directly to Octoprint. 
https://github.com/microcontrollersig/melbpc3DPrinter/blob/master/cura-2.6.2-infill30.curaprofile

You can use Advanced IP Scanner (http://filehippo.com/download_angry_ip_scanner/) to determine IP address of Pi. Alternatively, you can install Bonjour Print Services (https://support.apple.com/kb/DL999?locale=en_US), then access Pi with http://octopi.local (zeroconf)

## Tips and Tricks for Octopi/octoprint

Emergency webcam URL:
http://192.168.81.122:8080/?action=stream

From downstairs:

http://192.168.0.105 (provided there is an ethernet connection to pi. Remember to plug the USB cable from GT2560 board to one of the 4 USB ports on the Pi.)

http://192.168.0.105:8080 (webcam)


From upstairs:

Port forwarding has been enabled on the router attached to the Pi.


https://192.168.81.122


http://192.168.81.122:8080 (webcam)

#Place to Buy Filament
Plastrude (Bayswater)
http://shop.lybina.com/

Bilby
Aururum
 
SSH available also with user/passwd pi/raspberry

#Youtube Channel
https://www.youtube.com/channel/UClFt878ZUMr_Nmuxnf45obg
