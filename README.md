# Investor Behavior Analytics — Data Cleaning & Visualization

A data cleaning and exploratory analysis project on a 40-respondent survey about
personal investment behavior (Kaggle's "Finance Data" dataset). Built for a
Phase 2 data cleaning & visualization assignment.

## What's in this project

- `investment.csv` — the raw survey data (gender, age, investment preferences,
  rankings of 7 investment types, reasons for choosing them, etc.)
- `investor-behavior-analytics.ipynb` — the full analysis: load → explore →
  clean → visualize → summarize

## Dataset

40 survey respondents answered questions about how they invest, including
ranking 7 investment avenues (Mutual Funds, Equity Market, Debentures,
Government Bonds, Fixed Deposits, PPF, Gold) from 1-7 by preference, plus
demographic and behavioral questions (age, gender, investment duration,
what they monitor, expected returns, etc.).

## What I found during exploration

Unlike a lot of "messy" practice datasets, this one had **zero missing values
and zero duplicate rows**. So instead of the usual fill/drop-missing-values
cleaning, the real cleaning work here was:

- Fixed a typo'd column name (`Stock_Marktet` → `Stock_Market`)
- Renamed a long, awkward column name (`What are your savings objectives?` →
  `Savings_Objective`)
- Converted `Investment_Avenues` and `Stock_Market` from Yes/No text to proper
  booleans
- Encoded `Duration` as an ordered category (Less than 1 year → 1-3 years →
  3-5 years → More than 5 years) instead of an unordered string, so it sorts
  and plots correctly
- Converted `gender` to a category dtype

## Visualizations

1. **Histogram** — distribution of respondent age
2. **Bar chart** — preferred investment avenue, broken down by gender
3. **Correlation heatmap** — how the 7 ranked investment preferences relate
   to each other

## Key insights

1. **Sample size caveat:** with only 40 respondents, these patterns are
   suggestive, not statistically robust.
2. **Age:** respondents skew young — mostly in their 20s-30s, working-age
   professionals just starting to think seriously about investing.
3. **Most preferred avenue:** the most commonly selected top investment
   avenue was Mutual Funds/Equity (see chart for the exact split by gender).
4. **Ranking trade-off:** Government Bonds and Fixed Deposits showed the
   strongest correlation in the dataset (-0.53) — despite both being
   conservative, low-risk options, respondents who ranked one highly tended
   to rank the other low, treating them as substitutes rather than
   complementary choices.

## Tools

Python, pandas, numpy, matplotlib, seaborn — run in Google Colab.

## Why this dataset

Started with the Titanic dataset as suggested in the assignment brief, but
switched to this investment behavior survey to work with something closer
to real-world financial/behavioral data. It turned out to have less "mess"
than expected (no nulls/duplicates), which shaped what the cleaning step
focused on — worth noting since the assignment brief assumes a messier
dataset than this one turned out to be.
