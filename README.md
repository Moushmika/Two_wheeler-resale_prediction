# **🚀Predicting Two-Wheeler Resale Value Using Machine Learning**

A machine learning case study for predicting the resale value of used two-wheelers using historical motorcycle marketplace data and Multiple Linear Regression.

## **📌 Problem Statement**
Determining a fair resale price for a used motorcycle is challenging because price depends on factors such as vehicle age, kilometers driven, ownership history, brand, seller type, and original ex-showroom price.
This project develops a data-driven pricing model to estimate a reasonable resale value and support sellers, buyers, and used-bike marketplaces in making better pricing decisions.

## **🎯 Objectives**

Analyze factors influencing two-wheeler resale prices.
Perform data cleaning and exploratory data analysis.
Engineer meaningful features such as bike age and brand.
Build a Multiple Linear Regression model.
Evaluate the model using R², MAE, and RMSE.
Perform residual analysis and hypothesis testing.
Extract practical business insights.

## **📊 Dataset**

The project uses the BIKE DETAILS dataset containing 1,061 motorcycle records.
Feature
Description
Name
Motorcycle name
Selling_price
Used-bike selling price — target variable
Year
Manufacturing year
Seller_type
Type of seller
owner
Ownership category
km_driven
Kilometers driven
ex_showroom_price
Original ex-showroom price
Engineered Features
bike_age — calculated from the manufacturing year.
Brand — extracted from the motorcycle name.

## **🛠️ Technologies Used**

Python
Google Colab 
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
SciPy

## **🔄 Methodology**

Dataset Collection
       ↓
Data Inspection
       ↓
Missing Value Treatment
       ↓
Feature Engineering
       ↓
Exploratory Data Analysis
       ↓
Categorical Encoding
       ↓
80:20 Train-Test Split
       ↓
Multiple Linear Regression
       ↓
Prediction
       ↓
Model Evaluation
       ↓
Residual Analysis
       ↓
Hypothesis Testing
       ↓
Business Insights

## **🔧 Data Preparation**

Loaded and inspected the dataset.
Checked dimensions, data types, and missing values.
Handled missing ex_showroom_price values using median imputation.
Created bike_age from the manufacturing year.
Extracted brand from the name column.
Applied One-Hot Encoding to categorical variables.
Split the data into 80% training and 20% testing sets.

## **📈 Exploratory Data Analysis**

EDA included selling-price distributions, boxplots, correlation analysis, brand-wise analysis, and residual/actual-vs-predicted visualizations.
Key Correlations
Feature
Correlation with Selling Price

## **🤖 Machine Learning Model**

Multiple Linear Regression
Multiple Linear Regression was selected because the target variable, selling_price, is continuous and the model provides an interpretable relationship between the predictors and resale price.

Input features:
Bike age
Kilometers driven
Seller type
Owner
Brand
Ex-showroom price
Categorical variables were processed using OneHotEncoder within a Scikit-learn pipeline.

## **📊 Model Performance**

Metric
Result
R² Score
MAE
RMSE

Interpretation
R² = 0.807: Approximately 80.7% of resale-price variation is explained by the model.
MAE = ₹16,192: Average absolute prediction error is approximately ₹16,192.
RMSE = ₹22,545: Larger prediction errors have a stronger effect on this metric.

## **🧪 Statistical Analysis**

A hypothesis test was conducted to examine whether Royal Enfield and Bajaj motorcycles have significantly different selling prices.
H₀: There is no significant difference between the groups.
H₁: There is a significant difference between the groups.
T-statistic: 21.96
P-value: 7.35 × 10⁻⁶⁹
Since the p-value is far below 0.05, H₀ is rejected, indicating a statistically significant difference between the groups in this dataset.

## **💡 Key Findings**

Ex-showroom price is the strongest predictor of resale value.
Older motorcycles generally have lower resale prices.
Higher kilometers driven is associated with lower resale value.
The model achieved an R² of 0.807 on the test data.
Brand differences show a statistically significant association with selling price.

## **💼 Business Value**

The model can help used-bike marketplaces.
Provide data-driven price recommendations.
Reduce underpricing and overpricing.
Help sellers set competitive listing prices.
Help buyers evaluate fair market prices.
Improve consistency in automated vehicle valuation.

## **🚀 Future Improvements**

Future versions can incorporate:
	Vehicle condition
	Service and maintenance history
	Accident history
	Location
	Insurance validity
	Market demand and seasonal trends
	Model-specific depreciation
	Advanced models such as Random Forest, Gradient Boosting, and XGBoost can also be compared with Linear Regression.

## **📁 Suggested Repository Structure**

two-wheeler-resale-value-prediction/
│
├── README.md
├── notebooks/
│   └── two_wheeler_resale_prediction.ipynb
├── data/
│   └── README.md
├── outputs/
│   └── plots/
├── presentation/
│   └── Two_Wheeler_Resale_Value_Case_Study.pptx
└── requirements.txt

## **▶️ How to Run**

Google Colab
Open the project notebook in Google Colab.
Upload the dataset when prompted.
Run the notebook cells sequentially.
Review the generated visualizations, predictions, and evaluation metrics.

## **👥 Project Information**

Project: Predicting Two-Wheeler Resale Value Using Machine Learning
Domain: Automotive / Used Vehicle Marketplace
Task: Regression
Primary Model: Multiple Linear Regression
Target Variable: selling_price

## **📜 Conclusion**

The project demonstrates how machine learning can estimate used two-wheeler resale values from historical marketplace data. The Multiple Linear Regression model achieved an R² score of 0.807, showing that the selected vehicle and pricing attributes provide substantial predictive information. The approach provides an interpretable foundation for data-driven pricing recommendations and can be enhanced with richer vehicle-condition and market-demand features.
