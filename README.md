# Qualcomm-Snapdragon-Smart-PC-Guardian
AI-powered monitoring, prediction and guidance for next-generation smart PCs
# Qualcomm Snapdragon Smart PC Guardian

AI-powered laptop health, performance, thermal-risk and energy-intelligence system.

## 🚀 Quick Start

### 1. Download the project

Click **Code → Download ZIP**, then extract the project.

Recommended location:

```text
C:\Users\rahul\Downloads\AI_Laptop_Guardian_FINAL_WORKING
```

The project structure should look like:

```text
AI_Laptop_Guardian_FINAL_WORKING
└── ai_laptop_guardian
    ├── SETUP.bat
    ├── TRAIN.bat
    ├── RUN.bat
    ├── START_HERE.md
    ├── app.py
    ├── train_model.py
    ├── train_energy_model.py
    ├── download_kaggle_dataset.py
    ├── requirements.txt
    ├── data
    ├── models
    ├── scripts
    └── src
```

### 2. Open PowerShell

Open PowerShell inside the `ai_laptop_guardian` folder.

Or run:

```powershell
cd "$HOME\Downloads\AI_Laptop_Guardian_FINAL_WORKING\ai_laptop_guardian"
```

### 3. Install the project

Run:

```powershell
.\SETUP.bat
```

This creates the Python virtual environment and installs the required dependencies.

### 4. Train the AI models

Run:

```powershell
.\TRAIN.bat
```

The training process includes:

* Laptop thermal/load-risk prototype model
* Kaggle energy prediction model
* 20 candidate training runs for the energy model
* Model selection and final evaluation

### 5. Start the dashboard

Run:

```powershell
.\RUN.bat
```

The Streamlit dashboard will start locally.

Open:

```text
http://localhost:8501
```

### ⚠️ Important: localhost

`http://localhost:8501` is a **local development address**.

It works only on the computer where the application is running.

It should **not** be used as the public project/demo URL in GitHub.

For a public demo, deploy the Streamlit application and add the generated `https://....streamlit.app` URL to this README.

## 🧠 Main Features

* Real-time CPU monitoring
* GPU monitoring
* RAM and VRAM monitoring
* Battery monitoring
* GPU temperature monitoring
* Fan monitoring when supported
* Thermal/load risk prediction
* AI-generated recommendations
* Interactive Plotly dashboard
* Kaggle energy-demand prediction
* Historical telemetry visualization
* Read-only hardware monitoring

## 🤖 AI Architecture

```text
Laptop Hardware
       │
       ▼
Telemetry Collector
       │
       ├── CPU
       ├── GPU
       ├── RAM
       ├── VRAM
       ├── Temperature
       ├── Battery
       └── Power
       │
       ▼
Feature Engineering
       │
       ▼
Machine Learning
       │
       ├── Thermal / Load Risk
       └── Energy Prediction
       │
       ▼
AI Diagnosis
       │
       ▼
Interactive Dashboard
```

## 📊 Kaggle Energy Model

The project can use:

```text
energydata_complete.csv
```

Place the dataset inside:

```text
data/
```

Then run:

```powershell
.\TRAIN.bat
```

The Kaggle model predicts the dataset's appliance/household energy demand.

It is separate from the laptop thermal-monitoring model.

## 🔬 Research Development

The current thermal-risk model is a prototype.

For a research-grade version, collect real laptop telemetry such as:

```text
CPU utilization
GPU utilization
RAM utilization
VRAM utilization
CPU temperature
GPU temperature
CPU/GPU power
Fan RPM
Clock frequency
Battery percentage
Workload
Throttle state
Timestamp
```

This data can then be used to train a laptop-specific predictive health model.

## 🛡️ Safety

The application is designed as a read-only monitoring system.

It does not automatically:

* overclock the laptop
* undervolt the laptop
* modify firmware
* change fan firmware
* terminate processes
* disable thermal protection

