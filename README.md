# Predictive Maintenance – Machine Failure Prediction

**Machine failure prediction using industrial sensor data**

This project focuses on predicting machine failures in an industrial manufacturing setting using operational and sensor-level data. The objective is to support predictive maintenance strategies by identifying potential failures before they occur, thereby reducing unplanned downtime, maintenance costs, and operational risk.

The dataset represents realistic manufacturing conditions, including thermal behavior, mechanical load, tool wear, and multiple failure mechanisms commonly observed in production environments.

---

## 📌 Project Objectives

* Predict machine failures based on sensor and process data
* Model multiple failure types encountered in industrial systems
* Evaluate machine learning models using metrics suitable for imbalanced data
* Demonstrate an end-to-end predictive maintenance workflow

---

## 📊 Dataset Description

The dataset consists of simulated sensor readings and operational parameters collected during machine operation.

### Input Features

* **Type** – Product quality category (Low, Medium, High)
* **Air Temperature [K]** – Ambient air temperature surrounding the machine
* **Process Temperature [K]** – Temperature within the manufacturing process
* **Rotational Speed [rpm]** – Operating speed of the machine
* **Torque [Nm]** – Mechanical torque applied during operation
* **Tool Wear [min]** – Cumulative tool usage time

### Target Variables

* **Machine Failure** – Overall failure indicator
* **Tool Wear Failure** – Failure due to excessive tool usage
* **Heat Dissipation Failure** – Failure caused by insufficient heat dissipation
* **Power Failure** – Failure due to abnormal power requirements
* **Overstrain Failure** – Failure resulting from excessive mechanical stress
* **Random Failures** – Stochastic failures independent of operating conditions

This structure allows the model to capture both deterministic failure patterns and random failure events typically observed in industrial systems.

---

## 🧠 Modeling Approach

The task is formulated as a **classification problem** with significant class imbalance, which is characteristic of real-world failure prediction scenarios.

Key steps in the workflow include:

* Exploratory data analysis to understand sensor behavior and failure distribution
* Feature preprocessing and encoding of categorical variables
* Model training using algorithms well-suited for structured tabular data
* Evaluation using metrics that appropriately reflect performance on rare failure events

### Models Used

* **XGBoost**
* **LightGBM**

These ensemble methods were selected due to their robustness, scalability, and strong performance on industrial tabular datasets.

---

## 📈 Evaluation Metrics and Results

Given the imbalanced nature of the dataset, model performance was evaluated using:

* **ROC-AUC** – to measure discriminative ability
* **F1 Score** – to balance precision and recall

### Model Performance

* **ROC-AUC:** ~0.95
* **F1 Score:** ~0.87

These results indicate reliable failure detection while maintaining a balance between false positives and false negatives.

---

## 🛠 Tech Stack

* **Python**
* **NumPy, Pandas** – data manipulation and analysis
* **Matplotlib, Seaborn** – data visualization
* **Scikit-learn** – preprocessing and evaluation
* **XGBoost, LightGBM** – model training

---

## 📚 Key Takeaways

* Predictive maintenance problems typically involve highly imbalanced datasets
* Domain understanding is critical for meaningful feature interpretation
* Ensemble tree-based models provide strong performance on industrial sensor data
* Appropriate evaluation metrics are essential for assessing real-world utility

---

## 🔍 Use Case and Impact

Accurate machine failure prediction enables organizations to schedule maintenance proactively, reduce downtime, and improve operational efficiency. This project demonstrates how machine learning techniques can be applied to industrial reliability problems in a structured and interpretable manner.

---

This repository is intended for educational and applied data science exploration in the context of predictive maintenance.
