# Movie Release Date Analysis Project

This repository contains a Jupyter Notebook that analyzes and visualizes patterns in a comprehensive movie dataset, focusing on insights related to **release dates, genre trends, and revenue dynamics** in the cinematic industry.

## Table of Contents

- [Project Objective](#project-objective)
- [Dataset Overview](#dataset-overview)
- [Data Preprocessing](#data-preprocessing)
- [Analysis Methods](#analysis-methods)
- [Visualizations & Outputs](#visualizations--outputs)
- [Key Insights](#key-insights)
- [Usage Guide](#usage-guide)
- [Dependencies & Installation](#dependencies--installation)
- [Future Scope](#future-scope)
- [Acknowledgments](#acknowledgments)

***

## Project Objective

- To **uncover trends** in the film industry regarding the timing and frequency of movie releases.
- To **analyze genre popularity** across years and months.
- To **track average gross revenue** dynamics over time.
- To provide **visual, data-driven conclusions** accessible for further industry research or business intelligence.

## Dataset Overview

- **Primary Source:** CSV file named `moviescleaned.csv`
- **Rows:** 5,407 movies
- **Columns:** 17 data fields, including:
  - `name, rating, genre, year, released, score, votes, director, writer, star, country, budget, gross, company, runtime, month, day`
- Covers details from **1980 to 2020** with international scope (various production countries).
- **Sample row example**:  
  “The Shining”, R, Drama, 1980, June 13 1980 United States, 8.4, 927000, Stanley Kubrick, Stephen King, Jack Nicholson, United Kingdom, 19,000,000, 46,998,772, Warner Bros., 146, June, 13

## Data Preprocessing

- **Loading:** Data ingested using pandas.
- **Cleaning:**
  - Converted numeric columns (e.g., ‘gross’) to suitable types.
  - Managed missing values (e.g., coercing errors to `NaN`).
  - Feature engineering: Extracted 'month' and 'day' for temporal analysis.

## Analysis Methods

- **Core analysis tasks:**
  - Movie release counts per year.
  - Genre trends (yearly and monthly pivots).
  - Calculation and trend visualization of average gross revenue (year-wise).
  - Heatmap analysis for monthly genre popularity.
- **Grouping, aggregating, statistical summaries:** Used for uncovering patterns.

## Visualizations & Outputs

- **Line graphs:**
  - Movies released each year.
  - Genre-wise release trends over time.
  - Average gross revenue by year.
- **Pivot tables & Heatmaps:**
  - Genre popularity by month, visualized for quick pattern detection.
- **Descriptive stats:** Output of runtime, rating distribution, etc.

## Key Insights

- Visualization of **industry expansion or contraction** over decades.
- **Seasonal patterns** in genre releases (e.g., horror movies more frequent in October).
- Rising or falling trends in movie production and gross.
- Discovery of **genre cycles** and shifts in audience preference.

## Usage Guide

1. Ensure `moviescleaned.csv` is in the notebook directory.
2. Open the notebook (`Release-Date-1.ipynb`) and run all cells.
3. Review the generated plots, statistics, and insights inline.

## Dependencies & Installation

- **Python 3.10+**
- Required libraries:
  - pandas
  - matplotlib
  - seaborn

Install with:
```bash
pip install pandas matplotlib seaborn
```

## Future Scope

- Deeper dive into **budget-to-gross ratios**.
- Sentiment analysis on movie scores and reviews.
- Integration with additional datasets (awards, marketing, streaming data).
- Time series forecasting for movie release strategies.

