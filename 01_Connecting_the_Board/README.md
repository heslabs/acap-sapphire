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
