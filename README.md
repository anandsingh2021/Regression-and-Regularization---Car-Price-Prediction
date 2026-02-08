Car Price Prediction using Regularised Regression
Overview
This project builds a robust machine learning regression model to predict used car prices using historical vehicle data. The study focuses not only on predictive accuracy but also on model generalisation and interpretability through Ridge and Lasso regularisation techniques.
The solution demonstrates how data-driven pricing can help used car resellers make consistent, competitive, and profitable pricing decisions.

Problem Statement
Used car pricing depends on multiple variables such as:
•	Mileage
•	Vehicle age
•	Engine power
•	Fuel type
•	Safety & comfort features
•	Overall vehicle condition
Manual or rule-based pricing often leads to inconsistent decisions. This project aims to develop a statistically robust regression model for accurate and stable price prediction. 
Dataset
•	Source: AutoScout (German used-car marketplace)
•	Records: 15,915
•	Features: 23 attributes
•	Target Variable: price (log-transformed to log_price) 
Feature Categories
•	Numerical: Age, Mileage, Engine Power, Weight, Fuel Consumption
•	Categorical: Fuel Type, Body Type, Transmission, Drive Chain
•	Bundled Features: Comfort, Safety, Entertainment, Extras 

Data Processing
•	No missing values detected
•	Log transformation applied to price (to correct skewness)
•	Low-frequency categories grouped to reduce sparsity
•	Outliers capped using percentile clipping (1st & 99th percentile)
•	Feature scaling using StandardScaler 

Feature Engineering
•	Converted bundled feature lists into count-based variables:
o	Comfort_Convenience_count
o	Safety_Security_count
o	Entertainment_Media_count
o	Extras_count
•	Derived feature: Power-to-weight ratio 

Models Implemented
1. Linear Regression (Baseline)
•	R² ≈ 0.92
•	Good fit but showed multicollinearity
2. Ridge Regression
•	Handles multicollinearity
•	Optimal Alpha ≈ 0.001
•	Improved coefficient stability
3. Lasso Regression
•	Performs feature selection
•	Optimal Alpha ≈ 0.0001
•	Eliminated low-impact features
All models achieved similar predictive performance, with Ridge improving robustness and Lasso simplifying the model. 
Key Insights
•	Price strongly influenced by mileage, age, engine power, weight, and safety features
•	Regularisation improves model stability
•	Lasso provides a simpler, interpretable model without losing accuracy
•	Predictive pricing helps resellers make data-driven pricing decisions 
Assumptions & Limitations
•	Historical prices reflect fair market value
•	External factors (location, seasonality, seller behaviour) not included
•	Log transformation assumed appropriate for linear modelling 
Conclusion
Regularised regression techniques effectively model used car prices while balancing:
•	Accuracy
•	Robustness
•	Interpretability
•	Ridge: Best when features are correlated
•	Lasso: Best for simpler, feature-selected models
This approach reduces overfitting and supports real-world pricing decisions. 
Repository Structure
├── Car_Price_data.csv
├── Regularisation_Car_Price_Prediction_Anand_Singh.ipynb
├── Regularisation_Car_Price_Prediction_Anand_Singh.pdf
├── README.md

Tech Stack
•	Python
•	Pandas, NumPy
•	Scikit-learn
•	Matplotlib / Seaborn
<end of document>
