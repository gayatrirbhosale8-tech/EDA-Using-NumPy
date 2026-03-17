## STUDENT DATA

# 🧹 Data Preprocessing: Dealing with Missing Values

---

## 📌 Overview

Data preprocessing is a crucial step in data analysis and machine learning. One of the most common challenges is handling **missing values**, which can affect the performance and accuracy of models.

---

## ❓ What are Missing Values?

Missing values occur when data is not stored for a particular feature.

### 🔍 Representations:

* `NaN` (Not a Number)
* `NULL`
* Empty cells
* Special symbols (`?`, `-999`)

---

## ⚠️ Why Handle Missing Values?

* 📉 Prevents biased results
* ⚙️ Ensures smooth algorithm execution
* 📊 Improves data quality
* 🧠 Enhances model accuracy

---

## 🔎 Types of Missing Data

| Type | Description                  |
| ---- | ---------------------------- |
| MCAR | Missing Completely At Random |
| MAR  | Missing At Random            |
| MNAR | Missing Not At Random        |

---

## 🛠️ Techniques to Handle Missing Values

### 1️⃣ Removing Missing Data

✔️ Used when missing data is small

#### 🔹 Syntax:

```python
# Remove rows with missing values
df.dropna()

# Remove columns with missing values
df.dropna(axis=1)
```

---

### 2️⃣ Imputation (Filling Missing Values)

#### 📊 Mean / Median / Mode

✔️ Best for numerical/categorical data

```python
# Mean
df['Age'].fillna(df['Age'].mean(), inplace=True)

# Median
df['Age'].fillna(df['Age'].median(), inplace=True)

# Mode
df['City'].fillna(df['City'].mode()[0], inplace=True)
```

---

### 3️⃣ Forward Fill & Backward Fill

```python
# Forward Fill
df.fillna(method='ffill', inplace=True)

# Backward Fill
df.fillna(method='bfill', inplace=True)
```

---

### 4️⃣ Interpolation 📈

✔️ Useful for time-series data

```python
df.interpolate(method='linear', inplace=True)
```

---

### 5️⃣ Machine Learning Imputation 🤖

```python
from sklearn.impute import KNNImputer

imputer = KNNImputer(n_neighbors=3)
df_imputed = imputer.fit_transform(df)
```

---

### 6️⃣ Flag Missing Values 🚩

```python
df['Missing_Age'] = df['Age'].isnull()
```

---

## ⚖️ Comparison: Raw vs Cleaned Dataset

| Feature         | 🗂️ Raw Dataset (`student_data.csv`) | 🧼 Cleaned Dataset (`cleaned_dataset.csv`) |
| --------------- | ------------------------------------ | ------------------------------------------ |
| Missing Values  | ❌ Present                            | ✅ Handled                                  |
| Data Quality    | ⚠️ Inconsistent                      | ✔️ Clean & Structured                      |
| Model Readiness | ❌ Not suitable                       | ✅ Ready for ML                             |
| Errors          | High chance                          | Reduced                                    |
| Analysis        | Unreliable                           | Accurate                                   |

---

## 📊 Key Differences Explained

### 🔴 Raw Dataset

* Contains missing/null values
* May have inconsistent entries
* Requires preprocessing before use

### 🟢 Cleaned Dataset

* Missing values handled (removed/imputed)
* Standardized format
* Ready for analysis and model training

---

## 📦 Libraries Used

* 🐍 Pandas
* 🔢 NumPy
* 🤖 Scikit-learn

---

## 📈 Best Practices

* ✔️ Analyze missing data before handling
* ✔️ Avoid excessive deletion
* ✔️ Use appropriate imputation technique
* ✔️ Validate dataset after cleaning

---

## 🎯 Conclusion

Handling missing values is essential for building reliable and accurate models. A cleaned dataset significantly improves performance and ensures meaningful insights.

---



## CARS93

# 🚗 Data Preprocessing: Handling Missing Values (Cars Dataset)

---

## 📌 Overview

This project focuses on preprocessing the **Cars93 dataset**, specifically handling missing values to improve data quality and make it suitable for analysis and machine learning.

---

## ❓ What are Missing Values?

Missing values are data points that are not recorded or are unavailable in the dataset.

### 🔍 Representations:

* `NaN`
* `NULL`
* Blank cells
* Special placeholders

---

## ⚠️ Why Handle Missing Values?

* 📉 Avoid incorrect analysis
* ⚙️ Ensure algorithms run smoothly
* 📊 Improve dataset reliability
* 🚀 Enhance model performance

---

## 🔎 Dataset Description

### 🗂️ Original Dataset: `Cars93.csv`

* Contains raw car data
* Includes missing values
* Not directly suitable for modeling

### 🧼 Updated Dataset: `updated_cars93.csv`

* Cleaned and preprocessed
* Missing values handled
* Ready for analysis

---

## 🛠️ Techniques Used

### 1️⃣ Detect Missing Values

```python id="1a9n2b"
df.isnull().sum()
```

---

### 2️⃣ Removing Missing Data

```python id="b72kq1"
# Drop rows with missing values
df.dropna()

# Drop columns with excessive missing values
df.dropna(axis=1)
```

---

### 3️⃣ Imputation Techniques

#### 📊 Mean / Median (Numerical Data)

```python id="z91mqp"
df['Price'].fillna(df['Price'].mean(), inplace=True)
```

#### 🏷️ Mode (Categorical Data)

```python id="v5k8ds"
df['Manufacturer'].fillna(df['Manufacturer'].mode()[0], inplace=True)
```

---

### 4️⃣ Forward / Backward Fill

```python id="c3x9pl"
df.fillna(method='ffill', inplace=True)
df.fillna(method='bfill', inplace=True)
```

---

### 5️⃣ Interpolation 📈

```python id="x7q2lm"
df.interpolate(method='linear', inplace=True)
```

---

### 6️⃣ Advanced Imputation 🤖

```python id="r8w1kf"
from sklearn.impute import KNNImputer

imputer = KNNImputer(n_neighbors=5)
df_imputed = imputer.fit_transform(df)
```

---

## ⚖️ Comparison: Original vs Updated Dataset

| Feature           | 🚗 Original (`Cars93.csv`) | 🧼 Updated (`updated_cars93.csv`) |
| ----------------- | -------------------------- | --------------------------------- |
| Missing Values    | ❌ Present                  | ✅ Handled                         |
| Data Consistency  | ⚠️ Low                     | ✔️ High                           |
| Data Quality      | Poor                       | Improved                          |
| Analysis Ready    | ❌ No                       | ✅ Yes                             |
| Model Performance | Low                        | High                              |

---

## 📊 Key Improvements

### 🔴 Original Dataset

* Contains null values in multiple columns
* Inconsistent and incomplete data
* Requires preprocessing

### 🟢 Updated Dataset

* Missing values filled or removed
* Clean and structured format
* Ready for ML models and visualization

---

## 📦 Libraries Used

* 🐍 Pandas
* 🔢 NumPy
* 🤖 Scikit-learn

---

## 📈 Best Practices

* ✔️ Always check missing values before processing
* ✔️ Use mean/median for numerical features
* ✔️ Use mode for categorical features
* ✔️ Avoid dropping too much data
* ✔️ Validate results after cleaning

---

## 🎯 Conclusion

Preprocessing the Cars93 dataset by handling missing values significantly improves its usability. The cleaned dataset ensures better insights, smoother computations, and higher model accuracy.

---



