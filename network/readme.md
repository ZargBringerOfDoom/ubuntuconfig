https://help.ubuntu.com/lts/serverguide/network-configuration.html

To temporarily configure an IP address, you can use the ifconfig command

sudo ifconfig eth0 10.0.0.100 netmask 255.255.255.0

To configure a default gateway

sudo route add default gw 10.0.0.1 eth0

If you no longer need this configuration and wish to purge all IP configuration from an interface

ip addr flush eth0

Static IP Address Assignment

 file /etc/network/interfaces

auto eth0
iface eth0 inet static
address 10.0.0.100
netmask 255.255.255.0
gateway 10.0.0.1


