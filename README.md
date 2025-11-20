# Home Automation Current Sense Board

This repository holds the complete KiCad project files for a two-layer PCB designed to monitor AC current flow, suitable for integration into a home automation system.

## 📐 Project Overview

The board implements a four-stage signal conditioning circuit to safely measure and process high AC current (up to 30A) and output a standardized, proportional voltage signal (VOUT) compatible with microcontrollers (0V to 3.3V).

## ⚙️ Key Components and Function

| Component | Function | Details |
| :--- | :--- | :--- |
| **U1 (ACS712)** | **Current Sensor** | [cite_start]Hall Effect sensor capable of measuring up to 30A AC[cite: 89]. [cite_start]Provides a raw voltage output proportional to current flow (max 1.98V)[cite: 68]. |
| **U2 (MCP6002)** | **Op-Amps** | [cite_start]Dual Rail-to-Rail Op-Amp[cite: 92]. Used for buffering (U2A) and amplification (U2B). |
| **U2B Amplifier** | **Signal Scaling** | [cite_start]Configured for a gain of 1.66 to scale the sensor's maximum 1.98V output to the desired **3.3V** maximum VOUT[cite: 83, 85]. |
| **Copper Zone** | **GND Plane** | A large copper pour on the bottom layer ensures a robust, low-impedance ground return path, crucial for minimizing noise in analog sensing circuits. |

## ✅ Design Status

* **Routing:** 100% complete two-layer routing.
* **DRC Validation:** Passed all critical Design Rules Checks (DRC). All electrical connections are complete and all clearances are met.
* **Silkscreen:** Silkscreen warnings (clipping) resolved, ensuring clear component assembly markings.

