# Web-Series Rating Prediction – Machine Learning Project

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)]()
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)]()
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-F7DF1E?style=for-the-badge)]()
[![Data Science](https://img.shields.io/badge/Data%20Science-4B0082?style=for-the-badge)]()
[![Owner](https://img.shields.io/badge/Owner-RikzahK-blue?style=for-the-badge)]()

**Predicting Web Series Ratings Using Machine Learning Techniques**

This independent project leverages machine learning to analyze and predict web series ratings based on user engagement metrics, metadata, and content tags. It is designed to provide actionable insights for content creators, streaming platforms, and viewers, improving decision-making and personalization.
-
<img width="588" alt="image" src="https://github.com/user-attachments/assets/cfc610b3-64ae-4a8d-a691-60f74282ccc4">

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

## Data Exploration

**Dataset:** `anime_data.csv`  
**Features:** Title, Description, Media Type, Episodes, Duration, Studio, Tags, Viewer Engagement (`watched`, `watching`, `wantWatch`, `dropped`), Ratings, Votes, etc.

**Preview of the Dataset:**

| title | mediaType | eps | duration | ongoing | years_running | studio_primary | rating | votes |
|-------|-----------|-----|---------|--------|---------------|----------------|-------|-------|
| Fullmetal Alchemist: Brotherhood | TV | 64 | 1750 | False | 1 | Bones | 9.2 | 58831 |
| Your Name | Movie | 1 | 107 | False | 1 | CoMix Wave Films | 8.9 | 45892 |

**Exploratory Analysis:**  

- **Univariate Analysis** on `duration`
<img width="1014" height="602" alt="image" src="https://github.com/user-attachments/assets/7d049fce-376f-4f48-a99d-c896216eb5ee" />


- **Correlation Analysis** between numeric features:

<img width="1261" height="672" alt="image" src="https://github.com/user-attachments/assets/dc0332cb-1969-4d80-b691-8dfed5258c2b" />

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



## Model Performance

| Dataset | RMSE  | MAE   | R²    |
|---------|-------|-------|-------|
| Train   | 0.583 | 0.473 | 0.512 |
| Test    | 0.578 | 0.471 | 0.501 |

**Insights:**

- The model generalizes well to unseen data.
- Viewer engagement metrics (`watched`, `votes`) are strong predictors.
- Linear Regression provides interpretable relationships between features and ratings.

---

## Findings & Insights

- Ratings are mostly influenced by **votes, watched counts, and series duration**.
- Genre tags and production studios have **marginal effects**.
- Ensemble models or advanced regression techniques could further improve predictions.
- Visualizations and correlation analysis help content creators **optimize content strategy**.

---

## How to Use

1. **Clone the repository:**
```bash
git clone https://github.com/RikzahK/Web-Series-Rating-Prediction-Machine-Learning-Project.git



