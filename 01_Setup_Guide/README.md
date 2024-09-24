# Installation Guide

### Remote access to the IPC
```
   $ ssh demo@192.168.50.xxx -X
```

---
### Test: "PCIe"
```
  $ lspci -vd 10ee:
```
<img src="https://github.com/user-attachments/assets/64880e3b-c7c3-498d-870e-2cdbc1b924a6" width=600>

---
### Test: "XRT (Xilinx Runtime)"
 
```
  $ source /opt/xilinx/xrt/setup.sh
  $ xbmgmt examine
```
<img src="https://github.com/user-attachments/assets/d3491350-0035-448e-8552-bfbd094000dd" width=600>

---
### Test: "Verify"
```
  $ source /opt/xilinx/xrt/setup.sh
  $ xbutil validate -r verify -d --verbose
```
<img src="https://github.com/user-attachments/assets/565951d2-8d6f-4f1a-b132-3125234119ab" width=600>

---
### Test: "DMA"
```
  $ xbutil validate -r dma -d --verbose
```
<img src="https://github.com/user-attachments/assets/629a4b79-1c68-4d37-bd37-0c05bd893616" width=600>

### Test: "Bandwidth"
```
  $ xbutil validate -r mem-bw -d --verbose
```
<img src="https://github.com/user-attachments/assets/1a7810c6-af00-4bba-91b8-2281a4e60d34" width=600>


### Test: "AIE"
```
  $ xbutil validate -r aie -d --verbose
```
<img src="https://github.com/user-attachments/assets/a6f2ce65-7036-45de-ae35-7020ccbfa7bf" width=600>

---

