# Connecting to Board

1. Remote access to cloud PC
```
$ ssh acap@59.124.169.157 -X
Password:
```

2. Connect to SAPPHIRE EDGE+ box from cloud PC
```
ssh demo@192.168.51.134 -X
Password:
```

3. Connect to Versal CA72 from EDGE+ box by SSH
```
Login: xilinx
Password: petalinux
```

4. Connect to APU serial port from EDGE+ box by serial port
```
$ sudo picocom -b 115200 /dev/ttyUSB1
```

5. Connect to PLM/RPU serial port by serial port
```
$ sudo picocom -b 115200 /dev/ttyUSB2
```

---
<img src="https://github.com/user-attachments/assets/7dc21a82-b57f-430b-875d-e0b08c8f5b94" width=600>
