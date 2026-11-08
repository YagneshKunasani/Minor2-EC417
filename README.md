# Telecom Churn: A Model a Manager Can Use

## Project Overview
This project aims to predict which customers will leave a telecommunications service (churn). It is built for a retention team, prioritizing actionable metrics over standard accuracy. 

The models are evaluated using a fair comparison pipeline on three specific metrics: ROC-AUC, PR-AUC, and **recall in the top 10% of scores**[cite: 1, 2]. The top 10% recall represents the realistic volume of customers a management and retention team can actually contact.

## Dataset
* **Source:** IBM Telco Customer Churn (via Kaggle).
* **Details:** 7,043 customers, 21 columns (contract, tenure, services, charges).
* **Target:** Approximately 26.5% of the customers in the dataset churned.

## Repository Structure
* `download.py`: Script to programmatically download the dataset via the Kaggle API.
* `main.py`: The core pipeline containing data cleaning, the leak-free train/test split, model training, evaluation, and SHAP value generation[cite: 1, 2].
* `telecom_churn_report.pdf`: The final project report and one-page model card detailing intended use, metrics, limitations, and specific customer profiles.
* `.gitignore`: Ensures raw data, virtual environments, and binary archives are not tracked.

## Setup and Installation
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YagneshKunasani/Minor2-EC417.git](https://github.com/YagneshKunasani/Minor2-EC417.git)
   cd Minor2-EC417
