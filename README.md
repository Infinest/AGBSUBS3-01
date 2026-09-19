# AGBSUBS3-01

This PCB project aims to create a custom add-on board for the original AGB 64M (E201843), 128M (E201850) and 256M (E201868) development cartridges by Nintendo.

The board provides:

* 1Mbit Flash save memory
* Real-time clock with battery backup
* MachXO2 FPGA glue logic implementing the GBA cartridge GPIO registers, allowing the GBA to communicate with the RTC chip. Additionally on the board revision using modern chips the FPGA is also used as additional compatibility layer
* JTAG programming pads for the FPGA

## 

## Ordering PCBs

The gerber zip files can be found within the folder "gerber".

Please choose the gerber zip file according to the PCB version you need:

* AGBSUBS3-01.zip - 2 layer PCB using old RTC and flash chips - You will need to source these from a donor game
* AGSUBS3-01-M.zip - 4 layer PCB using modern alternative chips (compatibility layer via FPGA)



### Important:

Make sure to order your PCBs with a thickness of 0.6mm or they may not fit into the cartridge. For ease of soldering any fine-pitched components (like J1) ENIG or OSP as surface finish is recommended.



## BOM (Version with original chips)

|Reference|Quantity|Part Number|DigiKey|Description|
|-|-:|-|-|-|
|R1|1|ERJ-1GNF1001C|[P122413CT-ND](https://www.digikey.com/en/products/detail/panasonic-industry/ERJ-1GNF1001C/2036112)|1k ohm, 1%, 0201 (0603 metric) resistor|
|R2, R3, R5|3|ERJ-1GNF1002C|[P122414CT-ND](https://www.digikey.com/en/products/detail/panasonic-electronic-components/ERJ-1GNF1002C/2036226)|10k ohm, 1%, 0201 (0603 metric) resistor|
|R4|1|ERJ-1GNF1003C|[P122655CT-ND](https://www.digikey.com/en/products/detail/panasonic-industry/ERJ-1GNF1003C/2036340)|100k ohm, 1%, 0201 (0603 metric) resistor|
|C1, C3-C9|8|GRM033R60J104KE19D|[490-3167-1-ND](https://www.digikey.com/en/products/detail/murata-electronics/GRM033R60J104KE19D/702433)|100nF, 6.3V, X5R, 0201 (0603 metric) ceramic capacitor|
|C2|1|GRM0335C1E100JA01D|[490-8607-1-ND](https://www.digikey.com/en/products/detail/murata-electronics/GRM0335C1E100JA01D/4358173)|10pF, 25V, C0G/NP0, 0201 (0603 metric) ceramic capacitor|
|C10|1|GRM0335C1H200JA01D|[490-11315-1-ND](https://www.digikey.com/en/products/detail/murata-electronics/GRM0335C1H200JA01D/4358393)|20pF, 50V, C0G/NP0, 0201 (0603 metric) ceramic capacitor|
|U1|1|LCMXO2-256HC-4SG48I|[220-2176-ND](https://www.digikey.com/en/products/detail/lattice-semiconductor-corporation/LCMXO2-256HC-4SG48I/6595724)|Lattice MachXO2 FPGA, 48-pin QFN|
|U2|1|MX29L010TC-15A1 or LE26FV10N1TS|-|1Mbit Flash save memory, TSOP-I-32|
|U3|1|S-3516AE or<br />S-3511A|-|Real-time clock, SOP-8|
|Y1|1|ECS-.327-12.5-13X-C|[50-ECS-.327-12.5-13X-C-ND](https://www.digikey.com/en/products/detail/ecs-inc/ECS-327-12-5-13X-C/13532117)|32.768kHz, 12.5pF through-hole RTC crystal|
|BT1|1|CR-1616/F2N|[11-CR-1616/F2N-ND](https://www.digikey.com/en/products/detail/panasonic-energy/CR-1616-F2N/301860)|Panasonic 3V, 55mAh lithium coin cell with SMD solder tabs|
|J1|1|AXK640347YG|[255-2555-1-ND](https://www.digikey.com/en/products/detail/panasonic-industry/AXK640347YG/1986649)|Panasonic 40-position, 0.5mm-pitch mezzanine connector|



(U2 and U3 must be sourced from a compatible original cartridge.)





## BOM (version with modern alternative chips)

|Reference|Quantity|Part Number|DigiKey|Description|
|-|-:|-|-|-|
|R1|1|ERJ-1GNF1001C|[P122413CT-ND](https://www.digikey.com/en/products/detail/panasonic-industry/ERJ-1GNF1001C/2036112)|1k ohm, 1%, 0201 (0603 metric) resistor|
|R2, R3, R5|3|ERJ-1GNF1002C|[P122414CT-ND](https://www.digikey.com/en/products/detail/panasonic-electronic-components/ERJ-1GNF1002C/2036226)|10k ohm, 1%, 0201 (0603 metric) resistor|
|R4|1|ERJ-1GNF1003C|[P122655CT-ND](https://www.digikey.com/en/products/detail/panasonic-industry/ERJ-1GNF1003C/2036340)|100k ohm, 1%, 0201 (0603 metric) resistor|
|C1, C3-C9|8|GRM033R60J104KE19D|[490-3167-1-ND](https://www.digikey.com/en/products/detail/murata-electronics/GRM033R60J104KE19D/702433)|100nF, 6.3V, X5R, 0201 (0603 metric) ceramic capacitor|
|C2|1|GRM0335C1E9R1BA01D|[490-GRM0335C1E9R1BA01DTR-ND](https://www.digikey.com/en/products/detail/murata-electronics/GRM0335C1E9R1BA01D/11618841)|9.1 pF, 25V, C0G/NP0, 0201 (0603 metric) ceramic capacitor|
|C10|1|GRM0335C1H200JA01D|[490-11315-1-ND](https://www.digikey.com/en/products/detail/murata-electronics/GRM0335C1H200JA01D/4358393)|20pF, 50V, C0G/NP0, 0201 (0603 metric) ceramic capacitor|
|U1|1|LCMXO2-256HC-4SG48I|[220-2176-ND](https://www.digikey.com/en/products/detail/lattice-semiconductor-corporation/LCMXO2-256HC-4SG48I/6595724)|Lattice MachXO2 FPGA, 48-pin QFN|
|U2|1|SST39VF010-70-4C-TU or<br />SST39VF010-70-4I-TU|[150-SST39VF010-70-4C-TU-ND](https://www.digikey.com/en/products/detail/microchip-technology/SST39VF010-70-4C-TU/25904048) or<br />[150-SST39VF010-70-4I-TU-ND](https://www.digikey.com/en/products/detail/microchip-technology/SST39VF010-70-4I-TU/25903850)|1Mbit Flash save memory, TSOP-I-32|
|U3|1|S-35190A-J8T1U|[1662-3196-2-ND](https://www.digikey.com/en/products/detail/ablic-inc/S-35190A-J8T1U/6118944)|Real-time clock, SOP-8|
|Y1|1|VT200F-6PF20PPM|[728-1000-ND](https://www.digikey.com/en/products/detail/seiko-instruments/VT200F-6PF20PPM/1626715)|32.768kHz, 6pF through-hole RTC crystal|
|BT1|1|CR-1616/F2N|[11-CR-1616/F2N-ND](https://www.digikey.com/en/products/detail/panasonic-energy/CR-1616-F2N/301860)|Panasonic 3V, 55mAh lithium coin cell with SMD solder tabs|
|J1|1|AXK640347YG|[255-2555-1-ND](https://www.digikey.com/en/products/detail/panasonic-industry/AXK640347YG/1986649)|Panasonic 40-position, 0.5mm-pitch mezzanine connector|



## Programming

The FPGA will need to be programmed via the JTAG pads on the back of the PCB.

The JED files used for programming can be found in the folder "FPGA".

For this use the JED file that corresponds to your PCB version:

* AGBSUBS3-01.jed => 2 layer PCB version using old donor chips
* AGBSUBS3-01-M.jed => 4 layer PCB version using modern alternative chips

Use the official Lattice Diamond Programmer software and a compatible programmer to flash the jed onto the FPGA.



## Schematics



PDF files containing the schematics for both PCB versions can be found in the folder "schematics".

