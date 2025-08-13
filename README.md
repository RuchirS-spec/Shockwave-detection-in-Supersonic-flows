# Shockwave-detection-in-Supersonic-flows
Implementing ML Based Shock Wave Detection in Supersonic flows using ANSYS Fluent

# 🚀 Machine Learning-Based Shock Wave Detection in Supersonic Flows

---

## 📄 Overview
This project explores the intersection of **Computational Fluid Dynamics (CFD)** and **Machine Learning (ML)** to detect and analyze shock waves in supersonic fluid flows.  

The workflow involves two primary stages:  

1. **CFD Simulation** – Simulate supersonic flow scenarios in **ANSYS Fluent** (e.g., backward-facing step, convergent-divergent nozzle) to generate high-fidelity datasets.  
2. **Machine Learning Implementation** – Train neural networks on extracted CFD data to identify the location and characteristics of shock waves.

> **Project Structure:** A series of assignments progressing from CFD fundamentals to ML-based shock wave detection.

---

## 🎯 Objectives
- ✅ Perform CFD simulations of supersonic flows to generate datasets.  
- ✅ Extract **Mach number**, **pressure**, and **velocity** from simulation results.  
- ✅ Build & train an **ANN** to predict Mach number profiles and detect shocks.  
- ✅ Gain hands-on experience with the **end-to-end CFD-to-ML pipeline**.

---

## ⚙️ Methodology

### **Part 1 – CFD Simulations in ANSYS Fluent**
#### 1️⃣ Flow Over a Backward-Facing Step
- **Goal:** Understand flow separation & reattachment in subsonic flows.  
- **Steps:** Designed 2D geometry → meshed → simulated → generated **velocity**, **static pressure**, and **TKE** contours.

#### 2️⃣ Supersonic Flow Through a Nozzle
- **Goal:** Visualize shock formation in a convergent-divergent nozzle.  
- **Steps:** Designed 2D nozzle → meshed → simulated → generated **velocity**, **pressure**, **temperature**, **Mach number** contours.

---

### **Part 2 – Machine Learning Implementation**
#### 1️⃣ Foundational CNN Training *(Assignment 6)*
- **Goal:** Learn CNN basics for image-based tasks.  
- **Steps:**  
  - Implemented CNN in **TensorFlow/Keras**.  
  - Trained on **CIFAR-10 dataset** (image classification).  
  - Achieved **69% accuracy**.

#### 2️⃣ Shock Wave Detection with ANN *(Assignment 8)*
- **Goal:** Predict Mach number profiles & detect shock locations.  
- **Steps:**  
  1. Extracted `(Position, Mach Number)` data from nozzle simulation.  
  2. Trained **ANN** to map `Position → Mach Number`.  
  3. Detected shocks from sharp discontinuities in predicted profiles.

---

## 📊 Results

### **CFD Contours**
![CFD Contours Placeholder](images/cfd_contours.png)  
*Velocity, Pressure, and Mach number visualizations from ANSYS Fluent.*

### **ANN Prediction vs Actual**
![ANN Prediction vs Actual Placeholder](images/actual_vs_predicted.png)  
*ANN closely matches simulation results.*

### **Training Loss Curve**
![Training Loss Placeholder](images/training_loss.png)  
*Converged loss indicates successful model training.*

---

## 🛠️ Tools & Technologies
| Category               | Tools |
|------------------------|-------|
| **CFD Simulation**     | ANSYS 2025 R1 (Fluent, SpaceClaim, DesignModeler) |
| **Machine Learning**   | Python, TensorFlow, Keras |
| **Data & Visualization** | Pandas, Matplotlib |

---

## 📂 Repository Structure
```plaintext
.
├── data/               # Extracted CFD datasets
├── notebooks/          # Jupyter notebooks for ML
├── cfd_models/         # ANSYS Fluent simulation files
├── images/             # Contour plots and result graphs
├── src/                # Python scripts for preprocessing & training
└── README.md           # This file
📌 How to Run
