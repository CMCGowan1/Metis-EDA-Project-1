# Subway Station Analysis for Street Team Placement for WTWY

Cheryl McGowan

### Abstract

The goal of this project was to use MTA subway turnstile data to  identify locations for the WomenTechWomenYes organization to recommend placement of street teams to maximize email address collection points in NYC.  The data was cleaned up for reverse station entries, duplicates and outliers.  The information was plotted on a bar graph using Matplotlib.  I compared the stations with the most traffic to commercial real estate maps showing the locations of big tech and start-up tech companies. The commercial data is based on lease activity and real estate purchases for the tech sector.

### Design

This project originates as a client request from WTWY.  

from the DrivenData competition "Pump it Up: Data Mining the Water Table". The data is provided by Taarifa and the Tanzanian Ministry of Water, and presents a three-class operational status of functional, functional needs repair, and non-functional for waterpoints across the country. Classifying statuses accurately via machine learning models would enable the Tanzanian Ministry of Water to take action to improve operations and maintenance planning of these units, allocate resources more quickly to needed areas, and ensure potable water is accessible to as many people as possible.

### Data

The dataset is from the public MTA data set of turnstile records for 6 months from Jan 1, 2021 to Sept 3, 2021.  It contains over 7 million entries or rows from 379 stations.  One observation is the cumulative number of daily entries collected at a turnstile for a 24 hour period. The features of this data are C/A UNIT, SCP, STATION, LINENAME, DIVISION, DATE, TIME, DESc, ENTRIES AND EXITS.


calculations for PREV_DATE, PREV_ENTRIES, AND DAILY_ENTRIES are shown in the column headers.

C/A represents Control areas
UNIT is a remote unit for a station
SCP is a specific turnstile device
STATION is the station location where the device is located

59,400 waterpoints with 40 features for each, 32 of which are categorical. A few feature highlights include measurements of water quantity and quality, pump types, and latitude/longitude coordinates. Nearly a third of the individual features could be grouped into more general categories, and an in-depth analysis of 20 of them was undertaken to inform baseline models and feature engineering.

### Algorithms

Feature Engineering

Mapping latitude and longitude to 3-dimensional coordinates so nearby continuous values would also be close in reality
Converting categorical features to binary dummy variables
Combining particular dummies and ranges of numeric features to highlight strong signals and illogical values for waterpoint status identified during EDA
Selecting subsets of the total unique values for categorical features that were converted to dummies, according to the number of samples they were associated with and their contribution to certain statuses
Models

Logistic regression, k-nearest neighbors, and random forest classifiers were used before settling on random forest as the model with strongest cross-validation performance. Random forest feature importance ranking was used directly to guide the choice and order of variables to be included as the model underwent refinement.

### Tools

### Communication

Model Evaluation and Selection

The entire training dataset of 59,400 records was split into 80/20 train vs. holdout, and all scores reported below were calculated with 5-fold cross validation on the training portion only. Predictions on the 20% holdout were limited to the very end, so this split was only used and scores seen just once.

The official metric for DrivenData was classification rate (accuracy); however, class weights were included to improve performance against F1 score and provide a more useful real-world application where classification of the minority class (functional needs repair) would be essential.

Final random forest 5-fold CV scores: 99 features (7 numeric) with class weights

Accuracy 0.797
F1 0.791 micro, 0.679 macro
precision 0.792 micro, 0.722 macro
recall 0.797 micro, 0.658 macro
Holdout

Accuracy: 0.802
F1: 0.795 micro, 0.685 macro
Precision: 0.796 micro, 0.725 macro
Recall: 0.802 micro, 0.664 macro
Tools

Numpy and Pandas for data manipulation
Scikit-learn for modeling
Matplotlib and Seaborn for plotting
Tableau for interactive visualizations
Communication

In addition to the slides and visuals presented, Tanzania Waterpoints will be embedded on my personal website and blog.
