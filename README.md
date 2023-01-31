# Intel-CKT-Training

## Table of contents

- **Day 1 - Fundamentals of VLSI Design and
Overview of Sand-to-Silicon**
- **Day 2 - Details of IC Manufacturing Process**
- **Day 3 - Overview of Digital and Custom IC Design Flow and requirement of Computer-Aided Design (CAD) Tools and Process Design Kit (PDK)**
- **Day 4 - Metal-Oxide-Semiconductor Structure** 
- **Day 5 - Metal-Oxide-Semiconductor FIELD EFFECT TRANSISTOR** 
  
## Day 1 
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
</details>

<Details>
  <summary> Lab </summary>
  
  ![image](https://user-images.githubusercontent.com/122155193/212777972-3d05e02e-1d9e-40ab-acba-fa41b4cd8039.png)

  
  ![image](https://user-images.githubusercontent.com/122155193/212778069-7ee6a882-57e1-48c8-941b-44407e52732e.png)

  
  ![image](https://user-images.githubusercontent.com/122155193/212778105-4a20f06e-20c8-4c82-8302-8c0f57c0a0a4.png)

</details>

## Day2
  <details>
  <summary> Theory </summary>
  
 ## **Analog VLSI Design Flow and CMOS Fabrication Process**
  - **Analog IC Design Process**
  
  ![tempsnip](https://user-images.githubusercontent.com/122155193/211691046-388cdea4-312d-44c6-8dae-3ae16b00909f.png)
  
  ![image](https://user-images.githubusercontent.com/122155193/211691175-91c7f27c-d825-40d4-891b-8fdc6719a969.png)

  - **Analog IC Design Process and its Relation with CAD and PDK**
  
  ![image](https://user-images.githubusercontent.com/122155193/211691478-f31aea87-d443-4210-b7c5-4443de798448.png)

  - **Role of Circuit Designer**
    - Design a practical circuit based on the device limits, technology constraints and physical implementations rather than a ideal circuit.
    - Have very good understanding of layout design, so that in less iterations the design can be fridged.
    - Always discuss with the layout designer for better and efficient circuit design.
  
  - **CMOS Technology**
    - Comparison of BJT and MOSFET Technology
    ![image](https://user-images.githubusercontent.com/122155193/211692066-23cdd7bc-12da-458f-9637-16315e0f7969.png)

    - Categorization of the CMOS Technology:
      - Submicron Technology: Lmin ≥ 0.35 µm
      - Deep Submicron Technology (DSM): 0.1 µm ≤ Lmin ≤ 0.35 µm
      - Ultra-Deep Submicron Technology (UDSM): Lmin ≤ 0.1 µm
      - BiCMOS Technology: Lmin = 0.5 µm
      
  - **CMOS Fabrication Process**  
    ![image](https://user-images.githubusercontent.com/122155193/211721141-61278ee4-ba64-41dc-b42c-0d119b56b6ea.png)

 <Details>
 <summary> 1. Wafer formation (sand-to-silicon) </summary>
 
 - The basic raw material used in CMOS fabs is a **wafer or disk of silicon** (roughly 75 mm to 300 mm in diameter and less than 1 mm thick).
 - Wafers are cut from boules, cylindrical ingots of singlecrystal silicon.
 - In order to to provide the crystal with the required electrical properties, **controlled amounts of impurities** are added to the melt.
 - A seed crystal is dipped into the melt (**to initiate crystal growth**), and the seed is gradually withdrawn vertically from the melt while simultaneously being rotated.
 - Then, the molten silicon attaches itself to the seed and recrystallizes.
 - Growth rates vary from 30 to 180 mm/hour.
 </details>
 
 <Details>
 <summary> 2. Photolithography </summary>
 
 - The **patterning** is achieved by a process called photolithography.
 - Used as the primary method in defining areas of interest.
 - The wafer is coated with the photoresist and subjected to selective illumination through **the photomask**.
 - A **photomask** is constructed with chromium (chrome) covered quartz glass. 
 - A UV light source is used to expose the photoresist.
 - **Developer solvent** is then used to dissolve the soluble unexposed photoresist, leaving islands of insoluble exposed photoresist.
 </details>
 
 <Details>
 <summary> 3. Well and Channel Formation </summary>
 
 - There are 4 CMOS technology processes:
   1) **N-well process**
      - the pMOS transistors are built in a n-well and the nMOS transistor is placed in the p-type substrate.
      
      ![image](https://user-images.githubusercontent.com/122155193/211732817-ce8ab953-ea39-431d-af7b-6502177adafd.png)
    
   2) **P-well process**
      - the nMOS transistors are built in a p-well and the pMOS transistor is placed in the n-type substrate. 
      - Used to optimize the pMOS transistor performance.
   
      ![image](https://user-images.githubusercontent.com/122155193/211733248-1b1f249a-0d82-469e-bd19-5e97b8112e2c.png)
 
   3) **Twin-well process**
       - Accompanied the emergence of n-well processes. 
       - A twinwell process allows the optimization of each transistor type.
      
      ![image](https://user-images.githubusercontent.com/122155193/211733777-f1c19a5f-d0a5-4ae4-bb14-886ce4253585.png)
      
    4) **Triple-well process**
       - Provide good isolation between analog and digital blocks in mixed-signal chips; 
       - It is also used to isolate high-density dynamic memory from logic.  

        ![image](https://user-images.githubusercontent.com/122155193/211734116-ae807cfb-2c10-44a5-a50b-b227d9a45d31.png)
 </details>
 
 <Details>
 <summary> 4. Silicon Dioxide (Sio2) </summary>
 
 - Oxidation of silicon is achieved by heating silicon wafers in an oxidizing atmosphere.
 - Some common approaches:
 
    - **Wet Oxidation** (oxidizing atmosphere contains water vapor)
      - The temperature is usually between 900 °C and 1000 °C.
      - Wet oxidation is a rapid process.
      
    - **Dry Oxidation** (oxidizing atmosphere is pure oxygen)
      - Temperatures are in the region of 1200 °C to achieve an acceptable growth rate.
      - Dry oxidation forms a better quality oxide than wet oxidation.
      - It is used to form thin, highly controlled gate oxides, while wet oxidation may be used to form thick field oxides.
    
    - **Atomic Layer Deposition (ALD)** 
      - when a thin chemical layer (material A) is attached to a surface and then a chemical (material B) is introduced to produce a thin layer of the required layer.
  </details>
 
  <Details>
 <summary> 5. Isolation </summary>
  
  - Individual devices in a CMOS process need to be isolated from one another so that they do not have unexpected interactions.
  - The transistor gate consists of a **thin gate oxide layer**.
  - The **thick oxide** used to be formed by a process called Local Oxidation of Silicon (LOCOS).ed to be formed by a process called Local Oxidation of Silicon (LOCOS).
  - A problem with LOCOS-based processes is the transition between thick andthin oxide, which extended some distance laterally to form a so-called bird’s beak.
  - Starting around the 0.35 µm node, **shallow trench isolation (STI)** was introduced to avoid the problems with LOCOS.
  - STI forms insulating trenches of SiO2 surrounding the transistors (everywhere except the active area).
 </details>
 
 <Details>
 <summary> 6. Gate Oxide </summary>

 - This is most commonly in the form of silicon dioxide (SiO2).
 - The transistor gate consists of a **thin gate oxide layer**.
</details>

<Details>
 <summary> 7. Gate and Source/Drain Formations </summary>
 
 - Grow gate oxide wherever transistors are required.
 - **area = source + drain + gate**
 - Deposit polysilicon on chip.
 - Pattern polysilicon (both gates and interconnect).
 - Etch exposed gate oxide, at this stage, the chip has windows down to the well or substrate wherever a source/drain diffusion is required.
 - Implant pMOS and nMOS source/drain regions.
 </details>
 
 <Details>
 <summary> 8. Contacts and Metallization </summary>
 
 - Contact cuts are made to source, drain, and gate according to the contact mask. These are holes etched in the dielectric after the source/drain formation.
 - Older processes commonly use aluminum (Al) for wires, although newer ones offer copper (Cu) for lower resistance.
 - Tungsten (W) can be used as a plug to fill the contact holes.
 </details>
  
<Details>
 <summary> 9. Passivation </summary>
 
 - The final processing step is to add a protective glass layer called passivation or over glass that prevents the ingress of contaminants.
 - Openings in the passivation layer, called overglass cuts, allow connection to I/O pads and test probe points if needed.
 </details>
 
 <Details>
 <summary> 10. Metrology </summary>
 
 - Metrology is the science of measuring.
 - Everything that is built in a semiconductor process has to be measured to give feedback to the manufacturing process.
</details>
</details>

<Details>
 <summary> Lab </summary>
  
  [Assignment Day 2.pdf](https://github.com/Maryam288/Intel-CKT-Training/files/10389974/Assignment.Day.2.pdf)
</details>
 
## Day3
  <Details>
  <summary> Theory </summary>
  
 ## **CMOS Fabrication Process in DeepSubmicron (DSM) and Ultra DeepSubmicron (UDSM) Technology**
 
 - **Disadvantage of the Submicron CMOS Process**
 
    - Isolation of the Transistors:
      - The use of **reverse bias pn junctions** to isolate transistors becomes **impractical as the transistor sizes decrease**.
    
 - **Local Oxidation of Silicon (LOCOS) Isolation Process**
    - LOCOS is the traditional isolation technique used in submicron processes.
    
  ![image](https://user-images.githubusercontent.com/122155193/211982154-f8f38e6d-ec0d-4d9e-b6c8-30f3d6454cdc.png)    ![image](https://user-images.githubusercontent.com/122155193/211982694-d5600c58-a8c2-4875-9c4d-e6f1de87bdc5.png)
   
   - Limitation of this technique:
     - Bird’s beak effect
     - Surface area which is lost to this encroachment
     
   - Advantages of LOCOS fabrication process:
      - Simple process flow
      - High oxide quality because the whole LOCOS structure is thermally grown.
   
   
  - **Sallow Trench Isolation Technology**
  
    - STI isolation process is the preferred isolation process for deep-submicron process because it completely avoids Bird’s beak shape characteristics.
    
    ![image](https://user-images.githubusercontent.com/122155193/211989171-54995dfb-273f-42e8-8011-781d3c3458ed.png)
    - STI is more suitable for the increased density in a small area because it allows forming smaller isolation regions.
    - The disadvantage is larger number of process steps.

  - **Illustration of a Deep Submicron (DSM) CMOS Technology**
  
    - The DSM technology provides:
      - A deep n-well that can be utilized to reduce substrate noise coupling.
      - A MOS Varactor that can be used to make voltage controlled oscillators (VCOs).
      - Different kind of resistors like: **Diffused and/or implanted resistors**, **Well resistors**, **Poly resistors**, **Metal Resistors**.
      - At least 6 levels of metal that can form many useful structures such as inductors, capacitors, and transmission lines.
  
       ![image](https://user-images.githubusercontent.com/122155193/212009429-1cd43858-07c1-46c4-8753-2daf96f1b9b9.png)

- **Different Types of Capacitor in Deep Submicron (DSM) CMOS Technology**
  ![image](https://user-images.githubusercontent.com/122155193/212011793-ef905a9b-4e3e-4948-a520-d8fe48e1a840.png)

 - **Example of a DSM Technology Process (SKY130)** 
  
  ![image](https://user-images.githubusercontent.com/122155193/212012219-db2cf3a3-d372-4ea5-82a4-ba27bfdf4f95.png)
  
  - **Major Fabrication Steps for a DSM CMOS Process** 

  ![image](https://user-images.githubusercontent.com/122155193/212208610-02744f7c-4479-41d4-84d0-38e75fe3c879.png)

<Details>
 <summary> n and p-well Creation </summary>

- NMOS wil be fabricated in the p-well and PMOS in the n-well.
- Done by implantation followed by a deep diffusion.
 </details>
 
 <Details>
 <summary> Sallow Trench Isolation Creation </summary>

-  STI electrically isolates one region/transistor from another.
 </details>
 
 <Details>
 <summary> Threshold Shift and Anti-Punch through Implants </summary>

- The natural thresholds of the **NMOS is about 0V** and of the **PMOS is about –1.2V**.
- p-implant is used to make the NMOS harder to invert and the PMOS easier resulting in threshold voltages balanced around zero volts.
- Implant can be applied to create a higher-doped region beneath the channels to prevent punch-through from the drain depletion region extending to source depletion region.
 </details>
 
 <Details>
 <summary> Thin Oxide and Polysilicon Gate </summary>

- A thin oxide is deposited followed by polysilicon. These layers are removed where they are not wanted.
 </details>
 
 <Details>
 <summary> Lightly Doped Source and Drain </summary>

- A lightly-doped implant is used to create a lightly-doped source and drain next to the channel of the MOSFETs.
 </details>
 
 <Details>
 <summary> Sidewall Spacer </summary>

- A layer of dielectric is deposited on the surface and removed in such a way as to leave “sidewall spacers” next to the thin-oxide-polysilicon-polycide sandwich.
 - These sidewall spacers will prevent the part of the source and drain next to the channel from becoming heavily doped.
 </details>
 
 <Details>
 <summary> Implantation of Havily Doped Source and Drain </summary>

- Provide the completed sources and drains.
- Allows for ohmic contact into the wells and substrate.
  </details>
  
  <Details>
 <summary> Siliciding (Salicide and Polyside) </summary>

- Reduces the resistance of the bulk diffusions and polysilicon and forms an ohmic contact with material on which it is deposited.
  </details>
  
 <Details>
 <summary> Intermediate Oxide Layer </summary> 

- An oxide layer is used to cover the transistors and to planarize the surface.
 </details>
 
 <Details>
 <summary> First Level Metal </summary> 

- Tungsten plugs are built through the lower intermediate oxide layer to provide contact between the devices, wells and substrate to the first-level metal.
 </details>
 
 <Details>
 <summary> Second Level Metal </summary> 

- The previous step is repeated for the second-level metal.
 </details>
 
 - **Summary of Deep Submicron (DSM) CMOS Fabrication Process**
    - DSM technology typically has a minimum channel length between 0.35μm and 0.1μm.
    - DSM technology addresses the problem of excessive depletion region widths in junction isolation techniques by using shallow trench isolation.
    - DSM technology may have from 4 to 8 levels of metal.
    - Lightly doped drains and sources are a key aspect of DSM technology.
    
 - **Ultra Deep Submicron (UDSM) CMOS Technology**
    - Lmin ≤ 0.1 microns.
    - Minimum feature size less than 100 nanometers.
    - 22 nm drawn length, 5 nm lateral diffusion, 1 nm transistor gate oxide, 8 layers of copper interconnect.
    - Specialized processing is used to increase drive capability and maintain low off currents.
    
  - **Advantage of UDSM CMOS Technology**
  
 <Details>
 <summary> Digital Viewpoint </summary> 

- Improved Ion/Ioff
 - Reduced gate capacitance
 - Higher drive current capability
 - Reduced interconnect density
 - Reduction of active power
 </details>
 
  <Details>
 <summary> Analog Viewpoint </summary> 

- More levels of metal
 - Higher cutoff frequency
 - Higher capacitance density
 - Reduced junction capacitance per transconductance
 - More speed
 </details>
 
 - **Disadvantage of UDSM CMOS Technology**
 <Details>
 <summary> Analog Viewpoint </summary> 

- Reduction in power supply resulting in reduced headroom.
 - Gate leakage currents.
 - Reduced small signal intrinsic gain.
 - Increased nonlinearity.
 - Increased noise and poorer matching.
 </details>
 </details>

<Details>
 <summary> Lab </summary> 
  
 <Details>
 <summary> Q6) What are the advantages of ultra-deep submicron process over deep submicron process. </summary>
 
  - Improved Ion/Ioff
  - Reduced gate capacitance
  - Higher drive current capability
  - Reduced junction capacitance per transconductance
  - More speed
 </details>
  
 <Details>
 <summary> Q7) What is the difference between LOCOS and STI process? </summary>
   
 ![image](https://user-images.githubusercontent.com/122155193/212779336-9637f723-ba9d-4a7f-9591-d5aa9fa8fe06.png)
</details>
  
  <Details>
 <summary> Q8) Why for body connection a heavily doped n+ or p+ is used? </summary>
    
- A heavily doped N+ or P+ diffusion is made for the metallic contact. This creates a conductive junction between the metal and the semiconductor, thus giving a good electrical contact to the bulk.
    
</details>
<Details>
 <summary> Q9) What is use of silicide and poolside? </summary>  
  
  - To interconnect between N+ or P+ diffusion to the metal.
 </details>
  
 <Details>
 <summary> Q10) Which process steps used for control threshold voltage and punch-through effect? </summary>   
   
   - Oxidation and Diffusion
  </details>
  <Details>
 <summary> Q11) Draw a top view, front view and 3D view of a CMOS inverter and annotate the length and width of both PMOS and NMOS transistor. </summary>   
 </details>
  
   <Details>
 <summary> Q12) Why sidewall spacer are used in DSM technology? </summary>
     
 - To insulate the drain and source metal contacts from the gate of the transistor.
     
  </details>    
 <Details>
 <summary> Q13) What are the advantages of Deep N-well technology over n-well technology? </summary> 
 
   - Deep N-well decreases the noise coupling through it to the substrate and giving the advantage of fully isolated NMOS devices.
   
</details>    
 <Details>
 <summary> Q14) What is passivation layer? </summary>    
   
   - A layer normally used protect the active semiconductor surface from the surrounding environment.
   
 </details>    
 <Details>
 <summary> Q15) What is Bird’s beak in LOCOS process and what is the impact on the transistor performance? </summary>     
   
   - As the oxide grows, the nitride mask, which is meant to block the oxide from growing everywhere, is slightly bent due to stress caused by the oxide pushing the nitride as it grows.
   
   - The encroachment of field oxide in the active region reduces the area available to form a transistor and therefore it limits device scaling and device density in VLSI cuts which will limit the device performance. 
 </details>
 </details>
 
## Day4
  <details>
  <summary> Theory </summary>
  
 ## Metal-Oxide-Semiconductor Structure 
  - **Metal-Oxide-Semiconductor (MOS) Device Structure**
  
    - MOS junction simply a capacitor.
    - No current-voltage relationship, only capacitorvoltage relationship.
    
    ![image](https://user-images.githubusercontent.com/122155193/215636640-a6cc772b-f90a-4789-a4ce-cdfca27b0cc1.png)

- **MOS Device Structure and Fabrication**

<details>
<summary> Fabrication </summary>

   - Oxidation: process to create SiO2 on top of Silicon.
   - Metallization: process to deposit poly-silicon on top of SiO2.
</details> 

<details>
<summary> Device Structure </summary>

  - Gate and substrate are different material so there is a contact potential between them (expressed as metal to semiconductor work function (ϕms)).
  - Interface is between SiO2 and Silicon
</details> 

- **Ideal MOS Junction or Capacitor**

<details>
<summary> Case1: Accumulation Mode of Operation </summary>

## **Accumulation Mode (V < 0)**

  - Pile of majority carrier at the interface.
  - Charge at the surface directly proportional to voltage.

![image](https://user-images.githubusercontent.com/122155193/215638041-ec999fd0-297a-45ca-a9db-8b6615abe401.png)
</details> 

<details>
<summary> Case2: Depletion Mode of Operation </summary>

## **Depletion Mode (0 < V < VT)**    

  - The semiconductor surface starts to deplete and the type of charge at the surface is –ve and gradually increase with the increase of voltage.
  - **Weak inversion voltage** is the voltage at which the surface carrier concentration is exactly equal to bulk carrier concentration and from this point the weak inversion started.
  - Charge at the surface directly proportional to voltage.
  - **Threshold voltage** is the voltage at which the surface concentration exactly equal to the bulk concentration.
  - This is called inversion point and at this point depletion mode ends and strong inversion started.
  
![image](https://user-images.githubusercontent.com/122155193/215639254-0e3ee43f-18f0-4ec9-a02f-ee19bb2d2e54.png)
</details> 

<details>
<summary> Case3: Strong Inversion Mode of Operation </summary>

## **Strong Inversion Mode (V ≥ VT)**    

  - At threshold voltage a channel form at the surface of the semiconductor due to inversion charges.
  - Before threshold voltage the charge comes from negatively charged ionized acceptors.
  - After threshold voltage, the more charge comes from the electrons rather than depleting the holes.
  - The extra negative charge required for the semiconductor is comes from the mobile electrons which are very close to the surface.
  
  ![image](https://user-images.githubusercontent.com/122155193/215639559-c8ce74f2-3fa1-499f-9f67-bce9026215eb.png)
  
</details> 

- **Summary of the MOS Operation Modes**

![image](https://user-images.githubusercontent.com/122155193/215639865-0a6ba5fe-67cb-413a-baf5-f03e46c5240d.png)

  - Flat band voltage is 0 for ideal MOS structure.
  - Flat band means flatness of conduction and valence band edges at semiconductor surface.
  
- **Q-V Characteristics of MOS Structure** 
 
  ![image](https://user-images.githubusercontent.com/122155193/215640211-26a81d2c-c86b-462f-8b30-aa50f032b8f8.png)

 - Surface Charges at different regions
  
<details>
<summary> Accumulation </summary>

![image](https://user-images.githubusercontent.com/122155193/215664491-a76dd783-6bea-406f-9629-a6018f62a797.png)

</details> 

<details>
<summary> Depletion </summary>

![image](https://user-images.githubusercontent.com/122155193/215664814-2e512672-52f3-4e8a-b9a8-2107378e9e24.png)

</details>

<details>
<summary> Inversion </summary>

![image](https://user-images.githubusercontent.com/122155193/215665123-3d16ef04-191a-4f2e-b52c-c0ac80b980be.png)

</details>

<details>
<summary> Threshold Voltage </summary>

![image](https://user-images.githubusercontent.com/122155193/215665313-2b4ef7f0-b0e5-46bb-85eb-30b79f5788db.png)

</details>

- **C-V Characteristics of MOS Structure** 

![image](https://user-images.githubusercontent.com/122155193/215665604-025af0cf-c9c7-453a-aa23-972c5e13c186.png)

- **Non Ideal MOS Structure** 

<details>
<summary> Effect of fixed charge Qf </summary>

![image](https://user-images.githubusercontent.com/122155193/215665879-b3a0e828-18ee-4992-9da1-4a9683ef2e63.png)

- To cerate a zero charge on silicon a negative voltage is required to give at gate terminal.
- By applying a negative volute at gate the surface charge at silicon will be zero.
- Zero charge in the semiconductor corresponds to flat-band condition of a MOS junction.
</details>

<details>
<summary> Effect of work metal-semiconductor work function difference ϕms </summary>

![image](https://user-images.githubusercontent.com/122155193/215665963-4d0e0ccc-2872-4bae-8921-c744e36599f7.png)

- Electrons are always moves from higher energy level to lower energy level.
- Electrons are transferred through wire.
- To remove the electrons from semiconductor surface we have to provide a –ve voltage to the gate.
</details>

- **Summary of Nonideal MOS Capacitor** 

 1. Effect of fixed oxide charge 𝑄f
  
  ![image](https://user-images.githubusercontent.com/122155193/215668210-27ebfbf1-aa29-47e0-ad78-123634557852.png)
  
 2. Effect of work metal-semiconductor work function difference ϕms
  
  ![image](https://user-images.githubusercontent.com/122155193/215668285-22ce8cc9-fe8a-4198-b567-5649bb75d3b3.png)

 3. In presence of both fixed charge and metal-to-semiconductor work function

![image](https://user-images.githubusercontent.com/122155193/215668376-a188458d-30cc-4e27-b91e-03d5c3ea3d16.png)

 4. So threshold voltage od a nonideal MOS capacitor will be
  
  ![image](https://user-images.githubusercontent.com/122155193/215668468-9319084b-083d-47bb-b426-aba394a3374f.png)
  
</details>

<details>
<summary> Lab </summary>

<details>
<summary> 1. What are the main differences between ideal and real MOS structure? </summary>

![image](https://user-images.githubusercontent.com/122155193/215671227-45643d7a-e561-4598-9e89-ff562027b9a0.png)

</details>

<details>
<summary> 2. What are the different modes of operation in a MOS junction? </summary>

- Accumulation Mode (V < 0)
- Depletion Mode (0 < V < Vt)
- Strong Inversion Mode (V ≥ Vt)
</details>

<details>
<summary> 3. What is the difference between weak inversion and strong inversion of a MOS junction? </summary>

![image](https://user-images.githubusercontent.com/122155193/215672027-d394e1e7-f836-4776-a720-cf048c662891.png)
</details>

<details>
<summary> 4. What is metal-to-semiconductor work function? </summary>

- The energy difference between the metal and the semiconductor.
</details>

<details>
<summary> 5. For a heavily n-doped poly-silicon metal and a p-substrate semiconductor, what will be the metal-to-semiconductor work function? Positive or negative?</summary>

- The heavily n-doped poly-silicon will have the fermi-level very close to conduction band (Ec), while p-substrate semiconductor will have the fermi-level close to valance band (Ev).

- ϕms = ϕm - ϕs

- In this case, ϕm < ϕs

- Thus, ϕms will be negative.

</details>

<details>
<summary> 6. For a heavily p-doped poly-silicon metal and a n-substrate semiconductor, what will be the metal-to-semiconductor work function? Positive or negative?</summary>

- The heavily p-doped poly-silicon will have the fermi-level very close to valance band (Ev), while n-substrate semiconductor will have the fermi-level close to conduction band (Ec).

- ϕms = ϕm - ϕs

- In this case, ϕm > ϕs

- Thus, ϕms will be positive.
</details>

<details>
<summary> 7. What is threshold voltage of a MOS junction? Express threshold voltage for a non-ideal MOS junction. </summary>

- Threshold voltage is the voltage at which the surface concentration exactly equal to the bulk concentration

![image](https://user-images.githubusercontent.com/122155193/215674955-bd07a353-7590-4f39-ae66-88deaa119135.png)

</details>

<details>
<summary> 8. If the oxide (SiO2) increases for a MOS structure, the threshold voltage will increase or decrease? </summary>

- Threshold voltage will increase.
</details>

<details>
<summary> 9. Instead of a lightly doped p-substrate, if you use a heavily doped p-substrate in a MOS structure then what will be the change in threshold voltage? Will it increase or decrease? </summary>

- Threshold voltage will increase.
</details>

<details>
<summary> 10. Describe, why MOS capacitance stay minimum at very high frequency and back to high value at low frequency </summary>

- High frequency always fluctuate at a high speed.
- There is no long time for the capacitor to collect higher charge to achieve higher capacitance.
- Thus, higher frequency get lower capacitance. 
</details>
</details>

## Day5
  <details>
  <summary> Theory </summary>
  
 ## **Metal-Oxide-Semiconductor FIELD EFFECT TRANSISTOR**
 
 - **MOSFET Structure**
 
 ![image](https://user-images.githubusercontent.com/122155193/215681889-ee72fd9f-89b3-4b40-b9f0-ac424ba47fce.png)

 ![image](https://user-images.githubusercontent.com/122155193/215681942-acd39576-b92b-4a06-b0e3-8384fe730af1.png)

 
 <details>
 <summary> Top View (Layout View) </summary>
 
 ![image](https://user-images.githubusercontent.com/122155193/215681520-92e68393-48d6-47cb-a203-0394f7c1e2db.png)
 </details>
 
 <details>
 <summary> Layout Layers and Rules </summary>
 
 ## Layout Layers
 - P-substrate
 - Thin oxide
 - Polysilicon
 - n+ diffusion
 - Contact
 - Metal
 
 ## Layout Rules
 - Min. width
 - Max Width
 - Spacing
 - Area
 - Enclosure
 - Extension
  </details>
 
 <details>
 <summary> Front View (Cross-section) </summary>
 
 ![image](https://user-images.githubusercontent.com/122155193/215681683-08bf5370-3ba2-4310-b54a-5ef19fa24bc9.png)
</details>

- **MOSFET Operation**

<details>
<summary> Cut-off </summary>

![image](https://user-images.githubusercontent.com/122155193/215708266-3f68bdf1-7c72-48a2-bd70-a2d097ccb54d.png)

- Gate voltage lower than threshold voltage (Vgs < Vt).
- Drain current, Id = 0
- Application: Switch
</details>

<details>
<summary> Linear </summary>

![image](https://user-images.githubusercontent.com/122155193/215708488-14e39dd8-c3e7-4fa3-a2ee-e01c676c69a7.png)

- Gate voltage slightly above threshold voltage (Vgs - Vt >= Vds)
- Id increase with the increases of Vgs

![image](https://user-images.githubusercontent.com/122155193/215707513-ad4a434b-4220-4404-85d6-8408b013005a.png)

- Application: switch and linear resistor
</details>


<details>
<summary> Saturation </summary>

![image](https://user-images.githubusercontent.com/122155193/215708579-94c60ce7-00e5-4db2-8e9a-be2855fd061f.png)

- Gate voltage much more higher than threshold voltage (Vgs - Vt < Vds)
- The curent from drain to source is saturated even the Vds keep increasing.
- Maximum Id.

![image](https://user-images.githubusercontent.com/122155193/215709056-2e35fb69-2620-4013-9092-55a9f2bc5254.png)

- Application: Amplifier and constant current source
</details>

- **ID-VGS Characteristics**

![image](https://user-images.githubusercontent.com/122155193/215711062-29223102-1ba3-40dc-b5ea-4bf419f6eedb.png)

- **ID-VGS Characteristics with Body Bias**

![image](https://user-images.githubusercontent.com/122155193/215711285-585c0df5-1a7f-4fbd-8fe9-5735c99216ca.png)

- **ID-VDS Characteristics**

![image](https://user-images.githubusercontent.com/122155193/215711428-5e9e2930-f7e6-4eee-b92a-4facf71339db.png)
