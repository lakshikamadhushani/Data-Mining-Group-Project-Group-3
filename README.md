# Student Performance Prediction - Data Mining Project

A comprehensive data mining analysis to predict student academic success using machine learning techniques including classification, clustering, and association rule mining.

## 📊 Project Overview

This project analyzes student performance data from secondary school students to predict academic success (pass/fail) based on demographic, social, and school-related features. The analysis combines multiple data mining techniques to provide insights into factors affecting student performance and identify at-risk students.

**Main Objectives:**

- Predict student academic success using supervised learning models
- Identify distinct student segments through clustering analysis
- Discover patterns in student characteristics using association rule mining
- Provide actionable insights for educational interventions

## 📁 Dataset

The project uses the **Student Performance Dataset** which includes data from two Portuguese schools:

- **student-mat.csv**: Math course performance (395 students)
- **student-por.csv**: Portuguese course performance (649 students)

**Key Features (33 attributes):**

- **Demographic**: age, sex, address, family size, parent's cohabitation status
- **Social**: parent's education and jobs, family relationships, romantic status
- **School-related**: study time, failures, absences, educational support, extracurricular activities
- **Behavioral**: going out with friends, alcohol consumption, health status
- **Academic**: G1 (first period grade), G2 (second period grade), G3 (final grade - target)

**Target Variable:** Binary classification - Pass (G3 ≥ 10) or Fail (G3 < 10)

For detailed attribute descriptions, see `student.txt`.

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries:**
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computing
  - `scikit-learn` - Machine learning models and preprocessing
  - `matplotlib` & `seaborn` - Data visualization
  - `mlxtend` - Association rule mining

## 📋 Project Structure

```
Group Project/
│
├── data_mining_project.ipynb    # Main Jupyter notebook with full analysis
├── student-mat.csv              # Math course student data
├── student-por.csv              # Portuguese course student data
├── student.txt                  # Dataset attribute descriptions
├── student-merge.R              # R script to merge datasets
├── Data Mining Project.pdf      # Project documentation
├── README.md                    # This file
└── cleaned_student_data.csv     # Generated cleaned dataset (after running notebook)
```

## 🚀 Getting Started

### Prerequisites

Install required Python packages:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn mlxtend jupyter
```

### Running the Analysis

1. Clone or download this repository
2. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `data_mining_project.ipynb`
4. Run all cells sequentially (Cell → Run All)

**Note:** Update the file path in Cell 2 if your data files are in a different location.

## 📊 Analysis Workflow

### 1. **Exploratory Data Analysis (EDA)**

- Dataset inspection and descriptive statistics
- Distribution analysis of numeric and categorical features
- Correlation analysis to identify relationships
- Class balance evaluation (pass vs fail rates)

### 2. **Data Preprocessing**

- Missing value handling (median for numeric, mode for categorical)
- Feature encoding (One-Hot Encoding for categorical variables)
- Target variable creation (Pass: G3 ≥ 10, Fail: G3 < 10)
- Train-test split with stratification

### 3. **Supervised Learning (Classification)**

Three classification models are trained and evaluated:

- **Logistic Regression** - Baseline linear model
- **Random Forest** - Ensemble tree-based model
- **Gradient Boosting** - Advanced boosting model

**Evaluation Metrics:**

- Accuracy, Precision, Recall, F1-Score
- ROC AUC Score
- Cross-validation (5-fold Stratified K-Fold)
- Confusion Matrix
- Feature Importance Analysis

### 4. **Unsupervised Learning (Clustering)**

- **K-Means Clustering** to identify student segments
- Elbow method for optimal cluster selection
- PCA (Principal Component Analysis) for 2D visualization
- Cluster characteristic analysis

### 5. **Association Rule Mining**

- Frequent itemset discovery using Apriori algorithm
- Association rule generation with lift metric
- Pattern analysis in categorical features

### 6. **Visualizations & Reporting**

- ROC curves for model comparison
- Confusion matrices
- Feature importance charts
- Cluster visualizations
- Performance metric comparisons

## 📈 Key Findings

### Model Performance

- All three models achieve strong predictive performance
- Cross-validation ensures robust generalization
- Feature importance analysis reveals key predictors of success

### Important Features

Top factors influencing student success (typical findings):

- Previous failures
- Study time
- Absences
- Parent's education level
- Going out frequency
- Age

### Student Segments

K-Means clustering identifies distinct student groups with different:

- Academic performance levels
- Study habits and behaviors
- Socioeconomic backgrounds
- Risk profiles
