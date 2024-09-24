# Connecting to Board

1. Remote access to cloud PC
```
$ ssh acap@59.124.169.157 -X
Password:
```

2. Connect to SAPPHIRE EDGE+ from cloud PC
```
ssh demo@192.168.51.134 -X
Password:
```

3. Login to Versal CA72
```
Login: xilinx
Password: petalinux
```

4. Connect to APU serial port
```
$ sudo picocom -b 115200 /dev/ttyUSB1
```

### Connect to PLM/RPU serial port
```
$ sudo picocom -b 115200 /dev/ttyUSB2
```

<img src="https://github.com/user-attachments/assets/7dc21a82-b57f-430b-875d-e0b08c8f5b94" width=600>
