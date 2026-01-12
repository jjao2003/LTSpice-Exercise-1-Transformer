# LTSpice Exercise 1: Transformer & Rectifier Simulation

## 📌 Project Overview
This repository contains an LTSpice simulation of a step-down transformer circuit used for basic AC-to-DC conversion. It features a half-wave rectifier and a capacitive filter to smooth the output voltage.

## ⚡ Circuit Specifications
The circuit is designed with the following parameters:

### Input Source (V1)
* [cite_start]**Waveform:** Sine wave [cite: 1, 2]
* [cite_start]**Amplitude:** 311V Peak (~220V RMS) [cite: 1, 2]
* [cite_start]**Frequency:** 50 Hz [cite: 1, 2]
* [cite_start]**Series Resistance:** 0.1 Ω [cite: 1, 2]

### Transformer (L1, L2, k1)
* [cite_start]**Primary Inductance (L1):** 8100µH [cite: 1, 2]
* [cite_start]**Secondary Inductance (L2):** 100µH [cite: 1, 2]
* [cite_start]**Coupling Coefficient (k1):** 1.0 (Ideal) [cite: 1, 3]
* **Turns Ratio:** Calculated as $N = \sqrt{L1 / L2} = 9:1$

### Output Stage
* [cite_start]**Diode (D1):** Power Diode [cite: 1, 2]
* [cite_start]**Filter Capacitor (C1):** 1000µF [cite: 1, 2]
* [cite_start]**Load Resistor (R1):** 100 Ω [cite: 1, 2]

## 📊 Simulation Results
[cite_start]The simulation runs for 100ms using the `.tran 100m` command[cite: 1, 3]. 

![Circuit Waveform](waveform_screenshot.png)
[cite_start]*Figure 1: Comparison of Input Voltage (Blue) vs. Filtered Output Voltage (Green).*

### Initial Conditions
To observe the natural startup of the circuit, the following initial conditions were set to zero:
* [cite_start]`V(out) = 0` [cite: 1]
* [cite_start]`I(L1) = 0` [cite: 1]
* [cite_start]`I(L2) = 0` [cite: 1]

## 🚀 How to Run the Simulation
1. Install [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html).
2. Download the `LTSpice_Exercise1_Transformer.asc` file from this repo.
3. Open the file in LTSpice and click the **Run** (Running Man) icon.
4. Probe the nodes to see the transformation and rectification in real-time.
