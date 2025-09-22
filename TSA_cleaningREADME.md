# Movie Dataset Cleaning & Preparation (`TSA_cleaning.ipynb`)

This notebook provides a robust workflow for **cleaning and preparing a large-scale movie dataset** in preparation for analysis, modeling, or visualization. It is the essential first step before any data-driven project concerning this collection of film data.

***

## Table of Contents

- Project Purpose
- Raw Dataset Description
- Cleaning Process
- Output: Cleaned Dataset
- Usage Instructions
- Requirements
- Extensibility / Future Steps

***

## Project Purpose

- To **transform a raw movie database** into a clean, analysis-ready CSV file.
- To correct, unify, and fill missing values, ensuring consistent and reliable downstream analytics.
- To provide a sound base for further studies involving movie trends, revenue, scoring, and more.

***

## Raw Dataset Description

- **File:** `moviesoriginal.csv`
- **Rows:** ~7700
- **Columns (15):**  
    - `name`, `rating`, `genre`, `year`, `released`, `score`, `votes`, `director`, `writer`, `star`, `country`, `budget`, `gross`, `company`, `runtime`
- **Example row:**  
  *The Shining, R, Drama, 1980, June 13, 1980 United States, 8.4, 927000, Stanley Kubrick, Stephen King, Jack Nicholson, United Kingdom, 19000000, 46998772, Warner Bros., 146*

***

## Cleaning Process

- **Loading:** Data is read with pandas for flexible transformations.
- **Diagnostics:** Ran `.info()` and `.describe()` to identify missing or anomalous values.
- **Handling nulls:**  
    - Dropped all rows with missing essential fields to ensure analytic integrity.
    - Reduced dataset from ~7700 to ~5400 high-quality entries.
- **Column fixing:**  
    - Ensured all numeric columns are proper floats/integers.
    - Split and extracted the 'month' and 'day' from 'released' for improved temporal analysis.
- **Validation:** Rechecked datatypes and summary stats after cleaning.
- **Output:** Clean data written to `moviescleaned.csv`.

***

## Output: Cleaned Dataset

- **File generated:** `moviescleaned.csv`
- **Rows:** 5,400+
- **Columns:** 17 (includes new month and day features)
- **Ready for:** Trend analysis, modeling, visualization.

***

## Usage Instructions

1. Place `moviesoriginal.csv` in your working directory.
2. Run all cells in `TSA_cleaning.ipynb`.
3. Find the cleaned result as `moviescleaned.csv` in the same folder.
4. Use `moviescleaned.csv` for further analysis in downstream notebooks (budget, runtime, release date exploration, etc).

***

## Requirements

- **Python 3.10+**
- **Libraries:**  
    - pandas
    - seaborn (optional, for quick data checks)

Install with:
```bash
pip install pandas seaborn
```

***

## Extensibility / Future Steps

- Add data imputation or fuzzy matching for non-critical missing values.
- Unify naming conventions for companies/genres for better aggregation.
- Enrich with new features: e.g., release decade, region.
- Automate feature creation or outlier detection steps for larger data or periodic refresh.
