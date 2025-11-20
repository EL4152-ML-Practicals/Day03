## 📚 Day 03: Data Visualization & Analysis

---

## 📊 Exercise 1: Iris Dataset Visualization

### Overview 🌸

Learn to work with the famous **Iris dataset** and create different types of visualizations using matplotlib.

### What's Inside:

- 📥 **Load Iris Dataset**: Import sklearn's iris dataset with 150 samples and 4 features
- 📈 **Dataset Information**: Explore sample count, feature names, and target classes
- 📊 **Histogram Visualization**: Create color-coded histograms for each iris species
- 🔵 **Scatter Plot**: Visualize relationships between petal width and sepal length
- 🎨 **Color Coding**: Use different colors (red, blue, green) to distinguish between species

### Key Concepts:

✅ Data exploration and inspection  
✅ Feature extraction and analysis  
✅ Multi-class visualization  
✅ Matplotlib figure and axes management

### Code Snippet:

```python
# Load iris dataset
from sklearn.datasets import load_iris
iris = load_iris()

# Create scatter plot
fig, ax = plt.subplots()
colors = ['red', 'blue', 'green']
for label, color in zip(range(len(iris.target_names)), colors):
    ax.scatter(iris.data[iris.target == label, 3],
               iris.data[iris.target == label, 0],
               label=iris.target_names[label],
               color=color)
ax.set_xlabel(iris.feature_names[3])
ax.set_ylabel(iris.feature_names[0])
ax.legend()
plt.show()
```

---

## 📉 Exercise 2: DataFrame Plotting Techniques

### Overview 📋

Master different plotting methods available in pandas DataFrame for data visualization.

### Plot Types Demonstrated:

- 📈 **Line Plot**: Show data trends over time/categories
- 📊 **Histogram**: Display frequency distributions
- 📌 **Scatter Plot**: Reveal relationships between two variables
- 📦 **Bar Chart**: Compare categorical data
- 🥧 **Pie Chart**: Show proportional distributions
- 📭 **Box Plot**: Visualize data spread and outliers
- 🌊 **Density Plot (KDE)**: Show probability distribution
- 🏔️ **Area Plot**: Cumulative visualization
- 🔲 **Hexbin Plot**: 2D histogram for large datasets

### Key Concepts:

✅ Pandas DataFrame creation with random data  
✅ Multiple plotting methods using `.plot()`  
✅ Plot customization (kind, figsize, subplots)  
✅ Data visualization best practices

### Code Snippet:

```python
# Create sample DataFrame
import pandas as pd
import numpy as np

df1 = pd.DataFrame(np.random.rand(10, 4),
                   columns=('col1', 'col2', 'col3', 'col4'))

# Different plot types
df1.plot()                                    # Line plot
df1.plot(kind='hist')                        # Histogram
df1.plot(kind='scatter', x='col2', y='col1') # Scatter plot
df1.plot(kind='bar')                         # Bar chart
df1.plot(kind='box')                         # Box plot
df1.plot(kind='hexbin', x='col2', y='col1', gridsize=6)  # Hexbin plot
```

---

## 🛠️ Technologies Used

- 🐍 **Python 3**
- 📚 **Libraries**: pandas, numpy, matplotlib, scikit-learn
- 💻 **IDE**: Jupyter Notebook

## 🎯 Learning Outcomes

After these exercises, you'll be able to:

- ✨ Load and explore datasets
- ✨ Create multiple types of visualizations
- ✨ Customize plots with labels, colors, and legends
- ✨ Interpret visual data patterns and relationships
