# Setup the Board

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

---
### Installing XRT (Xilinx Runtime)

* Get the latest XRT xrt_202410.<date>_22.04-amd64-xrt.deb from the automated builds at:
   * https://www.xilinx.com/member/forms/download/xef.html?filename=xrt_202410.2.17.326_22.04-amd64-xrt.deb
   * Ensure that the XRT version is 2.17.306 or later

* Move xrt.deb package to the Embedded+ platform running Ubuntu 22.04

* Install the 5.15 headers. Use the ### associated with the generic kernel installed.
```
$ sudo apt install linux-headers-$(uname -r)
```

* Install the xrt package
```
$ sudo dpkg -i xrt_202410.<date>_22.04-amd64-xrt.deb
```
The previous step may take some time as it will build the driver locally on target. After it completes verify that the drivers are installed correctly using: lsmod

---
### Install Embedded+ VE2302 "base" Package

* Get the latest base package from
   * https://www.xilinx.com/member/forms/download/xef.html?filename=xrt-emb-plus-ve2302-base_0.5.deb

* Move package to the Embedded+ platform
  
* Install with: Install VE2302 base design files
```
$ sudo dpkg -i xrt-emb-plus-ve2302-base_0.5.deb
```

---
### Install Embedded+ VE2302 XRT

* Get the latest test bitstream packages from:
   * xrt-verify-test-ve2302_0.5.deb:
      * https://www.xilinx.com/member/forms/download/xef.html?filename=xrt-verify-test-ve2302_0.5.deb
   * xrt-bandwidth-dma-test-ve2302_0.5.deb:
      * https://www.xilinx.com/member/forms/download/xef.html?filename=xrt-bandwidth-dma-test-ve2302_0.5.deb
   * xrt-aie-test-ve2302_0.5.deb:
      * https://www.xilinx.com/member/forms/download/xef.html?filename=xrt-aie-test-ve2302_0.5.deb

* Move the packages to the Embedded+ platform

* Install XRT test bitstreams
```
$ sudo dpkg -i xrt-verify-test-ve2302_0.5.deb
$ sudo dpkg -i xrt-bandwidth-dma-test-ve2302_0.5.deb
$ sudo dpkg -i xrt-aie-test-ve2302_0.5.deb
```

### Install Versal APU software pacakge

* Get the latest APU SW package from:
   * https://www.xilinx.com/member/forms/download/xef.html?filename=xrt-apu-linux-ve2302_0.5.deb

* Move the package to the Embedded+ platform.

* Install Versal APU SW:
```
$ sudo dpkg -i xrt-apu-linux-ve2302_0.5.deb

---
### Reboot system and update FPGA Firmqare

* Update FPGA firmware 

   * The VPR-4616-MB and VPR-4616-SYS are both shipped with OSPI image. You can check their version with “xbmgmt examine” command. A UUID of 00000000-0000-0000-0000-000079DB078F corresponds to emb-plus-ospi-emb-plus-ve2302-20240620051522.bin (0.5 release). Upgrading OSPI is necessary if the UUID does not match the release.

* Software requirements
   1. Vivado Installed
   2. FPGA(Xilinx) F/W: Versal OSPI image file (*.bin) and PDI file (*.pdi), which can be downloaded from

* Reference
   * https://www.sapphiretech.com/en/commercial/edge-plus-vpr_4616#Download



```


