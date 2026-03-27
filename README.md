# Feature Selection and Predictive Modeling Portfolio

Welcome to my machine learning portfolio. This repository contains two distinct data science projects focused on **Exploratory Data Analysis (EDA)**, **Feature Engineering**, and **Advanced Feature Selection** methodologies. 

The primary objective across these projects is to demonstrate how strategically reducing the dimensionality of a dataset can optimize computational efficiency without sacrificing predictive accuracy.

## Table of Contents
- [Project Overview](#project-overview)
  - [Project 1: Student Mental Health & Burnout](#project-1-student-mental-health--burnout)
  - [Project 2: YouTube Shorts Engagement Velocity](#project-2-youtube-shorts-engagement-velocity)
- [Methodologies Applied](#methodologies-applied)
- [Technologies Used](#technologies-used)
- [How to Run the Code](#how-to-run-the-code)
- [License](#license)

---

## Project Overview

### Project 1: Student Mental Health & Burnout
**Objective:** Predict a student's Cumulative Grade Point Average (CGPA) based on academic pressures, lifestyle habits, and mental health indicators.
* **Dataset:** 150,000+ records containing metrics such as sleep hours, study hours, anxiety scores, and screen time.
* **Key Focus:** Handling categorical variables via One-Hot Encoding and identifying non-linear relationships using Mutual Information to prevent data loss.
* **Outcome:** Successfully demonstrated that a strategically selected subset of 5 features yields a predictive $R^2$ score comparable to the baseline model utilizing all 20+ features, thereby reducing model complexity and potential overfitting.

### Project 2: YouTube Shorts Engagement Velocity
**Objective:** Predict the total 'Views' of a YouTube Short utilizing core engagement metrics while handling heavy power-law (Pareto) distributions.
* **Dataset:** Real-world social media metrics including Likes, Comments, and Engagement Rates.
* **Key Focus:** Addressing severe multicollinearity among social metrics and actively preventing data leakage (e.g., removing deterministic features like `Views_Per_Day`).
* **Outcome:** Utilized Random Forest Regressors to capture non-linear relationships, identifying the most critical engagement signals that drive algorithmic reach.

---

## Methodologies Applied

Both projects utilize a rigorous, comparative pipeline to evaluate feature importance:

1. **Exploratory Data Analysis (EDA):**
   * Missing value detection and imputation.
   * Target variable distribution analysis (including log-scaling for extreme outliers).
   * Correlation heatmaps and pairplot visualizations to detect multicollinearity.
2. **Filter Methods (The Statistician):**
   * Utilizing `mutual_info_regression` to evaluate each feature's shared information with the target variable independently of any model.
3. **Wrapper Methods (The Trial Coach):**
   * Utilizing **Recursive Feature Elimination (RFE)** to iteratively train models and eliminate the weakest contributing features based on performance ranks.
4. **Embedded Methods (The Veteran):**
   * Utilizing **Random Forest Feature Importance** (Gini importance) to naturally evaluate and select features dynamically during the tree-building process.
5. **Final Evaluation:**
   * Isolating the top features from each selection method and testing them against a baseline model on unseen data to quantify the $R^2$ performance delta.

---

## Technologies Used

* **Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (`LinearRegression`, `RandomForestRegressor`, `SelectKBest`, `RFE`, `mutual_info_regression`)
* **Data Visualization:** `matplotlib`, `seaborn`
* **Environment:** Jupyter Notebook

---

## How to Run the Code

1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/Jayesh-001/Feature_selection.git](https://github.com/Jayesh-001/Feature_selection/.git)
