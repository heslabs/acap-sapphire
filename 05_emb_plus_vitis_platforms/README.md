## Embedded+ HW/PL platform repository.

The accelerator's Vitis platform repository can be found in 
https://github.com/Xilinx/emb_plus_vitis_platforms

---
### Introduction
This repo is used to capture Vivado XSA generation of the Embedded+ HW/PL platform & Reconfigurable Modules (RMs). The emb_plus_ve2302 hw_platform targets the ve2302 FPGA.

---
### Instructions
This repo contains submodules. To clone this repo, run:

git clone --recursive https://github.com/Xilinx/emb_plus_vitis_platforms.git

---
### Contents
This repo contains a DFX platform and multiple overlays.

Platforms list:
  * ve2302_pcie_qdma

Overlays list:
  * bandwidth_test
  * filter2d_aie*
  * filter2d_pl
  * validate_aie2_pl
  * verify_test

These overlays are untested in hardware. Testing will happen in the next release.

---
### Tools Version
This branch is targeting the Vivado and Vitis 2023.2 tools version. Note that not all platforms and overlays may be validated with this tools version. Consult the application specific documentation for the latest validated version.
