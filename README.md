# CodeAlpha_WorldHappinessAnalysis
CodeAlpha Data Analytics Internship: EDA and data visualization of the World Happiness Report (2005–2021), with a focus on South Asia.
# CodeAlpha Data Analytics Internship: World Happiness Report

**Dataset:** [World Happiness Report 2005–2021](https://www.kaggle.com/datasets/jahaidulislam/world-happiness-report-2005-2021) (Kaggle), 2,089 country-year rows, 12 columns, with a focus on South Asia.

This repo has two tasks:

| Task | File | What it does |
|---|---|---|
| Task 2: Exploratory Data Analysis | `Task_2.ipynb` | Cleaning, statistics, hypothesis tests, prediction models |
| Task 3: Data Visualization | `Task_3.ipynb` | Data story told through charts |

## Task 2: EDA
**Questions:** What drives happiness? Is South Asia different? How did COVID-19 change happiness? Can a model predict it?

- Cleaned the data: snake_case columns, missing values filled with country medians, duplicate checks
- Outlier check (IQR) and distribution and correlation analysis
- Hypothesis tests: Welch t-test, Mann-Whitney U, Pearson and Spearman correlation
- COVID comparison using the same countries in every year
- Models: Linear Regression (R² = 0.783) and Random Forest (R² = 0.874)

**Key findings**
- GDP per capita (r = 0.78), social support (0.71) and healthy life expectancy (0.71) are the strongest correlates of happiness.
- South Asia averages 4.52 vs 5.52 for the rest of the world (6 countries only, so this is descriptive).
- A model trained without South Asia fits it poorly (R² = -0.297), so the standard factors do not fully explain happiness there.

## Task 3: Visualization
Six charts, built with Matplotlib and Seaborn:
1. Top 10 and bottom 10 countries by happiness (2017–2021)
2. Global happiness trend, same 84 countries every year
3. What is most related to happiness (correlation bars)
4. GDP vs happiness, with South Asia highlighted
5. India, Nepal and Pakistan vs the rest of the world
6. South Asian countries over time, with Bangladesh highlighted

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, scikit-learn

## How to run
1. Open a notebook in Google Colab or Jupyter.
2. Run all cells. The dataset downloads automatically with `kagglehub`.

## Limitations
- Missing values were filled with medians.
- Only 6 South Asian countries are in the data, and fewer have data in every year.
- Correlation does not prove causation.

*Made for the CodeAlpha Data Analytics Internship.*
