# 🧪 Experiment 9: Study of Pandas Library 🐼

## 👩‍🎓 Student Information
**Name:** Gayatri Bhosale  
**PRN:** 25070123033  

---

## 🎯 Objective
To study and understand the basic functionalities of the Pandas library in Python, including:
- 📌 Creating Series and DataFrames  
- 📊 Exploring DataFrame structure  
- 🔍 Accessing and modifying data  
- 📈 Performing statistical analysis  
- 🧹 Applying filtering conditions  

---

## 🐼 About Pandas
Pandas is a powerful Python library used for:
- 📂 Structured data handling  
- 📊 Exploratory Data Analysis (EDA)  
- 🧽 Data Cleaning and preprocessing  

---

## 🛠️ Tools & Technologies Used
- 🐍 Python 3  
- 🐼 Pandas Library  
- 💻 Google Colab / Jupyter Notebook  

---

## 📖 Experiment Steps & Description

### 1️⃣ Import Pandas Library
```python
import pandas as pd
```

### 2️⃣ Create a Pandas Series
```python
s = pd.Series([10, 20, 30, 40])
print(s)
```

### 3️⃣ Create a DataFrame
```python
data = {
    "Name": ["A", "B", "C"],
    "Marks": [90, 95, 100]
}
df = pd.DataFrame(data)
print(df)
```

### 4️⃣ Explore DataFrame Structure 📊
```python
print("Shape:", df.shape)
print("Dimensions:", df.ndim)
print("Size:", df.size)
print("Columns:", df.columns)
print("Data Types:\n", df.dtypes)
```

### 5️⃣ Access Data 🔎
Access individual columns:
```python
print(df["Name"])
print(df["Marks"])
```

Access specific row:
```python
print(df.loc[1])
```

### 6️⃣ Add New Column ➕
```python
df["Grade"] = ["Second Class", "First Class", "Distinction"]
print(df)
```

### 7️⃣ Update Data in DataFrame ✏️
Change marks of student A to 88:
```python
df.loc[0, "Marks"] = 88
print(df)
```

### 8️⃣ Delete a Column ❌
```python
df.drop("Grade", axis=1, inplace=True)
print(df)
```

### 9️⃣ Perform Basic Statistical Analysis 📈
```python
mean_marks = df["Marks"].mean()
min_marks = df["Marks"].min()
max_marks = df["Marks"].max()

print("Mean:", mean_marks)
print("Minimum:", min_marks)
print("Maximum:", max_marks)
```

### 🔟 Apply Condition (Filtering) 🧹
Display students scoring more than 80:
```python
print(df[df["Marks"] > 80])
```

---

## 📊 Results
- ✅ Successfully created and manipulated a Pandas DataFrame.  
- ✅ Performed statistical operations (mean, minimum, maximum).  
- ✅ Applied conditional filtering.  
- ✅ Learned basic data cleaning and modification techniques.  

---

## 🏁 Conclusion
This experiment helped in understanding the fundamental operations of the Pandas library, including data structure creation, data exploration, modification, and basic analysis. Pandas is highly useful for handling structured datasets efficiently.

---

## 📚 References
- 🌐 Pandas Official Documentation: https://pandas.pydata.org/docs/  
- 🌐 Python Official Documentation: https://docs.python.org/3/  

---

⭐ End of Experiment 9
