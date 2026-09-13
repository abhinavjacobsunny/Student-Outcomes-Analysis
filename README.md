# 📊 Student Performance Analysis

## 📌 Project Overview

**Student Performance Analysis** is a Data Science and Machine Learning project that investigates how socio-economic, behavioral, and learning-environment factors are associated with student academic performance.

The project performs a complete data science workflow, including **data cleaning, exploratory data analysis (EDA), statistical analysis, data preprocessing, visualization, regression modeling, and model evaluation** to predict students' `Exam_Score`.

This project was **built as part of the Data Science & AI Internship/Training Program at India Data Research Academy (IDRA)**.

---

## 🎯 Objectives

* Analyze factors associated with student academic performance.
* Identify and handle missing, invalid, and inconsistent data.
* Explore relationships between student characteristics and `Exam_Score`.
* Perform exploratory and statistical analysis.
* Prepare numerical and categorical features for machine learning.
* Build and compare multiple regression models.
* Evaluate model performance using MAE, RMSE, and R².
* Identify the model with the best generalization performance.

---

## 📂 Dataset

The project uses the **Student Performance Factors** dataset supplied for the IDRA Data Science & AI Capstone Project.

### Dataset Details

| Property              | Details                |
| --------------------- | ---------------------- |
| Records               | 6,607                  |
| Features              | 19 predictor variables |
| Total Columns         | 20                     |
| Numerical Variables   | 7                      |
| Categorical Variables | 13                     |
| Target Variable       | `Exam_Score`           |

The dataset contains information related to study habits, attendance, parental involvement, educational resources, motivation, family income, teacher quality, peer influence, and other student characteristics.

---

## 🔍 Exploratory Data Analysis

The analysis investigates:

* Exam score distribution
* Attendance vs. exam score
* Study hours vs. exam score
* Numerical feature correlations
* Parental involvement
* Access to educational resources
* Peer influence
* Descriptive statistics
* Potential outliers and data-quality issues

The analysis found that **Attendance** had the strongest numerical association with `Exam_Score` (`r ≈ 0.581`), followed by **Hours_Studied** (`r ≈ 0.445`).

---

## 🧹 Data Cleaning & Preprocessing

The following steps were performed:

* Missing-value identification
* Most-frequent imputation for categorical variables
* Median imputation for numerical variables
* Duplicate-record verification
* Invalid `Exam_Score` removal
* One-hot encoding of categorical variables
* Standard scaling of numerical features
* 80/20 train-test split
* Prevention of data leakage through pipeline-based preprocessing

One invalid exam score of `101` was removed, resulting in **6,606 records after cleaning**.

---

## 🤖 Machine Learning Models

Three regression algorithms were trained and compared:

1. **Linear Regression**
2. **Random Forest Regressor**
3. **Gradient Boosting Regressor**

The models were evaluated using:

* **Mean Absolute Error (MAE)**
* **Root Mean Squared Error (RMSE)**
* **R² Score**

---

## 📈 Model Performance

| Model             | Test RMSE |  Test MAE |   Test R² |
| ----------------- | --------: | --------: | --------: |
| Linear Regression | **1.521** | **0.416** |     0.711 |
| Random Forest     |     1.912 |     1.028 | **0.877** |
| Gradient Boosting |     1.764 |     0.850 |     0.712 |

**Linear Regression** was selected as the final model because it achieved the lowest test RMSE and MAE and demonstrated more consistent train-test performance. Random Forest showed a larger train-test gap, indicating overfitting.

---

## 💡 Key Findings

* **Attendance** was the strongest numerical predictor of exam performance.
* **Study hours** showed a positive association with exam scores.
* Students with higher **parental involvement** tended to have higher average scores.
* Better **access to educational resources** was associated with higher average performance.
* **Positive peer influence** was associated with better average exam scores.
* Linear Regression provided the most consistent generalization among the evaluated models.

> **Note:** The findings represent predictive and associative relationships and should not be interpreted as causal effects.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computing
* **Matplotlib** – Data visualization
* **Scikit-learn** – Machine learning and preprocessing
* **Jupyter Notebook / Google Colab** – Development environment

---

## 📁 Project Structure

```text
Student-Performance-Analysis/
│
├── P_2_StudentPerformanceFactors.csv
├── Student_Performance_Analysis.ipynb
├── README.md
└── report/
    └── Capstone_Project_Report.pdf
```

---

## 🚀 Workflow

```text
Dataset
   ↓
Data Loading & Inspection
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Statistical Analysis
   ↓
Data Preprocessing
   ↓
Train-Test Split
   ↓
Regression Modeling
   ↓
Model Evaluation
   ↓
Final Model Selection
   ↓
Findings & Recommendations
```

---

## 🔮 Future Improvements

Potential future extensions include:

* Testing Ridge and Lasso regression.
* Improving tree-based models through hyperparameter tuning.
* Incorporating additional socio-economic and well-being variables.
* Validating the model on data from other academic cohorts.
* Exploring classification approaches such as pass/fail or performance categories.

---

## 🎓 Internship / Training

This project was developed as part of the **Data Science & AI Training Program at India Data Research Academy (IDRA)** and served as the capstone project for applying data analysis and machine learning concepts to a real-world-style dataset.

---

## 👨‍💻 Author

**Abhinav Jacob Sunny**

Data Science & AI Trainee
Vimal Jyothi Engineering College, Chemperi

---

## 📄 License

This project is intended for **educational and academic purposes** as part of the IDRA Data Science & AI training program.
