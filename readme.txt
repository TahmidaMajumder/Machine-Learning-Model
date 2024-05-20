Dataset used in this model is from Kaggle. Link: https://www.kaggle.com/datasets/azharsaleem/real-estate-goldmine-dubai-uae-rental-market

About the dataset: This dataset provides a detailed snapshot of rental property listings across major cities in the United Arab Emirates, including Abu Dhabi, Dubai, Sharjah, Ajman, Ras Al Khaimah, Umm Al Quwain, and Al Ain. Gathered from bayut.com, it includes various attributes such as property type, size, rent, and location details, making it a valuable resource for data-driven insights into the UAE rental market. Ideal for data analysts, researchers, and real estate professionals, this dataset allows for comprehensive analysis of trends, pricing, and market dynamics in the UAE's diverse rental landscape.

Shape: (73742, 17)

1. Problem Statement
- I wanted to understand the factors that affect the Rents also able to predict Rents based on the data/variables.

2. Data Preprocessing
- Before training the data I did Exploratory Data Analysis(EDA).
- Data cleaning(impute missing data, drop unnecessary column/feature)
- Data visualization(correlation , scatter plot, etc..)
- Investigate Categorical Values using various plot
- Investigating the distribution and outliers with Box plots
	- Find outliers both in Numeric and Categorical Column(box plot, self define 		function(Using lower and upper bound))
	- Remove outliers both in Numeric and Categorical Column(self define function(Using 	lower and upper bound))
- Converting Categorical Feature to Numerical Representation(One Hot Encoding)
- Finding Feature Importance
	- Splitting X & y.
	- Running Decision Tree(max_depth = 10)
	- Function to find feature importance 
	- Calculate Feature Importance
- Splitting Raw Data for validation and training
	- Feature Scaling(StandardScaler()) using pipeline
	- Train Model & Predict (R^2, RMSE, MAE Score)
		- Linear Regression
		- KNeighbors Regressor(n_neighbors=2)(Highest Score for R^2)
		- Neural Network Regressor
		- Random Forest Regressor
- Hyperparameter Tuning
	- Splitting X(top 10 correlation feature with respect to Rent) & y
	- Feature Scaling(StandardScaler()) using pipeline
	- Train Model & Predict (R^2, RMSE, MAE Score)
		- Linear Regression
		- KNeighbors Regressor(n_neighbors=2)(Highest Score for R^2)
		- Neural Network Regressor
		- Random Forest Regressor

KNeighbors Regressor was able to pull r2 score of 99.7% on training and 98.8% on testing.