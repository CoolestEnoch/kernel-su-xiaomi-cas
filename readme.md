## How to compile?
~STEP ZERO~
~OPEN A TERMINAL WINDOW HERE~
> Install dependences first:
</br>*Debian*
```shell
sudo apt install git-core gnupg flex bison gpres build-essential zip curl zlibig-dev
```
*Arch Linux*
```shell
sudo pacman -S base-devel
```
> Then set environment vars:
```shell
export ARCH=arm64
export CROSS_COMPILE=./gcc/gcc-arm64-gcc-master/bin/aarch64-elf-
export CROSS_COMPILE_ARM32=./gcc/gcc-arm-gcc-master/bin/arm-eabi-
```
***GO!!!***
```shell
cd kernel && make
```
