# Limitless Kernel
*A modification of jzinferno's OSS kernel for the Lenovo Z5s (jd2019).*

## Compiling

### Requirements
- **clang** *(arm64)*

### Pre-compilation
```
export ARCH=arm64
export CROSS_COMPILE=aarch64-linux-android-
export CLANG_TRIPLE=aarch64-linux-gnu-
```

### Procedure
```
git clone https://github.com/glblduh/limitless.git
cd limitless
mkdir out
make O=out jd2019_defconfig LLVM=1 LLVM_IAS=1
make O=out -j$(nproc --all) LLVM=1 LLVM_IAS=1
```
