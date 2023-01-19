# dummyty

## Day 12 -  VSDBabySoC Modelling

<details>
<summary>Theory</summary>

**Modelling in electroinic**
- The use of a physical or logical representation of a given system to create data and assist decide decisions or make predictions about the system is known as modelling and simulation.
- Models are representations that may be used to help define, analyse, and communicate a collection of concepts.
- The purpose of modelling including:
  - support analysis, specification,
  - design,
  - verification,
  - validation of a system,
  - and communicate certain information.
- In this session we will modelling VSDBabySoC.

**VSDBabySoc Modelling**
- Some initial input signals will be fed into vsdbabysoc module.
- Pll will start generating the proper CLK for the circuit. and  clock signal will make the rvmyth to execute instructions and some values are generated.
- These values then are used by DAC core to provide the final output signal named OUT.
- There  3 main elements (IP cores) and a wrapper as an SoC in this training.

**RVMYTH - Risc-V based MYTH**
- RISC is an abbreviation for Reduced instruction set computer. 
- The term **"ISA" (Instruction Set Architecture)** refers to a basic integer ISA that must be included in every implementation, as well as optional extensions to the base ISA. 
- The width of the integer registers and the associated size of the address space, as well as the number of integer registers, distinguish each base integer instruction set. RV32I and RV64I are the two basic base integer versions.

