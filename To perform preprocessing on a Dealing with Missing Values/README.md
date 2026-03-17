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

