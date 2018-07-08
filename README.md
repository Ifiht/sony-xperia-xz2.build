# sony-xperia-xz2.build
Custom resources for building AOSP 8.0.0 for the Xperia XZ2 Compact

References
----------
*. https://en.wikipedia.org/wiki/Sony_Xperia
*. https://developer.sony.com/develop/open-devices/guides/aosp-build-instructions/build-aosp-oreo-8-0-kernel-4-4/#tutorial-step-3

Procedure
---------
1. Follow Sony Dev Guide up to 4.3
2. cd ~/android/devices/sony
   1. git clone https://github.com/sonyxperiadev/device-sony-tama.git tama
   2. git clone https://github.com/sonyxperiadev/device-sony-apollo.git apollo
3. "ninja: error: 'kernel/sony/msm/arch/arm64/configs/aosp_tama_apollo_defconfig', needed by '/home/anna/android_8-0-0/out/target/product/apollo/obj/KERNEL_OBJ/.config', missing and no known rule to make it"
4. Pull config from current device:
   *. cat /boot/config-`uname -r`   OR
   *. adb pull /proc/config.gz  for current Kernel configuration options
