# Glass-Dataset
# 🧠 Random Forest on Glass Identification Dataset

This project applies **Random Forest**, **Bagging**, and **Boosting** algorithms to classify types of glass based on their chemical composition.  
It uses the **Glass Identification Dataset**, a well-known dataset used in forensic analysis.

---

## 📂 Project Structure


---

## 🎯 Objective

The goal is to:
1. Explore and visualize the dataset.
2. Preprocess the data (handle missing values, outliers, scaling, imbalance).
3. Implement and evaluate a **Random Forest Classifier**.
4. Compare its performance with **Bagging** and **Boosting** techniques.

---

## 📊 Dataset Description

The dataset contains measurements of different glass samples based on their oxide content.  
Each row represents a glass sample with its features and the corresponding glass type.

**Features include:**
- Refractive Index
- Sodium (Na)
- Magnesium (Mg)
- Aluminum (Al)
- Silicon (Si)
- Potassium (K)
- Calcium (Ca)
- Barium (Ba)
- Iron (Fe)

**Target Variable:**  
- Glass Type (1–7) — categorical variable indicating the glass category.

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked for missing values and data inconsistencies.
- Visualized distributions using:
  - **Correlation heatmap**
- Observed relationships among features and target classes.

---

## 🧹 Data Preprocessing

1. Converted all columns to numeric values.
2. Handled missing data using mean imputation.
3. Scaled features using **StandardScaler**.
4. Handled class imbalance using **SMOTE (Synthetic Minority Oversampling Technique)**.
5. Split the dataset into **training (70%)** and **testing (30%)** subsets.

---

## 🌳 Machine Learning Models

### 1. **Random Forest Classifier**
- Built an ensemble of decision trees.
- Evaluated using Accuracy, Precision, Recall, and F1-Score.

### 2. **Bagging Classifier**
- Implemented using `BaggingClassifier` with Random Forest as base estimator.
- Used bootstrap sampling to reduce variance.

### 3. **Boosting Methods**
- Implemented using:
  - **AdaBoost**
  - **Gradient Boosting**
- Compared results against Random Forest and Bagging.

---

## 📈 Results & Evaluation

| Model | Description | Accuracy |
|-------|--------------|-----------|
| Random Forest | Ensemble of Decision Trees | ~0.9 (varies slightly) |
| Bagging | Bootstrap Aggregating | Similar to RF |
| AdaBoost | Sequential Ensemble | Moderate |
| Gradient Boosting | Sequential Gradient Optimization | High |

*Performance may vary depending on random seeds and preprocessing.*

---

## 🧩 Key Concepts

### 🪵 Bagging
- Trains multiple models in parallel on random subsets of data.
- Reduces variance and overfitting.
- Example: Random Forest.

### 🚀 Boosting
- Trains models sequentially; each model corrects previous errors.
- Reduces bias and increases accuracy.
- Examples: AdaBoost, Gradient Boosting.

### ⚖️ Handling Imbalance
- **SMOTE** oversamples the minority class by generating synthetic examples.
- Prevents classifiers from being biased toward majority classes.

---

## 🧰 Tech Stack

- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **scikit-learn**
- **imbalanced-learn (SMOTE)**

---

## ▶️ How to Run on Google Colab

1. Upload the following files:
   - `glass.xlsx`
   - `random_forest_GLASS_dataset.ipynb`
2. Open the notebook in Google Colab.
3. Run the following to install required packages:
   ```bash
   !pip install imbalanced-learn
