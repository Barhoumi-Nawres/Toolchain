# Toolchain

This reposotory explain :
## Compilation process 
## Shared library 
## Makefile 

## Compilation types :

B=H=T -->Native compilation 

B=H#T -->Cross compilation 

B#H=T -->Cross-Native 

B#H#T -->Canadian Compilation or Cross-canadian 


## install toolchain :
Prefix of toolchain


```bash
<arch>-<os>-<clib><abi><hf>

```
 
example :

```bash
sudo apt install gcc-arm-linux-gnueabihf binutils-arm-linux-gnueabihf

```

We will find them under /usr/arm-linux-gnueabihf/

This directory contains :
bin ,include ,lib 

bin: contains binutils (linker ...) 

lib: libc.so ,libc.a,loader .....etc 

we need to set the environment variable :

```bash
export CROSS_COMPILE=arm-linux-gnueabihf-

```

#### Simulation 

install :

```bash
sudo apt install qemu-user qemu-user-static

```


to test the output main :

```bash
qemu-arm -L /usr/arm-linux-gnueabihf/ ./main

```


