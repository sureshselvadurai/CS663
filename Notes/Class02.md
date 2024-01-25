# Code Summary

## Import Libraries
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv(r"titanic.csv")


# Overview of Data
df.info()

# Descriptive Statistics
df.describe()

# Value Counts
df.Sex.value_counts()

# Using Seaborn Displot
sns.displot(df.Survived)

# Customized Displot for Fare
sns.displot(df.Fare, bins=50, kde=True)

# Multiple Histograms
fg, axs = plt.subplots(ncols=4, figsize=(20, 4))
sns.histplot(df.Survived, ax=axs[0])
sns.histplot(df.Pclass, ax=axs[1])
sns.histplot(df.Sex, ax=axs[2])
sns.histplot(df.Fare, ax=axs[3])

# More Histograms
fg, axs = plt.subplots(ncols=3, figsize=(20, 4))
sns.histplot(df['Age'], ax=axs[0])
sns.histplot(df['Siblings/Spouses Aboard'], ax=axs[1])
sns.histplot(df['Parents/Children Aboard'], ax=axs[2])

# Pandas DataFrame Histogram
df.hist(bins=50, figsize=(20, 8))


# Skewness and Kurtosis for Age
df.Age.skew()
df.Age.kurt()

# Scatter Plot
sns.scatterplot(data=df, x=df.Age, y=df.Fare, hue=df.Survived)

# Stack multiple histograms with KDE
sns.displot(data=df, x="Fare", hue=df.Survived, multiple='stack', kde=True)
