### ESP32 Pinout
![[esp32 pinout.avif|500]]
The BUSY, RST and NSS pins are configurable on top of the Arduino IDE project. Other pins are standard (SPI pins and power), with the exception of IRQ, which is not connected.

### Available libraries
##### ATrappmann's PN5180 Library
https://github.com/ATrappmann/PN5180-Library (Discontinued. Requires manual installation to Arduino IDE. Supports all types of cards, notably HID iClass cards as well. Does not support card emulation.)

##### Playfultechnology's PN5180 Library
https://github.com/playfultechnology/arduino-rfid-PN5180 Only supports ISO14443 and ISO15693, and only supports reading the UID. Nothing more, nothing less. Based on ATrappmann's code.