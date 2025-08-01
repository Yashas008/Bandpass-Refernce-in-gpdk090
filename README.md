# Bandgap Reference Circuit (BGR) — GPDK090

This project implements a Bandgap Reference Circuit (BGR) using the GPDK090 PDK on Cadence Virtuoso. The bandgap reference is designed to produce a temperature-stable output voltage close to 1.2 V, targeting a tempco of approximately 154 ppm/°C without trimming.

## Project Overview

Technology: 90nm GPDK (gpdk090)  
Tools: Cadence Virtuoso, Spectre (ADE), ADEL or ADXL  
Simulation Type: DC and temperature sweep  
Design Style: Custom schematic and testbench  
Transistors: Bipolar NPN-based PTAT and CTAT core  
Op-Amp: Off-the-shelf opamp from analogLib (custom OTA planned)

## Contents

brefsch/ — Schematic of the bandgap reference  
brefsymbol/ — Symbol for hierarchical use  
brefsch_tb/ — Testbench for DC and temperature simulation  
simulation/ — Spectre simulation outputs  
docs/ — Screenshots of performance curves (optional)

## Key Results

| Metric              | Value                   |
|---------------------|-------------------------|
| Vref                | Approximately 1.2 V     |
| Tempco              | Approximately 154 ppm/°C |
| Delta Vref          | Approximately 12 mV (27°C to 92°C) |
| Power Supply        | 2 V                     |

## Learnings

Temperature-compensated reference design using BJT  
Use of PTAT and CTAT voltage summation  
Integration of op-amp feedback for gain stability  
Temperature sweep simulations in ADEL or ADXL  
Analysis of Vref flatness and deviation

