# 🌞 Exploring Performance Enhancement of MPPT Techniques for Boost Converter in Solar PV System

### 📘 Overview

This project explores and compares different **Maximum Power Point Tracking (MPPT)** techniques used in solar photovoltaic (PV) systems integrated with a **DC–DC boost converter**.
The goal is to identify the most efficient MPPT algorithm that enhances solar power extraction under varying irradiance and temperature conditions using **MATLAB/Simulink** simulations.

---

### 🎯 Objectives

* Design and simulate a **boost converter** integrated with various MPPT algorithms.
* Compare performance parameters such as **maximum power**, **rise time**, **settling time**, **steady-state error**, and **efficiency**.
* Implement intelligent control techniques (Fuzzy Logic, PSO, ANFIS) for performance improvement.

---

### ⚙️ System Components

* **PV Module** modeled using the **single-diode model**.
* **DC–DC Boost Converter** for voltage step-up and control.
* **Closed-loop PI Controller** for voltage regulation.
* **MPPT Algorithms** implemented in MATLAB/Simulink function blocks.

---

### 🧠 MPPT Techniques Implemented

1. **Perturb and Observe (P&O)**

   * Simple and cost-effective but prone to oscillations around MPP.
   * Achieved efficiency: **~90.11%**

2. **Incremental Conductance (IncCond)**

   * High accuracy and faster convergence than P&O.
   * Efficiency: **~90.43%**

3. **Fuzzy Logic Control (FLC)**

   * Rule-based intelligent control adaptable to nonlinear PV behavior.
   * FLC + P&O: **90.51% efficiency**
   * FLC + IncCond: **89.96% efficiency**

4. **Particle Swarm Optimization (PSO)**

   * Metaheuristic optimization mimicking swarm intelligence.
   * Fast tracking, high accuracy, minimal oscillation.
   * Efficiency: **91.32%**

5. **Adaptive Neuro-Fuzzy Inference System (ANFIS)**

   * Combines fuzzy logic and neural networks for adaptive learning.
   * Highest performance among all tested algorithms.

---

### 📊 Comparative Analysis

| MPPT Method   | Max Power (W) | Settling Time (s) | Rise Time (ms) | Steady-State Error (%) | Efficiency (%)      |
| ------------- | ------------- | ----------------- | -------------- | ---------------------- | ------------------- |
| PI Control    | 894.3         | 0.198             | 60.85          | 1.136                  | 88.72               |
| P&O           | 906.6         | 0.196             | 60.75          | 1.132                  | 90.11               |
| IncCond       | 909.8         | 0.189             | 60.68          | 1.132                  | 90.43               |
| FLC (P&O)     | 910.6         | 0.188             | 59.60          | 1.132                  | 90.51               |
| FLC (IncCond) | 911.3         | 0.170             | 54.42          | 0.646                  | 89.96               |
| PSO           | 928.8         | 0.172             | 53.15          | 0.254                  | 91.32               |
| ANFIS         | **Highest**   | **Lowest**        | **Fastest**    | **Lowest**             | **Best Efficiency** |

---

### 🧩 Tools & Technologies

* **Software:** MATLAB/Simulink
* **Controller Design:** PI Controller, Fuzzy Logic, Neural Networks
* **Hardware Equivalent:** Boost Converter topology with MOSFET switching
* **Programming:** MATLAB scripting for custom MPPT algorithms

---

### 🔍 Key Findings

* Intelligent MPPT techniques like **PSO** and **ANFIS** outperform conventional methods.
* **PSO** achieves faster convergence and high efficiency with minimal steady-state error.
* **ANFIS** demonstrates superior adaptability under varying solar irradiance and temperature.

---

### 🚀 Future Enhancements

* Implement **real-time hardware testing** using microcontrollers (e.g., Arduino, DSP).
* Integrate **hybrid MPPT systems** combining multiple algorithms.
* Apply **IoT-based monitoring** for smart solar systems.

---

### 👨‍💻 Contributors

* **Kuruva Gudise Yamunappa**
* **Samneni Mahesh Kalyan**
* **Kuruba Madhusudhan**
* **Sake Prameela**
* **Pattem Sai Chandana**

**Supervisor:** Dr. M. S. Sujatha, M.Tech, Ph.D.
Professor & Head, Department of EEE,
Sree Vidyanikethan Engineering College, Tirupati.

---

### 🏫 Institution

**Department of Electrical and Electronics Engineering**
**Sree Vidyanikethan Engineering College (Autonomous)**
Affiliated to **Jawaharlal Nehru Technological University Anantapur (JNTUA)**


