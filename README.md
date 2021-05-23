# Huawei MediaPad M5 Android 9 PIE CMR EMUI 9.1.0 Kernel 4.9.148 Opensource from Huawei
### [newbit @ xda-developers](https://forum.xda-developers.com/m/newbit.1350876/)
Opensource Code for the Huawei MediaPad M5 AL09A Kernel

### Get some packages
`sudo apt-get install build-essential libssl-dev libncurses5-dev bison flex libqt4-dev pkg-config android-tools-fastboot android-tools-adb`

### Change to Kernel Dir
`cd kernel`

### Get the Toolchain
`./configure_gcc_toolchain`

### Exports
`source .exports`

### Compile it
`make ARCH=arm64 distclean`\
`rm ../out -Rf && make clean && make mrproper && mkdir ../out`\
`make ARCH=arm64 O=../out merge_hi3660_defconfig`\
`make ARCH=arm64 O=../out xconfig`\
`time make ARCH=arm64 O=../out -j$(nproc)`

### Repack Kernel and Flash it
`./repack_and_flash_kernel`

### Links
* [consumer huawei opensource CMR_EMUI9.1.0 MediaPad M5,CMR,EMUI9.1.0,Android 9](https://consumer.huawei.com/en/opensource/detail/?siteCode=worldwide&keywords=CMR-AL19&fileType=openSourceSoftware&pageSize=10&curPage=1)
* [Cameron-AL09A_PIE_EMUI9.1.0_opensource.tar.gz](http://download-c1.huawei.com/download/downloadCenter?downloadId=99968&version=425783&siteCode=worldwide)
* [Prebuild GCC Toolchain Android NDK 17c](https://dl.google.com/android/repository/android-ndk-r17c-linux-x86_64.zip)
* [osm0sis AIK-Linux v3.8](https://forum.xda-developers.com/t/tool-android-image-kitchen-unpack-repack-kernel-ramdisk-win-android-linux-mac.2073775)
