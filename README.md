This toolchain is for GD32 RISC-V Nano/Pico development board.

The origin repositry is at: https://github.com/riscv-mcu/riscv-gnu-toolchain provided by nuclei.  

The RISC-V original toolchain source is at : https://github.com/riscv/riscv-gnu-toolchain provided by RISC-V foundation.  

This toolchain is for MapleBoard GD32 RISC-V Nano/Pico users, please visit https://github.com/MapleBoard/Mpb-toolchain-Example
to get the example of this toolchain.  

Installition guide:
Install this repo first, and go into toolchain folder
<pre>
git clone https://github.com/MapleBoard/mpb-toolchain
cd mpb-toolchain
</pre>

Build dependent packages:  
<pre>
sudo apt install autoconf automake autotools-dev curl libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev
</pre>

Build for GD32VF103:  

<pre>
mkdir build
./configure --prefix=opt/mpb-toolchain/build --with-arch=rv32imac --with-abi=ilp32
make -j8
</pre>

* The -j8 means 8 threads, you can type more threads if your PC has more powerful CPU

RISC-V ISA Base and Extension: rv32imac  

* rv32i – Base Integer Instruction Set, 32-bit.  

* m – Standard Extension for Integer Multiplication and Division.  

* a – Standard Extension for Atomic Instructions.  

* c – Standard Extension for Compressed Instructions.  

Git Clone from MapleBoard repository:  

<pre>
$ git clone -o ces -b mapleboard --recursive git3@git.ces.com.tw:/git/riscv-gnu-toolchain.git
</pre>

Update from MapleBoard repository:  

<pre>
$ git pull ces mapleboard
</pre>

Update submodules:  

<pre>
$ git submodule foreach --recursive git pull  
</pre>

Push to MapleBoard repository (You need write privilege, please contact jb@ces.com.tw):  

<pre>
$ git push ces mapleboard 
</pre>

Origin GNU toolchain readme contant


