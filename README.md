# CMOS Mini-Project: Sawtooth Signal Generation

## Overview
This project implements a CMOS-based circuit to generate a sawtooth waveform with a period of **40ns** and a voltage range from **0.1V to 2.2V**. The design allows for digital control of the signal using a 3-bit input and voltage-controlled frequency modulation.

## Implementation Details
1. **Circuit Design**:
   - Designed the circuit using **LTSpice**, incorporating PMOS and NMOS transistors from the **library.mod** file provided.
   - Configured the circuit to operate within the specified constraints (minimum transistor length of 0.35µm, width of 0.4µm).

2. **Frequency Control**:
   - Implemented a voltage-controlled frequency modulation using an **Operational Transconductance Amplifier (OTA)**.
   - Ensured the input voltage linearly controls the sawtooth frequency without affecting the output voltage range.

3. **Digital Input Control**:
   - Set up the circuit to accept a **3-bit digital input**, allowing the generation of 0 to 7 sawtooth "teeth" for each incoming pulse.
   - The digital signal determines the number of cycles, and the circuit holds the output low after the specified number of cycles.

## Usage
- Include the `library.mod` file in your LTSpice project directory and add the directive:
   ```spice
   .inc library.mod
