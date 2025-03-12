
![[Pasted image 20250311031524.png|16]] Bluefin, a dolphin-despising penetration testing tool and framework with a pointy fin sharply focused on access cards. It's designed to support multiple readers, with initial support for the PN5180 and the Proxmark later down the line. It provides a simple to use electron-powered touch interface designed to run on a Raspberry Pi.

### Architecture
![[Bluefin-Architecture-Diagram.drawio.svg|250]]

### Requirements
- The application shall provide a way to perform the tests mentioned in the Capstone 1 proposal which are feasible to implement with current hardware, which are: READ, MODIFY, CLONE, ~~SKIM~~, BRUTEFORCE, and EMULATE 
- It shall also be designed from the get-go to be modular enough to support multiple readers, as a transition from the PN5180 to the Proxmark is foreseen.
- The interface shall be tightly coupled with the framework. For example, the interface should warn the user or illustrate the fact that a security measure failed the test, whilst relating the reason of failure to the framework.
- The obvious: The application should be reliable, and should produce repeatable results. The application should be simple to use and abstract away the nitty gritty details of the readers, but should still provide a way to fine tune them if need be.