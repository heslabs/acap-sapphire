# PL Test

GitHub examples
https://github.com/Xilinx/emb-plus-examples

---
<img src="https://github.com/user-attachments/assets/2e19daa2-e281-4bfb-a384-fe40ba4cd517" width=800>


---
## Test application: PL 2D Filter
```
$ source /opt/xilinx/xrt/setup.sh
$ export PATH="/opt/xilinx/filter2d-pl:$PATH"

# Filter2d Accelertation Example Application Usage:
$ <Executable Name> <Filter> -i [path/testimg] -u [path/user_xclbin]

# Use -h to find available filter options
$ <Executable Name> -h

# Example using default test image
$ filter2D_accel_pl.elf Blur
```

---
<img src="https://github.com/user-attachments/assets/ed9e0a0a-afe8-40c7-ac74-a73a1f6491f3" width=800>
 

--- 
