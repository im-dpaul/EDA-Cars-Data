# Auto Analytics: Exploring Car Market Dynamics

This project conducts Exploratory Data Analysis (EDA) on a dataset containing information about cars. It covers various aspects of data preprocessing, visualization, and analysis to derive insights into the characteristics and trends of the cars.

## Table of Contents
- [Introduction](#introduction)
- [Steps](#steps)
  1. [Importing Libraries](#1-importing-libraries)
  2. [Loading Data and Data Understanding](#2-loading-data-and-data-understanding)
  3. [Data Cleaning](#3-data-cleaning)
  4. [Detecting Outliers](#4-detecting-outliers)
  5. [Visualization](#5-visualization)

## Introduction
This project aims to explore and analyze a dataset related to cars, uncovering insights into various attributes such as price, horsepower, and cylinders. By performing EDA, we gain a deeper understanding of the dataset and its underlying patterns.

## Steps

### 1. Importing Libraries
- Pandas: Used for data manipulation and analysis.
- NumPy: Utilized for numerical computations.
- Seaborn: Employed for data visualization.
- Matplotlib: Utilized for creating plots and charts.

### 2. Loading Data and Data Understanding
   - The "cars_data.csv" file is loaded into a pandas DataFrame (`df`).
   - The first and last five rows (`df.head(5)`, `df.tail(5)`) are displayed to get a glimpse of the data structure.
   - Basic data information (`df.info()`) is explored, including data types (`df.dtypes`) and descriptive statistics (`df.describe()`).

### 3. Data Cleaning
   - Irrelevant columns (`'Engine Fuel Type'`, `'Market Category'`, etc.) are dropped (`df.drop(...)`).
   - Column names are made more descriptive (`df.rename(...)`).
   - Duplicate rows are identified (`duplicate_rows_df`) and removed (`df.drop_duplicates()`).
   - Missing values (`df.isna().sum()`) are examined and dropped (`df.dropna()`).

### 4. Detecting Outliers
   - Boxplots are generated (`sns.boxplot(...)`) to visualize potential outliers in columns like price and horse power.
   - Interquartile Range (IQR) is calculated to define outlier thresholds.
   - Rows with values outside the outlier range (`IQR`) are removed.

### 5. Visualization
   - A bar chart (`plt.bar(...)`) shows the distribution of car makes.
   - A heatmap (`sns.heatmap(...)`) visualizes correlations between numerical features.
   - A scatter plot (`plt.scatter(...)`) explores the relationship between horsepower and price.
