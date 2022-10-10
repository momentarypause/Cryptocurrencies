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
![original_dataframe](https://user-images.githubusercontent.com/102555125/194940136-d55da23d-e40a-481d-a798-a5197381c733.png)


## Data Munging
Un-needed columns, null values, cryptocurrencies with 0 coins mined, and those marked as not trading were removed. The coin names column was moved to a separate dataframe.  Then, non-numeric data was converted to binary and the whole dataframe was scaled in preparation for dimension reduction.

![names](https://user-images.githubusercontent.com/102555125/194940176-48d0aecf-12f4-4d18-bff0-abca82e89aac.png)
![cleaned_df](https://user-images.githubusercontent.com/102555125/194940192-948b87a9-a0f2-49e7-a8be-0997b16e9c89.png)


## Reducing Data Dimensions using PCA
The PCA model was initialized with 3 components to reduce dimension of the original dataset.


![PCA pdf](https://user-images.githubusercontent.com/102555125/194940224-b0004d29-8548-4ae9-9f6f-4b031bf3f4ee.png)


## Clustering using K-Means
K-Means was used to determine the appropriate number of clusters the dataset would fit into.  It was determined that 4 clusters would be used to class the data.  A new Dataframe was then created to include both the Primary Components and new class IDs.

![KMeans](https://user-images.githubusercontent.com/102555125/194940270-fa7ed728-9921-484f-acf7-28f86dc2aad7.png)
![component_class-_df](https://user-images.githubusercontent.com/102555125/194940285-a080839a-31bc-4f75-b902-c39e07ff5079.png)


## Visualizations
The PCA data was used to create a 3D Scatter plot that has the coin name and algorithm when hovering over the plotted point.

![3D_scatter](https://user-images.githubusercontent.com/102555125/194940322-62d24e02-f206-4b4f-ae04-75357b2d6374.png)


A table was created using hvplot that allows sorting.

![crypto_table](https://user-images.githubusercontent.com/102555125/194940361-caa064bb-2ec8-49ac-8ca6-7c1cff384363.png)


A 2D Scatter plot was created to show the relationship between Total Coins Mined and The Total Coin Supply.  This plot has Class, Coins Mined, Coin Supply, and Coin Name in a pop up when hovering over the data point.

![supplyVSMined](https://user-images.githubusercontent.com/102555125/194940394-4cbd63f6-0ad2-4b2d-8648-4c7310dec3f0.png)

