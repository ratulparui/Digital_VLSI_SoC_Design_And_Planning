# Digital_VLSI_SoC_Design_And_Planning
# Sponsored by NASSCOM <!-- Red -->
____________________________________
# Contents (Day 1 - Day 5)
# Table of Contents

- [Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/edit/main/README.md#sky130-day-1---inception-of-open-source-eda-openlane-and-sky130-pdk)
  - [SKY130_D1_SK1 - How to talk to computers](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/edit/main/README.md#sky130_d1_sk1---how-to-talk-to-computers)
    - [SKY_L1 - Introduction to QFN-48 Package, chip, pads, core, die and IPs](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/edit/main/README.md#sky_l1---introduction-to-qfn-48-package-chip-pads-core-die-and-ips) 
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
## Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK 
### SKY130_D1_SK1 - How to talk to computers
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
    ![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/75ee0826-833f-4868-a495-a72550487c45)
  - Core, die and pads are shown inside that package.
    ![9](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/fe3e4da3-c637-4546-a50d-b7a16c4af3a8)
  -The core consists of Foundry IP's, Macros etc. IP stands for Intelectual property.
    ![12](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/68b2506b-aecd-447c-9f57-41435e9639cf)
 
    
- Item 3




    

      
    


  
