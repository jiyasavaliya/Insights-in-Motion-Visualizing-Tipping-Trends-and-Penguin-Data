# Insights in Motion: Visualizing Tipping Trends and Penguin Data

This repository contains Jupyter Notebooks and datasets for visualizing tipping trends and penguin data using Seaborn and Matplotlib.

## Project Overview

The project is divided into two parts:

1. **Tipping Trends Analysis**: Focuses on tipping data, analyzing trends and patterns in restaurant tips.
2. **Penguin Data Analysis**: Focuses on data about penguins, including species, physical measurements, and environmental observations.

## Datasets

### Tips Dataset (`tips.csv`)

Contains information about tips received by waitstaff:
- `total_bill`: The total bill amount.
- `tip`: The tip amount.
- `sex`: The gender of the person paying the bill.
- `smoker`: Whether the person is a smoker or not.
- `day`: The day of the week.
- `time`: Time of day (Lunch/Dinner).
- `size`: Size of the party.

### Penguins Dataset (`penguins.csv`)

Contains data on penguin species and measurements:
- `species`: Species of the penguin.
- `island`: The island where the penguin was observed.
- `bill_length_mm`: Length of the penguin's bill (mm).
- `bill_depth_mm`: Depth of the penguin's bill (mm).
- `flipper_length_mm`: Length of the penguin's flipper (mm).
- `body_mass_g`: Body mass of the penguin (grams).
- `sex`: Sex of the penguin.

## Visualizations

### Tipping Trends  
Line plots, bar plots, and histograms are used to explore tipping trends in relation to party size, gender, smoking status, and day of the week.

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd

# Line plot example
x = [1, 2, 3, 4, 5, 6, 7]
y = [20, 40, 30, 40, 30, 50, 30]
df = pd.DataFrame({"Days": x, "No of people": y})
sns.lineplot(x="Days", y="No of people", data=df)
plt.show()


