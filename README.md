# Internal-Positioning
A project for our TSSR / IT training:
Setting up of a Internal Positioning project with 4 Raspberry Pi (model 3 b+), 1 Linux server (debian 10), which will also be a log server and 4 WiFi usb adapter (brand: Realtek, model: RTL8812b).

We will create an image of the Rpi OS and then clone it for each Rpi.

Step:

- Flash the OS of the Raspberry Pi to SD card whith the "dd if" command.

Link to Raspberry OS:
https://downloads.raspberrypi.org/raspios_lite_armhf_latest

exemple:
"dd if='source of the OS' of='path of the SD card'".

- Integrate in the Raspberry pi the following script in the folder "/etc".

Link to the install script:
https://github.com/NicolasVidal-Ch/launch

This script allows to put the Rpi on time, create a variable to set its IP address, and download the second part of the installation.

- Now go to "/etc/crontab" with a text editor (nano, vim or other) and enter the following command:
"@reboot root sh /etc/'path of the lauch script.sh'"

-The first step of our configuration for Rpi's is complete.


