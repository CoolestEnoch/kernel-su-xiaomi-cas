# *Kernel SU for Xiaomi Mi 10 Ultra*

[![ksuManagerScreenshot](/res/ksuManagerScreenShot.jpg)](https://github.com/CoolestEnoch/kernel-su-xiaomi-cas)

## 编译过程视频（算得上教程吧...?） / Video Tutorial
> [[ZH/CN] Bilibili](https://www.bilibili.com/video/BV1u24y167KE)

## 咋编译？ / How to compile?
**(我只在Arch Linux上测试过，Debian自己试 / I only did this on my Arch Linux, for Debian you should test it yourself.)**
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

> 编好的内核在哪？ / Where is the kernel image file?
```
./kernel/arch/arm64/boot/
```

## 鸣谢 / Thanks 
[KernelSU Project](https://github.com/tiann/KernelSU)
