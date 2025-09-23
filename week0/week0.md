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
```
<img width="940" height="685" alt="image" src="https://github.com/user-attachments/assets/f65dea7f-a4d5-46d7-ba40-889b28536187" />

### Iverilog
Steps to install iverilog:
```bash
sudo apt-get update
sudo apt-get install iverilog
```

<img width="940" height="242" alt="image" src="https://github.com/user-attachments/assets/74b84ddc-2683-4af8-9964-53f17577ba19" />

### gtkwave
Steps to install gtkwave
```bash
sudo apt-get update
sudo apt install gtkwave 
```
<img width="940" height="171" alt="image" src="https://github.com/user-attachments/assets/df2a4ecb-2981-472b-bc1c-fd5870f338bc" />
<img width="940" height="602" alt="image" src="https://github.com/user-attachments/assets/966b570d-2529-4259-90d2-d6a7710cead5" />


