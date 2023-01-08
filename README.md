# Intel-CKT-Training

## Table of contents

- **Day 1 - Fundamentals of VLSI Design and
Overview of Sand-to-Silicon**
  <details><summary> Theory </summary>
  
  ## **Overview of VLSI Design**
  - **Packaged Chip**
  
    -There are different types of packaging:
      - System in a package (SIP)
      - Dual in-line package (DIP)
      - Quad-flat no-leads (QFN)
      - Ball grid array (BGA)
  
    -The central part of the chip is call die.
  
   - **Die and Wafer**
 
        ![image](https://user-images.githubusercontent.com/122155193/211223009-eefb6003-b59f-45d3-867b-3a645ad9e624.png)

      - A Single wafer contains 10’s of thousands die
      - All the components fabricated on the die

    - **Inside the Die**
       -  Digital: Gates, Muxes, decoders, counters, Resistors, FSMs
       -  Analog and RF: Clock: VCO and PLL; Voltage Ref. and Reg.: Bandgap reference, LDO, DC-DC converter; Data: PRBS generator; Amplifiers and Filters
       -  Memory and Memory Controller: Static Random Access Memory (SRAM) and SRAM controller

    - **Moore’s Law**
      - The observation that the number of transistors in a dense integrated circuit (IC) doubles about every two years.
  
    - **VLSI Design Methodology**
      - Types of VLSI Design styles:
        1) **Field programming gate array (FPGA) design**
            - Faster prototyping and cost-effective
            - Consists of:
              - Input/output buffers
              - Array of configurable logic blocks (CLBs)
              - Programmable interconnect structures
            - The programming of interconnects is accomplished by programming of RAM
            - Signal routing between the CLBs and the I/O blocks made by configurable switching matrices
  
        2) **Application-specific integrated circuit (ASIC)**
            - **Standard cell based design**
              - It is one of the most prevalent full-custom design styles and requires development of a full-custom mask set.
              - All of the commonly used logic cells are developed, characterized, and stored in a standard-cell library.
              - Each cell is characterized according to several different categories:
                - Delay time vs load capacitance and input transition
                - Circuit simulation model, Timing simulation model, Fault simulation model
                - Cell data for place-and route
                - Mask data
            - **Full Custom Design**
              - the entire mask design is done without using any library.
              - Productivity is very low because the geometry, orientation, and placement of every transistor is done individually by the designers.
              - Developmental cost of such a design style is becoming huge.
              - All the analog and RF designs are full custom design.
  
  - **VLSI Design Quality**
  
      - Important criteria to measure the design quality:
  
         1) **Testability**
             - Generation of good test vecto.
             - Availability of good test fixture at speed.
             - Design of testable chip.
  
          2) **Yield and Manufacturability**
             - Yield: No. of tested ok chips/Total no. of Chips
             - Functional Yield: Checks at lower speed
             - Parametric Yield: Checks at required speed
  
          3) **Reliability**
              - ESD and EOS
              - Electromigration
              - Oxide breakdown
              - Power and ground bouncing
             - On-chip noise and cross-talk
  
           4) **Technology Upgradability**
              - functional module for design reuse can be achieved quickly with minimal cost.
              - Develop and use advanced CAD tools.
  
  - **Package Technology**
     - Chip designers should work closely with package designers from the start of the project to avoid failures of the VLSI chip.
  
     - Types of package:
        1) **Pin-through-hole (PTH):**
  
          - ![image](https://user-images.githubusercontent.com/122155193/211224732-7f1409d0-0dd4-49c4-aefa-23b01355a877.png)
  
          - holes drilled in PCB
          - Not cost effective 
  
        2) **Surface Mount Technology (SMT):**
  
          - ![image](https://user-images.githubusercontent.com/122155193/211224778-c207e8e2-0d2e-4a39-80e2-166091dddbf9.png)
  
          - Directly soldered on the PCB
          - Cost and space effective
  
        3) **Plastic:**
  
          - Permeable to environmental moisture
  
        4) **Ceramic:**
  
          - Power consumption, performance and environmental requirements
  
   - **CAD Tools**
      - Essential for timely development of integrated circuits.
      - CAD technology for VLSI chip design can be categorized into the following areas:
        - High-level synthesis
        - Logic synthesis
        - Circuit optimization
        - Layout
        - Placement and routing
        - Simulation
        - Design rules and checking


