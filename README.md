# 🌍 CO₂ Emission Savings Estimator

<div align="center">

![Project Banner](https://img.shields.io/badge/ML-Project-green?style=for-the-badge&logo=tensorflow)
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-red?style=for-the-badge&logo=streamlit)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**An AI-powered tool to predict and visualize CO₂ emission savings from Electric Vehicles**

[Features](#-features) • [Usage](#-usage) • [Architecture](#-system-architecture) 

---

### 🎯 Project Impact

```
🌱 Quantify Environmental Impact  |  📊 Data-Driven Insights  |  🚗 EV vs Petrol Comparison
```

</div>

---

## 📋 Table of Contents

- [Problem Statement](#-problem-statement)
- [Solution Overview](#-solution-overview)
- [Features](#-features)
- [System Architecture](#-system-architecture)
- [ML Pipeline](#-ml-pipeline)

---

## 🔴 Problem Statement

> **Climate change caused by excessive CO₂ emissions is a critical global challenge.**

### The Gap

| Current Scenario | The Problem |
|-----------------|-------------|
| ✅ EVs reduce pollution | ❌ No quantifiable metrics (kg/tons CO₂) |
| ✅ EV specs available | ❌ Not linked to emission data |
| ✅ Users want eco-choices | ❌ Can't compare environmental impact |

### Our Mission

Build an **ML-powered estimator** that converts EV specifications into measurable CO₂ savings, enabling:
- 🎯 Quantified environmental impact
- 📈 Predictive analytics for new EV models
- 🔍 Comparative analysis across vehicles
- 💚 Data-driven eco-conscious decisions

---

## 💡 Solution Overview

```mermaid
graph LR
    A[EV Specifications] --> B[ML Model]
    B --> C[CO₂ Savings Prediction]
    C --> D[Visualization Dashboard]
    D --> E[Actionable Insights]
    
    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#e8f5e9
    style D fill:#f3e5f5
    style E fill:#fce4ec
```

### Key Capabilities

| Feature | Description |
|---------|-------------|
| 🔮 **Predictive Modeling** | Regression algorithms estimate CO₂ savings from EV specs |
| 📊 **Data Visualization** | Interactive charts showing environmental impact |
| ⚡ **Real-time Calculation** | Instant predictions for custom EV configurations |
| 🌳 **Impact Translation** | Convert savings to trees planted or petrol saved |

---

## ✨ Features

### 🎯 Core Functionality

- **🔢 CO₂ Savings Calculator**
  - Input: Battery capacity, Range, Efficiency
  - Output: Total CO₂ saved (kg/year)
  
- **📊 Comparative Analysis**
  - EV vs Petrol vehicle emissions
  - Top 10 eco-friendly EVs ranking
  
- **🎨 Interactive Dashboard**
  - Streamlit-based web interface
  - Real-time slider inputs
  - Dynamic visualizations

- **🌱 Environmental Metrics**
  - Equivalent trees planted
  - Petrol consumption avoided
  - Annual carbon footprint reduction

---

## 🏗️ System Architecture

```mermaid
flowchart TB
    subgraph Input["📥 Data Input Layer"]
        A1[EV Dataset CSV]
        A2[User Input Specs]
    end
    
    subgraph Processing["⚙️ Processing Layer"]
        B1[Data Preprocessing]
        B2[Feature Engineering]
        B3[Normalization]
    end
    
    subgraph ML["🤖 Machine Learning Layer"]
        C1[Linear Regression]
        C2[Random Forest]
        C3[Model Evaluation]
        C4[Best Model Selection]
    end
    
    subgraph Output["📤 Output Layer"]
        D1[Predictions]
        D2[Visualizations]
        D3[Metrics Dashboard]
    end
    
    subgraph Deploy["🚀 Deployment"]
        E1[Streamlit App]
        E2[Web Interface]
    end
    
    A1 --> B1
    A2 --> B1
    B1 --> B2
    B2 --> B3
    B3 --> C1
    B3 --> C2
    C1 --> C3
    C2 --> C3
    C3 --> C4
    C4 --> D1
    D1 --> D2
    D2 --> D3
    D3 --> E1
    E1 --> E2
    
    style Input fill:#e3f2fd
    style Processing fill:#fff3e0
    style ML fill:#e8f5e9
    style Output fill:#f3e5f5
    style Deploy fill:#fce4ec
```

---

## 🔄 ML Pipeline

### Step-by-Step Workflow

```mermaid
graph TD
    A[📂 Data Collection] -->|EV_cars.csv| B[🧹 Data Cleaning]
    B -->|Handle Missing Values| C[🔧 Feature Engineering]
    C -->|Derive CO₂ Savings| D[✂️ Train-Test Split]
    D -->|80-20 Split| E[🤖 Model Training]
    E -->|Multiple Algorithms| F[📊 Model Evaluation]
    F -->|R², MAE, RMSE| G{Best Model?}
    G -->|Yes| H[💾 Save Model]
    G -->|No| E
    H --> I[🎨 Visualization]
    I --> J[🌐 Streamlit Deployment]
    
    style A fill:#4CAF50
    style E fill:#2196F3
    style F fill:#FF9800
    style H fill:#9C27B0
    style J fill:#F44336
```

### Feature Engineering Formula

The core calculation for CO₂ savings:

```python
# CO₂ emissions comparison
CO2_petrol = 150  # g/km (average petrol car)
CO2_EV = 80       # g/km (average EV with grid electricity)

# Total savings calculation
CO2_savings_total = Range_km × (CO2_petrol - CO2_EV) / 1000  # in kg
```

**Example:**
- EV Range: 400 km
- Savings per full charge: 400 × (150 - 80) / 1000 = **28 kg CO₂**
- Annual savings (15,000 km/year): **1,050 kg CO₂**

---


## 📊 Data Flow

```mermaid
sequenceDiagram
    participant U as 👤 User
    participant UI as 🖥️ Streamlit UI
    participant P as 🔮 Predictor
    participant M as 🤖 ML Model
    participant V as 📊 Visualizer
    
    U->>UI: Input EV Specs
    UI->>P: Process Input
    P->>M: Request Prediction
    M->>P: Return CO₂ Savings
    P->>V: Generate Visualizations
    V->>UI: Display Results
    UI->>U: Show Predictions & Charts
    
    Note over U,V: Real-time Processing
```

---




</div>
