# Customer Churn Prediction

## Overview

This project predicts whether a telecom customer is likely to churn (leave the service) or remain with the company. The solution combines Exploratory Data Analysis (EDA), Machine Learning, and Streamlit deployment.

The project uses the Telco Customer Churn dataset and implements a Random Forest Classifier to make predictions based on customer service and billing information.

---

## Project Files

| File                           | Description                                                               |
| ------------------------------ | ------------------------------------------------------------------------- |
| `Telecom_Customer_Churn.ipynb` | Data exploration, visualization, preprocessing, and model experimentation |
| `churn_main.py`                | Model training script that trains and saves the Random Forest model       |
| `churn_app.py`                 | Streamlit web application for real-time churn prediction                  |
| `Telco_Customer_Churn.csv`     | Dataset used for training and analysis                                    |
| `random_forest_model.joblib`   | Saved trained model                                                       |

---

## Project Workflow

```text
Dataset
   │
   ▼
Data Cleaning
   │
   ▼
Exploratory Data Analysis
   │
   ▼
Feature Engineering
   │
   ▼
Model Training
   │
   ▼
Random Forest Model
   │
   ▼
Model Saving (.joblib)
   │
   ▼
Streamlit Deployment
```

---

## Exploratory Data Analysis

The Jupyter Notebook includes:

* Dataset exploration
* Missing value handling
* Churn distribution analysis
* Gender distribution analysis
* Senior citizen analysis
* Contract type analysis
* Correlation analysis
* Feature importance visualization

### Libraries Used

* Pandas
* NumPy
* Matplotlib
* Seaborn

---

## Data Preprocessing

* Converted `TotalCharges` to numeric format.
* Replaced missing values using the median.
* Removed unnecessary columns (`customerID`).
* Converted Churn values:

  * Yes → 1
  * No → 0
* Applied One-Hot Encoding.
* Scaled features using MinMaxScaler.

---

## Machine Learning Models

### Logistic Regression

Used as a baseline classification model.

### Random Forest Classifier

Used as the final model for churn prediction.

Features used in deployment:

* Tenure
* Internet Service
* Contract Type
* Monthly Charges
* Total Charges

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Streamlit
* Joblib

---

## Installation

### Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn streamlit joblib
```

---

## Train the Model

```bash
python churn_main.py
```

This creates:

```text
random_forest_model.joblib
```

---

## Run the Streamlit App

```bash
streamlit run churn_app.py
```

---

## Sample Prediction

### Input

* Tenure = 24
* Internet Service = Fiber Optic
* Contract = Month-to-Month
* Monthly Charges = 80
* Total Charges = 1920

### Output

```text
This customer is likely to churn.
```

---

## Future Improvements

* Hyperparameter tuning
* XGBoost implementation
* Churn probability scoring
* Feature importance dashboard
* Cloud deployment

---

## Author

**Shobhita Sisodia**

B.Tech Biotechnology | Aspiring AI/ML Engineer

### Skills

Python | SQL | Statistics | Machine Learning | Deep Learning | NLP | Streamlit | Scikit-learn
