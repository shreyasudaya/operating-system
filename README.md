A basic operating system build in C and Assembly. Simulated using docker and qemu. Steps for deploying on virtual machine.
# Prerequisites
Docker for build environment and Qemu for emulating os.
# Directions
1. Clone repository and navigate to it.
2. Build image using following command: 
    ```dockerfile docker build buildenv -t myos-buildenv```
3. Enter environment:
    ```dockerfile docker run --rm -it -v "%cd%":/root/env myos-buildenv```
    
    If Linux, replace ```"%cd%"``` with "$(pwd)"
