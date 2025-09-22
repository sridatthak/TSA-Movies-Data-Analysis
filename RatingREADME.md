# TSA-Movies-Data-Analysis
Using Pandas libraries and Seaborn data analysis, I compiled a documentation portfolio analyzing the factors that influence success for movies.

# Movie Rating Analysis

This repository contains a comprehensive analysis of movie ratings and their relationship to various performance metrics using Python data visualization libraries.

## Project Overview

The analysis examines how movie ratings (G, PG, PG-13, R, etc.) correlate with:
- Average movie scores
- Number of votes received
- Gross revenue performance

## Dataset

The analysis uses a dataset (`movies_cleaned.csv`) containing information about movies from 1980 to 2020, including:
- Movie names and basic information
- MPAA ratings (G, PG, PG-13, R, etc.)
- IMDb scores and vote counts
- Financial data (budget and gross revenue)
- Production details (director, writer, stars, company)
- Release information

## Analysis File

### `Rating.ipynb`
A Jupyter notebook containing the complete rating analysis with:

**Data Exploration:**
- Dataset overview and statistical summaries
- Data structure examination

**Visualizations:**
- Bar plots comparing ratings across different metrics
- Score distribution by rating category
- Vote count analysis by rating
- Revenue performance by rating

**Key Findings:**
- **Score Analysis**: Most rating categories showed similar average scores, with "Approved" having the lowest average and "X" having the highest (by a small margin)
- **Popularity (Votes)**: PG-13 movies received the most votes on average, followed by G-rated films, while "Approved" movies received significantly fewer votes
- **Revenue Analysis**: Analysis of gross earnings across different rating categories

## Libraries Used

- **pandas**: Data manipulation and analysis
- **seaborn**: Statistical data visualization
- **matplotlib**: Plotting and visualization

## Key Insights

1. **Score Uniformity**: Movie ratings don't significantly impact critical scores, suggesting quality is consistent across rating categories
2. **Audience Engagement**: PG-13 movies attract the most audience engagement (votes), likely due to their broader appeal
3. **Market Performance**: Different rating categories show varying patterns in revenue generation

## Getting Started

1. Ensure you have the required libraries installed:
   ```bash
   pip install pandas seaborn matplotlib
   ```

2. Run the Jupyter notebook:
   ```bash
   jupyter notebook Rating.ipynb
   ```

3. Make sure `movies_cleaned.csv` is in the same directory as the notebook

## Future Enhancements

- Analysis of rating trends over time
- Correlation between budget and rating category
- Genre-specific rating analysis
- International vs domestic performance by rating

## Contributing

Feel free to fork this repository and submit pull requests for additional analyses or improvements to the existing code.
