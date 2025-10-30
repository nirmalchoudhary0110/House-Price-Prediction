# 🏠 House Price Prediction Using Machine Learning

## 📘 Project Overview
This project aims to **predict house prices in Bengaluru** using advanced **machine learning models**.  
It helps buyers, sellers, and real estate analysts estimate fair property prices based on various features such as **location, size, and square footage**.  
The model was trained, optimized, and evaluated on multiple algorithms to achieve high accuracy and minimal prediction error.

---

## 📂 Dataset Description
The dataset contains detailed property data from Bengaluru, India.  
Each record represents a property with the following key attributes:

| Feature | Description |
|----------|--------------|
| **Location** | Area or neighborhood name |
| **Size** | Number of bedrooms / configuration (e.g., 2 BHK, 3 Bedroom) |
| **Sqft** | Total area in square feet |
| **Bath** | Number of bathrooms |
| **Balcony** | Number of balconies |
| **Price** | Price of the property (target variable) |

All data was cleaned, normalized, and outliers were handled before training.

---

## 🧠 Model Development

Several regression algorithms were tested to find the best performer:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **LightGBM Regressor (LGBM)** ✅ *(Best performing model)*

### 🔧 Steps:
1. **Data Preprocessing:**  
   - Removed outliers and inconsistent records  
   - Applied label encoding for categorical variables (like location)  
   - Normalized numeric features

2. **Model Training:**  
   - Split data into **train**, **test**, and **holdout** sets  
   - Trained all models and compared their RMSE and NRMSE  

3. **Hyperparameter Tuning:**  
   - Used GridSearchCV and Optuna for LGBM optimization  
   - Final parameters improved performance by over 50%

---

## 📈 Evaluation Metrics

| Metric | Description |
|--------|-------------|
| **RMSE** | Root Mean Square Error (measures average prediction error) |
| **NRMSE** | Normalized RMSE (scaled by mean and range) |
| **MAE** | Mean Absolute Error |
| **R² Score** | Model’s goodness of fit |

**Final Results (LGBM):**
- **RMSE (original scale):** 46.89  
- **NRMSE (by mean):** 0.4575  
- **NRMSE (by range):** 0.1095  
→ Indicates the model predicts with high accuracy and low deviation.

---

## 📊 Results

> **Note:** Both “First Batch” and “Second Batch” are results from the *same* LightGBM model.  
> They represent predictions on two different random samples of 10 properties each,  
> allowing us to observe the model’s consistency and generalization ability.

### 🔹 First Batch - Sample of 10 Random Properties
![First Batch](images/first_batch.jpg)

### 🔹 Second Batch - Another Sample of 10 Random Properties
![Second Batch](images/second_batch.jpg)

### 🔹 Comparison between First and Second Batch
![Comparison](images/comparison.jpg)

**Observations:**
- Both batches are generated using the same model.  
- The comparison highlights the model’s consistent performance across random samples.  
- Prediction errors remain stable and within acceptable limits for most cases.  
- LightGBM demonstrates strong generalization and minimal overfitting.
