# Internal-Positioning

A project for our TSSR / IT training course:

Setting up of a Internal Positioning project with 4 Raspberry Pi (model 3 b+), 1 Linux server (debian 10), which will also be a log server and 4 WiFi usb adapter (brand: Realtek, model: RTL8812b).

Step 1:
We will create an image of the Rpi OS and then clone it for each Rpi.

- Flash the OS of the Raspberry Pi to SD card whith the "dd if" command.

Link to Raspberry OS:
https://downloads.raspberrypi.org/raspios_lite_armhf_latest

exemple:
"dd if='source of the OS' of='path of the SD card'".

- Integrate in the Raspberry pi the following script in the folder "/etc".

Link to the "launch" script:
https://github.com/NicolasVidal-Ch/launch

This script allows you to put the Rpi on time with NTP deamon, you will install all the necessary applications, SSH configuration, Rsyslog configuration, create and share the "hosts" folder between the server and the RPi, to retrieve the ip address of the RPI, with the NFS protocol, change password and suit keyboard settings to your language, delete the line in the "crontab" so it will not reboot on the initial "launch" script, remove the script "launch.sh" with a "Cron" and reboot.

- Now go to "/etc/crontab" with a text editor (nano, vim or other) and enter the following command:

"@reboot root sh /etc/'path of the launch script.sh'"

- The first step of our configuration for Rpi's is complete.

Step 2:

- 


