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
* Design Calculations of Boost Converter 

  The design calculations for the boost converter given as,
  Consider, the switching frequency as () = 40KHZ
  The input voltage for the converter () = 30v
  Consider, the Duty cycle (D) = 0.7             
  The inductance of a Inductor (L) =   L=78.75×H                                                                                
  The capacitance of a Capacitor (C) =    C=17.5×F
                                                                                 
* **Closed-loop PI Controller** for voltage regulation.
* **MPPT Algorithms** implemented in MATLAB/Simulink function blocks.
   <img width="687" height="327" alt="image" src="https://github.com/user-attachments/assets/1a422395-e650-44e3-a0ac-b5074cf0e378" />

### 🧠 Without MPPT Techniques Implemented by using PI controller
  <img width="774" height="327" alt="image" src="https://github.com/user-attachments/assets/d2e3be72-be39-46c3-a83a-da64de734299" />

  * Achieved efficiency: **~88.72%**   
---

### 🧠 MPPT Techniques Implemented

1. **Perturb and Observe (P&O)**

   * Simple and cost-effective but prone to oscillations around MPPt.
   * <img width="759" height="335" alt="image" src="https://github.com/user-attachments/assets/7b0874ad-c578-4532-b080-f3814f09e576" />
   
   * Achieved efficiency: **~90.11%**

2. **Incremental Conductance (IncCond)**

   * High accuracy and faster convergence than P&O.
    <img width="755" height="359" alt="image" src="https://github.com/user-attachments/assets/bf807940-b00c-47e2-be2e-e5dd6bf75a04" />
    
   * Efficiency: **~90.43%**

3. **Fuzzy Logic Control (FLC)**

   * Rule-based intelligent control adaptable to nonlinear PV behavior.
     <img width="728" height="339" alt="image" src="https://github.com/user-attachments/assets/82501eca-d18e-4649-a35a-0122b6bce3b2" />
     
   * FLC + P&O: **90.51% efficiency**
    <img width="746" height="343" alt="image" src="https://github.com/user-attachments/assets/99b81b8a-144f-440e-a51d-bd86bb5063a4" />
    
   * FLC + IncCond: **89.96% efficiency**

4. **Particle Swarm Optimization (PSO)**

   * Metaheuristic optimization mimicking swarm intelligence.
   * Fast tracking, high accuracy, minimal oscillation.
    <img width="749" height="393" alt="image" src="https://github.com/user-attachments/assets/15446385-9853-44cd-be36-a8b1519c4d49" />
    
   * Efficiency: **91.32%**

5. **Adaptive Neuro-Fuzzy Inference System (ANFIS)**

   * Combines fuzzy logic and neural networks for adaptive learning.
    <img width="756" height="342" alt="image" src="https://github.com/user-attachments/assets/6f306a18-4a46-4839-85c6-073ba015ff3e" />
    
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
| ANFIS         | 927.4 **Highest**   | 0.170 **Lowest**        | 52.00 **Fastest**    | 0.646 **Lowest**             | 91.54 **Best Efficiency** |
<img width="716" height="463" alt="image" src="https://github.com/user-attachments/assets/b0a26b38-7130-4881-bc76-6d9ff54fccc0" />

---

### 🧩 Tools & Technologies

* **Software:** MATLAB/Simulink
* **Controller Design:** PI Controller, Fuzzy Logic, Neural Networks
* **Hardware Equivalent:** Boost Converter topology with MOSFET switching
* **Programming:** MATLAB scripting for custom MPPT algorithms

---
DISCUSSIONS:

Based on the comparative study on Solar PV System MPPT Techniques for Boost Converter, the conclusion highlights the performance metrics including Maximum Power Extraction, Settling Time, Rise Time, Steady State Error, and Efficiency for various MPPT methods compared to the closed-loop PI controller.
Maximum Power Extraction:
•Among the MPPT methods investigated, Particle Swarm Optimization (PSO) and Adaptive Neuro Fuzzy Interface System (ANFIS) demonstrated the highest maximum power extraction, with PSO achieving 928.8W and ANFIS achieving 927.4W.
•Closed-loop PI controller achieved a maximum power output of 894.3W, lower compared to advanced MPPT methods.

Settling Time:
•Fuzzy Logic Control with Incremental Conductance and Adaptive Neuro Fuzzy Interface System exhibited the fastest settling times at 0.170sec, closely followed by Particle Swarm Optimization at 0.172sec.
•Closed-loop PI controller had a settling time of 0.198sec, comparatively slower than some of the MPPT methods.

Rise Time:
•Adaptive Neuro Fuzzy Interface System (ANFIS) demonstrated the fastest rise time at 52.006ms, followed by Fuzzy Logic Control with Incremental Conductance at 54.428ms.
•Closed-loop PI controller had a rise time of 60.855ms, slower compared to most of the MPPT methods.

Steady State Error (%):
•Particle Swarm Optimization exhibited the lowest steady-state error at 0.254%, followed by Fuzzy Logic Control with Incremental Conductance at 0.646%.
•Closed-loop PI controller had a steady-state error of 1.136%, higher than most of the advanced MPPT methods.

Efficiency (%):
•Adaptive Neuro Fuzzy Interface System (ANFIS) demonstrated the highest efficiency at 91.549%, followed closely by Particle Swarm Optimization at 91.327%.
•Closed-loop PI controller had an efficiency of 88.720%, lower compared to several MPPT methods.


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


