DSA210 Project: Director Fatigue Hypothesis

This project investigates whether directors experience a "fatigue effect" after making long movies, causing their next film to receive lower IMDb ratings.

Author: Kaan Toptas,
Course: DSA210 - Introduction to Data Science,
Date: 3 March 2026

Research Question:
Does a long movie (over 150 minutes) negatively affect the rating of a director's next movie?

Key Findings:
- Directors who made a movie longer than 150 minutes saw their next movie's rating drop by 0.205 points on average.
- Directors with shorter previous movies (under 150 minutes) experienced almost no change (-0.023).
- The difference is statistically significant (p = 0.0106).
- Linear Regression model achieved R² = 0.395 using previous movie runtime and rating as features.

Datasets Used:

1. IMDB Movies Dataset
   Source: Kaggle
   Link: https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows
   Description: Top 1000 movies with details including title, director, runtime, IMDb rating, and release year.

2. TMDB 5000 Movie Dataset
   Source: Kaggle
   Link: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata
   Description: 5000 movies with metadata including original title, runtime, popularity, budget, and revenue.

Methods Used:
- Data merging and cleaning
- Exploratory Data Analysis (EDA) with visualizations
- Independent t-test for hypothesis testing
- Linear Regression and Random Forest for prediction

Project Structure:
- Data loading and merging (IMDb + TMDB)
- Data cleaning and preprocessing
- EDA: distributions, correlation matrix
- Hypothesis testing: t-test with boxplot visualization
- Machine learning: Linear Regression vs Random Forest
- Findings summary and conclusion

How to Run:
1. Download both datasets from Kaggle links above
2. Place CSV files in the same directory as the notebook
3. Run all cells in order
4. Results will be printed and visualizations will appear

Requirements:
- Python 3.7+
- pandas
- matplotlib
- seaborn
- scipy
- scikit-learn

Results Summary:
| Hypothesis | Result | p-value / R² |
|------------|--------|--------------|
| Long previous movie lowers next movie rating | Supported | p = 0.0106 |
| Rating change can be predicted from previous movie features | Partially | R² = 0.395 |

Conclusion:
The project supports the director fatigue hypothesis. Directors who make long movies tend to have lower-rated subsequent films. A linear regression model using previous movie runtime and rating explains about 40% of the variation in rating change.

Limitations:
- Only 459 movies could be matched between the two datasets
- "Fatigue" is measured indirectly via movie runtime
- Other factors like budget, cast, and genre were not controlled

Future Work:
- Include additional features (budget, cast size, genre)
- Analyze specific director career patterns
- Apply time series analysis to detect recovery periods

Repository Contents:
- Jupyter notebook with complete project code
- README.md (this file)
- Project proposal report
- Final report

Contact:
kaan.toptas@sabanciuniv.edu
