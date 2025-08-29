# Predictive Maintenance Modeling for Aircraft Engine Failure
## About This Project

Have you ever wondered if we could predict when a machine is about to fail? This project tackles that exact question for one of the most critical machines of all: an aircraft engine. The main goal here is to use data from engine sensors to predict its **Remaining Useful Life (RUL)**—basically, how much longer the engine can run safely before it needs maintenance.

By accurately forecasting this, airlines can move from a fixed maintenance schedule to a much smarter **predictive maintenance** strategy. This means fixing parts right before they break, which saves money, increases safety, and improves efficiency.

This repository contains the complete code and analysis for this data science project.

---

## The Dataset 📊

This project uses the famous **NASA Turbofan Engine Degradation Simulation Dataset**. It's a collection of data from multiple simulated aircraft engines. For each engine, we have:

* **Time-series data:** Readings from 21 different sensors over many operational cycles.
* **Operational settings:** Information about the engine's settings during each cycle.
* **Failure data:** The data tracks each engine until it fails.

---

## Approach 🛠️

The process for solving this problem involved a few key steps:

1.  **Data Cleaning:** The first step was to load the raw data, give the columns meaningful names, and remove any empty or unnecessary columns to keep the dataset clean.

2.  **Feature Engineering:** This was the most important step! Since the dataset doesn't explicitly tell us the RUL for each cycle, we had to create it. Calculated the RUL by finding the last cycle of an engine's life and then counting backwards, creating our target variable for the models to predict.

3.  **Data Scaling:** The sensor values were all on different scales. To help the models learn better, normalized all the feature data to a common scale (between 0 and 1).

4.  **Modeling:** Built and compared four different machine learning models to see which one could predict the RUL most accurately.

---

## Models  Tested 🤖

Experimented with a range of models, from simple baselines to more complex neural networks:

* **Linear Regression:** A simple model to set a baseline performance score.
* **Random Forest:** A powerful ensemble model that uses multiple decision trees.
* **XGBoost:** A highly efficient and popular gradient-boosting model known for its performance.
* **LSTM (Long Short-Term Memory):** A specialized neural network designed to understand patterns in sequential data, like our time-series sensor readings.

---

## Results and Conclusion 📈

After training and evaluating all four models, the **LSTM model was the clear winner**.

While Random Forest and XGBoost performed well, the LSTM's ability to recognize patterns over time allowed it to make the most accurate predictions. This is because engine failure isn't a single event—it's a process of degradation over many cycles. The LSTM's architecture is perfectly suited to learn this kind of sequential pattern.

**Final Verdict:** For a critical task like predicting engine failure, the superior accuracy of the **LSTM model** Makes it the best and most effective choice for this problem.

---

## How to Run This Project 🚀

To run this notebook yourself, follow these steps:

1.  **Clone the repository or open in https://colab.research.google.com/drive/1-5BQK4GFH7eCoPXDdMFG1-KdtSUzpNvh**.
    ```bash
    git clone https://github.com/Nikhil-AGI/Predictive-Maintenance-Modeling-for-Aircraft-Engine-Failure.git
    ```
3.  **Install the required libraries:**
    ```bash
    pip install pandas numpy scikit-learn tensorflow keras xgboost matplotlib seaborn
    ```
4.  **Open the notebook:**
    Launch Jupyter Notebook or Google Colab and open the `Predictive_Maintenance_Modeling_for_Aircraft_Engine_Failure.ipynb` file.

5.  **Run the cells:**
    Execute the cells in order from top to bottom.







