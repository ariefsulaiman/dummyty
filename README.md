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

</details>
