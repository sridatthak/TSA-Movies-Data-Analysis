Here is the link for the full documentation portfolio with all the research and analysis. https://docs.google.com/document/d/1_pWxqzX64wA_v_j-V65ePLT6kV9vV-LTJtECPxc8_FA/edit?tab=t.38mzcbscwfm9

***

# Movie Data Analysis Pipeline

A complete **Jupyter-based pipeline** for transforming, exploring, and visualizing large-scale movie industry data. This project covers raw data cleaning, feature engineering, and thematic explorations into release trends, budget patterns, and runtime effects—with each notebook providing end-to-end code, commentary, and outputs.

***

## Table of Contents

- Overview
- Folder/Notebook Structure
- Data Sources & Features
- ETL & Data Cleaning
- Exploratory Data Analysis (EDA)
  - Release Date Trends
  - Budget Insights
  - Runtime Patterns
- Main Statistical Insights
- Visualization Suite
- Sample Code Snippets
- Requirements & Setup
- Usage Guide
- Extensibility & Advancements
- Credits

***

## Overview

- **Goal:** Deliver a flexible, reproducible pipeline to understand what shapes movie success, when releases peak, and how creative, financial, and temporal parameters shift across industry history.
- **Pipeline:** From raw messy CSV to rich statistical exploration and colorful visualizations.
- **For whom:** Data scientists, film researchers, business intelligence analysts, or hobbyists exploring movie data.

***

## Folder/Notebook Structure

- **TSA_cleaning.ipynb:** Cleans, diagnoses, and engineers features from the raw movies CSV, creating an EDA-ready dataset.
- **Release-Date-1.ipynb:** Analyzes time-based trends in movie releases and their correlation to genres, gross, and cinematic cycles.
- **Budget-1.ipynb:** Explores distribution/spread of movie budgets, their impact on ratings and revenue, and ROI outliers.
- **Runtime.ipynb:** Examines how runtime affects audience acclaim and box office performance, with density/trend plots.

*Each notebook stands alone but is best run as part of the above workflow sequence.*

***

## Data Sources & Features

- **Primary file**: `moviesoriginal.csv` (raw, ~7700 rows × 15 columns)
- **Engineered clean file**: `moviescleaned.csv` (5400+ rows × 17 columns)
- **Key features/columns:**  
  - `name, rating, genre, year, released, score, votes, director, writer, star, country, budget, gross, company, runtime, month, day`
- **Stats Example**:  
  - Years: 1980–2020
  - IMDB score: 1.9–9.3 (mean ≈6.4)
  - Budget: $6,000–$356,000,000; Gross: $309–$2.8B  
  - Runtimes: 63–271 minutes (mean ≈108)

***

## ETL & Data Cleaning

- **Type checks:** All numerics coerced/fixed; invalids dropped.
- **Missing values:** Rows with missing essentials are removed—robustness > quantity.
- **Diagnostics:** Used `df.info()`, `df.describe()`, value counts for nulls, outliers, and text inconsistencies.
- **Feature engineering:**  
  - Extracted `month`, `day` from messy release text.
  - All cleaned output logged and validated.
- **Result:** A consistently typed, gap-free, analysis-friendly CSV.

***

## Exploratory Data Analysis (EDA)

### Release Date Trends

- **Yearly chart:** How many movies released per year?  
  - *Line plot uncovers industry expansions, contractions, or crises.*
- **Genre breakdown:** Movie frequency trends by genre and year.
  - *See which genres surge or fade across decades.*
- **Monthly seasonality:**  
  - Find genre-specific release months (e.g., horror ⇨ October).
- **Gross revenue:**  
  - Average gross by year; macro-level financial trajectory.

### Budget Insights

- **Distribution:** Histogram of movie budget (log-transformed for clarity).
- **Budget vs. Score:** Scatter chart reveals if expensive movies earn better ratings.
- **Budget vs. Gross:** Correlate financial investment with commercial performance.  
  - Spot *big-budget flops* or *indie hits*.

### Runtime Patterns

- **Runtime histogram:** See the most typical (and unusual) movie lengths.
- **Runtime vs. Score/Gross:**  
  - Are longer or shorter movies more likely to get high scores or returns?
- **Outlier spotlight:** Highlight anomalies: short blockbusters, long artsy films, etc.

***

## Main Statistical Insights

- Industry output has ebbed/flowed; some years are blockbuster booms.
- Most films cluster at runtime ~90–120 minutes and modest budgets.
- High gross possible at all budget levels, but *ROI is not linear*.
- Genre cycles exist: some trends follow the calendar, some track with pop culture.
- Both budget and runtime have outliers—hit movies that break the usual rules.

***

## Visualization Suite

- **Matplotlib/Seaborn** powered:  
  - Yearly/Monthly/Genre Timeline Plots
  - Distribution Histograms, Boxplots
  - Scatterplots with log-scaling
  - Heatmaps for seasonality/pivots

*All visualizations include axes, grids, labels, and interpretive titles/comments.*

***

## Sample Code Snippet

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load cleaned data
df = pd.read_csv("moviescleaned.csv")
# Plot movie count per year
per_year = df['year'].value_counts().sort_index()
plt.figure(figsize=(12,6))
plt.plot(per_year.index, per_year.values, marker='o')
plt.title("Number of Movies Released Per Year")
plt.xlabel("Year")
plt.ylabel("Number of Movies")
plt.grid()
plt.show()
```

***

## Requirements & Setup

- **Python 3.10+**
- **Libraries:** `pandas`, `matplotlib`, `seaborn`
- **Installation:**
```bash
pip install pandas matplotlib seaborn
```

***

## Usage Guide

1. Place `moviesoriginal.csv` in the repo.
2. Run all cells in `TSA_cleaning.ipynb` (creates `moviescleaned.csv`).
3. Explore trends and relationships in thematic notebooks (`Release-Date-1.ipynb`, `Budget-1.ipynb`, `Runtime.ipynb`).
4. Review in-notebook code, outputs, and comments for full context.

***

## Extensibility & Advancements

- **Advanced Cleaning:** Impute non-critical nulls, harmonize extra text columns (e.g., fuzzy company/genre names).
- **Feature Expansion:** Add variables (decade, continent, inflation-adjusted budget).
- **Integration:** Merge with streaming platform, award, or rating sources.
- **ML Potential:** Use cleaned dataset for predictive tasks: forecast score/gross from text/numeric features.

***

## Credits

- Author: [Your Name / Team]
- Data cleaning, analysis, and visualization performed in Jupyter notebooks.
- Powered by Python open-source stack and community-contributed movie datasets.
