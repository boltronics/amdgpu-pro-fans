amdgpu-pro-fans
===============

Authors: DominiLux, Adam Bolte
License: Apache Version 2.0

It is a simple utility that allows you to set the fan speeds for AMD
cards when the AMDGPU Pro driver stack is in use. Originally written
by DominiLux as a proof of concept, I have adapted it here for use by
systemd.

Installation Instructions
-------------------------

    sudo apt-get install git
    git clone https://github.com/dominilux/amdgpu-pro-fans
    sudo install -o root -g root -m 0755 ./amdgpu-pro-fans/amdgpu-pro-fans.sh /usr/local/sbin/amdgpu-pro-fans
    sudo install -o root -g root -m 0644 ./amdgpu-pro-fans/amdgpu-pro-fans.service /etc/systemd/system
    sudo systemctl enable amdgpu-pro-fans.service
    sudo systemctl start amdgpu-pro-fans.service

Usage
-----

Edit adapter and fanpercent variables as required, and run:

    sudo ./amdgpu-pro-fans.sh

Bu default, this will set all GPU adapter fans to 85% of their maximum
speed.

Notes
-----

Fully tested on Ubuntu 16.04 with AMDGPU-PRO proprietary linux
drivers. It is now compatible with all Radeon R8 Series, R9 Series,
and RX Series graphics cards.
