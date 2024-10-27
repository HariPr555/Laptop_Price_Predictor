# Laptop_Price_Predictor
This project focuses on developing a laptop price prediction system using machine learning models to forecast prices based on key laptop specifications such as brand, RAM, screen size, CPU, and storage. Several models, including Linear Regression, Ridge, Lasso, Decision Tree, and Random Forest were implemented and evaluated. The Random Forest model delivered the highest accuracy with an R² score of 0.887 and MAE of 0.178.
This system can help the company optimize pricing strategies, manage inventory based on pricing trends, and gain deeper insights into the features that influence laptop pricing.

## Background
SmartTech Co has consistently delivered cutting-edge laptops that cater to both consumers and professionals worldwide. Committed to quality and customer satisfaction, the company leverages the latest technologies to enhance user experiences. They are now looking to leverage data science to enhance their pricing strategies and gain a competitive edge in the market.

## Project Objectives
The Primary goal is to develop a robust machine learning model that predicts laptop prices accurately. As the market for laptops continues to expand with a myriad of brands and specifications, having a precise pricing model becomes crucial for both consumers and manufacturers.
- **Accurate Pricing**: Develop a model that can accurately predict laptop prices based on various features, helping our clients stay competitive in the market.
- **Market Positioning**: Understand how different features contribute to pricing, enabling SmartTech Co. to strategically position its laptops in the market.
- **Brand Influence**: Assess the impact of brand reputation on pricing, providing insights into brand perception and market demand.


## Technical Stacks
- **Scripting**: Python
- **Frameworks**: Pandas, Numpy, Matplotlib, Seaborn, SkLearn
- **GUI**: Gradio
- **Data Source**: CSV containing Laptop Data

## Data Understanding
The Laptop Pricing Data from SmartTech Co includes 1303 records each with 13 features that includes:
- **Branding Feautures**: Company Name, TypeName
- **Specifications Features**: Inches, ScreenResolution, CPU, RAM, Memory, GPU, OS, Weight
- **Pricing**: Price

## Data Preprocessing
- **Remove Empty Columns and Rows**: Identify and remove any empty columns and rows.
- **Remove Duplicate**s: Deduplication of data to avoid redundancy.
- **Rename Columns**: Ensure appropriate names are used for better analysis.
- **Change Data Types**: Ensure columns have appropriate data types (e.g., dates, numbers, text).
- **Handle null values**: No null values once the unnamed columns were removed.
- **Feature Scaling**: Replaced and formatted values to maintain data consistency.
- **Feature Selection**: Selected relevant features and dropped the irrelevant columns.
- **Feature Extraction**: Created new columns for better understanding and to avoid multicollinearity.
- **Feature Encoding**: Encodes the categorical features to Numeric data to build ML model.

## Exploratory Data Analysis (EDA)
### Price Distribution
  - The price of laptops ranges from approximately ₹9,270 to ₹324,955, with a median price of ₹52,161.
  - The price distribution suggests a mix of budget, mid-range, and premium laptops.
### Top Laptop Brands
  - The most common brands are Lenovo (290 entries), Dell (287), and HP (266), followed by Asus (156) 
  - High-end brands like Apple (21) and premium gaming brands like Razer (7) are less common.
### CPU and RAM
  - There are a variety of CPU models, mainly Intel Core i5 and i7 processors.
  - RAM sizes include popular configurations such as 8GB and 16GB, indicating a focus on mainstream and high-performance laptops.
### Laptop Types
  - The majority of laptops are standard notebooks (710), followed by gaming laptops (203), and ultrabooks (191).
  - Convertible laptops (2-in-1) account for 116 entries, suggesting a growing market for versatile devices.

## Independent and Dependent Features
- **Independent Features**: Company, Type Name, RAM (GB), Operating System, Weight, Touchsreen, IPS, PPI, CPU name, HDD, SSD, GPU Brand.
- **Dependent Features**: Price

## Splitting the dataset
The dataset is split into training and testing sets in 80% and 20% respectively, with X_train having a shape of (1082, 12) and X_test (191, 12) using train_test_split(). This division ensures the model can be trained on a substantial portion of the data while still being evaluated on unseen data.

## Choose a Machine Learning Model
Multiple regression models were selected to predict the Price of laptops based on their features. Models included:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor

## Model Training
Each model is trained on the training set using model.fit().

## Model Testing
Each model is tested on the testing set using model.predict(). The performance is measured using appropriate metrics (e.g., R² and Mean Absolute Error) to assess how well the model learns the relationship between features and the target variable (Price).

## Model Evaluation
The performance metrics (R² and MAE) indicate how well each model predicts the price. The Random Forest Regressor achieved the highest R² score (0.855) and the lowest MAE (0.178), indicating it is the best model among those tested.

![image](https://github.com/user-attachments/assets/90f3a52b-a58c-4cf4-8c2b-567f4d244248)

## Regularization
Regularization techniques like Lasso (L1) and Ridge (L2) add a penalty to large coefficients, which can help reduce overfitting. Since the R² scores of Linear Regression (0.783), Lasso (0.793), and Ridge (0.795) are quite close, it indicates that the added complexity of Lasso and Ridge might not be necessary for your dataset. They might be providing some slight improvement, but not enough to suggest significant benefits. Regularization techniques generally shine in scenarios with more features, multicollinearity, or noise in the data, so their advantages can be context-dependent.

## Hyperparameter Tuning
Hyperparameter tuning is performed to optimize the models' performance. RandomizedSearchCV is used to find the best hyperparameters for Random Forest and Decision Tree regressors.
- **Parameters** : 'max_depth', 'max_features', 'ccp_alpha','min_samples_split','min_samples_leaf', n_estimators
- **CV**: 5
- **Best Model with scores and estimators**
  - 'model_name': 'RandomForest',
  - 'best_score': -0.07980855657507552,
  - 'best_estimator': RandomForestRegressor(ccp_alpha=0.0025, criterion='mse', max_depth=30,max_features='log2', min_samples_leaf=5, min_samples_split=10, n_estimators=1077

## Deployment
A Gradio app was built for deployment, allowing users to input laptop specifications and receive price predictions. This step makes the model accessible for real-time use.

![image](https://github.com/user-attachments/assets/8dcdb8da-6f9d-46fb-a3c0-6c1aa427c9df)

