
# House Price Prediction - Machine Learning Project

## 📌 Overview
This project predicts house prices based on property features (area, location, BHK, furnishing, etc.) using regression-based machine learning models. It covers the complete ML pipeline — data cleaning, EDA, feature engineering, model training, evaluation, and prediction on new data.

## 📂 Files in this Repository
| File | Description |
|------|-------------|
| `house_price_dataset.xlsx` | Raw dataset with property details and prices |
| `house_price_cleaned.xlsx` | Cleaned dataset (output after EDA/cleaning step) |
| `house_price_EDA.py` | Data cleaning + exploratory data analysis with visualizations |
| `house_price_model_building.py` | Feature engineering, model training, and evaluation |
| `house_price_best_model.pkl` | Saved trained model |
| `model_columns.pkl` | Saved column order used for encoding (for consistent predictions on new data) |
| `README.md` | Project documentation |

## 🧹 Data Cleaning Steps
- Handled missing values (Area, Furnishing, HasLift, NearbySchools)
- Removed duplicate records
- Fixed inconsistent text formatting (casing, extra whitespace)
- Removed invalid/outlier values (e.g., unrealistic property age, extreme area values)

## 📊 Exploratory Data Analysis
- **Univariate Analysis:** Price distribution, Area distribution, City-wise property counts, BHK distribution
- **Bivariate Analysis:** Average price by city, Price vs Area, Price by BHK/Furnishing/Locality Type, Price vs Age of property, Price vs Distance from city center
- **Correlation Heatmap:** Relationship between numerical features and Price

## 🤖 Model Building
- **Feature Engineering:** One-Hot Encoding for categorical variables, feature scaling for linear models
- **Models Trained & Compared:**
  - Linear Regression
  - Lasso Regression (L1 Regularization)
  - Ridge Regression (L2 Regularization)
  - Random Forest Regressor
  - Gradient Boosting Regressor
- **Evaluation Metrics:** MAE, RMSE, R² Score

## ✅ Model Validation
To ensure the model generalizes well and isn't overfitting:
- Compared Train vs Test R² scores (small gap confirms no overfitting)
- Performed 5-Fold Cross-Validation to verify score stability across different data splits
- Plotted Actual vs Predicted values and residual plots to visually inspect prediction quality

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Joblib (model persistence)

## ▶️ How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib openpyxl
python house_price_EDA.py              # Step 1: Cleaning + EDA
python house_price_model_building.py   # Step 2: Model training + evaluation
```

## 🔍 Key Insights
_(Add your findings here after running the analysis, e.g.)_
- [City] had the highest average property prices
- [Feature] was the most important predictor of price
- Best performing model: [Model Name] with R² score of [X]%
- Train-Test score gap was minimal, confirming the model generalizes well

## 🚀 Future Scope
- Hyperparameter tuning (GridSearchCV) to further improve accuracy
- Add more features like proximity to metro stations, crime rate, etc.
- Deploy the model as a web app (Streamlit/Flask) for interactive price prediction
