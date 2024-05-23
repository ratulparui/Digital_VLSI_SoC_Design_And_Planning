# Digital_VLSI_SoC_Design_And_Planning
# Sponsored by VSD and NASSCOM 
____________________________________
# Contents (Day 1 - Day 5)
``` Table of Contents ```

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
  - [SKY130_D2_SK3 - Cell design and characterization flows](#subsection-23)
    - [SKY_L1 - Inputs for cell design flow](#sub-subsection-231)
    - [SKY_L2 - Circuit design step](#sub-subsection-232)
    - [SKY_L3 - Layout design step](#sub-subsection-233)
    - [SKY_L4 - Typical characterization flow](#sub-subsection-234)
  - [SKY130_D2_SK4 - General timing characterization parameters](#subsection-24)
    - [SKY_L1 - Timing threshold definitions](#sub-subsection-241)
    - [SKY_L2 - Propagation delay and transition time](#sub-subsection-242)
   
    
- [Sky130 Day 3 - Design library cell using Magic Layout and ngspice characterization](#section-3)
  - [SKY130_D3_SK1 - Labs for CMOS inverter ngspice simulations](#subsection-31)
    - [SKY_L0 - IO placer revision](#sub-subsection-311)
    - [SKY_L1 - SPICE deck creation for CMOS inverter](#sub-subsection-312)
    - [SKY_L2 - SPICE simulation lab for CMOS inverter](#sub-subsection-313)
    - [SKY_L3 - Switching Threshold Vm](#sub-subsection-314)
    - [SKY_L4 - Static and dynamic simulation of CMOS inverter](#sub-subsection-315)
    - [SKY_L5 - Lab steps to git clone vsdstdcelldesign](#sub-subsection-316)
  - [SKY130_D3_SK2 - Inception of Layout And CMOS fabrication process](#subsection-32)
    - [SKY_L1 - Create Active regions](#sub-subsection-321)
    - [SKY_L2 - Formation of N-well and P-well](#sub-subsection-322)
    - [SKY_L3 - Formation of gate terminal](#sub-subsection-323)
    - [SKY_L4 - Lightly doped drain (LDD) formations](#sub-subsection-324)
    - [SKY_L5 - Source And drain formation](#sub-subsection-325)
    - [SKY_L6 - Local interconnect formation](#sub-subsection-326)
    - [SKY_L7 - Higher level metal formation](#sub-subsection-327)
    - [SKY_L8 - Lab introduction to Sky130 basic layers layout and LEF using inverter](#sub-subsection-328)
    - [SKY_L9 - Lab steps to create std cell layout and extract spice netlist](#sub-subsection-329) 
  - [SKY130_D3_SK3 - Sky130 Tech File Labs](#subsection-33)
    - [SKY_L1 - Lab steps to create final SPICE deck using Sky130 tech](#sub-subsection-331)
    - [SKY_L2 - Lab steps to characterize inverter using sky130 model files](#sub-subsection-332)
    - [SKY_L3 - Lab introduction to Magic tool options and DRC rules](#sub-subsection-333)
    - [SKY_L4 - Lab introduction to Sky130 pdk's and steps to download labs](#sub-subsection-334)
    - [SKY_L5 - Lab introduction to Magic and steps to load Sky130 tech-rules](#sub-subsection-335)
    - [SKY_L6 - Lab exercise to fix poly.9 error in Sky130 tech-file](#sub-subsection-336)
    - [SKY_L7 - Lab exercise to implement poly resistor spacing to diff and tap](#sub-subsection-337)
    - [SKY_L8 - Lab challenge exercise to describe DRC error as geometrical construct](#sub-subsection-338)
    - [SKY_L9 - Lab challenge to find missing or incorrect rules and fix them](#sub-subsection-339)
- [Sky130 Day 4 - Pre-layout timing analysis and importance of good clock tree](#section-4)
  - [SKY130_D4_SK1 - Timing modelling using delay tables](#subsection-41)
    - [SKY_L1 - Lab steps to convert grid info to track info](#sub-subsection-411)
    - [SKY_L2 - Lab steps to convert magic layout to std cell LEF](#sub-subsection-412)
    - [SKY_L3 - Introduction to timing libs and steps to include new cell in synthesis](#sub-subsection-413)
    - [SKY_L4 - Introduction to delay tables](#sub-subsection-414)
    - [SKY_L5 - Delay table usage Part 1](#sub-subsection-415)
    - [SKY_L6 - Delay table usage Part 2](#sub-subsection-416)
    - [SKY_L7 - Lab steps to configure synthesis settings to fix slack and include vsdinv](#sub-subsection-417)
  - [SKY130_D4_SK2 - Timing analysis with ideal clocks using openSTA](#subsection-42)
    - [SKY_L1 - Setup timing analysis and introduction to flip-flop setup time](#sub-subsection-421)
    - [SKY_L2 - Introduction to clock jitter and uncertainty](#sub-subsection-422)
    - [SKY_L3 - Lab steps to configure OpenSTA for post-synth timing analysis](#sub-subsection-423)
    - [SKY_L4 - Lab steps to optimize synthesis to reduce setup violations](#sub-subsection-424)
    - [SKY_L5 - Lab steps to do basic timing ECO](#sub-subsection-425)
  - [SKY130_D4_SK3 - Clock tree synthesis TritonCTS and signal integrity](#subsection-43)
    - [SKY_L1 - Clock tree routing and buffering using H-Tree algorithm](#sub-subsection-431)
    - [SKY_L2 - Crosstalk and clock net shielding](#sub-subsection-432)
    - [SKY_L3 - Lab steps to run CTS using TritonCTS](#sub-subsection-433)
    - [SKY_L4 - Lab steps to verify CTS runs](#sub-subsection-434)
  - [SKY130_D4_SK4 - Timing analysis with real clocks using openSTA](#subsection-44)
    - [SKY_L1 - Setup timing analysis using real clocks](#sub-subsection-441)
    - [SKY_L2 - Hold timing analysis using real clocks](#sub-subsection-442)
    - [SKY_L3 - Lab steps to analyze timing with real clocks using OpenSTA](#sub-subsection-443)
    - [SKY_L4 - Lab steps to execute OpenSTA with right timing libraries and CTS assignment](#sub-subsection-444)
    - [SKY_L5 - Lab steps to observe impact of bigger CTS buffers on setup and hold timing](#sub-subsection-445)

- [Sky130 Day 5 - Final steps for RTL2GDS using tritonRoute and openSTA](#section-5)
  - [SKY130_D5_SK1 - Routing and design rule check (DRC)](#subsection-51)
    - [SKY_L1 - Introduction to Maze Routing - Lee's algorithm](#sub-subsection-511)
    - [SKY_L2 - Lee's Algorithm conclusion](#sub-subsection-512)
    - [SKY_L3 - Design Rule Check](#sub-subsection-513)
  - [SKY130_D5_SK2 - Power Distribution Network and routing](#subsection-42)
    - [SKY_L1 - Lab steps to build power distribution network](#sub-subsection-521)
    - [SKY_L2 - Lab steps from power straps to std cell power](#sub-subsection-522)
    - [SKY_L3 - Basics of global and detail routing and configure TritonRoute](#sub-subsection-523)
  - [SKY130_D5_SK3 - TritonRoute Features](#subsection-53)
    - [SKY_L1 - TritonRoute feature 1 - Honors pre-processed route guides](#sub-subsection-531)
    - [SKY_L2 - TritonRoute Feature2 & 3 - Inter-guide connectivity and intra- & inter-layer routing](#sub-subsection-532)
    - [SKY_L3 - TritonRoute method to handle connectivity](#sub-subsection-533)
    - [SKY_L4 - Routing topology algorithm and final files list post-route](#sub-subsection-534)
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
- For Digital ASIC Design we require the following input files.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/5782eed7-afc7-411e-9f14-45ffd6780c8f)
- We can design open-source ASIC using open source RTL, EDA tools and PDK Data. RTL deigns provied mostly by github. The EDA tools are qflow, OpenROAD, OpenLANE.
 And open-source PDK provided by skywater.

![Screenshot (19)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/25303706-2f6a-4b01-99db-11048667d00b)
- PDK is process design kit provided by the foundary. There are two types of company
   - Design based or FABLESS.
   - Fabrication only
- Though companies like INTEL, SAMSUNG have both.
- PDK includes the
  - Process Design Rules : DRC , LVS , PEX
  - Device Models
  - Digital Standard Cell Libraries
  - I/O Libraries etc.
-In JUNE, 2020 GOOGLE with SKYWATER lauched *FOSS 130nm Production PDK* Opensource.

![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/6c5f4136-1b0b-46ba-a5ed-77f2d3ca1ffe)
- Now, current process technology node is 5nm, is 130nm still significant? 130nm has currently 6% market share, equivalent to *4.5 Billion Annual revenue*

![7](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/edc1bd6b-ed6f-4e14-a341-ea7f4df0e784)
____________________________________________________________________________________________________________________________________

<a name="sub-subsection-122"></a>
#### SKY_L2 - Simplified RTL2GDS flow
- Simplified ASIC design flow starts with RTL and ends with GDSII file. The steps are shown below:
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/c82a7bcb-b9e1-447c-85ff-6462dedaacc7)
- The flow starts with
     - **(1) Synthesis**: Converts RTL to GLN out of components from the standard cell libraries.
![Screenshot (20)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/2a430669-89d7-4c02-ab89-9cecb315db86)
     - **(2) Floor Planning & Power Planning**: Here we need to plan silicon area and distribute the power to the whole circuit. In macro floor planning, we define the dimensions, pin locations, rows definition.
       In power planning, the power network is constructed. The chip is powered by multiple VDD and GND. All components are connected to power supply horizontaly and vertically by metal strips.

       ![Screenshot (24)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/643cd19a-40e6-4a6c-9df8-1c749c5f41c3)
       
         ![Screenshot (25)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/9e588aa1-0423-4278-af77-6fc9441a3a32)

    - **(3) Placement**: We place the gate level netlist on the floor planning rows. It's done in 2 steps,
       - **Global placement**: Tries to find optimum positions of each cells, which are not always legal.
       
       - **Detailed placement**: In detailed placement the positions of the cells are manually altered to make them legal.
       ![Screenshot (27)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/9a42dfb9-c6cb-49ab-8bfd-fb2a77a81675)
    - **(4) Clock Tree Synthesis**: Before routing the signals, we need to route the clock. Here we need to create a clock distribution network(CDN).
      ![Screenshot (28)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/c7236811-5d95-40ea-8d9a-ad21642a5a3c)
    -  **(5) Routing**:  After routing the clock, we need to route the signals. We need horizontal and vertical wires to implement the nets to connect the cells.
      The sky130 PDK defines the 6 routing leyers.The routing grids are huge. So, devide and conquer approach is used for routing. The routing is of 2 types:
       -  **Global Routing**: Generates the routing guides.
       -  **Detailed Routing**: Uses the routing guides to implement the actual wiring.
       ![Screenshot (29)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ed83df2f-96bd-4d63-b24e-d15bf4547a4a)

    - **(5) Sign Off**: Once the routing is done, we can construct the final layout. This final layout will go under verification.
       - **Physical Verification Checks**: Design Rule Check (DRC), Layout Vs Schematic (LVS) checks.
       - **Timing Checks** : Static Timing Analysis (STA) is performed to check if there any timing violations exist.
______________________________________________________________________________________________________________________________________________

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
Some basic linux commands are listed below

      pwd : Stands for the present working directory and the command shows it's path.
      cd : Stands for change directory.
      ls -ltr: It's used for listing, and the switch ltr shows all the sub-directories and files present in the current directory.
      mkdir : Used for making a new directory.
      rm : Used to remove/delete the files.
      help : Helps to know more about any command.
      clear : Used to clear the terminal.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/88522227-70d5-4211-b8b6-b6ba9f4a99ce)

- Inside the PDK libs.ref is specific to the technology and libs.tech is specific to the tool. Tech file contains lef, lib etc. files.
.lib file contains all the timing files. tt for typical-typical, ss for slow slow and ff for fast fast.
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/92f56738-f2a7-4931-8fa8-58795ad7a4e4)
 ____________________________________________________________________________________________________________________________________________

<a name="sub-subsection-132"></a>
#### SKY_L2 - Design Preparation Step
- We open docker by typying ```docker``` in the terminal then search for flow.tcl file, then run it under interactive mode, after that openlane is launched.
![allnew1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b6fbc1ac-1453-48d8-9fc1-6689c9f25d5a)
- Then we go for the preparation step. Here merging of LEFS happens.
![allnew4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/29c98068-e773-45f9-8fd1-26290263d367)

___________________________________________________________________________________________________________________________________________
<a name="sub-subsection-133"></a>
#### SKY_L3 - Review files after design prep and run synthesis
- If we go to ```openlane/designs/picorv32a/runs/16-05_13_58 (today's date) ``` we can see results, reports, logs etc directories are created. If we go inside results directory, results regarding all steps are created.
![allnew3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/69d6e1d4-b09d-4c04-909f-a3ef699d2666)
- Once all preparations for synthesis is complete, we run ```run_synthesis``` command to perform synthesis. Upon sucess *Synthesis was sucessful* message is shown.
![allnew1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/2d6fc7a5-7f6c-4c77-af60-ff65e13eae49)

___________________________________________________________________________________________________________________________________________
<a name="sub-subsection-134"></a>
#### SKY_L4 - OpenLANE Project Git Link Description
- We can checkout OpenLANE github page, [Openlane](https://github.com/efabless/openlane)
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/2c5f640d-9134-4954-8250-a7ae11bf0599)
- The entire OpenLANE flow is shown below,
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/c4cb0733-bad7-45bb-84b3-623fae14c13e)
___________________________________________________________________________________________________________________________________________
<a name="sub-subsection-135"></a>
#### SKY_L5 - Steps to characterize synthesis results
- Once synthesis is done, We calculate the flop-ratiodefined by (No of D F-Fs) / (Total No of cells). It iss calculated to be 1613 / 14323 or 0.114 or 11.4 %
  ![a](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/1cb60ae8-4e8e-428a-ba48-4cca77b94eb4)
- Opening the reports under synthesis shows the samiliar data. 
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
![Screenshot (69)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/d72cfa2d-7513-41fa-b1cd-636beb526d94)
__________________________________________________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-214"></a>
#### SKY_L4 - Power planning
- Considering the circuit parallel to de-coupling capacitor as a black box or macro, let, this macro is repeated multiple times. Now, we have to make sure that driver to load maintains the same logic level.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/8b601b15-5680-44eb-832d-ade44ba919f5)
- Now, applying power supply, to these macros, we need to make sure that the line connecting driver and load must retain the same power.
![Screenshot (70)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/aed19462-ff2f-4405-a00a-f1207e876751)
- As the distance between the power supply and the interconnecting wire is more, there can be significant voltage drop.
- Now, the red line is a 16-bit bus. When each line may be at 0 or 1, depands on the charge on the capacitor of that particular line. When this bus is connected to an inverter, output will be inverted of that input applied. All the capacitors that were charged to 1 will be simultaneously discharged to 0 and vise-versa.
![Screenshot (72)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/13c15890-5a63-41a4-b57a-78e3b169e03a)
- When all the capacitors discharges simultaneously, ground bounce occurs.If the ground bounce exceeds noise margin level, it can enter into undefined state.
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/06024b6f-7830-4831-b66d-c755df72e844)
-  When all the capacitors charges simultaneously, voltage droop occurs. To reslove this problem there should be power supply in each line.
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/cc90e8d9-1ddf-4141-be66-1bcf0df0b71b)
- Instead power coming from a single source, if power comes from multiple supply (Vdd and Vss) lines, each block now can access power from these lines.
![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/bcc3eeee-efd7-4cee-b6f1-a1d2d2ff0efd)
- Multiple Vdd and Vss lines are used to give access power to each blocks.
![Screenshot (74)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/4705afc9-520e-40a6-b9a0-99ebf4a795da)

_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-215"></a>
#### SKY_L5 - Pin placement and logical cell placement blockage
________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-216"></a>
#### SKY_L6 - Steps to run floorplan using OpenLANE
- In the floorplan step we set the aspect ratio, the utilization factor, we place the input, output cells and the PDN.
- Now, in OpenLANE there is a readme file in the coniguration directory describing all the switches regarding each steps.
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/0af1e8bd-8e22-4046-841c-a40865770e27)
- Opening the readme file shows the switches. For example, for floorplan there is a switch named as FP_CORE_UTIL, which sets the default core utilization factor to 0.5
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a8db3dba-e871-4a3b-9570-97c6a5972e96)
- Now, if we open floorplan.tcl,we can see the default value set by the tool. For example, utilization factor default value is 50 (percent). Similarly, 'FP_IO_MODE' switch determines where the pins will be equidistant or not.
![7](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/3e90d237-f015-4a8f-ad26-3fea61628a01)
- Now if we go back to design folder and look for config.tcl file.
![8](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b199cd28-fe02-4127-9d47-d43d1a01ae4b)
 - We can see that it has the path of the netlist file and the sdc file. We have edited it to make utiliization factor = 65,No of Vertial IO pins = 4 and No of  Horizontal IO pins = 3.
![11](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/cea6755a-a192-4c8d-8b1e-e559ca0d0e0a)
- Now we can run the command run_floorplan. After sucessful run it will show message PDN generation was sucessful.
![12](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/4fcfa465-707b-4a1a-9cd3-61eb8d995ce0)



_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-217"></a>
#### SKY_L7 - Review floorplan files and steps to view floorplan
- After running floorplan, if we open config.tcl file, that exists inside runs folder, will show core utilization factor.
- If we try to run the magic tool in order to see the def file, we can run the following command

       magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
We can see magic is opened.
![layout](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/abce0af9-62ee-4fdd-8cdf-56ce56abfb4a)

_______________________________________________________________________________________________________________________________________________
<a name="sub-subsection-218"></a>
#### SKY_L8 - Review floorplan layout in Magic
- In magic, to select entire layout we press ```q+s``` and ```v``` for fit. By right and left click of mouse, we can select a partcular part of the layout. Pressing ```s``` will highlight that area.
   ![a](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/fa04429d-fb90-49b6-95ee-49ad3b7504e1)
- Now, after selecting a particular area, we can go to tkcon window and type ```what``` to know more about the selected area.
   ![b](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/7f88e53a-f1cd-474e-8706-888f0084904e)
- We can see the tapcells are used to prevent latch-up issues. Standard-cells are kept at lower left corners.
   ![c](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/4908a1af-1575-4f9b-b68b-0ee3e4b76396)


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
- In placement standard cells are placed. Placement The placement occurs in two stages. Global and detailed.
- Global placement tries reducing the length of wires. And detailed Placement legalization of the Placement happens.
- To do placement we give the command

        run_placement
- Once placement is done we can see, standard cells are placed in rows.
![last1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/849f5a33-3c7a-4e69-9796-d8393c96b240)
- Pressing ```z``` we zoom into the layout and see the standard cells placed
![last2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ef67094e-56f6-4d3d-bbdc-76edf9ff57bd)
__________________________________________________________________________________________________________________________________________________
<a name="subsection-23"></a>
### SKY130_D2_SK3 - Cell design and characterization flows
<a name="sub-subsection-231"></a>
#### SKY_L1 - Inputs for cell design flow




___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-232"></a>
#### SKY_L2 - Circuit design step


____________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-233"></a>
#### SKY_L3 - Layout design step

___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-234"></a>
#### SKY_L4 - Typical characterization flow
___________________________________________________________________________________________________________________________________________________
<a name="subsection-24"></a>
### SKY130_D2_SK4 - General timing characterization parameters
<a name="sub-subsection-241"></a>
#### SKY_L1 - Timing threshold definitions
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-242"></a>
#### SKY_L2 - Propagation delay and transition time
___________________________________________________________________________________________________________________________________________________
<a name="section-3"></a>
## Sky130 Day 3 - Design library cell using Magic Layout and ngspice characterization 
<a name="subsection-31"></a>
### SKY130_D3_SK1 - Labs for CMOS inverter ngspice simulations
<a name="sub-subsection-311"></a>
#### SKY_L0 - IO placer revision
- Till now, all the pins are placed equidistantly, if we want to change that, we need to change ```FP_IO_MODE``` value from 1 to 2. We can see pins are no longer equidistant
![a](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/1c82d751-ceb7-4a72-8173-f7404a4bdc8e)

____________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-312"></a>
#### SKY_L1 - SPICE deck creation for CMOS inverter
- To define a spice deck we start with Component connectivity where we define the connectivity of the substrate pin.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/4310e2a0-7128-4c63-9ef0-f3a6a87ac5f0)
- Then we  define the Component values  where we define the aspect ratios of the MOS and give power supply values.
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a8a0fcee-b855-4b5e-a173-0021818bcc41)
- After that we need to identify the nodes. We give name to those nodes.
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/aa3bc978-ff23-4802-a129-9d72cd95bc18)
- Now we are ready to define the spice deck for our inverter. For MOS should be connected as D G S Sub for a MOSFET.
![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a7772fbb-c72d-4533-a249-2bb899bdc759)
____________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-313"></a>
#### SKY_L2 - SPICE simulation lab for CMOS inverter
- Now, we have to define connectivities for each of the components. We are sweeping the gate input voltage from 0 to 2.5 at an interval of 0.05. We need to find the output voltage, while we sweep the input voltage.Finally, we describe the model file.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/d28b341b-47a3-41a6-beaa-2e5098dc8ac8)
- If we see the model file, it describes all the information regarding NMOS.
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/32a3df27-82b7-4cae-aea7-7ed533d1d62c)
- Similarly, we can check the entire spice netlist in the text format
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b746a70a-605b-4171-a240-b6af0e95c27c)
- Now if we try to perform simulation using NGspice, by entering following commands to get dc transfer characteristics,
![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/49e161f1-9ee4-4d99-bc85-5b592c8d8a05)
- Once simulation is is perform, a new window will pop-up showing the waveform. Here, we have considered the width of both PMOS and NMOS are same.

![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/82a37a53-c5ea-40d0-a527-d913bd31199a)
- Now, considering differnt aspect ratios for NMOS and PMOS, where PMOS witdh is 2.5 times that of the NMOS, Now, swithing threshold will get shifted.

![7](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/33524c90-aa73-4b25-b0bb-da5e2b5b8d50)

____________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-314"></a>
#### SKY_L3 - Switching Threshold Vm
- We can see, the comparitive results for both the aspect ratios of the CMOS inverter.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/dea5ab89-2a00-46a0-a2ec-eecfd00e6426)
- Switching Threshold is defined as the voltage when Vin = Vout. We can see Vm is different for two different aspect ratios.
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a1eda108-0d76-4ee9-860a-044ae36f41f6)
- At switching Threshold Vm, Vgs = Vds. Both PMOS and NMOS remain at saturation at this point.
![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/f38d139b-4072-498f-b143-81e7a479df2d)
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-315"></a>
#### SKY_L4 - Static and dynamic simulation of CMOS inverter
- For, thoretical calculation, we can make equal both the currents and solve for Vm.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/e3b5092f-9f6b-4f3f-90c5-0069db232299)
- To calculate propagation delay, we need to do transient analysis, we have to define a pulse in the netlist description for spice simulation
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/1b3d2198-06ac-48b7-aaa9-bfd9642fd01c)
- We need to plot both input and output and see 50% of output and input differnce for rise and fall delay.
![Screenshot (75)](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/33c82997-e1a7-47c1-96cd-4edfcc9b058a)
- NMOS and PMOS having the same aspect ratio, for that we have calculated the rise and fall delay.
![last](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/24cf9cec-8def-4664-afb4-72fc37724a7e)
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-316"></a>
#### SKY_L5 - Lab steps to git clone vsdstdcelldesign
- First we have clone the following repository from Github

        https://github.com/nickson-jose/vsdstdcelldesign
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/c7e0550a-c8a8-40a5-8db4-45f4e7710519)
- After copying the technology file to vsdcelldesign directory, we can type the follwing command to invoke magic to see the layout of the inverter

              magic -T sky130A.tech sky130_inv.mag &
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/4a29f896-d934-4aef-b593-364d2fdaceca)
___________________________________________________________________________________________________________________________________________________
<a name="subsection-32"></a>
### SKY130_D3_SK2 - Inception of Layout And CMOS fabrication process
<a name="sub-subsection-321"></a>
#### SKY_L1 - Create Active regions
-  We have a p-type silicon substrate(100)
  ![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/dd931a20-2806-4252-adf3-3e1f28f8f94a)
-  First the isolation layer is created by depositing the Si02 layer (~40nm) on the substrate. Then  the Si3N4 layer (~80 nm) is deposited on the Sio2 layer. Then photoresist is coated on top of the nitrite layer, for further photolithography stage. Then mask is applied to create exposed and unexposed regions. During photolithography, UV rays are used to change the chemical properties of the exposed regions.

![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/de07e496-906b-4963-903e-04e49ebbf7d9)

- Then developer's solution removes exposed region. So that we have the following structure, after that we etch Silicon Nitrite layer foe exposed region and mask is removed.
 ![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/21ea3a34-6b99-4527-84b7-2ba370f498c1)
- After that we remove the photoresist chemically and Si3N4 layer behaves as a mask. Then we  place it in the oxidation furnace. After oxidation field oxide isa grown and the process is called LOCOS, after that nitrite layer is etched in phosphoric acid. This grown sio2 will provide the  isolation between two devices. This is how field oxide works as isolation between two devices.
![12](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ebe3bf4e-1448-443f-8bba-e46f2948b1e8)
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-322"></a>
#### SKY_L2 - Formation of N-well and P-well
- We have to form P-well and N-well once at a time. We have to protect one region while forming one of the region by photoresist. And then using mask 2 and UV light, we will do patterning of photoresist to form P-well.
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-323"></a>
#### SKY_L3 - Formation of gate terminal
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-324"></a>
#### SKY_L4 - Lightly doped drain (LDD) formations
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-325"></a>
#### SKY_L5 - Source And drain formation
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-326"></a>
#### SKY_L6 - Local interconnect formation
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-327"></a>
SKY_L7 - Higher level metal formation
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-328"></a>
#### SKY_L8 - Lab introduction to Sky130 basic layers layout and LEF using inverter
- In magic we press ```s``` to select a highlighted area and in tkcon typing ```what``` gives information about that selected area

![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/6b413cce-8665-4af8-bf94-6bf1c914bc55)

___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-329"></a>
#### SKY_L9 - Lab steps to create std cell layout and extract spice netlist
- To extract the spice netlist  file from the layout, we have to write the command in tkcon window

              extract all
              ext2spice cthresh 0 rthresh 0
              ext2spice
- After that we can see the message '''exttospice finished and * sky130_inv.spice * file is generated.
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/9f8cd17b-b242-46d6-b55d-3cec10c47f73)
__________________________________________________________________________________________________________________
<a name="subsection-33"></a>
### SKY130_D3_SK3 - Sky130 Tech File Labs
<a name="sub-subsection-331"></a>
#### SKY_L1 - Lab steps to create final SPICE deck using Sky130 tech
- Once the extraction of the sky130_inv.spice file n is done, we have updated our spice netlist.
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ad4e6834-d0fc-4f0a-94c0-d4c7641f2359)

__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-332"></a>
#### SKY_L2 - Lab steps to characterize inverter using sky130 model files
- Once we run ```NgSpice``` by giving the following command, We can see the node volotages

      ngspice sky130_inv.spice
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/9babb60f-0090-4edd-ba6f-0daa011751b0)
- We can see the transcient characteristics of the inverter.
 ![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/3ce63058-88e9-4c77-8fd8-932ac748b125)
- Now, max value of voltage is 3.5 V. 20% of 3.5 is 0.66 and 80% is 2.64
- Rise transition time is the time taken by the output to rise from 20% to 80%.
       Rise transition time = (2.18-2.12) ns = 0.06 ns
- Fall transition time is time taken by output to fall from 80% to 20%
       Fall transition time = 0.04 ns
- Propagation delay is defined as the output crossing 50% to input crossing 50%
       Propagation delay = 0.002 ns

![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/eec5770f-ff77-428a-99f3-1f0c236f2f07)
___________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-333"></a>
#### SKY_L3 - Lab introduction to Magic tool options and DRC rules
- To know more about magic we can visit [magic](http://opencircuitdesign.com/magic/index.html).
- We can see in DRC section under mannual.
- To check Google/SkyWater DRC rules we can visit [SkyWater SKY130 PDK](https://skywater-pdk.readthedocs.io/en/main/rules/periphery.html).
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-334"></a>
#### SKY_L4 - Lab introduction to Sky130 pdk's and steps to download labs
- Sky130 Gihub repository [sky130 Github](https://github.com/google/skywater-pdk)
- To download the lab files for performing DRC corrections we type in terminal from home

       wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
       tar xfz drc_tests.tgz
       ls -al
       vi .magicrc
  - To start  magic tool with better graphics, we type the command

         magic -d XR &
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-335"></a>
#### SKY_L5 - Lab introduction to Magic and steps to load Sky130 tech-rules
- We use command to open magic

         magic -d XR
- We open met3.mag file from the file menu. Different layouts with different DRC values are shown, known as rule numbers.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/62fe14a6-e651-4a9b-a73f-b953e611edca)

- We can check [Skywater PDK](https://skywater-pdk.readthedocs.io/en/main/rules/periphery.html#m3) for more information.
- Now, select an area in the tool and guide the pointer on to the metal 3 layer contact and middle click mouse. The selected region will be filled with metal 3.
  After that typing ```cif see VIA2``` in tkcon, the metal 3 filled area will be filled with VIA2 mask.
  ![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/e7ce66f1-c373-4cab-824b-a196fc52cedf)


__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-336"></a>
#### SKY_L6 - Lab exercise to fix poly.9 error in Sky130 tech-file
- First we load ```poly.mag``` file into magic tool
![0](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/420b64f3-e7a4-4c39-ac38-a968784b1f5c)
- We can know more about poly from [Sky130 PDK](https://skywater-pdk.readthedocs.io/en/main/rules/periphery.html)
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/0de33176-8ac3-44af-bafc-e059bb5f0a43)
- To get the area of the selected area, we type in the tkcon window,

       box
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ea8d2bc6-f4f4-4c0c-80fb-2edbf728cf0e)
- We can check the following definition regarding poly-9
![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/87015926-fc81-4e2c-bc29-a8b7fb929cb6)
- Now we load the tech file by typing

       tech load sky130A.tech
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/64c503d2-bdf2-466f-a432-5eb554784477)
_ Now, we run command, to check if there any DRC errors present or not

     drc check
![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/175cf12a-84eb-41ba-8fec-d61b5e02b7b9)
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-337"></a>
#### SKY_L7 - Lab exercise to implement poly resistor spacing to diff and tap

__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-338"></a>
#### SKY_L8 - Lab challenge exercise to describe DRC error as geometrical construct

__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-339"></a>
#### SKY_L9 - Lab challenge to find missing or incorrect rules and fix them

__________________________________________________________________________________________________________________________________________________
<a name="section-4"></a>
## Sky130 Day 4 - Pre-layout timing analysis and importance of good clock tree
<a name="subsection-41"></a>
### SKY130_D4_SK1 - Timing modelling using delay tables
<a name="sub-subsection-411"></a>
#### SKY_L1 - Lab steps to convert grid info to track info
- We need '.lef'  file of the invverter cell to place it into the picorv32a flow,
- Now we can open the track file from ```pdk/sky130/libs.tech /openlane/sky130_fd_sc_hd/track.info``` .
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/7fce797e-6bb4-4133-b2b7-d2a717d0e37d)
- Designing standard cells, we must consider
    - The Input and output ports must lie on the intersection of the  Horizontal, vertical tracks.
 - Now, we open the tkcon window and give the  following command

         help grid
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/e9c83f5c-203b-46ce-8daf-19e1d0059b48)

- Then we type the follwing command in the tkcon window, according to the track file.

         grid  0.46um 0.34um 0.23um 0.17um
- Now both input and output ports are placed at the intersection of the tracks.  
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/c6b1936d-25e6-4d50-962e-c65ede981d70)
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-412"></a>
#### SKY_L2 - Lab steps to convert magic layout to std cell LEF
- We need to define ports assign them as input, output and inout pins . We have followed [readme.md](https://github.com/nickson-jose/vsdstdcelldesign/blob/master/README.md)
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b857d26d-96a8-4b16-9272-1b8c1bbc0883)
- After that we save our design by giving the command

      save sky130_vsdinv.mag
  And open the layou using following command

      magic -T sky130A.tech sky130_vsdinv.mag &
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/1f7f60d5-e099-48e2-adef-04bc98a7c246)
- We extract the LEF file using following command

      lef write
- We can see that ```sky130_vsdinv.lef``` file has been created.
![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/054db969-b8f7-470b-9c51-cd25241624de)
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-413"></a>
#### SKY_L3 - Introduction to timing libs and steps to include new cell in synthesis
- Now, we have to copy the ```.lef```  file ```sky130_vsdinv.lef``` to design source folder.
- After that we have to copy three ```.lib``` files Typical, Fast and Slow to our design source folder.
- Then we can edit the ```config.tcl``` file, so that  we have given path for ```.lib``` and ```.lef``` files.
  ![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a09bc842-47c4-4e69-a7ba-01904295dfc1)
- Now, we have to run ```docker``` and go though the previous design preparation steps. After that we have to give the following commands to read the ``` .lef``` file

and then run synthesis.

          set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
  
          add_lefs -src $lefs
          run_synthesis
- Once Synthesis is done, it will show that   *Synthesis was sucessful* message.
 ![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a3ea8a9e-cdf3-4cac-9a7b-248856f45eb4)
__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-414"></a>
#### SKY_L4 - Introduction to delay tables


__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-415"></a>
#### SKY_L5 - Delay table usage Part 1


__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-416"></a>
#### SKY_L6 - Delay table usage Part 2


__________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-417"></a>
#### SKY_L7 - Lab steps to configure synthesis settings to fix slack and include vsdinv
- We perform synthesis again by modifying the ```config.tcl``` file to minimize negative slack.
![config](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/e3d689b1-94ab-4db6-8034-257fdb9fe8c5)
- Then we run the following commands

  run_synthesis
  run_floorplan
- The command *run_floorplan* throws error, to rectify it we need to run_floorplan in steps

      init_floorplan
      place_io
      tap_decap_or
 ![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/d87376db-5bad-406d-b0aa-df8deff4281b)
- Once floorplan is prformed, we can then go for placement, by running the following command

        run_placement 
- Once placement is finished, we can run magic tool to see the layout by runnung the following command

      magic -T sky130A.tech lef read merged.lef def read picorv32a.placement.def &
![placed_final](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/37dd5d1a-8e9a-4da2-a88c-a8883659dbc5)
- Now, if we zoom in and look for ```sky130_vsdinv``` cell, we can see
![placed2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/5f26946d-d7a2-41ee-bf28-d153078ed5f7)
- After selecting the ```sky130_vsdinv``` cell and typing ```expand``` in the tkcon window, we can see the desired results
![placed3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/02546765-3cf0-4c24-ad64-da47a3e00f89)
__________________________________________________________________________________________________________________________________________________
<a name="subsection-42"></a>
### SKY130_D4_SK2 - Timing analysis with ideal clocks using openSTA
<a name="sub-subsection-421"></a>
#### SKY_L1 - Setup timing analysis and introduction to flip-flop setup time


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-422"></a>
#### SKY_L2 - Introduction to clock jitter and uncertainty


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-423"></a>
#### SKY_L3 - Lab steps to configure OpenSTA for post-synth timing analysis
- To run STA, first we create a ```pre_sta.conf``` file of the following specifications
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/d9220898-6c3c-4c1b-a549-52012537a6ff)
- Then we go to repository [extras](https://github.com/nickson-jose/vsdstdcelldesign/tree/master/extras) to get the ```my_base.sdc``` file and do the following changes
![4](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b1f2a82a-d7ab-49ed-9b0d-e0e97fa9cc96)
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-424"></a>
#### SKY_L4 - Lab steps to optimize synthesis to reduce setup violations
- To reduce negative slack, we re-run synthesis, by giving the following command

        set  ::env(SYNTH_MAX_FANOUT) 4
![config](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/24483343-5e5d-4e77-a94d-55ad8a846d0e)
- To perform STA, we go to the OpenLANE directory and run the following command

           sta pre_sta.conf
![before](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/752e6d62-3ec2-45e4-8a73-825c7fe64ccf)
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-425"></a>
#### SKY_L5 - Lab steps to do basic timing ECO
- To minimize negative slack further, we try to replace the buffers with smaller drive strengths by buffers with larger drive strengths.
- We had slack
![before](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/11a13b4a-988d-429e-95f2-8693ab332b2b)
- To replace the buffers, we run the following commands

      report_net -connections _12536_
      replace_cell _13528_ sky130_fd_sc_hd__buf_8
      report_checks -fields {net cap slew input_pins} -digits 4
- After replacement of the buffer we have reduced the negative slack
![after](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ce6b5db2-28bf-4da2-978d-1ff11f1b0d9d)
- We perform this steps multiple times so that the negative slack is reduced.
-  We have to perform this step iteratively, we can see the slack has met
![finally](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/1cc451db-0cee-4c30-aa3d-c56c725df7e2)

_________________________________________________________________________________________________________________________________________________
<a name="subsection-43"></a>
### SKY130_D4_SK3 - Clock tree synthesis TritonCTS and signal integrity
<a name="sub-subsection-431"></a>
#### SKY_L1 - Clock tree routing and buffering using H-Tree algorithm


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-432"></a>
#### SKY_L2 - Crosstalk and clock net shielding


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-433"></a>
#### SKY_L3 - Lab steps to run CTS using TritonCTS
- Now, we have to replace exisiting gate-level-netlist existing in the ```results/synthesis``` directory. By giving the following command in OpenSTA

      write_verilog /home/vsduser/desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/21-05_07-43/results/synthesis/picorv32a.synthesis.v
- We again run STA and try minimizing the negative slack.
- We run cts by giving the following command

      run_cts
- Once cts is performed we run the following commands

![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/5bb355e7-b682-46c8-89fa-1cab511dde42)
- Then we again run STA inside the OpenLANE itself and give the following commands
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/1174f4b7-f47d-4d81-bbcb-71f615cdcb6b)

_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-434"></a>
#### SKY_L4 - Lab steps to verify CTS runs
- If we go to scripts directory under openlane directory, we can see that there are different script files existing for different steps
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/a095a1b1-88e6-407c-a6e7-9f31fcaa9add)
- After sucessful ```cts``` run, we can see that our ```DEF``` file is updated
![cts](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/c9f3133c-13b9-4094-b825-6754e995784c)
______________________________________________________________________________________________________________________________
<a name="subsection-44"></a>
### SKY130_D4_SK4 - Timing analysis with real clocks using openSTA
<a name="sub-subsection-441"></a>
#### SKY_L1 - Setup timing analysis using real clocks


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-442"></a>
#### SKY_L2 - Hold timing analysis using real clocks


_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-443"></a>
#### SKY_L3 - Lab steps to analyze timing with real clocks using OpenSTA
- To run STA with real clocks with ```OpenSTA```, we invoke ```OpenROAD``` inside ```OpenLANE``` and load the ```.lef``` and ```.def``` files to create ```pico_cts.db``` file.
![3](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b83f9bc3-3269-4ea1-8b4e-5b1337fefb02)
- Now, we read the ```pico_cts.db``` file, ```picorv32a.synthesis.v``` file, and differnt library files, ```my_base.sdc``` file and again perform STA
![5](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/84ee3343-c2b3-4183-9b67-d472b183bbf0)
- We can see the slack reult
![6](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/276847d7-d898-4652-bff6-3535fca868df)
- Here, we can check that HOLD time violation has occured. We need to fix that in routing stage
![7hold viol](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/ac679f6b-68f7-4fe0-a35c-5868c5c2a0aa)

_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-444"></a>
#### SKY_L4 - Lab steps to execute OpenSTA with right timing libraries and CTS assignment
 - Now, we have performed synthesis using typical library, so we need to again perform the previous step by reading the typical library.
![1](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/04d0a017-46f8-4cf9-8cdc-edf28ae0f90e)
- We have closed OpenLANE and relaunched it, again we perform ```CTS```.
![2](https://github.com/ratulparui/Digital_VLSI_SoC_Design_And_Planning/assets/154420885/b497f68f-78c6-4acb-89cc-34b5c808e7b5)
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-445"></a>
#### SKY_L5 - Lab steps to observe impact of bigger CTS buffers on setup and hold timing
- We have seen the CTS results for buffers of size 8, now if we want we can revert back and add the buffers of size 1 and again re-run ```cts```.

_________________________________________________________________________________________________________________________________________________
<a name="section-5"></a>
## Sky130 Day 5 - Final steps for RTL2GDS using tritonRoute and openSTA
<a name="subsection-51"></a>
### SKY130_D5_SK1 - Routing and design rule check (DRC)
<a name="sub-subsection-511"></a>
#### SKY_L1 - Introduction to Maze Routing - Lee's algorithm
    
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-512"></a>
#### SKY_L2 - Lee's Algorithm conclusion
    
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-513"></a>
#### SKY_L3 - Design Rule Check
    
_________________________________________________________________________________________________________________________________________________
<a name="subsection-52"></a>
### SKY130_D5_SK2 - Power Distribution Network and routing
<a name="sub-subsection-521"></a>
#### SKY_L1 - Lab steps to build power distribution network
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-522"></a>
#### SKY_L2 - Lab steps from power straps to std cell power
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-523"></a>
#### SKY_L3 - Basics of global and detail routing and configure TritonRoute
_________________________________________________________________________________________________________________________________________________
<a name="subsection-53"></a>
### SKY130_D5_SK3 - TritonRoute Features
<a name="sub-subsection-531"></a>
#### SKY_L1 - TritonRoute feature 1 - Honors pre-processed route guides
_________________________________________________________________________________________________________________________________________________
<a name="sub-subsection-532"></a>
#### SKY_L2 - TritonRoute Feature2 & 3 - Inter-guide connectivity and intra- & inter-layer routing
_________________________________________________________________________________________________________________________________________________

<a name="sub-subsection-533"></a>
#### SKY_L3 - TritonRoute method to handle connectivity
_________________________________________________________________________________________________________________________________________________

<a name="sub-subsection-534"></a>
#### SKY_L4 - Routing topology algorithm and final files list post-route
_________________________________________________________________________________________________________________________________________________


