# 🏡 House Price Prediction

This project predicts **median house values** in California districts using regression models.  
It demonstrates the full machine learning pipeline — from data cleaning and exploratory data analysis (EDA) to feature engineering and model evaluation.  

---

## 📊 Dataset
- **Source**: California Housing Dataset (`housing.csv`)  
- **Size**: 20,640 rows × 10 columns  
- **Features**:
  - `longitude`, `latitude` – location of the district
  - `housing_median_age` – median age of houses
  - `total_rooms`, `total_bedrooms`, `population`, `households` – housing details
  - `median_income` – median income of households
  - `ocean_proximity` – categorical feature describing closeness to ocean
- **Target**: `median_house_value` – median house price in the district

---

## ⚙️ Workflow
1. **Data Preprocessing**
   - Handled missing values (`dropna`)
   - Encoded categorical variables (`ocean_proximity` → one-hot encoding)
   - Log transformation applied to reduce skewness in numerical features
   - Standardized numerical features with `StandardScaler`

2. **Exploratory Data Analysis (EDA)**
   - Histograms to study distributions  
   - Heatmaps for correlation analysis  
   - Scatter plots (latitude vs longitude, colored by median price)

3. **Feature Engineering**
   - Created new features:
     - `bedroom_ratio = total_bedrooms / total_rooms`
     - `household_rooms = total_rooms / households`

4. **Model Training**
   - **Linear Regression**
   - **Random Forest Regressor**

5. **Model Evaluation**
   - Used R² Score to measure accuracy
   - Compared performance of both models

---

## ✅ Results
- **Linear Regression**: R² = **0.67**  
- **Random Forest Regressor**: R² = **0.80** (Best Model)  

---

## 🛠️ Tech Stack
- **Python**
- **Jupyter Notebook**
- **Libraries**:
  - `pandas`, `numpy` – data handling
  - `matplotlib`, `seaborn` – data visualization
  - `scikit-learn` – preprocessing, model building, evaluation

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/house-price-prediction.git
