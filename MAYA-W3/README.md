# MAYA-W3 series

## Description
This contains the module specific deliverables for u-blox MAYA-W3 series 
Wi-Fi/Bluetooth modules.

### What you can find here
* NVRAM files (*nvrams*)
  * Board configurations for MAYA-W3 modules
* CLM blob file (*clm_blob*)
  * Regulatory settings for certified MAYA-W3 modules
* Bluetooth patchram files (*bt-hcd*)
  * Bluetooth firmware updates and module specific configurations

## MAYA-W3 NVRAM files
The NVRAM files contain module specific parameters and configurations for 
MAYA-W3 series modules. Select the NVRAM file for your module variant and copy 
it as `cyfmac55500-sdio.txt` into the `/lib/firmware/cypress` folder on the target 
system.

The following NVRAM files are available:
* maya-w381-00b.nvram: NVRAM file for MAYA-W3x1/W3x0
* maya-w386-00b.nvram: NVRAM file for MAYA-W3x6/W3x2/W3x3

Additional NVRAM files supporting antenna diversity using RF_CNTL4 (J5):
* maya-w381-00b-ant_div.nvram: NVRAM file for MAYA-W3x1/MAYA-W3x0
* maya-w386-00b-ant_div.nvram: NVRAM file for MAYA-W3x6/W3x2/W3x3

## MAYA-W3 CLM blob
The clm_blob contains regulatory settings for the certified MAYA-W3 modules and 
antennas. See the MAYA-W3 system integration manual for the list of approved 
antennas and other regulatory requirements. 

The clm_blob supports the following country codes and radio type approvals:

| Country code | Country / region             |
|:------------:|:---------------------------- |
| CA           |  Canada (ISED)               |
| DE           |  EU/Great Britain (RED/UKCA) |
| JP           |  Japan (Giteki)              |
| US           |  US (FCC)                    |

Copy the clm_blob as `cyfmac55500-sdio.clm_blob` into the `/lib/firmware/cypress` 
folder on the target system.

## MAYA-W3 Bluetooth patchram files
The Bluetooth patchram files contain Bluetooth firmware updates and module 
specific settings. Patchram files are provided for different
* Module variants
  * MAYA-W3x0/W3x1
  * MAYA-W3x2/W3x3
  * MAYA-W3x6
* LPO configurations
  * eLPO for external LPO clock
  * XTAL for external crystal
  * iLPO for internal LPO (not adequate if low power Bluetooth LE is required)
* Regulatory standards and TX power configurations
  * FCC for US/CA/BT-SIG
  * RED for EU/Great Britain/Japan
  * Tx20 for max. TX power evaluation

Select the patchram file for your module variant, LPO configuration, and 
regulatory standard, and copy it as `/lib/firmware/brcm/BCM.hcd` to the target 
system.
