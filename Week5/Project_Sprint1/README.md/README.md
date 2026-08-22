# Customer Churn Risk Prediction & Analysis

An end-to-end machine learning project for predicting customer churn, identifying high-risk customers, understanding the factors behind churn, and supporting customer retention decisions.

**Status:** Phase 3 — Capstone Project | Sprint 1 (Data Understanding & Baseline) — Planning Complete, Implementation In Progress

---

## 1. Project Overview

Customer churn occurs when a customer stops using a company's products or services. Companies usually discover this only after the customer has already left.

This project goes beyond a simple Yes/No churn prediction by building a **Customer Churn Risk System** that:

* Predicts the probability that a customer will churn.
* Assigns the customer a clear risk level.
* Identifies the main factors contributing to that risk.
* Suggests a possible retention action.

### System Flow

```text
Customer Data
      ↓
EDA & Preprocessing
      ↓
Churn Prediction Model
      ↓
Churn Probability
      ↓
Risk Level
      ↓
Risk Factors
      ↓
Recommended Action
```

## 2. Problem Statement

The main challenge is identifying customers who are likely to leave **before** they actually churn.

This project uses customer data to build a machine learning solution that flags high-risk customers and explains the factors behind their risk, so the business can act early instead of reacting after the customer is already gone.

## 3. Project Objectives

* Understand the customer churn dataset through Exploratory Data Analysis (EDA).
* Clean and preprocess the data.
* Build a baseline classification model.
* Compare and evaluate different machine learning models.
* Improve the selected model using appropriate techniques.
* Predict churn probability for individual customers.
* Convert churn probability into Low, Medium, and High risk levels.
* Identify the main factors contributing to churn risk.
* Provide possible customer retention actions.
* Deploy the final solution as a usable application.

## 4. Dataset

|                      |                                  |
| -------------------- | -------------------------------- |
| **Selected Dataset** | IBM Telco Customer Churn Dataset |
| **Size**             | 7,043 customers × 21 columns     |
| **Problem Type**     | Binary Classification            |
| **Target Variable**  | `Churn` (Yes / No)               |
| **Source**           | IBM Sample Datasets              |

The dataset contains customer demographics, subscribed services, account and contract details, payment methods, and billing information — a combination of features well suited to explaining and predicting churn.

**Note:** the `TotalCharges` column contains 11 blank entries that need to be converted to numeric and handled during preprocessing.

## 5. Expected System Output

For each customer, the system provides:

| Output             | Description                                        |
| ------------------ | -------------------------------------------------- |
| Churn Probability  | Estimated probability that the customer will churn |
| Risk Level         | Low, Medium, or High                               |
| Prediction         | Likely to Churn or Likely to Stay                  |
| Risk Factors       | Main factors contributing to the customer's risk   |
| Recommended Action | Suggested customer retention action                |

**Example**

```text
Customer: C1024
Churn Probability: 82%
Risk Level: HIGH
Prediction: Likely to Churn

Main Risk Factors:
- Short contract
- Low engagement
- High monthly cost

Recommended Action:
Offer a retention plan
```

## 6. Project Scope — Four Sprints

| Sprint       | Focus                                                                                                                               |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint 1** | Data Understanding & Baseline — dataset selection, cleaning, EDA, preprocessing, baseline model                                     |
| **Sprint 2** | Model Development & Improvement — train/compare multiple models, feature engineering, handle class imbalance, hyperparameter tuning |
| **Sprint 3** | Risk Analysis & Explainability — churn probabilities, risk levels, key churn factors, retention recommendations                     |
| **Sprint 4** | Deployment & Finalization — build and integrate the final app, test the system, finalize documentation                              |

### Sprint 1 — Current Sprint

**Goal:** Understand the IBM Telco Customer Churn Dataset, complete initial data analysis and preprocessing, and establish a reliable baseline classification model that later sprints can improve on.

| ID  | Task                      | Status    |
| --- | ------------------------- | --------- |
| T1  | Dataset Selection         | ✅ Done    |
| T2  | Data Understanding        | ⬜ Pending |
| T3  | Data Cleaning             | ⬜ Pending |
| T4  | Exploratory Data Analysis | ⬜ Pending |
| T5  | Data Preprocessing        | ⬜ Pending |
| T6  | Baseline Model            | ⬜ Pending |
| T7  | Baseline Evaluation       | ⬜ Pending |
| T8  | Documentation             | ⬜ Pending |
| T9  | GitHub Setup              | ✅ Done    |

## 7. Definition of Done

The project is considered complete when:

* The complete ML pipeline is documented.
* EDA and preprocessing are implemented.
* A baseline model is trained and evaluated, and multiple models are compared.
* The final model is selected based on evaluation results.
* Churn probability and risk levels are generated for customers.
* Important risk factors are identified and retention recommendations are provided.
* The final solution is deployed.
* A clean GitHub repository is maintained with `README.md`, `requirements.txt`, model artifacts, and a short technical write-up.

## 8. Technology Stack

| Category         | Tools               |
| ---------------- | ------------------- |
| Language         | Python              |
| Data Analysis    | Pandas, NumPy       |
| Visualization    | Matplotlib          |
| Machine Learning | Scikit-learn        |
| Development      | Jupyter Notebook    |
| Deployment       | Streamlit / FastAPI |
| Version Control  | Git & GitHub        |

## 9. Repository Structure

```text
Project_Sprint1/
│
├── data/              # Raw and processed datasets
├── notebooks/         # EDA, preprocessing, and modeling notebooks
├── src/                # Reusable Python scripts (preprocessing, training, etc.)
├── models/            # Saved trained model artifacts
├── app.py             # Deployment app (Streamlit / FastAPI)
├── requirements.txt   # Project dependencies
└── README.md          # Project documentation (this file)
```

## 10. How to Run (once implemented)

```bash
# 1. Clone the repository
git clone <repo-url>
cd Project_Sprint1

# 2. Install dependencies
pip install -r requirements.txt

# 3. Explore the notebooks
jupyter notebook notebooks/

# 4. Run the app
streamlit run app.py
```

## 11. Project Status

| Item            | Status                                      |
| --------------- | ------------------------------------------- |
| Phase           | Phase 3 — Capstone Project                  |
| Current Sprint  | Sprint 1                                    |
| Current Focus   | Data Understanding, EDA, and Baseline Model |
| Mentor Sign-off | Pending                                     |