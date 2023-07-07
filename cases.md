# Raspberry Pi Cases

An (incomplete) list of Raspberry Pi Cases with use cases and setup instructions.

## Argon One M.2 

### Use
- Fits the Raspberry Pi 4 and 4b
- The primary use of this case is to attach a M.2 SATA SSD
  - The board accepts B Key and B+M Key
- Also offers a power button with some software defined functionality and an Infrared Reciever

### Setup 
- Once built and connected to the internet, install the Argon One Pi 4 script in order to use the power button, modify the fan speeds, and configure the Infrared Receiver
```
curl https://download.argon40.com/argon1.sh | bash
```
- To configure the fan:
```
argonone-config
```
- To uninstall:
```
argonone-uninstall
```

### Other Usage
- The built-in infrared receiver can be configured with:
```
argonone-ir
```
- The power button has extra functionality as well
  - When off, click the button to turn on
  - When on:
    - A double tap will reboot
    - A press of 3 or more seconds will soft shutdown (power cut)
    - A press of 5 or more seconds will force shutdown