# Insights in Motion: Visualizing Tipping Trends and Penguin Data

This repository contains Jupyter Notebooks and datasets for visualizing tipping trends and penguin data using Seaborn and Matplotlib.

## Project Overview

The project is divided into two main parts:

1. **Tipping Trends Analysis**:
   - Dataset: `tips.csv`
   - Visualizations: Line plots, bar plots, histograms, etc.

2. **Penguin Data Analysis**:
   - Dataset: `penguins.csv`
   - Visualizations: Line plots, bar plots, histograms, etc.

## Datasets

### Tips Dataset (`tips.csv`)

The tips dataset contains information about tips received by waitstaff at a restaurant. The columns in the dataset include:
- `total_bill`: The total bill amount.
- `tip`: The tip amount.
- `sex`: The gender of the person paying the bill.
- `smoker`: Whether the person is a smoker or not.
- `day`: The day of the week.
- `time`: The time of day (Lunch/Dinner).
- `size`: The size of the party.

### Penguins Dataset (`penguins.csv`)

The penguins dataset contains information about different species of penguins. The columns in the dataset include:
- `species`: The species of the penguin.
- `island`: The island where the penguin was observed.
- `bill_length_mm`: The length of the penguin's bill in millimeters.
- `bill_depth_mm`: The depth of the penguin's bill in millimeters.
- `flipper_length_mm`: The length of the penguin's flipper in millimeters.
- `body_mass_g`: The body mass of the penguin in grams.
- `sex`: The sex of the penguin.

## Visualizations

### Tipping Trends

#### Line Plot

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd

x = [1, 2, 3, 4, 5, 6, 7]
y = [20, 40, 30, 40, 30, 50, 30]

df = pd.DataFrame({"Days": x, "No of people": y})
sns.lineplot(x="Days", y="No of people", data=df)
plt.show()
