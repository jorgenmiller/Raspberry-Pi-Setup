# Raspberry-Pi-Setup
How I set up my pi's. <br />

## Operating System
Raspbian Stretch with desktop and recommended software <br />
[download](https://www.raspberrypi.org/downloads/raspbian/) <br />

## Raspi-Config
configure basic settings <br />
`sudo raspi-config`
- change password <br />
- connect to wifi <br />
- set hostname <br />
- ssh enabled <br />
- i2c enabled if needed for HATS <br />
- expand filesystem <br />
- finish and reboot <br />

## SSH
Passwordless SSH from my computer to the pi's <br />
- check for ssh keys on your computer in ~/.ssh <br />
- if none, generate them <br />
`ssh-keygen` <br />
- send ssh public key to the pi from your computer <br />
`ssh-copy-id <PI-USERNAME>@<PI-IP-ADDRESS>`  <br />
- now ssh to your pi! <br />
`ssh <PI-USERNAME>@<PI-IP-ADDRESS>` <br />

## Pi Hostname Alias
add an alias for the pi's hostname <br />
- on your computer, edit /etc/hosts <br />
- add <PI-IP-ADRESS> <ALIAS> to the file <br />
- now ssh to your pi with the alias! <br />
`ssh <PI-USERNAME>@<ALIAS>` <br />
