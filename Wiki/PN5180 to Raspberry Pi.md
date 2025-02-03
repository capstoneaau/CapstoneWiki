### Pinout

| PN5180 | Pi                              |
| ------ | ------------------------------- |
| 5V     | 5V                              |
| 3.3V   | 3.3V                            |
| RST    | GPIO 7 (SPI Chip Select 1) (26) |
| NSS    | GPIO 8 (SPI Chip Select 0) (24) |
| MOSI   | GPIO 10 (SPI0 MOSI) (19)        |
| MISO   | GPIO 9 (SPI0 MISO) (21)         |
| SCK    | GPIO 11 (SPI0 SCLK) (23)        |
| BUSY   | GPIO 25 (22)                    |
| GND    | GND                             |
| GPIO   | Not Connected                   |
| IRQ    | GPIO 23 (16)                    |
| AUX    | Not Connected                   |
| REQ    | Not Connected<br>               |
**For reference:**
The number at the end of each RPi connection is the physical pin location (the small darker number beside each pin in the diagram below)
![[Pasted image 20250203212129.png|300]]
(courtesy of [pinout.xyz](https://pinout.xyz/))

### Available libraries
- pyPN5180 - https://github.com/fservida/pyPN5180 (uses different pinout)
- NXP's Library - https://www.nxp.com/applications/technologies/security/industrial-security/nfc-reader-library-software-support-for-nfc-frontend-solutions:NFC-READER-LIBRARY?tab=In-Depth_Tab (requires free NXP account)

### Usage of NXP Library
As of now, the only complete software implementation of the PN5180's feature-set is NXP's in-house library. It supports all cards (with the exception of iClass cards, which do work on the Arduino library, see [[PN5180 to Arduino and ESP32]]) and, more importantly, supports card emulation.

_⚠️ That said, their latest implementation uses the deprecated sysfs gpio interface, which is slated for removal some time in the near future._

##### Raspberry Pi configuration
Make sure that SPI is enabled. If it's not, enable it in the `raspi-config` utility under Interface Options.
##### Installation
1. Unzip `NxpNfcRdLib_PN5180_v07.10.00_Pub.zip`
2. Find out your Raspberry Pi's GPIO offset value if using a Raspberry Pi 2 or above. To do this, run `ls /sys/class/gpio`, one of the files/directories should be named gpiochipNUMBER. Said number if your offset value.
3. Patch `Platform/DAL/boards/Board_PiPn5180.h`. This file requires 2 patches.
	- First, unless you have a Raspberry Pi 1, we need to modify the pin definitions in that file to add the offset value we found out earlier. Simply add the offset values to the pin definitions, for example, for an offset value of 512, the line `#define PHDRIVER_PIN_RESET         16` becomes `#define PHDRIVER_PIN_RESET         512+16`, and so on for the rest of the pins in that definition block. (the code in red is what *should* be there.)
	-  ![[Pasted image 20250203214904.png]]
	-  Second, we need to prevent the library from using the obsoleted "bal" driver. To do that, simple uncomment `#define PHDRIVER_LINUX_USER_SPI` and comment out `#define PHDRIVER_LINUX_KERNEL_SPI`.
	- ![[Pasted image 20250203215158.png]]
4. After patching `Board_PiPn5180.h`, we can finally compile the demos. Make sure that gcc and cmake are installed (*sudo apt install* them if they aren't). Then in the root folder of the project (the `ComplianceApp`, `Examples`, `NxpNfcRdLib` and etc folders should be visible), run the following commands:
	- `mkdir _build`
	- `cd _build`
	- `cmake ..`
	- `make all`
5. After everything has (hopefully) compiled, you can run each example binary in `_build/Examples/`. A description of each example can be found in `AN11802.pdf`.