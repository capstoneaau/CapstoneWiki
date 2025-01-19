### Security Measures 
##### Encryption
(Explain how encryption is used in the DESFire Object portion of NXP cards)

##### UID
Explain how UIDs work for cards

##### Rolling codes
Explain them

### Technologies
#### ISO
- ISO 14443-4 (Used by #BankCard #EmiratesID #PublicBusCard)
- ISO 14443-3A (Used by #UniversityCard)
### Implementations & Companies
#### Cards
##### NXP
###### DESFire
https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-desfire:MC_53450

| Products                                                                                                                                                             | Description                                              | ISO/IEC Support                      | Security                                                | Certifications | Datasheet                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- | ------------------------------------ | ------------------------------------------------------- | -------------- | ------------------------------------------------------------------------ |
| [MIFARE DESFire EV3](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-desfire/mifare-desfire-ev3-high-security-ic-for-contactless-smart-city-services:MF3DHx3) | High-security IC for contactless smart city services     | ISO/IEC 14443 A 1-4 and ISO/IEC 7816 | DES/2K3DES/3K2DES/AES crypto algorithms                 | CC EAL5+       | (408 kB)                                                                 |
| [MIFARE DESFire Light](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-desfire/mifare-desfire-light:MIFARE_DESFIRE_LIGHT)                                     | Secure, easy-to-integrate, cost-effective contactless IC | ISO/IEC 14443 A 1-4 and ISO/IEC 7816 | AES 128-bit and LRP authentication and secure messaging | CC EAL4        | [PDF](https://www.nxp.com/docs/en/data-sheet/MF2DLHX0.pdf)  <br>(1.2 MB) |
**Used by:** 
- #PublicBusCard (NXP - Mifare DESFire EV1 4K)

###### Mifare Plus
https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-plus:MC_57609

| Products                                                                                                                                            | Description                                                                                                                                                                                                                                    | ISO/IEC support                    | Security                     | Certifications | Datasheet                                                                 |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------- | ---------------------------- | -------------- | ------------------------------------------------------------------------- |
| [MIFARE Plus EV2](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-plus/mifare-plus-ev2-secure-ic-for-contactless-smart-city-services:MFPEV2) | As the next generation of NXP’s MIFARE Plus product family, the MIFARE Plus EV2 IC is designed to be both a gateway for new Smart City applications and a compelling upgrade, in terms of security and connectivity, for existing deployments. | ISO/IEC 14443 A 1-4 and ISO 7816-4 | 48-bit Crypto-1, 128-bit AES | CC EAL5+       | [PDF](https://www.nxp.com/docs/en/data-sheet/MF1P(H)x2.pdf)  <br>(298 kB) |

**Used by:**
- #EmiratesID (NXP - Mifare Plus)
- #BankCard (NXP - Mifare Plus)

###### Mifare Classic
https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic:MC_41863

| Products                                                                                                                | ISO/IEC Support | Bit Rate | Security       | UID Type        | Write Endurance | EEPROM      | Datasheet                                                                    |
| ----------------------------------------------------------------------------------------------------------------------- | --------------- | -------- | -------------- | --------------- | --------------- | ----------- | ---------------------------------------------------------------------------- |
| [MIFARE Classic EV1](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic/mifare-classic-ev1-4k:MF1S70YYX_V1) | 14443-3 Type A  | 106      | MIFARE CRYPTO1 | 4NUID and 7 UID | 100000          | 1 kB - 4 kB | [PDF](https://www.nxp.com/docs/en/data-sheet/MF1S70YYX_V1.pdf)  <br>(452 KB) |
**Used by:**
- #UniversityCard (NXP - Mifare Classic 1k)