# FastIC+ readout 

This repository contains the project files and manufacturing outputs for the FastIC+ readout. The files for the [userboard](https://github.com/WojtaCZ/fastic-userboard-hw) are also available to simplify development of sensor boards compatible with the readout.

<div align="center">
  <img src="outputs/images/3d-top.png" width="45%" />
  <img width="8%"> </img>
  <img src="outputs/images/3d-bottom.png" width="45%" /> 
</div>

## Output files
Schematic, BOM and 3D renders are available in the outputs folder aswell as the gerbers and pick and place files needed for assembly. Gerbers and P&P files for both a single board and a 2x2 panel are provided.

## Flashing the firmware

Before the first startup, the onboard [Tag-Connect 6 pin SWD connector](https://www.tag-connect.com/product/tc2030-ctx-stdc14-for-use-with-stm32-processors-with-stlink-v3) shall be used with a compatible programmer like [STLINK-V3](https://www.st.com/en/development-tools/stlink-v3set.html) to flash the device with the bootloader provided.

After the bootloader has been flashed, the boot address option bytes shall be programmed to the following values:
**BOOT_CM7_ADD0** = 0x08020000
**BOOT_CM7_ADD1** = 0x08000000

After this procedure is complete, connect the device 