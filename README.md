## Prediction of Product Sales

**Author:** Moamen ayyad

### Project Overview
In the competitive retail landscape, accurately predicting sales is vital for effective inventory management and revenue growth. This project analyzes historical sales data to identify key factors—such as product price, visibility, and store type—that drive performance.

### Methodology
1. **Data Cleaning:** Handled missing values (Item_Weight and Outlet_Size) and corrected inconsistent categorical entries (Item_Fat_Content).
2. **Exploratory Data Analysis (EDA):** Visualized distributions and correlations to identify primary drivers of sales.
3. **Preprocessing:** Utilized Scikit-Learn pipelines to handle imputation, scaling for numerical data, and one-hot encoding for categorical features.
4. **Modeling:** Evaluated Linear Regression and Random Forest models.
5. **Optimization:** Performed Hyperparameter tuning via GridSearchCV to maximize model performance.

### Key Findings
- **Item_MRP (Price):** Showed the strongest positive correlation with sales (r = 0.57).
- **Outlet Type:** 'Supermarket Type 3' outlets significantly outperformed smaller formats like Grocery Stores.
- **Item Visibility:** Showed a surprising weak negative correlation, suggesting high visibility is often assigned to lower-turnover items.

### Final Model Performance
The **Tuned Random Forest Regressor** was selected as the final model:
- **Testing R²:** 0.604 (60.4% of variance explained)
- **Testing MAE:** $727.90
- **Testing RMSE:** $1,044.93

### Technical Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-Learn

### How to Use
1. Ensure you have the dataset `sales_predictions_2023.csv`.
2. Run the notebook to see the data cleaning, visualization, and modeling steps.
3. Use the final `best_rf_model` pipeline for predictions on new data.
