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
- [Sky130 Day 2 - Good floorplan vs bad floorplan and introduction to library cells](#section-2)
  - [SKY130_D2_SK1 - Chip Floor planning considerations](#subsection-21)
    - [SKY_L1 - Utilization factor and aspect ratio](#sub-subsection-211)
    - [SKY_L2 - Concept of pre-placed cells](#sub-subsection-212)
    - [SKY_L3 - De-coupling capacitors](#sub-subsection-213)
    - [SKY_L4 - Power planning](#sub-subsection-214)
    - [SKY_L5 - Pin placement and logical cell placement blockage](#sub-subsection-215)
    - [SKY_L6 - Steps to run floorplan using OpenLANE](#sub-subsection-216)
    - [SKY_L7 - Review floorplan files and steps to view floorplan](#sub-subsection-217)
    - [SKY_L8 - Review floorplan layout in Magic](#sub-subsection-218)
  - [SKY130_D2_SK2 - Library Binding and Placement](#subsection-22)
    - [SKY_L1 - Netlist binding and initial place design](#sub-subsection-221)
    - [SKY_L2 - Optimize placement using estimated wire-length and capacitance](#sub-subsection-222)
    - [SKY_L3 - Final placement optimization](#sub-subsection-223)
    - [SKY_L4 - Need for libraries and characterization](#sub-subsection-224)
    - [SKY_L5 - Congestion aware placement using RePlAce](#sub-subsection-225)
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
<a name="subsection-12"></a>
### SKY130_D1_SK2 - SoC design and OpenLANE
<a name="sub-subsection-121"></a>
#### SKY_L3 - SKY_L1 - Introduction to all components of open-source digital asic design


____________________________________________________________________________________________________________________________________

<a name="sub-subsection-122"></a>
#### SKY_L2 - Simplified RTL2GDS flow


________________________________________________________________________________________________________________________________________

<a name="sub-subsection-123"></a>
#### SKY_L3 - Introduction to OpenLANE and Strive chipsets


__________________________________________________________________________________________________________________________________________
<a name="sub-subsection-124"></a>
#### SKY_L4 - Introduction to OpenLANE detailed ASIC design flow


___________________________________________________________________________________________________________________________________________
<a name="subsection-13"></a>
### SKY130_D1_SK3 - Get familiar to open-source EDA tools
<a name="sub-subsection-131"></a>
#### SKY_L1 - OpenLANE Directory structure in detail



____________________________________________________________________________________________________________________________________________

<a name="sub-subsection-132"></a>
#### SKY_L2 - Design Preparation Step




___________________________________________________________________________________________________________________________________________
<a name="sub-subsection-133"></a>
#### SKY_L3 - Review files after design prep and run synthesis
___________________________________________________________________________________________________________________________________________
<a name="sub-subsection-134"></a>
#### SKY_L4 - OpenLANE Project Git Link Description
___________________________________________________________________________________________________________________________________________
<a name="sub-subsection-135"></a>
#### SKY_L5 - Steps to characterize synthesis results
___________________________________________________________________________________________________________________________________________
<a name="section-2"></a>
## Sky130 Day 2 - Good floorplan vs bad floorplan and introduction to library cells 
<a name="subsection-21"></a>
### SKY130_D2_SK1 - Chip Floor planning considerations
<a name="sub-subsection-211"></a>
#### SKY_L1 - Utilization factor and aspect ratio
-The first step of the physical design is to define the width and the height of the core and the die.
![Screenshot (48)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/95a6b297-fccb-40e4-9b53-05e947996a48)


- Let us consider a netlist consists of a lanunch and a capture Flip-Flop and some combinational logic circuits in between them.
![Screenshot (49)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/4b93fc36-2b6b-45b3-9c50-97ac0cf30f0f)
 - So, we are dependant on the width and height of the gates that are inside the netlist. If we give them proper dimensions, we have,
![Screenshot (50)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ece42d19-af22-4913-8899-7a87ca1c9fd3)

 - Let us consider the standard cells having unit length and width making 1 square unit area. Similarly the Flip-Flops having 1 square unit area.
 
 - Now, if we put them back-to-back without consdiering the interconnects, we have total area 4 square unit.
![Screenshot (51)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/abd96317-4db4-4fbb-87d3-94c6b32af01b)

 - We have the Utilization Factor defined by (Area occpied by the netlist) / (total area)
![Screenshot (53)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/9feca4bc-93bc-4349-b636-727516872f08)
 - For the example taken Utilization Factor = 1 (100% utilization) and Aspect ratio is also equal to 1.
![Screenshot (54)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/df295632-a5bf-4e18-9bb5-9762ecd03890)
- When the aspect ratio is not equal to 1, then the height and width are not same, so the chip is no longer square shaped, it's rectangular.
_____________________________________________________________________________________________________________________________________________
<a name="sub-subsection-212"></a>
#### SKY_L2 - Concept of pre-placed cells
- For the example mentioned below, Utilization Factor = 0.25 (25% utilization) and aspect ratio = 1. So 75% of the area is still available.
![Screenshot (57)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/42ee65fa-b640-47ac-ad41-e6e1498d3ff0)
 -Now we need to define the locations of the preplaced cells.
![Screenshot (59)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/53ccd126-5311-437a-b07a-f33a85dbdf86)
 - Let's consider a combinational circuit, we can devide the circuit into two parts. We have considered two blocks, block 1 and 2
![Capture](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/6f6b75a3-0293-4c25-83e6-509689d82638)
 - We have extened the IO pins for both the blocks and seperated them as two black boxes. They can me reused multiple times, known as IPs.
![Screenshot (60)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/f12fb797-004a-4421-8597-3089afcae67e)
 - Now, these cells should be placed before actual placement and routing, that's why these cells are called pre-placed cells. Their locations are fixed.
![Capture2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/653ade3b-03d6-442d-ac85-346efb5d1115)
______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-213"></a>
#### SKY_L3 - De-coupling capacitors
- We have 3 cells represented as, block A, B and C, based on the requirement, they are placed towards the input side of the core.
![Screenshot (61)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/8f51479c-700b-41b3-b03f-a878d9b24ca8)
- For the below circuit Vdd be 1V and Vdd' be 0.7 V. This drop occurs due to resistance and inductance present in the path. Now, during a switching event, let a charging is happening as shown, max voltage can't go beyond 0.7 V. Now that 0.7 V to be detected as logic 1, should be within the noise margin range.
![Screenshot (65)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/78432b58-a7d1-438c-bb59-941de17c935d)
- The region between Vol and Vil is treated as logic 0, the region between Vih and Voh is treated as logic 1, and the region between Vil and Vih is known as undefined region.
![Screenshot (66)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/e5a84084-dd12-4f23-8260-313b8d44bab1)
- If Vdd' becomes 0.5V, that may lie in the undefined region, which can lead to problem.
- To solve the problem, we need to use de-coupling capacitor, parallel to the circuit. Whenever, there is a switching operation happening, de-coupling capacitor will supply the current to the circuit. When there is no switching operation happening, de-coupling capacitor, will get charged. It simply de-couples the circuit from the source.
![Screenshot (67)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/0948bcaf-503d-4a71-8ff1-4204cffc6c99)
- So, we place de-coupling capacitors, beside the pre-placed cells, to avoid crosstalk.
![Screenshot (68)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/63afb81b-e2a0-487a-a509-d3aa939208d9)


 
_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-214"></a>
#### SKY_L4 - Power planning
_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-215"></a>
#### SKY_L5 - Pin placement and logical cell placement blockage
________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-216"></a>
#### SKY_L6 - Steps to run floorplan using OpenLANE
_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-217"></a>
#### SKY_L7 - Review floorplan files and steps to view floorplan
_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-218"></a>
#### SKY_L8 - Review floorplan layout in Magic
_______________________________________________________________________________________________________________________________________________
<a name="subsection-22"></a>
### SKY130_D2_SK2 - Library Binding and Placement
<a name="sub-subsection-221"></a>
#### SKY_L1 - Netlist binding and initial place design


________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-222"></a>
#### SKY_L2 - Optimize placement using estimated wire-length and capacitance


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-223"></a>
#### SKY_L3 - Final placement optimization


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-224"></a>
#### SKY_L4 - Need for libraries and characterization


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-225"></a>
#### SKY_L5 - Congestion aware placement using RePlAce

__________________________________________________________________________________________________________________________________________________

   





    

      
    


  
