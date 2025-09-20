# 🚀 Week 0: VLSI System Design (VSD) Program Foundation & Tool Setup

## 📌 VLSI Week Status
Welcome to my VLSI System Design (VSD) Program repository! This week focused on setting up the development environment and installing essential open-source tools. The goal is to create a reliable workspace for synthesis, simulation, and design tasks.

---

## 🎯 System & Virtual Machine Configuration
To ensure optimal performance, the VM was configured with the following specifications:

| Specification 💻       | Details 📋        |
|------------------------|-----------------|
| Operating System 🐧    | Ubuntu 20.04+   |
| RAM 💾                 | 6GB             |
| Storage 💿             | 50GB HDD        |
| vCPUs ⚡                | 4               |

💡 **Pro Tip:** This setup provides enough resources for toolchain demands and smooth simulation runs.

---

## ⚙️ Tool Installation & Verification
Installed tools for RTL synthesis, simulation, circuit analysis, and layout design.

**Tool Flow:** 🧠 Yosys → 📟 Iverilog → 📊 GTKWave → ⚡ Ngspice → 🎨 Magic VLSI

---

### 🧠 1. Yosys – RTL Synthesis Tool
**Purpose:** Converts RTL code into gate-level representations.

**Installation:**
```bash
# Clone Yosys repository
git clone https://github.com/YosysHQ/yosys.git
cd yosys 

# Install dependencies
sudo apt install make
sudo apt-get install build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev

# Build and install
make
sudo make install
````

✅ **Verification:** Yosys successfully installed

![yosys](https://github.com/user-attachments/assets/ac0b6b20-ae2c-4e4e-8816-685e48389a18)


---

### 📟 2. Iverilog – Verilog Simulator

**Purpose:** Compiles and simulates Verilog designs for functional verification.

**Installation:**

```bash
sudo apt-get install iverilog
```

✅ **Verification:** Iverilog successfully installed

![iverilog](https://github.com/user-attachments/assets/49aa0aac-531c-4e81-9431-6e6500c6fa53)


---

### 📊 3. GTKWave – Waveform Viewer

**Purpose:** Visualizes and analyzes simulation waveforms for debugging.

**Installation:**

```bash
sudo apt update
sudo apt install gtkwave
```

✅ **Verification:** GTKWave successfully installed

![gtkwave](https://github.com/user-attachments/assets/f21c3c28-cc4c-4d47-a8cb-bdc7f645ce73)


---

### ⚡ 4. Ngspice – Circuit Simulator

**Purpose:** Performs analog and mixed-signal circuit simulations.

**Installation:**

```bash
sudo apt update
sudo apt install ngspice
```

✅ **Verification:** Ngspice successfully installed

![ngspice](https://github.com/user-attachments/assets/f269e9d6-fb16-4282-88b1-b5fa266a5999)


---

### 🎨 5. Magic VLSI – Layout Tool

**Purpose:** Creates, edits, and analyzes VLSI layouts with DRC capabilities.

**Installation:**

```bash
# Install dependencies
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev \
libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev

# Clone Magic repository
git clone https://github.com/RTimothyEdwards/magic
cd magic

# Configure, build, and install
./configure
make
sudo make install
```

✅ **Verification:** Magic VLSI successfully installed

![magic](https://github.com/user-attachments/assets/87995eab-94cf-44ec-9197-0d155dd3dfb6)


---

## 🎉 Installation Summary

| Tool          | Status     | Primary Use        |
| ------------- | ---------- | ------------------ |
| 🧠 Yosys      | ✅ Complete | RTL Synthesis      |
| 📟 Iverilog   | ✅ Complete | Verilog Simulation |
| 📊 GTKWave    | ✅ Complete | Waveform Analysis  |
| ⚡ Ngspice     | ✅ Complete | Circuit Simulation |
| 🎨 Magic VLSI | ✅ Complete | Layout Design      |

🚀 **Environment ready for your VLSI design journey!**
