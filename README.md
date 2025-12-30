#### Dataset Link : https://www.kaggle.com/datasets/harrimansaragih/dummy-advertising-and-sales-data
## Project Overview
________________________
> This project focuses on predicting Sales
> based on different advertising channels
> such as TV, Radio, and Social Media.
> Multiple regression-based machine learning 
> models are implemented and compared to
> identify the best-performing model

##  Dataset Description
_______________________________
> **Dataset Link** : 
> Dataset: Dummy Advertising and Sales Data
> Total Records: 4572
 
> **Features**:

- TV – Advertising budget on TV
- Radio – Advertising budget on Radio
- Social Media – Advertising budget on Social Media
- Influencer – Type of influencer (Mega, Macro, Micro, Nano)
- Sales – Target variable (Sales)
- 
##  Data Preprocessing
_________________________

**Missing Value Treatment**
> Missing values in TV, Radio, Social Media, and Sales 
> were handled using random value imputation
> from existing data distributions.


**Outlier Detection & Handling**
> Boxplots were used to detect outliers.
> Social Media column contained significant outliers.
> Outliers were handled using IQR-based
> capping to reduce their impact.


**Feature Selection**
> Influencer column was removed for regression models.
> REASON :
 
    The Main reason why i removed influencer 
    because is has minimal corelation with sales data
    and hence it may create noise while training
    
>  Final input features:
- TV
- Radio
- Social Media

 
**Exploratory Data Analysis**
- Boxplots used to analyze feature distributions.
- Scatter plots used to observe relationships between advertising channels and sales.
- Sales showed a strong positive relationship with TV advertising.

## Models Implemented
___________________________________

### 1️. Linear Regression

> Features scaled using StandardScaler
 
> **Performance:**
 
_ **R² Score:**  = **0.98**
_ **MSE:**  =     **154**

### 2️. Random Forest Regressor

**Hyperparameter tuning using GridSearchCV**

> Best n_estimators: 50
 
> **Performance:**

**R² Score:** = **0.9967**
**MSE: = 28.5**

### Polynomial Regression (Degree = 3)

> Polynomial feature expansion applied

> **Performance:**
> **R² Score: ~0.9966**
> **MSE: ~28.7**

### XGBoost Regressor

> Hyperparameter tuning using GridSearchCV

**Best n_estimators** : **50**

> **Performance:**
**R² Score:** =  **0.9937**
**MSE:** =       **52.2**

## Model Comparison Summary
_________________________________
Model	R² Score	MSE
Linear Regression	~0.98	~154
Random Forest	~0.9967	~28.5
Polynomial Regression	~0.9966	~28.7
XGBoost	~0.9937	~52.2

✅ Random Forest Regressor performed best overall.

## ⚙️ Installation and Usage
_______________________________

> Follow the steps below to set up the project locally:
 
> - **1️. Clone the Repository**
 
    git clone https://github.com/your-username/advertising-sales-prediction.git
    cd advertising-sales-prediction
   
> - **2 Create Virtual Environment**
 
    python -m venv venv
    source venv/bin/activate # For Linux / Mac
    venv\Scripts\activate    # For Windows
   
> - **3️ Install Required Libraries**

     pip install numpy pandas matplotlib
     seaborn scikit-learn statsmodels xgboost



  
