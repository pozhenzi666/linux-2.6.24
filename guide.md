# 运行指导
## 编译（基于ubuntu 22.04）
```shell
# 64位编译
apt install -y gcc-9 g++-9
make defconfig
make menuconfig
//启动gdb调试的选项
    - Kernel hacking  --->
        -  [*] Compile the kernel with debug info
make CC=gcc-9 -j$(nproc)
# 32位编译
apt install gcc-9-multilib g++-9-multilib
make ARCH=i386 defconfig
make ARCH=i386 menuconfig
//启动gdb调试的选项
    - Kernel hacking  --->
        -  [*] Compile the kernel with debug info
make ARCH=i386 CC='gcc-9 -m32' -j$(nproc)
```
## 巨人的肩膀
https://gitee.com/hgc21/linux-2.6.24/blob/master/%E7%BC%96%E8%AF%91%E9%97%AE%E9%A2%98.md
https://juejin.cn/post/7160349299401277476