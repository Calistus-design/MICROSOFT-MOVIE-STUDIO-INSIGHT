# MICROSOFT MOVIE STUDIO INSIGHT
# Table of Content
>* Title
>* Project Overview
>* Business Problem
>* Project Goal
>* Project Objectives
>* Imprted Libraries
>* Datasets 
`1. im.db`
`2. tn.movie_budgets.csv.gz`
>* Data Loading
>* Data Cleaning
>* Data Preparation
>* Data Analysis
>* Conclusion
>* Business Recommendations


## PROJECT OVERViEW
- The aim of this project is to analyze which type of films are currently doing the best at the box office to help the company decide which type of films to create.

## BUSINESS PROBLEM
- A company has decided to create a new movie studio, but they don’t know anything about creating movies. We are charged with exploring what types of films are currently doing the best at the box office. We must then translate those findings into actionable insights that the head of this company's new movie studio can use to help decide what type of films to create.

## PROJECT GOAL

- To identify the key factors that drive movie success (financially and with audiences) in order to guide the new movie studio on what types of films to produce, invest in, and promote.

##  Objectives

1. **Identify high-performing movie genres** based on average viewer ratings and worldwide gross revenue.
2. **Determine which directors, writers, and actors** are associated with top-performing movies.
3. **Assess the impact of production budgets** on movie performance.

##  Datasets

- **IMDb (SQLite Database: `im.db`)**
  - `movie_basics`
  - `movie_ratings`
  - `directors`
  - `persons`

- ** (`tn.movie_budgets.csv.gz`)**
  - Contains data on production budgets and worldwide gross.

## Tools & Libraries
### python
`import pandas as pd`
`import gzip`
`import numpy as np`
`import sqlite3`
`import matplotlib.pyplot as plt`
`%matplotlib inline`
`import seaborn as sns`
`import scipy.stats as stats`

## Data Preparation Steps
- Loaded and merged IMDb and The Numbers datasets.

- Filtered top 10 genres based on frequency.

- Exploded multi-genre rows for genre-level analysis.

- Assigned experience levels to directors and actors.

- Binned production budgets and worldwide gross into Low, Medium, and High categories.

- Merged and cleaned all relevant tables for analysis.

## Exploratory Data Analysis (EDA)
1. Genre vs. Performance
### Research Question:
- Can average rating be used as an indicator of film performance?

### Hypotheses:

- H0: No significant difference exists between genres and average ratings.

- H1: A significant difference exists between genres and average ratings.

### Visualizations:

- Bar plot of average rating by genre

- Bar plot of average worldwide gross by genre

### ANOVA test to assess significance

 **Director, Writer, and Actor Influence**
### Steps:

- Calculated number of movies each director has made (experience count)

- Mapped experience to names

- Filtered data to top 10 genres for focused analysis

### Visualizations:
- Box plot of Average ratings by Genre
  ![image](https://github.com/user-attachments/assets/13fcb1af-dd55-474e-89a7-9508307dc9fe)

- Bar plots of average rating by director (top 10 genres)

- Bar plots of average rating by actor (top 10 genres)

2. Budget vs. Movie Performance
### Hypotheses:

- H0: No association exists between production budget and worldwide revenue.

- H1: A significant association exists between production budget and worldwide revenue.

##3 Statistical Tests & Visuals:

- Pearson correlation between budget and gross

- Chi-squared test on binned budget/gross categories

- Heatmap showing the relationship between budget and gross

### Additional Visuals
- Distribution plots of production budgets and worldwide gross

- Binned budget and gross categories with corresponding bar plots

## Conclusion




## Recommendations
