## Embedded+ HW/PL platform repository.

The accelerator's Vitis platform repository can be found in https://github.com/Xilinx/emb_plus_vitis_platforms

---
### Introduction
This repo is used to capture Vivado XSA generation of the Embedded+ HW/PL platform & Reconfigurable Modules (RMs). The emb_plus_ve2302 hw_platform targets the ve2302 FPGA.

---
### Instructions
This repo contains submodules. To clone this repo, run:
```
git clone --recursive https://github.com/Xilinx/emb_plus_vitis_platforms.git
```

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

---
### Tool Flow
At a high-level, the builds steps are as follows:

1. AMD Vivado™ platform design: The Vivado design is augmented with platform parameters that describe the meta data and physical interfaces available to the AMD Vitis™ compiler for stitching in programmable logic (PL) or artificial intelligence engine (AIE) kernels.

2. Platform creation: The software command-line tool (XSCT) utility is used to create an extensible platform whose main component is the XSA created by Vivado in step 1.

3. PL kernels: The Vitis compiler is used to compile PL accelerator kernels from C/C++ using high-level synthesis (HLS) or to package register transfer level (RTL) kernels. The kernels are compiled into xo files and consumed by the Vitis linker in the next step.

4. AIE kernels: The Vitis compiler is used to compile AIE accelerator kernels from C/C++ into a libadf.a file and consumed by Vitis.

5. Vitis linker and packager: The Vitis linker integrates the PL kernels into the platform and implements the design. The packager combines the PL and the AIE portions. It generates a new device image (bitfile) as well as xclbin file containing meta data information about the PL and/or AIE kernels.

NOTE: Adding PL and/or AIE kernels to a platform is optional. If the system design needs certain acceleration or processing functions, then this build step is needed.

