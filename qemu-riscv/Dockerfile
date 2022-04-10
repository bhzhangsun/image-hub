FROM ubuntu-base

## 考虑手动构建qemu
RUN apt install qemu-system-riscv -y && \
    apt install build-essential device-tree-compiler -y && \
    cd /tmp && \
    git clone https://github.com/riscv-software-src/riscv-isa-sim.git && \
    cd riscv-isa-sim/ && \
    mkdir build && \
    cd build && \
    ../configure --prefix=/usr/local && \
    make && \
    make install && \
    cd /tmp && \
    rm -rf ./riscv-isa-sim