# 🚗 Price Prediction of Used Cars using Machine Learning

📊 Dataset: [Craigslist Cars & Trucks – Kaggle](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)

---

## 🧠 Project Summary
This project builds a **machine learning pipeline** to predict **used car prices** from large-scale Craigslist listings.  
Using 427K+ data points and 26 attributes (e.g., year, manufacturer, fuel, condition, odometer), the team developed and compared multiple regression models to identify the most accurate price predictor.

---

## ⚙️ Key Workflow
1. **Exploratory Data Analysis (EDA):**  
   Statistical overview, correlation matrix, and outlier detection.  

2. **Data Cleaning:**  
   - Removed 53K duplicate rows.  
   - Handled missing values via imputation and categorical replacement (`unknown`).  
   - Standardized numeric columns (`year`, `odometer`, `price`).  

3. **Feature Engineering:**  
   - Encoded categorical columns using One-Hot & Ordinal Encoding.  
   - Normalized continuous variables with `StandardScaler`.  
   - Removed irrelevant pre-2000 vehicle records.  

4. **Modeling:**  
   Trained and evaluated multiple regression algorithms:  
   - **Linear Regression** – Baseline  
   - **K-Nearest Neighbors (KNN)**  
   - **Decision Tree Regressor**  
   - **XGBoost Regressor (Best Performer)**  

---

## 📈 Results

| Model | R² Score | MAE | RMSE | Notes |
|--------|----------|------|------|-------|
| Linear Regression | 0.65 | 5305 | 7010 | Good baseline |
| KNN Regressor | 0.81 | 3135 | 5217 | Solid non-parametric model |
| Decision Tree | 0.79 | 2561 | 5482 | Interpretable but prone to overfit |
| **XGBoost Regressor** | **0.897** | **2239** | **4457** | 🚀 Best performing model |

✅ **XGBoost achieved an R² score of 89.7%**, showing strong predictive performance and generalization.

---

## 🧰 Tech Stack
- **Language:** Python 3.11  
- **Libraries:** pandas · numpy · matplotlib · seaborn · scikit-learn · XGBoost  
- **Tools:** Jupyter / Google Colab  
- **Dataset Source:** Kaggle (Craigslist Cars & Trucks)

---

## 🔍 Insights
- Car **year**, **odometer**, and **manufacturer** were the most influential predictors.  
- **Fuel type** and **condition** had moderate effects on pricing trends.  
- Outlier removal and scaling substantially improved model performance.  

---

## 🚀 Future Improvements
- Implement **hyperparameter tuning** for XGBoost using `GridSearchCV`.  
- Integrate **deep learning regression (ANN)** for non-linear pattern capture.  
- Deploy as a **Flask API** for real-time price estimation.  
- Add **interactive dashboard (Streamlit / PowerBI)** for visual analytics.

---


---

## 📜 Reference Links
- [Project Report PDF](./DS675005_project_final_report_teamnumber-02_MohanSai_Bandarupalli.pdf)  
- [Kaggle Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)

Presentation Link: https://drive.google.com/file/d/125kwwRN-sYcBy3TnVXN-UXcfkAc34zHc/view?usp=drive_link
