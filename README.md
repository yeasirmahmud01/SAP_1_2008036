# 🧠 SAP-1 Microprocessor — Manual & Automatic Implementation (CUET ETE-404)

> ⚠️ **Important:** Please **wear earphones or headphones** while watching the documentation videos for clear narration and timing explanations.

---

## 🏫 Project Information
**Course:** VLSI Technology Sessional  
**Course Code:** ETE-404  
**Department:** Electronics and Telecommunication Engineering  
**University:** Chittagong University of Engineering and Technology (CUET)  
**Student:** Yeasir Mahmud (ID: 2008036)

---

## 🎯 Project Overview
This project implements a complete **SAP-1 (Simple-As-Possible) Microprocessor** in **Logisim Evolution**, featuring both **Manual** and **Automatic (Auto Loader)** operation modes.

- **Manual Mode:** Classic SAP-1 design with manual program entry and step execution.  
- **Automatic Mode:** Enhanced version with an **Instruction Loader** that automatically transfers programs from ROM to SRAM.  

A **Python-based Assembler** is included to convert assembly code into machine-readable binary/hex format for direct ROM programming.

---

## 🧩 Features
- ✅ Full SAP-1 implementation in Logisim Evolution  
- ⚙️ **Hardwired Control Sequencer** designed from Boolean equations  
- ⏱️ **Ring Counter (T₁–T₆)** generating instruction timing pulses  
- 🔡 **Instruction Decoder (4-to-16)** one-hot opcode expansion  
- 💾 **Instruction Loader** automating ROM → SRAM transfer (Auto Mode)  
- 💻 **Python Compiler/Assembler** to generate `.txt` and `.hex` code  
- 🧾 **Comprehensive Documentation Report** (PDF)  
- 🎥 **YouTube Documentation Videos** for both manual and auto operation  

---

## 🧱 Architecture Overview
| Component | Description |
|------------|-------------|
| **Program Counter (PC)** | Generates next instruction address; supports reset & jump. |
| **Memory Address Register (MAR)** | Holds address for memory access. |
| **SRAM** | Instruction & data memory controlled by `sram_rd/sram_wr`. |
| **Instruction Register (IR)** | Stores opcode + operand. |
| **Decoder** | Converts opcode into one-hot instruction lines. |
| **Ring Counter** | Generates timing pulses (T1–T6). |
| **Control Sequencer** | Generates control signals using opcode & timing. |
| **Instruction Loader** | Copies program from ROM → SRAM automatically. |
| **Registers A & B** | General-purpose registers (A = Accumulator). |
| **ALU** | Performs add/sub; controlled by `alu_sub`. |
| **Output Register** | Displays final result from Accumulator. |

---

## 💾 Files Included
| File | Description |
|------|-------------|
| `sap1_2008036.circ` | Manual SAP-1 circuit |
| `sap1_2008036_auto.circ` | Automatic SAP-1 circuit (with loader) |
| `sap_1_compiler.py` | Python-based assembler/compiler |
| `sample_program.txt` | Example assembly code |
| `Documentation_Report.pdf` | Full project report (LaTeX/PDF) |
| `Documentation_video_links.md` | YouTube documentation video links |
| `APP_LINK.md` | Application or compiler app link |

---

## 🎥 Documentation Videos

> ⚠️ Please use earphones/headphones for clear voice and timing narration.

- 🎬 **Video 1 – Manual SAP-1 Implementation and Working**  
  ▶ [https://youtu.be/Qg41prMnh7M?si=I5qifFfr43NMmPTR](https://youtu.be/Qg41prMnh7M?si=I5qifFfr43NMmPTR)

- ⚙️ **Video 2 – Automatic SAP-1 (Instruction Loader & Control Sequencer)**  
  ▶ [https://youtu.be/Fg9NOlhEnMM?si=H7XgJqqebU_cU_0Q](https://youtu.be/Fg9NOlhEnMM?si=H7XgJqqebU_cU_0Q)

📁 [View all documentation video links → `Documentation_video_links.md`](Documentation_video_links.md)

---

## 🧠 Example Program

**Assembly Code**
LDA 7
LDB 8
ADD
ST 9
HLT

DATA 7 10
DATA 8 5
DATA 9 0


**Machine Code (Hex)**
17 28 30 59 E0 00 00 0A 05 00 00 00 00 00 00 00

➡️ This program loads 10 into A, 5 into B, performs A+B, stores 15 at address 9, then halts.

---

## 🧰 Tools Used
- 🧩 **Logisim Evolution** – for circuit design & simulation  
- 🐍 **Python 3.x** – for assembler/compiler development  
- 📄 **LaTeX** – for documentation report  
- ☁️ **GitHub** – for project hosting & version control  

---

## 📄 Documentation
📘 [Download Full Project Report (PDF)](Documentation_Report.pdf)  
📺 [Watch Documentation Videos](Documentation_video_links.md)

---

## 🧩 Demonstration Workflow
1. Load program into ROM (via compiler output).  
2. In **Auto Mode**, set `debug = 1` → loader copies ROM → SRAM using `I1/I2` handshake.  
3. After loading, set `debug = 0`, reset PC, enable `rc_en`.  
4. Apply clock pulses — each 6 pulses = one instruction cycle.  
5. Observe Register A, B, ALU, and Output registers update accordingly.

---

## 📘 Repository Link
🔗 **GitHub:** [https://github.com/yeasirmahmud01/SAP_1_2008036](https://github.com/yeasirmahmud01/SAP_1_2008036)

---

### 🏁 Acknowledgment
Special thanks to the **Department of Electronics and Telecommunication Engineering, CUET**,  
for continuous support and guidance during the **VLSI Technology Sessional Project**.

---

© 2025 **Yeasir Mahmud**  
Department of Electronics and Telecommunication Engineering  
Chittagong University of Engineering and Technology (CUET)
