# Day 2 - Timing libs, Hierarchical vs Flat Synthesis and Efficient Flop Coding Styles

## Introduction to Timing .libs
Standard cell libraries are characterized across different PVT corners to capture variations in circuit behavior.

- **Process (P):** Variations due to fabrication.  
  - `tt` → typical  
  - `ff` → fast-fast (stronger transistors, faster)  
  - `ss` → slow-slow (weaker transistors, slower)  
  - `fs / sf` → mixed cases  

- **Voltage (V):** Supply voltage variations.  
  - Example: `1v80` = 1.8 V  

- **Temperature (T):** Operating temperature variations.  
  - Example: `025C` = 25 °C
<img width="910" height="753" alt="image" src="https://github.com/user-attachments/assets/4e05901e-c66c-43a7-9280-8a9319e687b8" />

- **Additional information included in cell are:**
    - Leakage power based on the combination of inputs
    - Area
    - Power ports
    - Input capacitance
    - Power associated with the pin
    - Transition
    - Delay

      
# Synthesis Approaches

## Hierarchical vs Flat Synthesis

- **Hierarchical Synthesis**
  - Preserves the module hierarchy in the synthesized design.
  - Sub-modules are instantiated separately in the netlist (e.g., `sub_module1`, `sub_module2`).
  <img width="1197" height="750" alt="image" src="https://github.com/user-attachments/assets/58fa83c0-0187-40ed-abe4-f6b24fb67fb2" />

  - Example:
    - `sub_module1` → contains an **AND** gate.
    - `sub_module2` → contains an **OR** gate.
  - When running `show`, we see **sub-modules** instead of flattened gates.
  <img width="1289" height="800" alt="image" src="https://github.com/user-attachments/assets/4cd2dd18-b667-43fc-8c50-2ef3fd7b1f6a" />

  - Note: In CMOS, an `OR` gate is often implemented as **INV + NAND** (instead of directly stacking PMOS transistors, which is inefficient due to lower PMOS mobility).
  - The `.lib` file provides the characterization data (area, delay, leakage, etc.) used for such gate-level mapping.

- **Flat Synthesis**
  - The design hierarchy is removed using the `flatten` command.
  - The entire design is synthesized as one flat block.
  - Instead of seeing sub-modules in the netlist, we directly see logic gates (AND, OR, NAND, etc.).
  - Easier for tools to optimize across module boundaries, but less reusable.
<img width="1209" height="746" alt="image" src="https://github.com/user-attachments/assets/8c4ca9bb-b206-419e-8fb2-b36aeddb35e4" />

---

## Sub-Module Level Synthesis

- **Why it is necessary**
  - **Optimization & Area Reduction**: Each sub-module can be optimized independently for logic, technology mapping, and area efficiency.
  - **Reusability**: Sub-modules can be designed, verified, and reused across larger projects.
  - **Parallel Processing**: Large designs can be synthesized faster by handling sub-modules concurrently.

- **Commands Example**
  ```tcl
  read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
  read_verilog multiple_modules.v
  synth -top sub_module1
  abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
  show
  ```
  
## Various Flop Coding Styles and Optimization
- Different coding styles for flip-flops in RTL  
- How coding style impacts synthesis and optimization  
- Efficient flop coding to reduce area/power  
- Examples:
  - Asynchronous vs synchronous reset flops  
  - Use of enable signals  
  - Avoiding redundant flops  
