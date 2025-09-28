# Day 2 - Timing libs, Hierarchical vs Flat Synthesis and Efficient Flop Coding Styles

## Introduction to Timing .libs
# Standard Cell Libraries and PVT Characterization

## PVT (Process, Voltage, Temperature)
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

- **Additional information included in cell are:**
    - Leakage power based on the combination of inputs
    - Area
    - Power ports
    - Input capacitance
    - Power associated with the pin
    - Transition
    - Delay

      
## Hierarchical vs Flat Synthesis
- **Hierarchical Synthesis**
  - Maintains design hierarchy during synthesis  
  - Pros: Better readability, modular design, reuse of blocks  
  - Cons: May lead to suboptimal timing/area  

- **Flat Synthesis**
  - Flattens hierarchy before synthesis  
  - Pros: Better optimization, improved timing and area  
  - Cons: Longer runtime, harder debugging, loss of modularity  

## Various Flop Coding Styles and Optimization
- Different coding styles for flip-flops in RTL  
- How coding style impacts synthesis and optimization  
- Efficient flop coding to reduce area/power  
- Examples:
  - Asynchronous vs synchronous reset flops  
  - Use of enable signals  
  - Avoiding redundant flops  
