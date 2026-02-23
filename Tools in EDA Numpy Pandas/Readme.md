# 🧪 Experiment 8: Tools in EDA – NumPy & Pandas 📊

## 👩‍🎓 Student Information
**Name:** Gayatri Bhosale  
**PRN:** 25070123033  

---

## 🎯 Objective
To study the basic tools used in Exploratory Data Analysis (EDA), especially:
- 🔢 NumPy for numerical computations  
- 🐼 Understanding its importance as the base of Pandas  
- 📊 Performing array operations and statistical analysis  

---

## 📚 Theory

### 📊 What is EDA?
Exploratory Data Analysis (EDA) is the process of analyzing datasets to summarize their main characteristics, often using statistical methods and visualizations. It helps in:
- Understanding data structure  
- Detecting patterns and trends  
- Identifying outliers  
- Preparing data for further analysis  

---

### 🔢 What is NumPy?
NumPy (Numerical Python) is a powerful Python library used for numerical and mathematical operations. It provides:
- ⚡ Faster computation compared to Python lists  
- 🧮 Support for multi-dimensional arrays  
- 📐 Mathematical and statistical functions  
- 🐼 A foundation for libraries like Pandas, Matplotlib, and Scikit-learn  

NumPy arrays consume less memory and perform operations efficiently using vectorization.

---

## 🤔 Why NumPy?
- ⚡ Faster than Python lists  
- 🔢 Used for numerical computations  
- 🐼 Forms the base of Pandas library  

---

## 🛠️ Tools & Technologies Used
- 🐍 Python 3  
- 🔢 NumPy Library  
- 💻 Google Colab / Jupyter Notebook  

---

## 📖 Experiment Steps & Code

### 1️⃣ Import NumPy Library
```python
import numpy as np
```

---

### 2️⃣ Create NumPy Arrays 🔢
```python
a = np.array([10,20,30,40])
b = np.array([[1,2,3],[4,5,6]])

print(a)
print(b)
```

---

### 3️⃣ Check Dimension of Array 📏
```python
print(a.ndim)
print(b.ndim)
```

---

### 4️⃣ Check Shape of Array 📐
```python
print(a.shape)
print(b.shape)
```

---

### 5️⃣ Check Data Type 🧾
```python
print(a.dtype)
print(b.dtype)
```

---

### 6️⃣ Create Special Arrays ✨

🔹 Zeros Array
```python
np.zeros((2,3))
```

🔹 Ones Array
```python
np.ones((7,7))
```

🔹 Identity Matrix
```python
np.eye(3)
```

---

### 7️⃣ Generate Number Sequences 🔄

🔹 Using arange()
```python
np.arange(1,10,2)
```

🔹 Using linspace()
```python
np.linspace(0,1,5)
```

---

### 8️⃣ Perform Arithmetic Operations ➕✖️
```python
c = a * 2
d = a + 5

print(c)
print(d)

print(a + 5)
```

---

### 9️⃣ Statistical Functions 📊

🔹 Mean
```python
np.mean(a)
np.mean(b)
```

🔹 Median
```python
print(np.median(a))
print(np.median(b))
```

🔹 Maximum
```python
print(np.max(a))
print(np.max(b))
```

🔹 Minimum
```python
np.min(a)
np.min(b)
```

🔹 Sum
```python
np.sum(a)
np.sum(b)
```

---

## 📊 Results
- ✅ Successfully created 1D and 2D NumPy arrays.  
- ✅ Explored array properties (dimension, shape, datatype).  
- ✅ Generated special arrays (zeros, ones, identity matrix).  
- ✅ Performed arithmetic operations on arrays.  
- ✅ Applied statistical functions like mean, median, max, min, and sum.  

---

## 🏁 Conclusion
This experiment helped in understanding NumPy as a fundamental tool for numerical computing in Python. It enables efficient array operations and statistical analysis, which are essential in Exploratory Data Analysis (EDA) and form the foundation for advanced libraries like Pandas.

---

## 📚 References
- 🌐 NumPy Official Documentation: https://numpy.org/doc/  
- 🌐 Python Official Documentation: https://docs.python.org/3/  

---

⭐ End of Experiment 8
