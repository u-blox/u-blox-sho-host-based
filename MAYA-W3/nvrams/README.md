# MAYA-W3 NVRAM files

This directory contains NVRAM files for MAYA-W3 series modules, which
are needed in addition to the firmware by the driver.
Select the NVRAM file for your module and copy it as cyfmac55500-sdio.txt
into the /lib/firmware/cypress folder on the target system.

* maya-w381-00b.nvram: NVRAM file for MAYA-W3x1 and MAYA-W3x0
* maya-w386-00b.nvram: NVRAM file for MAYA-W3x6, MAYA-W3x2, and MAYA-W3x3

NVRAM files supporting antenna diversity using RF_CNTL4 (J5):
* maya-w381-00b-ant_div.nvram: NVRAM file for MAYA-W3x1 and MAYA-W3x0
* maya-w386-00b-ant_div.nvram: NVRAM file for MAYA-W3x6, MAYA-W3x2, and MAYA-W3x3
