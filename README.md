# Operations-Research-Project
# Project Overview
This project aims to identify common characteristics of popular songs using a dataset of approximately 232,000 tracks from Kaggle's 'Spotify Tracks DB'. We analyze various attributes, such as energy, danceability, and acousticness, to train machine learning models that can predict whether a track is popular.

# Dataset
The dataset used for this project, SpotifyFeatures.csv, contains 232,725 tracks and their attributes, including:

Categorical: Genre, artist name, track name, key, mode, time signature
Numerical: Popularity, acousticness, danceability, duration, energy, instrumentalness, loudness, speechiness, tempo, and valence
Features
We engineered a new feature is_popular, which categorizes a song as popular based on its popularity score (cutoff score: 58).

# Data Preprocessing
Handling Duplicates: We identified and removed 55,951 duplicated rows based on track_id.
Feature Engineering: Merged genres with minor discrepancies and engineered binary columns to represent each genre.
Missing Values: No missing values were found.
Outlier Removal: Applied IQR-based methods to handle outliers.
One-Hot Encoding: Categorical features such as key, mode, and time_signature were one-hot encoded.
Model Training
We employed Random Forest Classifier as the main model and used SMOTENC to address class imbalance. The dataset was split into training and testing sets with 30% reserved for testing.

# Evaluation
The project provides functions for:

-Generating classification reports
-Plotting confusion matrices
-Displaying ROC curves to evaluate model performance

# Requirements
Python 3.x
Libraries:
pandas
numpy
matplotlib
seaborn
scikit-learn
imbalanced-learn
Acknowledgments
The dataset used in this project comes from Kaggle's 'Spotify Tracks DB'.
