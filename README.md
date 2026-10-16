# LEGO Data Analysis

An exploratory analysis of LEGO sets and themes using Python and pandas. The notebook investigates release trends and licensed themes, including how Star Wars compares with other licensed LEGO themes across years.

## Project overview

This project uses four related CSV datasets covering LEGO sets, themes, parent themes, and the set catalogue. The notebook loads the data into pandas DataFrames, combines related tables, filters records, and groups data to answer exploratory questions.

## Tools and technologies

- **Python**
- **pandas**
- **Jupyter Notebook**
- **CSV datasets**

## Questions explored

- What proportion of licensed LEGO sets are themed around Star Wars?
- In which year was Star Wars not the most popular licensed theme by number of sets released?
- How many LEGO sets were released in each year represented in the dataset?

The analysis joins set information to parent-theme metadata, filters to licensed sets for the licensed-theme questions, and excludes records with missing set identifiers from relevant calculations.

## Repository contents

- `Lego data analysis.ipynb` — the exploratory analysis and code.
- `LEGO datasets/lego_sets.csv` — set records with set number, name, year, part count, theme, and parent theme.
- `LEGO datasets/sets.csv` — set records including set number, release year, theme identifier, and part count.
- `LEGO datasets/themes.csv` — theme identifiers, names, and parent-theme relationships.
- `LEGO datasets/parent_themes.csv` — parent-theme metadata, including whether the theme is licensed.

## Getting started

### Prerequisites

- Python 3
- Jupyter Notebook or JupyterLab

### 1. Clone the repository

```bash
git clone https://github.com/M-Jethro/Lego-Data-Analysis.git
cd Lego-Data-Analysis
```

### 2. Install dependencies

```bash
pip install pandas jupyter
```

### 3. Update the dataset paths

The notebook currently uses local Windows file paths. Update its `pd.read_csv(...)` calls to use paths to the CSV files in the repository. For example:

```python
from pathlib import Path
import pandas as pd

data_dir = Path("LEGO datasets")

lego_sets = pd.read_csv(data_dir / "lego_sets.csv")
sets = pd.read_csv(data_dir / "sets.csv")
themes = pd.read_csv(data_dir / "themes.csv")
parent_themes = pd.read_csv(data_dir / "parent_themes.csv")
```

Check that the variable names used in later notebook cells match the DataFrames you have loaded before running the notebook from top to bottom.

### 4. Launch Jupyter

```bash
jupyter notebook
```

Open `Lego data analysis.ipynb` and run the cells in order.

## Approach

1. **Inspect the data** — review available columns and sample records.
2. **Combine related datasets** — connect set information to parent-theme metadata.
3. **Filter records** — focus on licensed sets for licensed-theme questions and remove records missing set identifiers where appropriate.
4. **Aggregate and compare** — count sets by year and theme to explore release patterns.
5. **Interpret trends** — compare the relative popularity of licensed themes over time.

## What this project demonstrates

Exploratory analysis with pandas, merging related datasets, filtering records, handling missing identifiers, grouping data, and translating questions into measurable summaries.

## Repository

[View the source code and notebook on GitHub](https://github.com/M-Jethro/Lego-Data-Analysis)
