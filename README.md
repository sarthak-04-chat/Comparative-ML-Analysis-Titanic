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



