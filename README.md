# Spotify Trends 2019-2023

## Comparative Music Data Analysis

This project explores how popular Spotify tracks changed between 2019 and 2023, with a specific focus on **danceability** and how listener preferences may have shifted before and after the COVID period.

At the center of the notebook is one guiding question:

> Are Spotify tracks in 2023 more danceable than tracks in 2019?

The notebook approaches that question through a combination of:

- data cleaning
- feature comparison
- clustering
- association rule mining
- statistical hypothesis testing

## Why this notebook is interesting

- It compares two real music datasets across different years.
- It combines exploratory data analysis with machine learning techniques.
- It links numerical audio features to broader cultural and listening trends.
- It moves beyond simple charts by including clustering, Apriori analysis, and a t-test.

## Research question

- Is it true that tracks in 2023 have higher danceability than tracks in 2019?

## Datasets used

The analysis uses two Spotify datasets:

- `top2019.csv`
- `top2023.csv`

These datasets are primarily analyzed side by side rather than merged into one master table, which keeps the year-to-year comparison clearer throughout the notebook.

## Tech stack

- Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy
- mlxtend

## What the notebook does

### 1. Data cleaning and preparation

The notebook begins by preparing both datasets for analysis.

This includes:

- loading the raw CSV files
- checking column names and preview rows
- computing summary statistics
- converting selected columns to numeric format
- filling missing values in both numeric and categorical fields
- standardizing selected 2023 feature names so they align with 2019 naming
- exporting cleaned datasets for later reuse

Generated cleaned files:

- `top 2019_cleaned.csv`
- `top2023_cleaned.csv`

### 2. Feature comparison across years

The notebook compares important Spotify audio features such as:

- danceability
- energy
- valence
- acousticness
- instrumentalness
- liveness
- speechiness
- tempo

These comparisons help identify how the musical profile of popular songs changed between 2019 and 2023.

### 3. Clustering analysis

KMeans clustering is used to group songs by musical similarity.

The clustering sections focus especially on:

- `energy`
- `instrumentalness`

This makes it possible to identify broad song groups such as:

- high-energy, low-instrumentalness tracks
- balanced tracks with moderate energy and instrumentalness
- low-energy, highly instrumental tracks

The notebook visualizes these clusters and compares how their distributions changed across the two years.

### 4. Association rule mining

The notebook also applies the **Apriori algorithm** to discover frequent combinations of danceability and energy levels.

This section:

- normalizes danceability and energy
- bins those features into levels such as `very_low`, `low`, `medium`, and `high`
- builds grouped frequency tables
- extracts frequent itemsets
- generates association rules using lift
- visualizes relationships with heatmaps and bar charts

This helps reveal how danceability and energy tend to appear together in the 2023 Spotify data.

### 5. Hypothesis testing

To answer the main research question more formally, the notebook runs a **t-test** comparing danceability in 2019 and 2023.

This section includes:

- average danceability comparison
- distribution plots for both years
- t-statistic and p-value calculation
- interpretation of statistical significance

## Main finding

The notebook concludes that tracks in 2023 are more danceable than tracks in 2019, and that the difference is statistically significant according to the test used in the analysis.

The final interpretation suggests a broader shift toward more energetic, socially engaging, and upbeat music in the post-COVID period.

## Notebook structure

The notebook is organized into the following sections:

- introduction and research framing
- terminology for Spotify audio features
- data cleaning
- data integration and feature selection
- data transformation
- clustering
- Apriori analysis
- statistical testing
- conclusion
- bibliography
