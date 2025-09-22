# Movie Runtime Exploration and Analysis

Explore the role of **movie runtimes** in shaping audience reception and box office outcomes. This Jupyter Notebook (`Runtime.ipynb`) provides a comprehensive data analysis workflow for uncovering trends, patterns, and insights around the length of films.

***

## Table of Contents

- Project Overview
- Dataset Description
- Preprocessing & Cleaning
- Analytical Approach
- Visualizations & Outputs
- Summary of Insights
- How to Use
- Requirements
- Future Improvements

***

## Project Overview

- Investigate the **distribution and effects of movie runtimes** over several decades.
- Analyze how runtime relates to **IMDB score** and **gross box office revenue**.
- Address key questions, such as:  
  - Are longer movies generally better rated?
  - Does runtime impact commercial success?

***

## Dataset Description

- **Input dataset:** `moviescleaned.csv`
- **Key Columns Used:**  
    - `runtime`, `score`, `gross`, `genre`, `year`, `name`, `released`
- **Scope:**  
    - Multidecade, multigenre movie listing covering large-scale industry trends.

***

## Preprocessing & Cleaning

- Data loaded via pandas, numerics cast to correct types.
- **Missing and irregular data** (e.g., films with no runtime) are addressed for robust analysis.
- Ready for numeric, statistical, and visualization-based study.

***

## Analytical Approach

- **Runtime Distribution:**  
  - Histogram of run times, highlighting most common movie lengths.
- **Runtime vs. IMDB Score:**  
  - Scatter plot to discern whether longer or shorter films cluster at certain ratings.
- **Runtime vs. Gross Revenue:**  
  - Scatter plot comparing log-scaled box office revenue to runtime, revealing outliers and earning patterns.
- **Summary statistics** for each aspect.

***

## Visualizations & Outputs

- **Histogram:**  
    - Visualizes where most film runtimes fall (e.g., 90–120 minutes is most common).
- **Scatter Plots:**  
    - Runtime vs. IMDB Score, showing the diversity of ratings across runtimes.
    - Runtime vs. Gross Revenue (log scale) to handle vast differences in earnings.
- **Descriptive Comments:**  
    - Interprets each plot and highlights interesting or counterintuitive patterns.

***

## Summary of Insights

- Most movies have runtimes between **90 and 120 minutes**.
- **No strong correlation** between runtime and IMDB score: both long and short films achieve high and low scores.
- Outliers (long or short yet high-earning or highly rated films) highlight industry exceptions.
- **Earnings patterns** are scattered; success isn’t strictly a function of runtime.

***

## How to Use

1. Place `moviescleaned.csv` in your notebook folder.
2. Open `Runtime.ipynb` and run all cells in sequence.
3. Examine the resulting charts and inline explanations for a quick grasp of runtime-related trends.

***

## Requirements

- **Python 3.10+**
- **Libraries:**  
    - `pandas`, `matplotlib`, `seaborn`

Install with:
```bash
pip install pandas matplotlib seaborn
```

***

## Future Improvements

- Explore **runtime trends by genre, country, or year** for richer segmentation.
- Integrate streaming/OTT data to see if runtimes are changing in the digital era.
- Build predictive models for the impact of runtime on awards or critical success.
