# EDC  
Implementation of Embedded Dense Coding using Qiskit and IBM Quantum Computers.

---

## Overview

**Dense Coding** is a quantum communication protocol that allows the transmission of **two classical bits using only one qubit**, made possible through the prior sharing of entangled states. This project extends traditional dense coding by embedding it into a logical multi-qubit framework, allowing a **higher density of classical information** to be transmitted per logical qudit.

This embedded dense coding scheme aims to:
- Encode classical data using entangled logical states
- Interface embedded systems with quantum simulators or real hardware
- Compare error rates between standard dense coding schemes and embedded protocols
- Use IBM Quantum hardware to validate our theoretical and simulation-based predictions

---

## Key Features

-  Implementation of the dense coding protocol using unitary operations, measurements, and classical decoding
-  Use of embedded systems by constructing **logical qudits from multiple qubits** (due to Qiskit's lack of native high-dimensional qudit support)
-  Simulation and testing using Qiskit, with optional extension to QuTiP
-  Classical-to-quantum signal encoding that supports either real-time or simulated interaction

---

## Write-Up

In our approach to **embedded dense coding**, we simulate higher-dimensional qudits by constructing them from **logical combinations of multiple qubits**. Since Qiskit does not currently support native qudits, we emulate a `d`-dimensional system using `log₂(d)` physical qubits.

By embedding our entanglement structure into this logical setup, we enable dense communication protocols that can theoretically support `d × D` classical symbols per logical qudit pair—where `d` corresponds to the embedding depth (related to the number of `Z` gates or entangled basis states), and `D` corresponds to the control space (related to the number of `X` gates or encoded logical states).

This design explores how the **limit of entanglement (Z gates)** and **the structure of the embedding (X gates)** interact to produce **higher-density transmission schemes**. We compare this approach to conventional dense coding protocols in terms of noise resilience, classical channel capacity, and physical qubit efficiency.

---

## Technologies Used

- **Qiskit** – Quantum circuit simulation and IBM hardware access
- **IBM Quantum Experience** – For running experiments on real quantum hardware
- **Python** – General scripting and control
- *(Optional: Arduino or other embedded microcontroller interface if hardware integration is used)*

---

## 📁 Project Structure

