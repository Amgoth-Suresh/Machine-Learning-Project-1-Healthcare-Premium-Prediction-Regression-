# Machine Learning — Premium Prediction

This repository contains a full **data science and machine learning pipeline** to predict insurance premium amounts based on customer demographics, financial status, and risk factors. The workflow includes **data cleaning, exploratory data analysis (EDA), feature engineering, model training, and evaluation**.

> Notebook: **`ml_premium_prediction.ipynb`**

## 📂 Project Structure
```
.
├── ml_premium_prediction.ipynb   # Main Jupyter Notebook for the project
├── data/                          # (Optional) Folder for datasets
└── README.md                      # Project documentation
```

> Note: The notebook expects the dataset in CSV format (update the file path in the notebook if needed).

## 📦 Requirements
Install the following Python packages (or use `requirements.txt`):

```
pandas
numpy
matplotlib
seaborn
scikit-learn
statsmodels
xgboost
notebook
```

Install with:
```bash
pip install -r requirements.txt
```

## 🔍 Workflow Overview

### **1. Data Loading & Inspection**
- Import raw CSV data using **pandas**
- Initial inspection of shapes, column types, and missing values

### **2. Data Cleaning**
- Handle missing values and duplicates
- Specific cleaning for numerical and categorical variables (e.g., `number_of_dependants`)
- Type conversions and formatting

### **3. Exploratory Data Analysis (EDA)**
- **Univariate analysis** for numeric and categorical variables
- **Bivariate analysis** to identify relationships between predictors and target variable
- Boxplots, histograms, bar plots for visualization

### **4. Outlier Treatment**
- Identify and treat outliers in `Age`, `Income`, and other numeric features

### **5. Feature Engineering**
- Risk score calculation
- Encoding of categorical variables (`LabelEncoder`, `OneHotEncoder`)
- Feature scaling
- Variance Inflation Factor (VIF) calculation for multicollinearity

### **6. Model Development**
Implemented models include:
- **Linear Regression**
- **Ridge Regression**
- **XGBoost Regressor**

### **7. Model Evaluation**
- Evaluate models using metrics such as:
  - R² Score
  - Mean Squared Error (MSE) / Root Mean Squared Error (RMSE)
- Compare performance across algorithms

### **8. Post-Processing**
- Reverse scaling transformations for predictions

## 📊 Libraries Used
- **pandas** — data manipulation
- **numpy** — numerical operations
- **matplotlib** & **seaborn** — visualization
- **scikit-learn** — preprocessing, modeling, evaluation
- **statsmodels** — statistical tests & VIF calculation
- **xgboost** — gradient boosting regression

## ▶️ Running the Project
1. Place the dataset in the correct path (update the notebook cell if needed).
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `ml_premium_prediction.ipynb`.
4. Run cells sequentially to reproduce the workflow.

## 📌 Next Steps / Improvements
- Hyperparameter tuning for XGBoost and Ridge Regression
- Add cross-validation for better model generalization
- Save trained models (`joblib`/`pickle`) for deployment
- Integrate pipeline into a web app (Flask/Streamlit)

## 📄 License
Specify your license (MIT, Apache 2.0, etc.)

---
**Author:** Amgoth Suresh  
**Notebook:** `ml_premium_prediction.ipynb`
