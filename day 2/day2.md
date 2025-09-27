# Day 2 - Timing libs, Hierarchical vs Flat Synthesis and Efficient Flop Coding Styles

## Introduction to Timing .libs
- Explanation of what a timing library (.lib) is  
- Role of .lib in synthesis and timing analysis  
- How standard cell characterization is stored in .lib files  
- Key parameters: setup time, hold time, propagation delay, power, etc.  

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