**A simple one cycle CPU**
![image](https://user-images.githubusercontent.com/118953928/210686265-32cc3ada-51b9-4850-8232-abc1765d60a0.png)

 **Phase Locked Loop**
- A phase-locked loop (PLL) is an electrical circuit that has a voltage or voltage-driven oscillator that continually changes its frequency to match the frequency of an input signal. 
- PLLs are used to create, maintain, modulate, and demodulate signals, including other things.
- The clock will provide several blocks on the chip, and it will have delays because to lengthy connections (if just one clock source is utilised).
- Some blocks may require 200Mhz, while others may require 100Mhz - the idea is that various frequencies may exist on a same tiny chip.
- A ppm (clock accuracy) idea is introduced; whenever quartz is obtained, it comes with an x ppm error.
- The accuracy of a crystal clock is expressed in units of ppm, or parts per million, and it provides a handy manner of comparing the accuracies of different crystal standards.
- A common microcontroller crystal has a 100ppm standard (every day inaccuracy of 8.6s).
- A watch crystal has an inaccuracy of 20ppm, however this equates to 20/1e6 (2e-5) which produces an error over a day of 86400 * 2e-5 = 1.73 seconds each day, 
- thus in a month it loses 30x1.72 = 51 seconds or error rate per day: 1.73 seconds.

**Digital-to-Analog Converter**
- A DAC is a device that transforms a digital input signal to an analogue output signal. 
- A binary code, which is a combination of bits 0 and 1, is used to represent a digital signal. 
- A Digital to Analog Converter (DAC) has several binary inputs and a single output. 
- In general, a DAC's number of binary inputs will be a power of two.
- DACs are classified into two types: R-2R Ladder DAC with Weighted Resistor DAC

</details>

## Day 17 - Design and characterise one library cell using Layout tool and spice simulator
 
### Labs for CMOS inverter ngspice simulations

<details>
<summary>Utilization factor and aspect ratio</summary>

![Slide4](https://user-images.githubusercontent.com/118953928/213086268-1d085c92-b552-4b7e-8163-79c7320b087e.JPG)
![Slide5](https://user-images.githubusercontent.com/118953928/213086271-fc6dab65-c120-457c-b33b-f4e8f98f59cd.JPG)
![Slide6](https://user-images.githubusercontent.com/118953928/213086277-0f29fe77-8b47-40e8-9e3e-f4aacdf542af.JPG)
![Slide7](https://user-images.githubusercontent.com/118953928/213086289-6425e396-8435-435d-b3d2-147978211cfd.JPG)
![Slide8](https://user-images.githubusercontent.com/118953928/213086296-5b5bea8b-8859-4406-9359-34b262d57d49.JPG)
![Slide9](https://user-images.githubusercontent.com/118953928/213086311-5bcd56bb-dd38-4898-9476-95a3f7b940c6.JPG)
</details>
	
<details>
<summary>Concept of pre-placed cells</summary>

![Slide11](https://user-images.githubusercontent.com/118953928/213086348-597ab457-b024-41fb-8b4a-8780bf310bc5.JPG)
![Slide12](https://user-images.githubusercontent.com/118953928/213086351-622a6646-4535-4c6b-82b9-6fd193117b5a.JPG)
![Slide13](https://user-images.githubusercontent.com/118953928/213086352-85c6113d-3132-4b14-9ea2-717481055dc4.JPG)
![Slide14](https://user-images.githubusercontent.com/118953928/213086353-d777c367-aafa-4662-b4d9-1cf95e72d57f.JPG)
</details>
	
<details>
<summary>De-coupling capacitors</summary>

![Slide16](https://user-images.githubusercontent.com/118953928/213086402-2e144505-2494-4ead-85c5-bd3449a339d5.JPG)
![Slide17](https://user-images.githubusercontent.com/118953928/213086411-d4de27f3-2ac2-4fcf-9810-614ef864b7cb.JPG)
![Slide18](https://user-images.githubusercontent.com/118953928/213086414-20184613-6d78-401c-9cdf-2ac4780bb5e2.JPG)
![Slide19](https://user-images.githubusercontent.com/118953928/213086416-9c6af726-0335-47f8-b137-9e939fa5bcd2.JPG)
![Slide20](https://user-images.githubusercontent.com/118953928/213086418-5054d46e-6c2e-4c53-8d72-fc03b3ea5479.JPG)
</details>

<details>
<summary>Power planning</summary>

![Slide22](https://user-images.githubusercontent.com/118953928/213086450-0c928a76-a3ff-4123-96e9-04de79f0f762.JPG)
![Slide23](https://user-images.githubusercontent.com/118953928/213086459-bd402fd9-3fc8-4f84-a663-b1aff9faf423.JPG)
</details>

<details>
<summary>Pin placement and logical cell placement blockage</summary>

![Slide25](https://user-images.githubusercontent.com/118953928/213086485-482f1369-d3f2-44f4-9b07-491b25e16515.JPG)
</details>

<details>
<summary>Steps to run floorplan using OpenLANE</summary>

![Slide27](https://user-images.githubusercontent.com/118953928/213086577-f2381ef4-c56d-459c-8879-e3837e70b9af.JPG)
![Slide28](https://user-images.githubusercontent.com/118953928/213086582-5a0b4ed4-cea2-46f3-a9ba-ce716c2757d7.JPG)
![Slide29](https://user-images.githubusercontent.com/118953928/213086587-3c26c48c-c4da-48b2-92a5-b6164c816e9f.JPG)
</details>

<details>
<summary>Review floorplan files and steps to view floorplan</summary>

![Slide31](https://user-images.githubusercontent.com/118953928/213086651-5005d8d7-65b9-4a43-ae25-a4dfcfc5f08e.JPG)
![Slide32](https://user-images.githubusercontent.com/118953928/213086658-ac52d767-7cef-4c5a-9752-8b8eeb849dab.JPG)
![Slide33](https://user-images.githubusercontent.com/118953928/213086660-12a9d148-978b-43f3-9919-703ad9ddc217.JPG)
![Slide34](https://user-images.githubusercontent.com/118953928/213086665-5ee16373-f151-4558-815a-17f8b196ce2d.JPG)
</details>

<details>
<summary>Review floorplan layout in Magic</summary>

![Slide36](https://user-images.githubusercontent.com/118953928/213086672-e1417034-5b1f-420e-b360-2acd61146c3d.JPG)
![Slide37](https://user-images.githubusercontent.com/118953928/213086675-05c4af67-7785-4e12-a2d3-c4e548ab4464.JPG)
</details>

###  Library Binding and Placement
	
<details>
<summary>Netlist binding and initial place design</summary>

![Slide3](https://user-images.githubusercontent.com/118953928/213139036-6c01f64d-d08d-4517-a766-6c8d32701a8c.JPG)
![Slide4](https://user-images.githubusercontent.com/118953928/213139046-eb113470-1026-4c25-94e1-af9fec8b13c3.JPG)
![Slide5](https://user-images.githubusercontent.com/118953928/213139051-2b026853-5aa1-40b5-989a-5655dfda7493.JPG)
![Slide6](https://user-images.githubusercontent.com/118953928/213139057-c7d08586-96cc-405c-a868-c028a13e35f6.JPG)
![Slide7](https://user-images.githubusercontent.com/118953928/213139059-35306ef5-e051-48f5-8061-ae64f2346de8.JPG)
</details>
	
<details>
<summary>Optimize placement using estimated wire-length and capacitance</summary>

![Slide9](https://user-images.githubusercontent.com/118953928/213139115-ee95d099-f21d-485d-bbfb-c9fb54322c8a.JPG)
</details>
	
<details>
<summary>Final placement optimization</summary>

![Slide11](https://user-images.githubusercontent.com/118953928/213139207-5c7ef283-150d-48a5-b1bf-8b3df1bff392.JPG)
</details>

<details>
<summary>Need for libraries and characterization</summary>

![Slide13](https://user-images.githubusercontent.com/118953928/213139269-7d833fe9-5fb9-4287-82b6-6a98f53e44a6.JPG)
</details>

<details>
<summary>Congestion aware placement using RePlAcee</summary>

![Slide15](https://user-images.githubusercontent.com/118953928/213139357-66e2b225-a3cc-4104-812f-7cb6974d4a6d.JPG)
![Slide16](https://user-images.githubusercontent.com/118953928/213139369-791b81b3-4fb5-4b09-9474-af886f6de189.JPG)
</details>

## Day 17 - Design and characterise one library cell using Layout tool and spice simulator

###  Cell design and characterization flows
	
<details>
<summary>IO placer revision</summary>

content
</details>
	
<details>
<summary>SPICE deck creation for CMOS inverter</summary>

content
</details>
	
<details>
<summary>SPICE simulation lab for CMOS inverter</summary>

content
</details>

<details>
<summary>Switching Threshold Vm</summary>

content
</details>

<details>
<summary>Static and dynamic simulation of CMOS inverter</summary>

content
</details>

<details>
<summary>Steps to run floorplan using OpenLANE</summary>

content
</details>
	
<details>
<summary>Review floorplan files and steps to view floorplan</summary>

content
</details>
	
<details>
<summary>Lab steps to git clone vsdstdcelldesign</summary>

content
</details>

###  Inception of Layout & CMOS fabrication process

<details>
<summary>Create Active regions</summary>

content
</details>
	
<details>
<summary>Formation of N-well and P-well</summary>

content
</details>
	
<details>
<summary>Formation of gate terminal</summary>

content
</details>

<details>
<summary>Lightly doped drain (LDD) formation</summary>

content
</details>

<details>
<summary>Source & drain formation</summary>

content
</details>

<details>
<summary>Local interconnect formation</summary>

content
</details>
	
<details>
<summary>Higher level metal formation</summary>

content
</details>
	
<details>
<summary>Lab introduction to Sky130 basic layers layout and LEF using inverter</summary>

content
</details>

<details>
<summary>Lab steps to create std cell layout and extract spice netlist</summary>

content
</details>


### Cell design and characterization flows
	
<details>
<summary>Lab steps to create final SPICE deck using Sky130 tech</summary>

content
</details>
	
<details>
<summary>Lab steps to characterize inverter using sky130 model files</summary>

content
</details>
	
<details>
<summary>Lab introduction to Magic tool options and DRC rules</summary>

content
</details>

<details>
<summary>Lab introduction to Sky130 pdk's and steps to download labs</summary>

content
</details>

<details>
<summary>Lab introduction to Magic and steps to load Sky130 tech-rulesn</summary>

content
</details>

<details>
<summary>Lab exercise to fix poly.9 error in Sky130 tech-file</summary>

content
</details>
	
<details>
<summary>Lab exercise to implement poly resistor spacing to diff and tap</summary>

content
</details>
	
<details>
<summary>Lab challenge exercise to describe DRC error as geometrical construct</summary>

content
</details>

<details>
<summary>Lab challenge to find missing or incorrect rules and fix themt</summary>

content
</details>

