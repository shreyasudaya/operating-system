A basic operating system build in C and Assembly. Simulated using docker and qemu. Steps for deploying on virtual machine.
# Prerequisites
Docker for build environment and Qemu for emulating os.
# Directions
1. Clone repository and navigate to it.
2. Build image using following command: 

    ```docker build buildenv -t myos-buildenv```
3. Enter build environment:
    ```docker run --rm -it -v "%cd%":/root/env myos-buildenv```
    
    If Linux, replace ```"%cd%"``` with ```"$(pwd)"```
4. Type in command ```make build-x86_64``` . If successful, then exit the environment using exit.
5. Emulate using ```qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso```

# More tentative to add

- Keyboard and mouse interface
- GUI
- Physical Memory management
- read/write

  # Issues
- deadlock between keyboard and cpu
  
