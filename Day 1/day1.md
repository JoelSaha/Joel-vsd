# Day 1 - Introduction to Verilog RTL Design and Synthesis

## Introduction to open-source simulator iverilog
- Introduction to iverilog design test bench  
This is the basic workflow of a simulation
<img width="726" height="340" alt="image" src="https://github.com/user-attachments/assets/e4914467-736d-44ff-bdbb-e371277862ba" />

## Labs using iverilog and gtkwave
An example of 2:1 mux was taken as example.
Sample code of the module:
<img width="841" height="348" alt="image" src="https://github.com/user-attachments/assets/d76e93f0-32de-4889-afad-acf0773c394b" />
Testbench for the same:
<img width="531" height="518" alt="image" src="https://github.com/user-attachments/assets/4be2540c-954a-4a3d-aa8b-c6ae5f9b55cf" />
Command to run the design and testbench:
<img width="940" height="52" alt="image" src="https://github.com/user-attachments/assets/ed633044-339f-46a5-9797-1961b163b8ca" />
A .vcd file is created along with a.out file that is used for execution
- Output waveforms are observed using the following gtk commands:
<img width="940" height="138" alt="image" src="https://github.com/user-attachments/assets/3afa1f3f-a711-426d-b722-325314f8a3c5" />
<img width="915" height="587" alt="image" src="https://github.com/user-attachments/assets/529afac3-9086-4fee-a9a9-ad7e561cf4b2" />

## Introduction to Yosys and Logic Synthesis
Yosys is an synthesizer used to convert RTL to netlist
RTL is the behavioural representation in HDL, whereas netlist is the representation of the design in the form of standard cells present in the .lib
Testbench for netlist is same as that for RTL

.lib is a collection of all modules, standard cells of different flavours, etc
This process is also carried out using certain constraints that help in the selection of modules, involving trade-offs between speed and area and power.
<img width="940" height="493" alt="image" src="https://github.com/user-attachments/assets/49db670f-f9c4-47f5-a49a-409a90df1dde" />
<img width="940" height="670" alt="image" src="https://github.com/user-attachments/assets/51250c51-a29a-4d26-b6f1-9b05fc962c6f" />

## Labs using Yosys and Sky130 PDKs
Reading verilog files and creating synthesis:
<img width="940" height="665" alt="image" src="https://github.com/user-attachments/assets/1a784d08-6949-4d63-84da-37b804771cbf" />
<img width="940" height="653" alt="image" src="https://github.com/user-attachments/assets/f702c460-5415-4f83-a755-76bd5453d61c" />
A visual representation of the netlist:
<img width="940" height="597" alt="image" src="https://github.com/user-attachments/assets/4a7d2fc9-d6a9-4bd8-a4b0-4ce00b4c8a39" />
Writing into the netlist verilog file:
<img width="940" height="544" alt="image" src="https://github.com/user-attachments/assets/381e18de-8159-42d6-994a-237f3afe4136" />




