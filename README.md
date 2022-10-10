# Cryptocurrencies
Using a clustering algorithm and data visualization to report on what cryprocurrencies are on the trading market and how they can be grouped to create a classification system for a potential investment.

## Purpose
Cryptocurrencies can be overwhelming when creating or adding to an investment portfolio.  This repository includes code that takes a dataset of cryptocurrencies, cleans the dataset to be usable by unsupervised machine learning models, and groups them using a clustering algorithm to be put  into data visualizations that can be used to share findings and make decisions regarding future investment.

## Software, Languages, and Libraries

### Software
- Jupyter Notebook

### Languages
- Python

### Libraries
- pandas
- pathlib
- plotly
- sklearn


## Original csv Loaded into a Dataframe
ORIGINAL DF PIC

## Data Munging
Un-needed columns, null values, cryptocurrencies with 0 coins mined, and those marked as not trading were removed. The coin names column was moved to a separate dataframe.  Then, non-numeric data was converted to binary and the whole dataframe was scaled in preparation for dimension reduction.

NAMES AND CLEANED_DF PIC

## Reducing Data Dimensions using PCA
The PCA model was initialized with 3 components to reduce dimension of the original dataset.

PCA PIC

## Clustering using K-Means
K-Means was used to determine the appropriate number of clusters the dataset would fit into.  It was determined that 4 clusters would be used to class the data.  A new Dataframe was then created to include both the Primary Components and new class IDs.

KMEANS PIC
COMPONENT PIC

## Visualizations
The PCA data was used to create a 3D Scatter plot that has the coin name and algorithm when hovering over the plotted point.

3D PIC

A table was created using hvplot that allows sorting.

TABLE

A 2D Scatter plot was created to show the relationship between Total Coins Mined and The Total Coin Supply.  This plot has Class, Coins Mined, Coin Supply, and Coin Name in a pop up when hovering over the data point.

SUPPLYVSMINED