## Overview

| NFC Tag Type | Standard                 | Examples                  |
| ------------ | ------------------------ | ------------------------- |
| Type 1       | ISO 14443A               | Topaz                     |
| Type 2       | ISO 14443A               | Ultralight, NTAGX, ST25TN |
| Type 3       | ISO 14443A, JIS X 6319-4 | Sony FeliCa               |
| Type 4       | ISO 14443A, ISO 14443B   | DESFire                   |
| Type 5       | ISO 15693                | SLI, SLIX, ST25TV         |

## ISO / Non-ISO Standards
#### ISO 14443
The most popular type of card, mainly due to its use in NXP Mifare Classic cards.
##### Levels / Parts
   - ISO/IEC 14443-1:2018 Part 1: Physical characteristic
   - ISO/IEC 14443-2:2020 Part 2: Radio frequency power and signal interface
   - ISO/IEC 14443-3:2018 Part 3: Initialization and anticollision
   - ISO/IEC 14443-4:2018 Part 4: Transmission protocol
##### The difference between type A and B cards

The first interface was type A, supported by Mikron and their Mifare technology, later bought by Philips (NXP). Some limitations quickly occurred: the initial implementation was a memory card, and not a microprocessor card. At the time, type A couldn't power up a microprocessor continuously. The Innovatron company had working microprocessor cards, so their technology was integrated as type B in the standard. This separation is not relevant anymore since you can have type A or type B memory or microprocessor cards, and we ended up with two competing technologies in the same standard.

*(source: https://electronics.stackexchange.com/questions/222055/why-are-there-types-a-and-b-in-iso-14443)*

#### ISO 15693
Mainly used for inventory management and industrial applications, however, as we find in the card scanning excel sheet, that's not always necessarily the case.
#### ISO/IEC 18092 / JIS X 6319-4
This standard refers to Sony FeliCa type cards.
#### ISO 18000-3
## NFC Forum Standards
#### Type 1
Not commonly used. Refers to legacy parts. Now no longer needed for backwards compatibility even; NFC Type 5 v1.2 cards need to support all the way back to Type 2 at least, [but can ignore Type 1 if they choose. ](https://nfc-forum.org/build/specifications)
#### Type 2
The most popular kind. 

#### Type 3
Sony FeliCa. See [[#ISO/IEC 18092 / JIS X 6319-4]].
#### Type 4
Supports more security standards, and supports ISO-DEP communication, which is just a fancy name for ISO 14443.
#### Type 5
NfcV. See [[#ISO 15693]].