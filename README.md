# Project Sentinel: Hazardous Asteroid Prediction AI 

## Table of Contents
* [Overview](#overview)
* [Core Features & Pipeline](#core-features--pipeline)
* [Repository Structure](#repository-structure)
* [Tech Stack](#tech-stack)
* [Installation & Execution](#installation--execution)
* [Using the Interactive Predictor](#using-the-interactive-predictor)
* [Acknowledgments](#acknowledgments)

---

## Overview
Project Sentinel is a machine learning system designed to automatically classify Near Earth Objects (NEOs) as **Hazardous** or **Non-Hazardous**. By analyzing a historical NASA dataset of physical and orbital characteristics, this project automates the complex multi-factor risk assessment required for planetary defense.

---

## Core Features & Pipeline
This project was developed in a single, streamlined Jupyter Notebook following a strict 6-phase data science pipeline:

1. **Data Preprocessing:** Cleaned the NASA NEO dataset, handled multicollinearity by dropping redundant units of measurement, and scaled numerical features using `StandardScaler`.
2. **Exploratory Data Analysis (EDA):** Visualized class imbalances and mapped feature relationships using Seaborn correlation heatmaps and scatter plots.
3. **Feature Engineering:** Isolated the most critical scientific metrics to optimize model performance.
4. **Model Development:** Trained a `RandomForestClassifier` with balanced class weights to successfully capture the non-linear relationships between an asteroid's velocity, mass, and proximity to Earth, while heavily penalizing false negatives.
5. **Explainability (XAI):** Extracted and visualized feature importances to provide scientific justification for model predictions.
6. **Interactive Deployment:** Built an integrated, widget-based User Interface directly within the notebook to accept custom asteroid parameters and instantly output a hazard prediction.

---

## Repository Structure
```text
├── .gitignore
├── README.md
├── hazardous_asteroid_prediction_final.ipynb
└── neo_data.csv
```
---

## Tech Stack
* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Data Visualization:** Matplotlib, Seaborn
* **User Interface:** ipywidgets

---

## Installation & Execution
### Prerequisites
Ensure you have Python 3.8+ installed on your local machine along with Jupyter Notebook. You will also need Git to clone the repository.

### 1. Clone the Repository
```bash
git clone git@github.com:your-username/hazardous-asteroid-prediction.git
```
---

### 2. Navigate to the Directory
```bash
cd hazardous-asteroid-prediction
```
---

### 3. Install Dependencies
```bash
pip install pandas numpy scikit-learn matplotlib seaborn ipywidgets
```
---

### 4. Launch the Application
```bash
jupyter notebook
```
---

### 5. Execute the Pipeline
1. Once the Jupyter interface opens in your web browser, locate and click on the hazardous_asteroid_prediction_final.ipynb file.
2. In the top navigation menu, click Cell (or Run, depending on your Jupyter version) and select Run All to execute the machine learning pipeline sequentially.
3. Scroll down to the final cell (Phase 6) to use the interactive Hazardous Asteroid Prediction UI.

---

## Using the Interactive Predictor
The final cell of the notebook generates a user interface. To test a Hazardous classification (the "City-Killer" scenario), input the following parameters:
* Absolute Magnitude (H): 16.10
* Min Diameter (km): 1.60
* Relative Velocity (km/s): 22.5
* Miss Distance (astronomical): 0.15

---

## Acknowledgments
* Data sourced from NASA's Planetary Defense Coordination Office via the NEO Earth Close Approaches dataset.
### Prerequisites
Ensure you have Python 3.8+ installed on your local machine along with Jupyter Notebook. You will also need Git to clone the repository.
### 1. Clone the Reposi
