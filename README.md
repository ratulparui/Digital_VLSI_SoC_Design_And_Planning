# Digital_VLSI_SoC_Design_And_Planning
# Sponsored by NASSCOM <!-- Red -->
____________________________________
# Contents (Day 1 - Day 5)
# Table of Contents

- [Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK](#section-1)
  - [SKY130_D1_SK1 - How to talk to computers](#subsection-11)
    - [SKY_L1 - Introduction to QFN-48 Package, chip, pads, core, die and IPs](#sub-subsection-111)
    - [SKY_L2 - Introduction to RISC-V](#sub-subsection-112)
    - [SKY_L3 - From Software Applications to Hardware](#sub-subsection-113)
  - [SKY130_D1_SK2 - SoC design and OpenLANE](#subsection-12)
    - [SKY_L1 - Introduction to all components of open-source digital asic design](#sub-subsection-121)
    - [SKY_L2 - Simplified RTL2GDS flow](#sub-subsection-122)
    - [SKY_L3 - Introduction to OpenLANE and Strive chipsets](#sub-subsection-123)
    - [SKY_L4 - Introduction to OpenLANE detailed ASIC design flow](#sub-subsection-124)
  - [SKY130_D1_SK3 - Get familiar to open-source EDA tools](#subsection-13)
    - [SKY_L1 - OpenLANE Directory structure in detail](#sub-subsection-131)
    - [SKY_L2 - Design Preparation Step](#sub-subsection-132)
    - [SKY_L3 - Review files after design prep and run synthesis](#sub-subsection-133)
    - [SKY_L4 - OpenLANE Project Git Link Description](#sub-subsection-134)
    - [SKY_L5 - Steps to characterize synthesis results](#sub-subsection-135)
- [Section 2](#section-2)
  - [Subsection 2.1](#subsection-21)
    - [Sub-subsection 2.1.1](#sub-subsection-211)
  - [Subsection 2.2](#subsection-22)
    - [Sub-subsection 2.2.1](#sub-subsection-221)
  - [Subsection 2.3](#subsection-23)
    - [Sub-subsection 2.3.1](#sub-subsection-231)
- [Section 3](#section-3)
  - [Subsection 3.1](#subsection-31)
    - [Sub-subsection 3.1.1](#sub-subsection-311)
  - [Subsection 3.2](#subsection-22)
    - [Sub-subsection 3.2.1](#sub-subsection-321)
  - [Subsection 3.3](#subsection-33)
    - [Sub-subsection 3.3.1](#sub-subsection-331)
- [Section 4](#section-4)
  - [Subsection 4.1](#subsection-41)
    - [Sub-subsection 4.1.1](#sub-subsection-411)
  - [Subsection 4.2](#subsection-42)
    - [Sub-subsection 4.2.1](#sub-subsection-421)
  - [Subsection 4.3](#subsection-43)
    - [Sub-subsection 4.3.1](#sub-subsection-431)
- [Section 5](#section-5)
  - [Subsection 5.1](#subsection-51)
    - [Sub-subsection 5.1.1](#sub-subsection-511)
  - [Subsection 5.2](#subsection-42)
    - [Sub-subsection 5.2.1](#sub-subsection-521)
  - [Subsection 5.3](#subsection-53)
    - [Sub-subsection 5.3.1](#sub-subsection-531)
_______________________________________________________________________
<a name="section-1"></a>
## Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK 
<a name="subsection-11"></a>
### SKY130_D1_SK1 - How to talk to computers
<a name="sub-subsection-111"></a>
#### SKY_L1 - Introduction to QFN-48 Package, chip, pads, core, die and IPs

- We have taken an example of an audrino board. 
   - We can see the IC inside that audrino board.
   
   ![Day1_Lecture1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/9e222e48-f467-4221-80af-dca80074c2d6)
  
  - If we zoom in to that IC we can see that it's a processor/SoC, consists of I/O pins, SDRAM chip etc.
    
    ![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/97e8dc74-6db1-4a1e-87a1-62db58d38559)
  - Opening up that particular IC in the audrino board, we can see something like this.\
    ![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/33fe975d-bf23-4370-95df-35838ed0743e)
  - The above package can be named as QFN-48, having a size of 7mm x 7mm.
  - The core sits in the centre of that package and the wires are used for connections between the I/O pads and the core(chip).
    ![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ab30561a-ee46-415c-b36d-51ed65506ab5)
  - Core, die and pads are shown inside that package.
    ![9](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/fe3e4da3-c637-4546-a50d-b7a16c4af3a8)
  -The core consists of Foundry IP's, Macros etc. IP stands for Intelectual property.
    ![12](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/68b2506b-aecd-447c-9f57-41435e9639cf)
 
_______________________________________________________________________________________________________________________________\
    <a name="sub-subsection-112"></a>
#### SKY_L2 - Introduction to RISC-V
 - If we have a RISC-V ISA, then a particular C program can be converted into a Layout based on RISC-V ISA.
   - The C program is first compiled into assembly to machine language. Then the bits are executed inside that particular Layout. 
   ![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/5c841ee4-3979-487f-962e-32cee73215df)
   - The RISC_V architechture must be defined using RTL coding. Now RTL to Layout is known as RTL2GDSII Flow.
  ![Screenshot (5)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/f62d5958-ff25-4bf5-a864-23c8f4c7ee61)
___________________________________________________________________________________________________________________________________
<a name="sub-subsection-113"></a>
#### SKY_L3 - From Software Applications to Hardware
- All the apps we use runs on this hardware. This apps enters into system software. There are various levels of system software.
 - It consists of OS, compiler and the assembler. Depending on the ISA the C program will be converterd to its respective machine language. Then it's fed to the hardware.
   ![Screenshot (15)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a78fcea6-ffe9-4e64-a0c3-54dd5399268a)
 - Based on the ISA, we need to write the RTL code, then perform synthesis to generate GLN and then perform physical design implementation of that netlist.
____________________________________________________________________________________________________________________________________




   





    

      
    


  
