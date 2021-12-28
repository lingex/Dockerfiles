# gcc-arm-none-eabi 

chs: 基于 alpine 的轻量化 gcc-arm-none-abi docker 镜像, 大约 830M 大小(alpine 3.14.3 + arm-none-eabi 10.2.0).

en: minimal docker image for building arm-embedded projects, depends on alpine linux, about 830M (alpine 3.14.3 + arm-none-eabi 10.2.0).


# Usage

**1. Build an image using latest packages**: 
  
  a. docker build -t arm-none-eabi .
  
  b. docker run --rm -it -v $PWD:/work arm-none-eabi /bin/sh -c "cd /work; make clean; make -j"


**2. Compile directly using my image**:

  docker run --rm -it -v $PWD:/work lingex/arm-none-eabi /bin/sh -c "cd /work; make clean; make -j"
