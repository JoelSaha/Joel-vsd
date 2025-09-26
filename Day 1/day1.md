# Day 1 - Introduction to Verilog RTL Design and Synthesis

---

## Introduction to open-source simulator iverilog
- Introduction to iverilog design test bench  
- This is the basic workflow of a simulation  

<p align="center">
  <img src="https://github.com/user-attachments/assets/e4914467-736d-44ff-bdbb-e371277862ba" alt="iverilog workflow" style="width:70%; max-width:700px;">
</p>

---

## Labs using iverilog and gtkwave
- An example of **2:1 MUX** was taken.  

**Sample module code:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/d76e93f0-32de-4889-afad-acf0773c394b" alt="2:1 mux module" style="width:70%; max-width:700px;">
</p>

**Testbench:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/4be2540c-954a-4a3d-aa8b-c6ae5f9b55cf" alt="2:1 mux testbench" style="width:55%; max-width:500px;">
</p>

**Command to run design & testbench:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/ed633044-339f-46a5-9797-1961b163b8ca" alt="iverilog command" style="width:60%; max-width:600px;">
</p>

- A `.vcd` file is created along with `a.out` file that is used for execution.  
- Output waveforms are observed using **gtkwave** commands:  

<p align="center">
  <img src="https://github.com/user-attachments/assets/3afa1f3f-a711-426d-b722-325314f8a3c5" alt="gtkwave commands" style="width:65%; max-width:650px;">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/529afac3-9086-4fee-a9a9-ad7e561cf4b2" alt="mux output waveform" style="width:70%; max-width:700px;">
</p>

---

## Introduction to Yosys and Logic Synthesis
- **Yosys** is a synthesizer used to convert **RTL → netlist**.  
- RTL is the behavioral representation in HDL.  
- Netlist is representation of the design using **standard cells** from `.lib`.  
- Testbench for netlist is same as RTL.  
- `.lib` contains all modules, standard cells of different flavors.  
- Constraints help in selecting modules (trade-offs: speed, area, power).  

<p align="center">
  <img src="https://github.com/user-attachments/assets/49db670f-f9c4-47f5-a49a-409a90df1dde" alt="yosys flow" style="width:70%; max-width:700px;">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/51250c51-a29a-4d26-b6f1-9b05fc962c6f" alt="yosys constraints" style="width:70%; max-width:700px;">
</p>

---

## Labs using Yosys and Sky130 PDKs
**Reading Verilog files and creating synthesis:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/1a784d08-6949-4d63-84da-37b804771cbf" alt="yosys read verilog" style="width:70%; max-width:700px;">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f702c460-5415-4f83-a755-76bd5453d61c" alt="yosys synthesis" style="width:70%; max-width:700px;">
</p>

**Visual representation of netlist:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/4a7d2fc9-d6a9-4bd8-a4b0-4ce00b4c8a39" alt="yosys netlist view" style="width:70%; max-width:700px;">
</p>

**Writing into netlist Verilog file:**

<p align="center">
  <img src="https://github.com/user-attachments/assets/381e18de-8159-42d6-994a-237f3afe4136" alt="yosys write netlist" style="width:70%; max-width:700px;">
</p>
