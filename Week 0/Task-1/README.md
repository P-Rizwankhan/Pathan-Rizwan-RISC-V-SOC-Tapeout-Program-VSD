# 🚀 Journey into RISC-V SoC Design – Task 1

Welcome to my adventure in digital hardware – a practical exploration of **System-on-Chip (SoC) creation using RISC-V** as part of India’s massive collaborative tapeout challenge!  
This documentation records insights and progress from each hands-on milestone, as I build an SoC from initial C code to the brink of chip fabrication.

---

## 🎬 Task 1: Exploring the SoC Design Pathway

In this section, I walk through the sequential steps behind constructing a working silicon chip, focusing on how algorithms and code translate into real, testable hardware.

---

### 1️⃣ Application Code Verification

- Start with a simple C application (e.g., a calculator).
- Compile and validate the code using standard tools (like GCC).  
- This standalone check (output `O0`) guarantees the application logic works before linking it with hardware.
  <img width="1622" height="203" alt="image" src="https://github.com/user-attachments/assets/8c7fe2fa-a9a2-44e9-8431-bf5bfd58af2b" />


---

### 2️⃣ Processor Specification and Functional Modelling

- Convert the intended processor specifications to a C-like executable model.
- Use an architecture-specific compiler (RISC-V GCC, for example) to create a new output (`O1`).
- Match results (`O0` vs `O1`). Success here “locks in” the intended behavior for future design steps.
  

---

### 3️⃣ Building RTL: Hardware in Code

- Transform the verified spec into **Register Transfer Level (RTL)** logic (usually in Verilog or other hardware description languages).
- This model, still virtual (“soft” hardware), simulates how hardware will behave — producing `O2`.
- Match with previous results to ensure functionality is preserved.
  <img width="1659" height="223" alt="image" src="https://github.com/user-attachments/assets/34a1e6af-56cb-4b33-a412-930d5d633081" />


---

### 4️⃣ SoC Block Partitioning

- Split the RTL into modular blocks:
  - Processor (synthesizable)
  - Peripherals and custom macros
  - Analog blocks (e.g., ADCs, PLLs)
- Analog IP only needs functional models, not full synthesis.
- Validate the design flow again (`O3`) and ensure all prior outputs match.
  <img width="1711" height="661" alt="image" src="https://github.com/user-attachments/assets/f081f132-664f-4c98-9453-449b47cfad2e" />


---

### 5️⃣ Microprocessors vs Microcontrollers

- **Microprocessors:** Just the processing core—external chips needed for I/O and memory.
- **Microcontrollers:** An all-in-one package with the CPU plus necessary support circuits, ideal for embedded platforms.
- This distinction is foundational for both design and interviews.
  <img width="703" height="165" alt="image" src="https://github.com/user-attachments/assets/c893a491-4c1d-4ae1-9e25-ec62f193301c" />

---

### 6️⃣ From Logic to Layout: Physical Design

- Transition the finalized RTL into real hardware elements (gates, transistors, etc.).
- The design journey continues through:
  - Floorplanning
  - Placement
  - Clock-tree synthesis
  - Routing
- The finished product: a **GDSII layout file**, ready for chip fabrication (“tapeout”).
  <img width="871" height="100" alt="image" src="https://github.com/user-attachments/assets/bf47c171-67cc-4df6-8ce5-d9faaad56004" />

---

### 7️⃣ On-Board Testing and Validation

- Chips are placed onto development boards with required components (memory, interfaces, oscillators).
- The original application code is now run on actual silicon, creating the last output (`O4`).
- All build phases (`O1`, `O2`, `O3`, `O4`) must yield identical results—final proof that the silicon behaves as intended.
  <img width="1661" height="914" alt="image" src="https://github.com/user-attachments/assets/af12d838-88d4-4cc7-809b-174ec3bc1e10" />

---

## ⏳ Timeline & Reflections

- The full process, from design to chip manufacture, usually takes over a year (fabrication alone can exceed four months).
- Example outputs reached up to 130 MHz—perfect for embedded devices like Arduino alternatives or IoT controls.

---

## 🗝️ Key Definitions

- **Silicon Proven:** The design has been made into a chip and shown to function.
- **Tapeout / Tape-in:** Sending the final GDSII for manufacturing and receiving built chips in return.
- **Synthesizable RTL:** Hardware code that can be directly turned into gates.  
- **Functional RTL:** Used for simulation, not hardware generation.


Heartfelt thanks to the **VSD team**, the vibrant global RISC-V community, and all program collaborators for enabling this innovative learning experience.

---

**Stay tuned for more step-by-step insights as Task 2 approaches!**
