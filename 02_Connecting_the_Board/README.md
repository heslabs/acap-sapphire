# Connecting to Board

1. Remote access to cloud PC
```
$ ssh acap@59.124.169.157 -X
Password:
```

---
2. Connect to SAPPHIRE EDGE+ box from cloud PC
```
$ ssh demo@192.168.51.134 -X
Password:
```
```
demo@embplus:~$ uname -a
Linux embplus 5.15.0-122-generic #132-Ubuntu SMP Thu Aug 29 13:45:52 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux
```
```
demo@embplus:~$ cat /proc/cpuinfo
processor       : 0
vendor_id       : AuthenticAMD
cpu family      : 23
model           : 24
model name      : AMD Ryzen Embedded R2314 with Radeon Graphics
stepping        : 1
microcode       : 0x8108109
cpu MHz         : 1400.000
cache size      : 512 KB

```

---
3. Install the utilities on Edge+ Box
```
$ apt install -y putty
$ sudo putty -serial -sercfg 115200,8,n,1,N -fn "client:Ubuntu Mono 16"  /dev/ttyUSB1
```
---
4. Connect to APU serial port from EDGE+ box by serial port

```
$ sudo picocom -b 115200 /dev/ttyUSB1
Password: petalinux
```

---
5. Connect to PLM/RPU serial port from EDGE+ box by serial port

```
$ sudo picocom -b 115200 /dev/ttyUSB2
Password: petalinux
```

---
<img src="https://github.com/user-attachments/assets/7dc21a82-b57f-430b-875d-e0b08c8f5b94" width=600>
