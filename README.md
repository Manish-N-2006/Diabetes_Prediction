# Diabetes Prediction using Machine Learning

## 📌 Project Overview
This project focuses on analyzing healthcare data and predicting diabetes using machine learning techniques.  
The objective is to handle real-world medical data challenges such as missing values, perform exploratory data analysis (EDA), and evaluate multiple machine learning models using appropriate metrics.

---

## 📊 Dataset
- **Dataset:** Pima Indians Diabetes Dataset  
- **Target Variable:** Diabetes (0 = No Diabetes, 1 = Diabetes)
- Medical features include glucose level, blood pressure, BMI, insulin, age, and others.
- Some medical features contain missing values represented as `0`, which are not clinically valid.
- **Dashboard:** Also added in repo.

---

## 🧹 Data Preprocessing

### Handling Missing Values
- **Glucose:**  
  - Zero values were replaced using **median imputation**, as glucose data can contain outliers and median is robust. Because it has only few zero rows.
- **Other medical features:**  
  - The following columns were handled using **KNN Imputation**:
    ```
    ['Pregnancies', 'BloodPressure', 'SkinThickness', 'Insulin', 'BMI']
    ```
  - KNN imputation estimates missing values based on similar patient records, helping preserve relationships between features.

---

## 🔍 Exploratory Data Analysis (EDA)
- Distribution analysis of key medical features
- Comparison of diabetic vs non-diabetic patients
- Outlier detection using box plots
- Visualization of relationships between features and diabetes outcome

EDA was used to understand patterns and risk factors before model training.

---

## 🤖 Machine Learning Models Evaluated
The following machine learning models were trained and evaluated:

### 1️⃣ Logistic Regression
- **Accuracy:** 77.92%
- **Confusion Matrix:**
  [[89 10]
  [24 31]]

- **Classification Report:**
- Precision (Diabetes = 1): 0.76  
- Recall (Diabetes = 1): 0.56  
- F1-score (Diabetes = 1): 0.65  

---

### 2️⃣ Random Forest Classifier
- **Accuracy:** 82.47%
- **Confusion Matrix:**
  [[87 12]
  [15 40]]

- **Classification Report:**
- Precision (Diabetes = 1): 0.77  
- Recall (Diabetes = 1): 0.73  
- F1-score (Diabetes = 1): 0.75  

---

### 3️⃣ K-Nearest Neighbors (KNN)
- **Accuracy:** 73.38%
- **Confusion Matrix:**
  [[82 17]
  [24 31]]

- **Classification Report:**
- Precision (Diabetes = 1): 0.65  
- Recall (Diabetes = 1): 0.56  
- F1-score (Diabetes = 1): 0.60  

---

## 📈 Model Selection Rationale
Although Logistic Regression and KNN achieved reasonable accuracy, **Random Forest** demonstrated the best overall performance, particularly in terms of **recall**.

In healthcare-related problems, recall is a critical metric because:
- A **false negative** (missed diabetes case) can be harmful
- Higher recall helps identify more high-risk patients

👉 **Final Model Selected:** Random Forest Classifier

---
### Dashboard Preview
![Dashboard Preview](Dashboard.pdf)

---
## 🛠 Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Google Colab

---

## 🧠 Key Learnings
- Handling real-world missing healthcare data
- Using KNN imputation for realistic value estimation
- Importance of recall over accuracy in healthcare ML problems
- Role of EDA and visualization before predictive modeling

---

By Manish N
