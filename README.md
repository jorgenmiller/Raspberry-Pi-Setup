# Raspberry-Pi-Setup
How I set up my pi's.

## Operating System
[Raspbian Stretch](https://www.raspberrypi.org/downloads/raspbian/) with desktop and recommended software  
Flash the SD card using [Etcher](https://www.balena.io/etcher/) (for Mac OS)  

## Raspi-Config
configure basic settings  
`sudo raspi-config`
- change password  
- connect to wifi  
- set hostname  
- SSH enabled  
- I2C or SPI enabled if needed for HATs  
- expand filesystem  
- finish and reboot  
  
full usage guide at [raspberrypi.org](https://www.raspberrypi.org/documentation/configuration/raspi-config.md)  

## SSH
Passwordless SSH from my computer to the pi's  
- check for ssh keys on your computer in ~/.ssh  
- if none, generate them  
`ssh-keygen`  
- send ssh public key to the pi from your computer  
`ssh-copy-id <PI-USERNAME>@<PI-IP-ADDRESS>`   
- now ssh to your pi!  
`ssh <PI-USERNAME>@<PI-IP-ADDRESS>`  
  
full ssh guide at [raspberrypi.org](https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md)  

## Pi Hostname Alias
add an alias for the pi's hostname  
- on your computer, use sudo to edit /etc/hosts  
- add `<PI-IP-ADRESS> <ALIAS>` to the file  
- now the alias is linked to the IP address
- now ssh to your pi with the alias!  
`ssh <PI-USERNAME>@<ALIAS>`  

## SCP
- copy file to the raspberry pi
`scp <FILE> <PI-USERNAME>@<PI-IP-ADDRESS>:<PATH>`

## GitHub
clone relevant github directory as new folder  
`git init`  
`git clone <REPO>`  
