Tools Installation Guide
System Requirements
6 GB RAM

50 GB HDD

Ubuntu 20.04 or higher

4 vCPU

Resizing Ubuntu Virtual Machine Window
bash
$ sudo apt update
$ sudo apt install build-essential dkms linux-headers-$(uname -r)
$ cd /media/spatha/VBox_GAs_7.1.8/
$ ./autorun.sh
Tool Installation
Yosys (Verilog Synthesis Tool)
bash
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ git submodule update --init --recursive
$ make 
$ sudo make install
Iverilog (Verilog Simulation Tool)
bash
$ sudo apt-get update
$ sudo apt-get install iverilog
GTKWave (Waveform Viewer)
bash
$ sudo apt-get update
$ sudo apt install gtkwave
Verification
After installation, verify each tool is working correctly by checking their versions:

bash
$ yosys -V
$ iverilog -v
$ gtkwave --version
