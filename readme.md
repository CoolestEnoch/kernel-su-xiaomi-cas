## 咋编译？ / How to compile?
*~第一步：在这个文件夹开个命令行窗口 / STEP ZERO: OPEN A TERMINAL WINDOW HERE~*
> 装依赖 / Install dependences first:


*Debian*
```shell
sudo apt install git-core gnupg flex bison gpres build-essential zip curl zlibig-dev
```
*Arch Linux*
```shell
sudo pacman -S base-devel
```
> 设置环境变量 / Then set environment vars:
```shell
export ARCH=arm64
export CROSS_COMPILE=./gcc/gcc-arm64-gcc-master/bin/aarch64-elf-
export CROSS_COMPILE_ARM32=./gcc/gcc-arm-gcc-master/bin/arm-eabi-
```
***开整 / GO!!!***
```shell
cd kernel && make
```
