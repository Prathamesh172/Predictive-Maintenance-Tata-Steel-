# Predictive Maintenance – Machine Failure Prediction

**Anticipating industrial machine failures using sensor data and machine learning**

This project focuses on predicting machine failures in an industrial setting using operational sensor data. The goal is to move from *reactive maintenance* to **predictive maintenance**, reducing unplanned downtime, maintenance costs, and production losses.

The dataset simulates realistic manufacturing conditions, including tool wear, thermal behavior, torque, speed, and multiple failure modes. The project treats failure prediction as a **real-world classification problem** rather than a toy ML exercise.

---

## ✨ Project Highlights

* End-to-end predictive maintenance pipeline
* Multiple failure modes modeled, not just a single binary label
* Strong emphasis on feature understanding and failure logic
* Tree-based ensemble models suitable for industrial data

---

## 📊 Dataset Overview

The dataset represents sensor readings and operational parameters collected from industrial machines during production.

### Input Features

* **Type** – Product quality category (Low, Medium, High)
* **Air Temperature [K]** – Ambient air temperature around the machine
* **Process Temperature [K]** – Internal process temperature
* **Rotational Speed [rpm]** – Machine operating speed
* **Torque [Nm]** – Applied torque during operation
* **Tool Wear [min]** – Accumulated tool usage time

### Target Variables

* **Machine Failure** – Overall failure indicator
* **Tool Wear Failure** – Failure due to excessive tool usage
* **Heat Dissipation Failure** – Failure caused by insufficient thermal difference
* **Power Failure** – Failure when power requirements exceed limits
* **Overstrain Failure** – Failure due to excessive mechanical stress
* **Random Failures** – Stochastic failures independent of sensor readings

This structure allows the model to learn both **systematic failures** and **random failure behavior**, which is common in real industrial environments.

---

## 🧠 Modeling Approach

The problem is treated as a **classification task** with strong class imbalance, typical of failure prediction systems.

Key steps:

* Exploratory Data Analysis (EDA) to understand sensor distributions and failure patterns
* Feature preprocessing and encoding for categorical variables
* Handling class imbalance using appropriate evaluation metrics
* Training ensemble-based models well-suited for tabular sensor data

### Models Used

* **XGBoost**
* **LightGBM**

These models were chosen for their robustness, interpretability, and strong performance on structured industrial datasets.

---

## 📈 Evaluation Metrics

Because failures are rare events, accuracy alone is misleading. The project focuses on:

* **ROC-AUC** – Ability to distinguish failure vs non-failure
* **F1 Score** – Balance between precision and recall

### Performance

* **ROC-AUC:** ~0.95
* **F1 Score:** ~0.87

These results indicate strong predictive capability while maintaining practical reliability.

---

## 🛠 Tech Stack

* **Python**
* **NumPy, Pandas** – data manipulation
* **Matplotlib, Seaborn** – visualization
* **Scikit-learn** – preprocessing and evaluation
* **XGBoost, LightGBM** – model training

---

## ▶️ How to run the project

1. Clone the repository

```bash
git clone https://github.com/your-username/predictive-maintenance.git
cd predictive-maintenance
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Open the notebook

```bash
jupyter notebook
```

4. Run `Tata Steel Machine Failure Prediction.ipynb`

---

## 🔍 Key Learnings

* Predictive maintenance is fundamentally an **imbalanced classification** problem
* Feature understanding is as important as model choice in industrial ML
* Ensemble tree models provide an excellent balance between performance and interpretability
* Evaluating failure prediction systems requires domain-aware metrics, not just accuracy

---

## 🌱 Why this project matters

In real manufacturing environments, even small improvements in failure prediction can translate into significant cost savings and improved safety.

This project demonstrates how machine learning can be applied responsibly to **industrial reliability problems**, with an emphasis on interpretability, robustness, and business impact.

---

If you are interested in industrial ML, predictive maintenance, or applied data science for manufacturing systems, feel free to explore the notebook and experiment with the models.
