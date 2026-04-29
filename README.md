import matplotlib
matplotlib.use('TkAgg')
# Import libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Create dataset (sample data)
data = {
    'Attendance': [75, 80, 85, 90, 60, 70, 95, 88, 76, 84],
    'Internal_Marks': [65, 70, 75, 80, 50, 60, 85, 78, 68, 74],
    'Assignment_Score': [60, 65, 70, 75, 55, 58, 80, 77, 66, 72],
    'Study_Hours': [2, 3, 4, 5, 1, 2, 6, 5, 3, 4],
    'Final_Grade': [66, 70, 74, 82, 55, 60, 88, 80, 69, 75]
}

df = pd.DataFrame(data)

# Display dataset
print("Dataset:\n", df)

# Descriptive statistics
print("\nMean:\n", df.mean())
print("\nMedian:\n", df.median())
print("\nVariance:\n", df.var())

# Correlation
print("\nCorrelation:\n", df.corr())

# Visualization

# Scatter plot
plt.scatter(df['Attendance'], df['Final_Grade'])
plt.xlabel("Attendance")
plt.ylabel("Final Grade")
plt.title("Attendance vs Final Grade")
plt.show()

# Histogram
df['Final_Grade'].hist()
plt.title("Distribution of Final Grades")
plt.show()

# Boxplot
sns.boxplot(data=df)
plt.title("Boxplot of Student Features")
plt.show()
import matplotlib.pyplot as plt
plt.show(block=True)
