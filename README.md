# Raspberry-Pi-Setup
How I set up my pi's.

## Operating System
Raspbian Stretch with desktop and recommended software
[download](https://www.raspberrypi.org/downloads/raspbian/)

## Raspi-Config
configure basic settings
`sudo raspi-config`
- change password
- connect to wifi
- set hostname
- ssh enabled
- i2c enabled if needed for HATS
- expand filesystem
- finish and reboot

## SSH
Passwordless SSH from my computer to the pi's
- check for ssh keys on your computer in ~/.ssh
- if none, generate them
`ssh-keygen`
-send ssh public key to the pi from your computer
`ssh-copy-id <PI-USERNAME>@<PI-IP-ADDRESS>`
- now ssh to your pi!
`ssh <PI-USERNAME>@<PI-IP-ADDRESS>`

## Pi Hostname Alias
add an alias for the pi's hostname
- on your computer, edit /etc/hosts
- add <PI-IP-ADRESS> <ALIAS> to the file
- now ssh to your pi with the alias!
`ssh <PI-USERNAME>@<ALIAS>`
