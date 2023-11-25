# *Kernel SU for Xiaomi Mi 10 Ultra*

## *[点我获取每周自动在线构建的最新ksu内核 / Click to get CI version!](https://github.com/CoolestEnoch/kernelsu-xiaomi-cas-online)*
[![Kernel Builder Xiaomi Mi 10 Ultra (cas) (legacy)](https://github.com/CoolestEnoch/kernelsu-xiaomi-cas-online/actions/workflows/legacy.yml/badge.svg)](https://github.com/CoolestEnoch/kernelsu-xiaomi-cas-online/actions/workflows/legacy.yml)
[![Kernel Builder Xiaomi Mi 10 Ultra (cas) (cloud)](https://github.com/CoolestEnoch/kernelsu-xiaomi-cas-online/actions/workflows/cloud.yml/badge.svg)](https://github.com/CoolestEnoch/kernelsu-xiaomi-cas-online/actions/workflows/cloud.yml)

[![ksuManagerScreenshot](/res/ksuManagerScreenShot.jpg)](https://github.com/CoolestEnoch/kernel-su-xiaomi-cas)

## 编译过程视频（算得上教程吧...?） / Video Tutorial
> [[ZH/CN] Bilibili](https://www.bilibili.com/video/BV1u24y167KE)

## 咋编译？ / How to compile?
[在Ubuntu上编译 / Compile on Ubuntu](https://github.com/CoolestEnoch/kernel-su-xiaomi-cas/issues/1)<br/>
**(我只在Arch Linux上测试过，Debian自己试 / I only did this on my Arch Linux, for Debian you should test it yourself.)**
*~第一步：在这个文件夹开个命令行窗口 / STEP ZERO: OPEN A TERMINAL WINDOW HERE~*
> 装依赖 / Install dependences first:


*Debian*
```shell
sudo apt install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev libgl1-mesa-dev libxml2-utils xsltproc unzip bc
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

[Kernel for Xiaomi sm 8250](https://github.com/Laulan56/kernel_xiaomi_sm8250)
