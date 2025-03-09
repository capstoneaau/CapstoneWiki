### Abbreviations
- CLIF - ContactLess InterFace
- LPCD - Low Power Card Detection
- RATS and ATS - (Request) Answer To Select. Used for negotiation of data rates and supported protocols during initialization.
- CC File - Capability Container File. A descriptor of the card's features and contents. Mandatory to be present.
- phOsal -> Operating system abstraction layer
- HAL -> Hardware Abstraction Layer

### Structure
- NxpNfcRdLib/
	- intfs/phhalHw_Pn5180_Reg.h -> Register map and definitions for PN5180
	- intfs/phhalHw_Pn5180_Instr.h -> Instruction (op-codes) definitions for PN5180
	- comps/phhalHw/src/Pn5180/phhalHw_Pn5180.c -> PN5180-related methods (Init, DeInit, AntiCollision, Transmit, ...)