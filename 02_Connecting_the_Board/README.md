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
### Connect to APU serial port from EDGE+ box by serial port

 
```
demo@embplus:~$ sudo picocom -b 115200 /dev/ttyUSB1
picocom v3.1
Type [C-a] [C-h] to see available commands
Terminal ready
```

#### picocom available command (Ctrl-h)
```
*** Picocom commands (all prefixed by [C-a])

*** [C-x] : Exit picocom
*** [C-q] : Exit without reseting serial port
*** [C-b] : Set baudrate
*** [C-u] : Increase baudrate (baud-up)
*** [C-d] : Decrease baudrate (baud-down)
*** [C-i] : Change number of databits
*** [C-j] : Change number of stopbits
*** [C-f] : Change flow-control mode
*** [C-y] : Change parity mode
*** [C-p] : Pulse DTR
*** [C-t] : Toggle DTR
*** [C-g] : Toggle RTS
*** [C-|] : Send break
*** [C-c] : Toggle local echo
*** [C-w] : Write hex
*** [C-s] : Send file
*** [C-r] : Receive file
*** [C-v] : Show port settings
*** [C-h] : Show this message

```

---
#### Login to APU
Press Enter to login 

```
emb-plus-ve2302 login: petalinux
Password: petalinux
```

<img src="https://github.com/user-attachments/assets/7ce9862e-0bb4-46db-a9cf-f04fc20601cd" width=450>

---

<img src="https://github.com/user-attachments/assets/696df224-bb72-4b31-ac55-87db3eb2217b" width=750>
 
---
#### APU Info

<img src="https://github.com/user-attachments/assets/92d3a09a-672f-4dd6-bee6-f6adfa613653" width=750>


---
### Connect to PLM/RPU serial port from EDGE+ box by serial port

```
$ sudo picocom -b 115200 /dev/ttyUSB2
Password: petalinux
```

