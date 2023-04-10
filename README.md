# curso-desenvolvimento-aplicacoes-linux-embarcado

# Desafio

- Configurar o VScode para compilação cruzada
Material de referencia:

VAR-SOM-MX6 - Yocto Programming with Visual Studio Code
https://variwiki.com/index.php?title=Yocto_Programming_with_VSCode&release=RELEASE_DUNFELL_V1.1_VAR-SOM-MX6

Yocto toolchain installation for out of Yocto builds
https://variwiki.com/index.php?title=Yocto_Toolchain_installation&release=RELEASE_DUNFELL_V1.1_VAR-SOM-MX6

$ source /opt/fslc-xwayland/3.1/environment-setup-cortexa9t2hf-neon-fslc-linux-gnueabi

$ make
arm-fslc-linux-gnueabi-g++  -mthumb -mfpu=neon -mfloat-abi=hard -mcpu=cortex-a9 -fstack-protector-strong  -D_FORTIFY_SOURCE=2 -Wformat -Wformat-security -Werror=format-security --sysroot=/opt/fslc-xwayland/3.1/sysroots/cortexa9t2hf-neon-fslc-linux-gnueabi  -O2 -pipe -g -feliminate-unused-debug-types  -Og main.cpp -g -o hello.bin -march=armv7-a -mthumb -mfpu=neon -mfloat-abi=hard
cc1plus: warning: switch ‘-mcpu=cortex-a9’ conflicts with ‘-march=armv7-a’ switch

$ file hello.bin 
hello.bin: ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux-armhf.so.3, BuildID[sha1]=b69e0c48a7b79ec5114210040ab6859c7207819c, for GNU/Linux 3.2.0, with debug_info, not stripped
