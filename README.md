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
