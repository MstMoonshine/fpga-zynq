# Zedboard Workflow

### Compile RISC-V Linux kernel

``` bash
1. (only once) make ARCH=riscv defconfig
2. make ARCH=riscv menuconfig
3. make ARCH=riscv CROSS_COMPILE=riscv64-unknown-linux-gnu- vmlinux
```

### Build BBL

``` bash
1. (only once) mkdir -p build
2. cd build
3. ../configure --prefix=$RISCV --host=riscv64-unknown-elf --with-payload=~/src/linux/vmlinux --enable-logo
4. make
```

### 
