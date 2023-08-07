# Data-Analysis-using-KNIME-and-Data-Visualization-using-PowerBI


## 1. Data Profiling 

### a. Key Insights

- Data has 14 columns and 1899 rows showing individual food orders
- Key attributes: order ID, customer ID, restaurant name, cuisine, cost, rating, preparation time etc
- Important data types:
  - Numeric - Cost, rating, preparation time
  - Categorical - Cuisine, day of week
  - Text - Order ID, customer ID, restaurant name

In summary, probing the data uncovered crucial metadata about columns, rows, features and data types to facilitate deeper analysis.

### b. Data Cleaning 

- Filled missing values using average for numerical columns and removing rows for textual columns
- Removed duplicate rows to avoid statistical bias
- Added total_time column combining preparation_time and delivery_time
- Standardized customer_region using rules to expand abbreviations 
- Converted order_ID and customer_ID columns to strings
- Removed irrelevant columns like order_ID and preparation_time
- Label encoded string columns like cuisine_type and day_of_week

In summary, multiple data wrangling techniques in KNIME were used to clean, shape and prepare the data while retaining original feature names.

### c. Other Improvements

- Handled class imbalance via SMOTE oversampling
- Normalized numerical features using z-score and min-max scaling  
- Identified highly correlated variables through correlation analysis
- Removed collinear inputs to derive optimal predictors

Together, these crucial data preparation steps transformed the data into the best dataset to feed into ML models.

## 2. Linear Regression

- Developed linear model to predict customer ratings using predictors like cost, order volume, prep time etc.
- Model quantified impact of factors through regression coefficients and statistical tests like p-values.
- Key drivers like cost, frequency, prep time showed significant explanatory power.  
- But overall model performance was only moderate (R-squared ~0.62).
- Substantial unexplained variance highlights complex non-linear effects.
- Enhancements through more variables, non-linear models and tuning can improve predictions.

In essence, the linear model establishes a baseline with important factors. But insights reveal avenues to further boost accuracy through sophisticated modeling.

## 3. Clustering 

- Applied k-means clustering to segment restaurants based on traits like cost, rating, demand etc.
- Transformed order volume into buckets - Low, Mid, High and Very High.
- Cluster profiles showed notable differences:
  - Group 0: Upscale restaurants with expensive food, high ratings and orders
  - Group 1: Casual dining with average costs and ratings
  - Group 2: Fast food chains with lower prices but high volumes
  - Group 3: Budget eateries with lower metrics and diverse cuisines
- Checking traits pointed to a segmentation of high-end, mid-range, fast casual and economical restaurants. 
- Relating clusters to features provided customer and competitive insights for strategic decisions.

In summary, thoughtful preprocessing and analysis enabled data-driven restaurant segmentation to inform tailored branding, marketing and positioning strategies per cluster.
