## Terminology
**Tear-off:** Sometimes considered an attack, but it's just simply removing the card from the reader mid-transmission.
## File Structure
![[Pasted image 20250421100533.png|500]]
[10.13140/RG.2.2.19591.42401](http://dx.doi.org/10.13140/RG.2.2.19591.42401)

A card holds multiple "application"s. Each applications holds different files of these types:
- Normal files
- Value files
- Cyclic record files
- Backup files
Normal files are just binaries, they're the only file type to have no tear-off protection. Value files are a numerical value (or variable), they store just a number, and they have debit/credit methods for use in top-up systems. Cyclic records are used to store transaction history, when full, it returns to the first record (hence, cyclic). Backup files are binaries (like normal files) but with tear-off protection.

Each file can use one of three keys, and each file has the standard permissions of R/W but with the addition of another permission "can modify". If not present, then the permissions are set forever and cannot be modified.