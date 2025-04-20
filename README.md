# 📊 EDA & Regression Modeling on Store Sales Dataset

This project explores and models a store sales dataset using **Exploratory Data Analysis (EDA)** and multiple **machine learning regression algorithms**. The goal is to understand key drivers of store sales and compare models that can accurately predict them. 

## 📁 Project Structure

1. **Data Loading**  
   Load the sales dataset using Pandas and inspect the first few rows.

2. **Data Cleaning & Exploration**  
   - Dropped redundant columns  
   - Explored basic stats and structure  
   - Visualized missing values  
   - Inspected distributions and unique values  
   - Identified outliers using boxplots and LOF (Local Outlier Factor)

3. **Feature Analysis**  
   - Calculated correlations with the target variable `Store_Sales`  
   - Generated heatmaps for top correlated features  
   - Analyzed relationships using pair plots

4. **Outlier Detection & Removal**  
   Used **LocalOutlierFactor** to detect and remove anomalies in the data to improve model reliability.

5. **Model Training & Evaluation**  
   Trained multiple regression models and compared their performance using **RMSE** (Root Mean Squared Error) and **MAE** (Mean Absolute Error):
   - `RandomForestRegressor`
   - `LinearRegression`
   - `ElasticNet`
   - `KNeighborsRegressor`
   - `XGBRegressor`

## 🧠 Model Performance Summary

| Model                | RMSE            | MAE        |
|---------------------|-----------------|------------|
| LinearRegression     | 254,003,891.85  | 13,228.17  |
| ElasticNet           | 254,003,889.17  | 13,228.17  |
| KNeighborsRegressor  | 299,733,602.93  | 14,503.15  |
| RandomForestRegressor| 321,968,351.02  | 14,861.22  |
| XGBRegressor         | 344,107,232.00  | 15,160.01  |

## ✅ Key Insights & Conclusion

- **Linear Regression** and **ElasticNet** performed best with the lowest RMSE and MAE, suggesting they are well-suited for predicting store sales.
- **RandomForest** and **XGBoost** showed higher error, but may still be useful for uncovering complex nonlinear patterns and customer behavior trends.
- To increase store sales, strategies like:
  - Enhancing **product availability**
  - Stimulating **impulse buying**
  - Improving **store layout**
  - Using **cross-promotions**
  can be effective, as shown by patterns captured in the models.

## 🚀 How to Run the Notebook

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/store-sales-analysis.git
   cd store-sales-analysis
   ```
2. Open the notebook using [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
3. Mount your Google Drive and update the path to the dataset if needed.
4. Run each cell step by step.

## 📦 Requirements

Install required packages (if not using Colab):
```bash
pip install pandas numpy matplotlib seaborn missingno scikit-learn xgboost
```
