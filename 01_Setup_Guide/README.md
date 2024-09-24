# Connecting to Board

## Remote access to the IPC
```
   $ ssh demo@192.168.50.xxx -X
```

### Login to Versal CA72
* Login: xilinx
* Password: petalinux

### Connect to APU serial port
```
$ sudo picocom -b 115200 /dev/ttyUSB1
```

### Connect to PLM/RPU serial port
```
$ sudo picocom -b 115200 /dev/ttyUSB2
```

<img src="https://github.com/user-attachments/assets/7dc21a82-b57f-430b-875d-e0b08c8f5b94" width=600>

## Installation Guide

* [FPGA Software Installation and Firmware Update](https://www.sapphiretech.com/en/commercial/edge-plus-vpr-4616-sys)

### Install Buntu OS

* Ubuntu 22.04，Linux Kernel version 5.15.0 
<img src="https://github.com/user-attachments/assets/1cd1413f-91f6-41e8-b280-a8387cdf95a8" width=600>

* Modify "grub"
```
$ uname -a
$ vi /etc/default/grub
GRUB_DEFAULT="Advanced options for Ubuntu>Ubuntu, with Linux 5.15.0-###-generic
```
* Update grub config & reboot
```
$ sudo update-grub
$ sudo reboot now
```

### Installing XTR



