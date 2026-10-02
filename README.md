# 🚦 FSM Traffic Light Controller in Verilog

A **Finite State Machine (FSM)** implementation of a two-way Traffic Light Controller designed in **Verilog HDL**, simulated using **Icarus Verilog**, and verified with waveform analysis using **EPWave / GTKWave**.

---

## 📌 Project Overview
This project models an automated traffic light controller for an intersection between a **Main Highway** and a **Side Road**. The controller cycles through 4 distinct operational states controlled by an internal timer and clock generator.

### 🚥 Light Signal Encoding
* `3'b100` = **RED**
* `3'b010` = **YELLOW**
* `3'b001` = **GREEN**

---

## 🔄 State Transition Logic

| State | State Code | Highway Light (`R Y G`) | Side Road Light (`R Y G`) | Next State |
| :---: | :---: | :---: | :---: | :---: |
| **S0** | `2'b00` | `3'b001` (Green) | `3'b100` (Red) | **S1** |
| **S1** | `2'b01` | `3'b010` (Yellow) | `3'b100` (Red) | **S2** |
| **S2** | `2'b10` | `3'b100` (Red) | `3'b001` (Green) | **S3** |
| **S3** | `2'b11` | `3'b100` (Red) | `3'b010` (Yellow) | **S0** |

---

## 🛠️ Tools & Environments
* **Language:** Verilog HDL (IEEE 1364-2001)
* **Simulator:** Icarus Verilog (`iverilog`)
* **Waveform Viewer:** EPWave / GTKWave
* **Development Platform:** EDA Playground / GitHub Web
*
