# 🌍 World Population Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Latest-green?style=flat&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Latest-orange?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-success?style=flat)

A data analysis project that analyzes real world population data from 234 countries using Python, Pandas and Matplotlib.

---

## 📊 What This Project Does

- Loads a real CSV dataset with population data from 234 countries
- Finds the top 10 most populated countries in 2022
- Analyzes population by continent
- Shows population growth from 1970 to 2022
- Displays world population statistics
- Creates bar charts, line charts and pie charts

---

## 📸 Charts Generated

- 📊 Top 10 Most Populated Countries (Bar Chart)
- 🌍 Total Population by Continent (Bar Chart)
- 📈 Population Growth Over Years (Line Chart)
- 🥧 World Population Share by Continent (Pie Chart)

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python 3 | Core programming language |
| Pandas | Loading and analyzing the dataset |
| Matplotlib | Creating charts and visualizations |
| Jupyter Notebook | Interactive development environment |

---

## 🧠 Key Functions Explained

### `pd.read_csv()`
Loads a CSV file into a Pandas DataFrame — like opening an Excel file in Python.
```python
df = pd.read_csv('world_population.csv')
```

### `df.shape`
Returns the number of rows and columns in the dataset.
```python
print(df.shape)  # (234, 17) — 234 countries, 17 columns
```

### `df.head()`
Shows the first 5 rows of the dataset — useful for quickly checking your data.
```python
print(df.head())
```

### `df.nlargest()`
Finds the rows with the largest values in a specific column.
```python
top10 = df.nlargest(10, '2022 Population')  # top 10 most populated
```

### `df.groupby()`
Groups data by a category and performs calculations on each group.
```python
continent_pop = df.groupby('Continent')['2022 Population'].sum()
# adds up population of all countries in each continent
```

### `df['column'].describe()`
Shows basic statistics — count, mean, min, max — for a column.
```python
df['2022 Population'].describe()
```

### `df.loc[df['column'].idxmax()]`
Finds the row with the highest value in a column.
```python
df.loc[df['2022 Population'].idxmax(), 'Country/Territory']
# returns the most populated country
```

### `plt.plot()`
Creates a line chart — great for showing trends over time.
```python
plt.plot(years, population, marker='o', label='Country Name')
```

### `plt.bar()`
Creates a bar chart — great for comparing values.
```python
plt.bar(countries, populations, color='#6c63ff')
```

### `plt.pie()`
Creates a pie chart — great for showing percentage breakdowns.
```python
plt.pie(values, labels=labels, autopct='%1.1f%%')
```

---

## 📋 Dataset Information

- **Source:** Kaggle — World Population Dataset by Sourav Banerjee
- **Countries:** 234
- **Years covered:** 1970 — 2022
- **Columns:** Rank, Country, Continent, Population by year, Area, Density, Growth Rate

---

## 💡 What I Learned

- How to load and explore real world datasets using Pandas
- How to filter, sort and group data
- How to create different types of charts using Matplotlib
- How to extract meaningful insights from raw data

---

## 👩‍💻 Author

**Nooriya Ilyas**
- Portfolio: [nooriya20.github.io](https://nooriya20.github.io)
- GitHub: [@nooriya20](https://github.com/nooriya20)

---

⭐ If you found this project interesting, please give it a star!
