 Bandgap Reference Circuit (BGR) — GPDK090

This project implements a Bandgap Reference Circuit (BGR) using the GPDK090 PDK on Cadence Virtuoso. The bandgap reference is designed to produce a temperature-stable output voltage close to 1.2 V, targeting a tempco of approximately 154 ppm/°C without trimming.

  Project Overview

Technology: 90nm GPDK (gpdk090)  
Tools: Cadence Virtuoso, Spectre (ADE), ADEL/ADXL  
Simulation Type: DC and Temperature sweep  
Design Style: Custom schematic and testbench  
Transistors: Bipolar NPN-based PTAT/CTAT core  
Op-Amp: Off-the-shelf opamp from analogLib (custom OTA planned)

  Contents

brefsch/ — Schematic of the bandgap reference  
brefsymbol/ — Symbol for hierarchical use  
brefsch_tb/ — Testbench for DC and temperature simulation  
simulation/ — Spectre simulation outputs  
docs/ — Screenshots of performance curves (optional)

  Key Results

| Metric              | Value                   |
|---------------------|-------------------------|
| Vref                | ~1.2 V                  |
| Tempco              | ~154 ppm/°C             |
| ΔVref               | ~12 mV (27°C to 92°C)   |
| Power Supply        | 1.8 V                   |

  Learnings

Temperature-compensated reference design using BJT  
Use of PTAT and CTAT voltage summation  
Integration of op-amp feedback for gain stability  
Temperature sweep simulations in ADEL/ADXL  
Analysis of Vref flatness and deviation

  How to Use

1. Clone this repository.
2. Add the library to your Cadence Library Manager.
3. Open `brefsch` schematic to view or modify the design.
4. Use `brefsch_tb` to simulate DC and temperature characteristics in ADEL.

  To-Do

Replace analogLib opamp with custom 2-stage OTA  
Layout, DRC/LVS, and RCX  
GDS Export and documentation

  License

This project is licensed under the MIT License.
