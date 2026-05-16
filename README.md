### A Comprehensive Analysis of Product and Outlet
**Author:** Moamen ayyad

## Business problem:
Retailers face significant challenges in managing inventory and setting prices without a clear understanding of what drives sales. This analysis aims to predict product sales across various outlets, allowing management to optimize stock levels and identify high-performing store characteristics to improve overall profitability.

## Data:
The dataset consists of 8,523 observations and 12 features, including product attributes (weight, fat content, price) and outlet information (size, location, establishment year). The source data provides historical sales figures which serve as our target variable.

## Methods
- **Missing Data Handling:** Imputed `Item_Weight` with the median and `Outlet_Size` with the most frequent category to maintain dataset integrity without losing valuable rows.
- **Feature Engineering:** Corrected inconsistent categorical labels in `Item_Fat_Content` (e.g., 'LF' to 'Low Fat') to ensure clean data for the model.
- **Scaling & Encoding:** Applied Standard Scaling to numerical features and One-Hot Encoding to categorical features via a Scikit-Learn Pipeline to prevent data leakage and prepare the features for regression algorithms.

## Results

### Correlation of Features vs. Sales
![heat_map.png](https://github.com/devMoamen/Prediction-of-Product-Sales/blob/main/heat_map.png)

Maximum Retail Price (`Item_MRP`) shows the strongest positive relationship with sales (r = 0.57), suggesting that pricing strategy is the primary lever for revenue.

### Actual vs. Predicted Performance
![feature_vs_target.png](https://github.com/devMoamen/Prediction-of-Product-Sales/blob/main/feature_vs_target.png)

## Model
The final model is a **Tuned Random Forest Regressor** optimized via GridSearchCV.

**Performance Metrics:**
- **R² Score:** 0.604
- **MAE:** $727.90
- **RMSE:** $1,044.93

The model explains approximately 60.4% of the variance in sales. With an average error (MAE) of $727.90, the model provides a reliable baseline for monthly inventory planning, significantly reducing the risk of massive overstock or understock scenarios.

## Recommendations:
1. **Focus on High-Tier Pricing:** Since MRP is a high driver, emphasize premium product tiers in high-performing locations.
2. **Scale Supermarket Type 3:** This outlet type showed the highest average sales; future expansions should mirror the operational structure of these specific stores.

## Limitations & Next Steps
- **Limitations:** The model struggles with extremely high-value outliers (unusually high sales) which are not fully captured by current features.
- **Next Steps:** Incorporate external data such as local economic indicators or promotional calendars to capture more variance in sales fluctuations.

## For further information
For any additional questions, please contact **moamen.ayyad@email.com**
