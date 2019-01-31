# Raspberry-Pi-Setup
How I set up my pi's. <br />

## Operating System
[Raspbian Stretch](https://www.raspberrypi.org/downloads/raspbian/) with desktop and recommended software <br />
Flash the SD card using [Etcher](https://www.balena.io/etcher/) <br />

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
full usage guide at [raspberrypi.org](https://www.raspberrypi.org/documentation/configuration/raspi-config.md) <br />

## SSH
Passwordless SSH from my computer to the pi's <br />
- check for ssh keys on your computer in ~/.ssh <br />
- if none, generate them <br />
`ssh-keygen` <br />
- send ssh public key to the pi from your computer <br />
`ssh-copy-id <PI-USERNAME>@<PI-IP-ADDRESS>`  <br />
- now ssh to your pi! <br />
`ssh <PI-USERNAME>@<PI-IP-ADDRESS>` <br />
full ssh guide at [raspberrypi.org](https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md) <br />

## Pi Hostname Alias
add an alias for the pi's hostname <br />
- on your computer, edit /etc/hosts <br />
- add <PI-IP-ADRESS> <ALIAS> to the file <br />
- now ssh to your pi with the alias! <br />
`ssh <PI-USERNAME>@<ALIAS>` <br />

## GitHub
copy relevant github directories <br />
`git init` <br />
- create new folder as current state of the git repo <br />
`git clone <REPO>` <br />
