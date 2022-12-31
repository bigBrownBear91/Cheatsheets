# Connect with ssh to a server or device in a network
## Find the device to connect to
In a first step, you have to find the device in the network, you want to connect to. This is assuming, you want to connect to a device in the same network. You have first to find the ip-adress of your network.

`ip a`

Then, you can use the ip address to find all devices in the network. Note, that you have to replace the last block of the ip address with 0 and you have to attach a '/24' to the ip address

`nmap 192.168.101.0/24`

## Connect to the device
nmap lists all devices in the network and which ports (if any) are open. Pick the ip address of the device you wish to connect to and connect with the user.

`ssh pi@192.168.101.44`

where 'pi' is the user and 192.168.101.44 is the ip address of the server or device.

## Work on server or device
ssh opens a console, on which you can work.

## Exit ssh
Closing the terminal will interrupt the connection. You can also exit with the command 'exit'

`exit`
