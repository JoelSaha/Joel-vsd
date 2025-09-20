# Week 0 - Digital VLSI SoC Design and Planning

This file contains my submissions for **Week 0**.

---

## Task 1: Video Summary  

**Video Title:** Getting started with Digital VLSI SoC Design and Planning  

### Key Learnings:
- **Chip Modeling (O1):**
  Specifications captured in **C model**. Testbench is also in C language.  

- **RTL Architecture (O2):**
  RTL description (**Verilog**) provides a *soft copy of hardware*. Processor, peripherals, macros, and analog IPs are defined here.  

- **SoC Integration (O3):**
  Integration of processor, macros, peripherals, and analog IPs into a single SoC. GPIOs and other modules tied together.  

- **ASIC Flow Overview:**
  Specs → RTL → Synthesis → SoC Integration → RTL2GDS → DRC/LVS checks before fabrication.  

---

## Task 2: Tool Installation  

### System Requirements
- 6 GB RAM  
- 50 GB HDD  
- Ubuntu 20.04+  
- 4 vCPU  

### Virtual Machine
[Oracle VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)

---

### Yosys
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make build-essential clang bison flex \
 libreadline-dev gawk tcl-dev libffi-dev git \
 graphviz xdot pkg-config python3 libboost-system-dev \
 libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install
