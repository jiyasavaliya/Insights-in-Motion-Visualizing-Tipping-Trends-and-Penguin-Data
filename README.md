# Insights in Motion: Visualizing Tipping Trends and Penguin Data

This repository contains Jupyter Notebooks and datasets for visualizing tipping trends and penguin data using Seaborn and Matplotlib.

## Project Overview

The project analyzes two main datasets:

1. **Tipping Trends Analysis**: Explores patterns in restaurant tipping behavior using various visualizations
2. **Penguin Data Analysis**: Examines physical characteristics and distribution of different penguin species

## Datasets

### Tips Dataset (`tips.csv`)
- `total_bill`: Total bill amount
- `tip`: Tip amount
- `sex`: Gender of the person paying the bill
- `smoker`: Whether the person is a smoker or not
- `day`: Day of the week
- `time`: Time of day (Lunch/Dinner)
- `size`: Size of the party

### Penguins Dataset (`penguins.csv`)
- `species`: Species of the penguin
- `island`: Island where the penguin was observed
- `bill_length_mm`: Length of the penguin's bill in millimeters
- `bill_depth_mm`: Depth of the penguin's bill in millimeters
- `flipper_length_mm`: Length of the penguin's flipper in millimeters
- `body_mass_g`: Body mass of the penguin in grams
- `sex`: Sex of the penguin

## Example Visualizations

```python
# Line Plot Example
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd

x = [1, 2, 3, 4, 5, 6, 7]
y = [20, 40, 30, 40, 30, 50, 30]
df = pd.DataFrame({"Days": x, "No of people": y})
sns.lineplot(x="Days", y="No of people", data=df)
plt.show()

# Bar Plot Example
z = sns.load_dataset("penguins").head(51)
sns.barplot(x="island", y="bill_length_mm", data=z, color="r")
plt.show()

# Histogram Example
sns.displot(z["flipper_length_mm"], 
           bins=[170, 180, 190, 200, 210, 220, 230, 240], 
           kde=True, 
           rug=True, 
           color="r")
plt.show()
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/jiyasavaliya/Insights-in-Motion-Visualizing-Tipping-Trends-and-Penguin-Data.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Insights-in-Motion-Visualizing-Tipping-Trends-and-Penguin-Data
   ```

3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

## License

This project is licensed under the MIT License.
