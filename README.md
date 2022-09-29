# Mixed Signal Circuit Design and Simulation Marathon

# 4-Bit Asynchronous Up Counter using Mixed Signal

- [Abstract](#abstract)
- [Reference Circuit Diagram](#reference-circuit-diagram)
- [Reference Waveform](#reference-waveform)
- [Circuit Details](#circuit-details)
- [Truth Table](#truth-table)
- [Software Used](#software-used)
  - [eSim](#esim)
  - [NgSpice](#ngspice)
  - [Makerchip](#makerchip)
  - [Verilator](#verilator)
- [Circuit Diagram in eSim](#circuit-diagram-in-esim)
- [Verilog Code](#verilog-code)
- [Makerchip](#makerchip-1)
- [Makerchip Plots](#makerchip-plots)
- [Netlists](#netlists)
- [NgSpice Plots](#ngspice-plots)
- [GAW Plots](#gaw-plots)
- [Steps to run generate NgVeri Model](#steps-to-run-generate-ngveri-model)
- [Steps to run this project](#steps-to-run-this-project)
- [References](#references)
- [Acknowlegdements](#acknowlegdements)
- [Author](#author)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## Abstract

In recent years, asynchronous counters have gained
popularity due to their low power consumption and low noise
emissions. Furthermore, they are used as frequency dividers,
as divide-by-N counters. This project involves designing a 4-bit
asynchronous up counter. The circuit will consist of T flip-flops,
a multivibrator and an Analog to Digital Converter (ADC), used
as an interface between digital and analog signal. The emphasis
of the project is to design a mixed signal circuit of a 4-bit
asynchronous up counter. The T flip-flops are for designing a
digital circuit written in Verilog and the multivibrator is for
designing an analog circuit

## Reference Circuit Diagram

![image]()

## Reference Waveform

![image]()

## Circuit Details

A 4-bit Asynchronous up counter contains four T flip-flops
(digital block) and a multivibrator (analog block) as shown
in Reference Circuit Diagram. It counts from 0 to 2 <sup>4</sup> -1, i.e. 15. All flip-flops
have their T-input connected to 1. In each flip-flop, the output
changes asynchronously on the negative edges of its clocks. In
the first T flip-flop, the clock signal is directly applied, which
is a multivibrator signal converted to digital by ADC. When
the clock signal is on a negative edge, the output of the first
T flip-flop toggles. A second T flip-flop is controlled by the
output of the first T flip-flop. Thus, every negative edge of the
output of the first T flip-flop toggles the output of the second
T flip-flop. In the same way, the third and fourth T flip-flops
toggle for every negative edge of clock of the second and third
T flip-flops, respectively
</br>
In the case of T flip-flops, assume the initial status from
rightmost to leftmost is Q3Q2Q1Q0=0000. Here, Q3 & Q0 are
MSB & LSB respectively. In Reference Waveform, we can see the output
waveforms of Q0, Q1, Q2, and Q3, and the working of the
4-bit asynchronous up counter is described in Truth Table.

## Truth Table

| No of negative edge of Clock | Q<sub>0</sub> (LSB) | Q<sub>1</sub> | Q<sub>2</sub> | Q<sub>3</sub> (MSB) |
| ---------------------------- | ------------------- | ------------- | ------------- | ------------------- |
| 0                            | 0                   | 0             | 0             | 0                   |
| 1                            | 1                   | 0             | 0             | 0                   |
| 2                            | 0                   | 1             | 0             | 0                   |
| 3                            | 1                   | 1             | 0             | 0                   |
| 4                            | 0                   | 0             | 1             | 0                   |
| 5                            | 1                   | 0             | 1             | 0                   |
| 6                            | 0                   | 1             | 1             | 0                   |
| 7                            | 1                   | 1             | 1             | 0                   |
| 8                            | 0                   | 0             | 0             | 1                   |
| 9                            | 1                   | 0             | 0             | 1                   |
| 10                           | 0                   | 1             | 0             | 1                   |
| 11                           | 1                   | 1             | 0             | 1                   |
| 12                           | 0                   | 0             | 1             | 1                   |
| 13                           | 1                   | 0             | 1             | 1                   |
| 14                           | 0                   | 1             | 1             | 1                   |
| 15                           | 1                   | 1             | 1             | 1                   |
| 16                           | 0                   | 0             | 0             | 0                   |

## Software Used

### eSim

It is an Open Source EDA developed by FOSSEE, IIT Bombay. It is used for electronic circuit simulation. It is made by the combination of two software namely NgSpice and KiCAD.
</br>
For more details refer:
</br>
https://esim.fossee.in/home

### NgSpice

It is an Open Source Software for Spice Simulations. For more details refer:
</br>
http://ngspice.sourceforge.net/docs.html

### Makerchip

It is an Online Web Browser IDE for Verilog/System-verilog/TL-Verilog Simulation. Refer
</br> https://www.makerchip.com/

### Verilator

It is a tool which converts Verilog code to C++ objects. Refer:
https://www.veripool.org/verilator/

## Circuit Diagram in eSim

The following is the schematic in eSim:
![image]()

## Verilog Code

![image]()

## Makerchip

```

```

## Makerchip Plots

![image]()

## Netlists

![image]()

## NgSpice Plots

![image]()

## GAW Plots

![image]()

## Steps to run generate NgVeri Model

1. Open eSim
2. Run NgVeri-Makerchip
3. Add top level verilog file in Makerchip Tab
4. Click on NgVeri tab
5. Add dependency files
6. Click on Run Verilog to NgSpice Converter
7. Debug if any errors
8. Model created successfully

## Steps to run this project

1. Open a new terminal
2. Clone this project using the following command:</br>
   `git clone https://github.com/syedimaduddin/4-bit_Asynchronous_Counter_using_Mixed-Signal.git`</br>
3. Change directory:</br>
   `cd eSim Project Files/`</br>
4. Run ngspice:</br>
   `ngspice file_name.cir.out`</br>
5. To run the project in eSim:

- Run eSim</br>
- Load the project</br>
- Open eeSchema</br>

## References

1. Digital Electronics: 4 Bit Asynchronous Up Counter, Neso Academy, https://www.youtube.com/watch?v=eEeBh8jfDjg
2. LTspice tutorial 13 : Design and simulation of multivibrator circuit using op-amp, Circuit Generator, https://youtu.be/Zch8gf0l-sI

## Acknowlegdements

1. FOSSEE, IIT Bombay
2. Steve Hoover, Founder, Redwood EDA
3. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com
4. Sumanto Kar, eSim Team, FOSSEE

# Author

[Syed Imaduddin](https://github.com/syedimaduddin), B.Tech Electronics Engineering, Zakir Husain College of Engineering and Technology (ZHCET), Aligarh Muslim University(AMU), Aligarh.