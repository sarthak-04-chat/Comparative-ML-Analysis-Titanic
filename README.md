# Comparative-ML-Analysis-Titanic

## 📌 Overview
This project applies various Machine Learning algorithms to the classic Titanic dataset to predict passenger survival. The goal is to compare the performance and accuracy of different classification models, highlighting the end-to-end process of data preprocessing, feature engineering, and model evaluation.

## 🛠️ Technologies & Libraries Used
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn

## 📊 Dataset
The dataset used is the standard `titanic` dataset loaded directly via Seaborn. It contains demographic and travel information for the passengers, such as:
* `pclass`: Ticket class (1st, 2nd, 3rd)
* `sex`: Gender
* `age`: Age in years
* `fare`: Passenger fare
* `embarked`: Port of Embarkation
* `survived`: Target variable (0 = No, 1 = Yes)

## ⚙️ Methodology

### 1. Data Cleaning & Preprocessing
* Handled missing values (e.g., filled missing `age` values with the mean, dropped rows with missing `embarked` data).
* Dropped redundant or unnecessary columns (`who`, `adult_male`, `deck`, `embark_town`, `alive`, `class`) to reduce noise.

### 2. Feature Engineering
* **Label Encoding:** Converted categorical text variables (`sex`, `embarked`, `alone`) into numerical formats using `LabelEncoder`.
* **Feature Scaling:** Applied `StandardScaler` to normalize the feature ranges, which is critical for distance-based algorithms like KNN and SVM.

### 3. Model Building & Evaluation
The data was split into training (80%) and testing (20%) sets. Five different classification models were trained and evaluated using Accuracy Score, Confusion Matrix, and Classification Reports:

| Model | Accuracy Score |
|-------|----------------|
| **Support Vector Machine (SVM)** | **~82.6%** |
| Logistic Regression | ~80.3% |
| K-Nearest Neighbors (KNN) | ~79.2% |
| Gaussian Naive Bayes | ~77.5% |
| Decision Tree Classifier | ~75.8% |

*Note: Cross-validation (cv=5) was also performed on the SVM and KNN models to ensure robust performance metrics, yielding mean accuracies of ~82.8% and ~79.7% respectively.*


# 🚗  Car Price Prediction

## 📌 Project Overview
This project focuses on building a machine learning workflow to predict the prices of used Ford cars based on various vehicle performance, specification, and market features. Using Python's data science ecosystem, the project covers data ingestion, comprehensive exploratory data analysis (EDA), and data preprocessing techniques like categorical feature encoding.  
IPYNB
+ 1

## 📊 Dataset Features
The dataset (ford.csv) consists of 17,966 records and 9 structural columns:  
IPYNB

### Target Variable:

price: The listed price of the used vehicle.  
IPYNB

### Numerical Features:

year: The vehicle's registration year.  
IPYNB

mileage: Total miles the car has been driven.  
IPYNB

tax: Road tax applied to the vehicle.  
IPYNB

mpg: Fuel efficiency measured in miles per gallon.  
IPYNB

engineSize: Engine capacity of the car.  
IPYNB

### Categorical Features:

model: The specific Ford car model (e.g., Fiesta, Focus, Puma, Kuga, EcoSport).  
IPYNB

transmission: Gearbox type (e.g., Manual, Automatic, Semi-Auto).  
IPYNB

fuelType: Engine fuel category (e.g., Petrol, Diesel, Hybrid, Electric, Other).  
IPYNB

##  🛠️ Project Workflow
### 1. Data Ingestion & Initial Inspection
Loaded structured tabular vehicle data from a CSV file into a Pandas DataFrame.  
IPYNB

Inspected structural data types and verified the shape of the dataset.  
IPYNB

Executed missing value audits (df.isnull().sum()) to confirm a completely clean dataset with zero null values across all dimensions.  
IPYNB

Evaluated central tendencies and data distributions using descriptive statistical summaries.  
IPYNB

### 2. Exploratory Data Analysis (EDA)
Target Distribution: Generated a distribution histogram with an overlaid kernel density estimate (KDE) line to analyze price spreads.  
IPYNB

Correlation Mapping: Calculated a correlation matrix and visualized it using a Seaborn heatmap to detect multi-collinearity and linear relationships among continuous variables.  
IPYNB

Categorical Visualizations: Built relational boxplots (sns.boxplot) to analyze how distinct categories—such as vehicle models, transmission configurations, fuel types, engine sizes, and tax tiers—impact resale pricing.  
IPYNB

### 3. Data Preprocessing & Feature Engineering
Isolated independent structural features (X) from the target pricing label (y).  
IPYNB

Implemented One-Hot Encoding using pd.get_dummies with a drop-first configuration to transform categorical features into safe, multi-column boolean structures for regression models.  
IPYNB

Implemented Label Encoding using Scikit-learn's LabelEncoder as an alternative technique to map text categories into single-column integer sequences.  
IPYNB

## 💻 Tech Stack & Libraries
Language: Python  
IPYNB

Data Frameworks: Pandas, NumPy  
IPYNB

Visualization: Seaborn, Matplotlib  
IPYNB

Machine Learning Tools: Scikit-learn (LabelEncoder)  
IPYNB

Environment: Jupyter Notebook  
IPYNB



