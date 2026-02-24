# Web-Series Rating Prediction – Machine Learning Project

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)]()
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)]()
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-F7DF1E?style=for-the-badge)]()
[![Data Science](https://img.shields.io/badge/Data%20Science-4B0082?style=for-the-badge)]()
[![Owner](https://img.shields.io/badge/Owner-RikzahK-blue?style=for-the-badge)]()

**Predicting Web Series Ratings Using Machine Learning Techniques**

This independent project leverages machine learning to analyze and predict web series ratings based on user engagement metrics, metadata, and content tags. It is designed to provide actionable insights for content creators, streaming platforms, and viewers, improving decision-making and personalization.

---

## Project Overview

- **Objective:** Predict web series ratings using metadata, viewer engagement, and tags.  
- **Goal:** Facilitate data-driven decisions for content production and streaming platforms.

---

## Key Features

- **Data Analysis:** Identify patterns, trends, and correlations in web series data.  
- **Machine Learning Models:** Linear Regression to predict ratings accurately.  
- **Visualizations:** Heatmaps, distributions, and charts for easy insights.  
- **Interactive Notebook:** Users can input custom parameters to predict ratings.

---

## Dataset

- **File:** `anime_data.csv`  
- **Columns:** `title, description, mediaType, eps, duration, ongoing, seasonOfRelease, years_running, studio_primary, studios_colab, tags, rating, votes, watched, watching, wantWatch, dropped` (44 total)  
- Includes metadata, viewer engagement, and tag-based features.

---

## Methodology

1. **Data Preprocessing**  
   - Load dataset with `pandas` and handle missing values.  
   - Convert categorical variables using one-hot encoding.  
   - Scale numerical features for consistent input to ML models.

2. **Exploratory Data Analysis (EDA)**  
   - Univariate analysis of `duration`, `episodes`, and `years_running`.  
   - Correlation heatmaps to identify relationships among features.  
   - Key insights: engagement metrics (`votes`, `watched`) strongly influence ratings.

3. **Feature Selection**  
   - Selected relevant continuous and categorical features.  
   - Removed redundant or low-impact features for optimal performance.

4. **Model Development**  
   - Linear Regression for interpretable results.  
   - Trained on `X_train` and evaluated on `X_test`.  
   - Input included both numeric and encoded categorical features.

5. **Evaluation Metrics**  
   - **RMSE:** Root Mean Squared Error  
   - **MAE:** Mean Absolute Error  
   - **R²:** Coefficient of Determination

---

## Data Analysis & Visualizations

- Univariate & bivariate analyses to understand distributions and correlations.  
- Heatmaps revealed:  
  - High correlation between `votes` and `rating`.  
  - Moderate correlation between `watched` and `rating`.  
  - Minimal effect of collaborative studios on ratings.  

*Visualizations are included in the Jupyter Notebook.*

---

## Model Building

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score

# Load and preprocess dataset
dataset = pd.read_csv("anime_data.csv")
X = pd.get_dummies(dataset.drop(['rating'], axis=1), drop_first=True)
Y = dataset['rating']

# Train-test split
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size=0.2, random_state=42)

# Linear Regression Model
lin_model = LinearRegression()
lin_model.fit(X_train, Y_train)

# Evaluation Function
def evaluate_model(model, X, Y):
    pred = model.predict(X)
    rmse = mean_squared_error(Y, pred, squared=False)
    mae = mean_absolute_error(Y, pred)
    r2 = r2_score(Y, pred)
    return rmse, mae, r2

train_metrics = evaluate_model(lin_model, X_train, Y_train)
test_metrics = evaluate_model(lin_model, X_test, Y_test)





# Web-Series-Rating-Prediction
The Web Series Rating Prediction project leverages machine learning techniques to analyze and predict the ratings of various web series based on user preferences and metadata. With the surge in streaming platforms, understanding viewer sentiment and ratings can help content creators tailor their offerings more effectively. This project aims to provide accurate rating predictions, facilitating better decision-making for both viewers and producers.


# Key Features:
Data Analysis: Comprehensive exploration of web series data, identifying trends and patterns.
Machine Learning Models: Implementation of various algorithms to predict ratings effectively.
User Interface: A simple interface for users to input parameters and receive predictions.
Visualizations: Graphical representations of data to facilitate easy comprehension of insights.

<img width="588" alt="image" src="https://github.com/user-attachments/assets/cfc610b3-64ae-4a8d-a691-60f74282ccc4">
