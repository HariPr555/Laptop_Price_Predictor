# Laptop_Price_Predictor
This project focuses on developing a laptop price prediction system using machine learning models to forecast prices based on key laptop specifications such as brand, RAM, screen size, CPU, and storage. Several models, including Linear Regression, Ridge, Lasso, Decision Tree, and Random Forest were implemented and evaluated. The Random Forest model delivered the highest accuracy with an R² score of 0.855 and MAE of 0.178.
This system can help the company optimize pricing strategies, manage inventory based on pricing trends, and gain deeper insights into the features that influence laptop pricing.

# 1. Background
SmartTech Co has consistently delivered cutting-edge laptops that cater to both consumers and professionals worldwide. Committed to quality and customer satisfaction, the company leverages the latest technologies to enhance user experiences. They are now looking to leverage data science to enhance their pricing strategies and gain a competitive edge in the market.

# 2. Project Objectives
The Primary goal is to develop a robust machine learning model that predicts laptop prices accurately. As the market for laptops continues to expand with a myriad of brands and specifications, having a precise pricing model becomes crucial for both consumers and manufacturers.
- Accurate Pricing: Develop a model that can accurately predict laptop prices based on various features, helping our clients stay competitive in the market.
- Market Positioning: Understand how different features contribute to pricing, enabling SmartTech Co. to strategically position its laptops in the market.
- Brand Influence: Assess the impact of brand reputation on pricing, providing insights into brand perception and market demand.


# 3. Technical Stacks
- **Scripting**: Python
- **Frameworks**: PANDAS, NUMPY, MATPLOTLIB, SEABORN, SKLEARN
- **GUI**: Gradio
- **Data Source**: CSV containing Laptop Data

# 4. Data Understanding
The Laptop Pricing Data from SmartTech Co includes 1303 records with various features such as:
- **Branding Feautures**: Company Name, TypeName
- **Specifications Features**: Inches, ScreenResolution, CPU, RAM, Memory, GPU, OS, Weight
- **Pricing**: Price

# 5. Data Preprocessing
- **Remove Empty Columns and Rows**: Identify and remove any empty columns and rows.
- **Remove Duplicate**s: Deduplication of data to avoid redundancy.
- **Rename Columns**: Ensure appropriate names are used for better analysis.
- **Change Data Types**: Ensure columns have appropriate data types (e.g., dates, numbers, text).
- **Handle null values**: No null values once the unnamed columns were removed.
- **Feature Scaling**: Replaced and formatted values to maintain data consistency.
- **Feature Selection**: Selected relevant features and dropped the irrelevant columns.
- **Feature Extraction**: Created new columns for better understanding and to avoid multicollinearity.
- **Feature Encoding**: Encodes the categorical features to Numeric data to build ML model.

# 6. Exploratory Data Analysis (EDA)
- **Price Distribution**
  - The price of laptops ranges from approximately ₹9,270 to ₹324,955, with a median price of ₹52,161.
  - The price distribution suggests a mix of budget, mid-range, and premium laptops.
- **Top Laptop Brands**
  - The most common brands are Lenovo (290 entries), Dell (287), and HP (266), followed by Asus (156) 
  - High-end brands like Apple (21) and premium gaming brands like Razer (7) are less common.
- **CPU and RAM**
  - There are a variety of CPU models, mainly Intel Core i5 and i7 processors.
  - RAM sizes include popular configurations such as 8GB and 16GB, indicating a focus on mainstream and high-performance laptops.
- **Laptop Types**
  - The majority of laptops are standard notebooks (710), followed by gaming laptops (203), and ultrabooks (191).
  - Convertible laptops (2-in-1) account for 116 entries, suggesting a growing market for versatile devices.









