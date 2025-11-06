# SpaceX Falcon 9 Launch Analysis and Prediction

**Author:** Heet Dave
**GitHub Repository:** https://github.com/heetmdave/SpaceX_Data_analysis

---

## Executive Summary

This project examines historical launch data for the SpaceX Falcon 9 rocket. The primary goal is to analyze launch performance, identify key factors that influence mission success rates, and build a predictive model to forecast future launch outcomes. By analyzing trends and building predictive models, this work aims to enhance the understanding of Falcon 9 reliability and help optimize future launch strategies.

---

## Table of Contents

* [Project Objective](#project-objective)
* [Methodology](#methodology)
    * [1. Data Collection & Wrangling](#1-data-collection--wrangling)
    * [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
    * [3. Predictive Analysis](#3-predictive-analysis)
* [Technologies Used](#technologies-used)
* [Key Results & Findings](#key-results--findings)
* [Model Performance](#model-performance)
* [Conclusion](#conclusion)

---

## Project Objective

The capstone project aims to:
* Analyze the historical launch performance of the SpaceX Falcon 9.
* Assess its reliability and efficiency over time.
* Develop predictive models to forecast the probability of mission success on future launches.
* Identify key factors (e.g., launch site, payload mass, orbit) that correlate with success.

---

## Methodology

The project followed a structured data science pipeline:

### 1. Data Collection & Wrangling

* **Data Sources:**
    * **SpaceX REST API:** Used to retrieve structured launch data, including flight numbers, payload mass, orbit, launch site, and landing outcomes.
    * **Web Scraping:** Scraped Wikipedia pages to supplement the dataset and fill in missing details on payload mass and mission outcomes.
* **Data Wrangling:**
    * Handled missing values by imputing the mean (e.g., for `PayloadMass`).
    * Cleaned the data by removing duplicates and standardizing formats.
    * Converted the target variable (launch outcome) into a binary indicator (0/1) for modeling.

### 2. Exploratory Data Analysis (EDA)

* **Trend & Correlation Analysis:**
    * Visualized relationships between attributes using scatter plots (e.g., Payload vs. Orbit) and bar charts.
    * Used `one-hot encoding` to convert categorical variables (like `Orbit` and `LaunchSite`) into numerical formats for analysis.
* **Interactive Visual Analytics:**
    * Used **Folium** to create interactive maps of launch sites.
    * Employed **Plotly Dash** to build interactive dashboards for data exploration.
* **Database Analysis:**
    * Loaded the dataset into an **SQL** database to perform complex queries.
    * Answered specific questions, such as finding the total payload mass for NASA (CRS) launches or identifying boosters with successful drone ship landings within a specific payload range.

### 3. Predictive Analysis

* **Model Selection:** Trained and evaluated three different classification models to predict launch success:
    1.  **Logistic Regression**
    2.  **Support Vector Machine (SVM)**
    3.  **Decision Trees**
* **Hyperparameter Tuning:** Utilized **GridSearchCV** to find the optimal hyperparameters for each model to maximize performance.

---

## Technologies Used

* **Python**
* **Data Collection:** `requests` library
* **Data Analysis:** SQL (SQLite), Pandas
* **Data Visualization:** Matplotlib, Seaborn, `Folium`, `Plotly Dash`
* **Machine Learning:** Scikit-learn (for Logistic Regression, SVM, Decision Trees, and GridSearchCV)

---

## Key Results & Findings

### EDA Insights
* **Success Trend:** The launch success rate generally increased from 2013 to 2017, dipped in 2018, and then increased again.
* **Highest Success Year:** 2019 was identified as the year with the highest success rate in the visualized data.
* **Best Orbits (Success Rate):** `ES-L1`, `GEO`, `HEO`, and `SSO` showed the highest success rates.
* **Best Orbits (High Payload):** `ISS`, `PO`, and `VLEO` were the most common orbits for high payload masses.

### SQL Query Highlights
* **Total NASA (CRS) Payload:** 619,967 KG
* **Avg. Payload (F9 v1.1):** 2,534.66 KG
* **First Ground Pad Success:** 2010-06-04 (Note: This date appears to be the first *launch* in the dataset, not the first *ground pad success* which was later).
* **Successful Drone Ship Boosters (4-6k KG Payload):** `F9 FT B1022`, `F9 FT B1026`, `F9 FT B1021.2`, `F9 FT B1031.2`

---

## Model Performance

After training and tuning, the models were evaluated based on their accuracy scores:

| Model | Accuracy |
| :--- | :--- |
| **Decision Tree** | **88.9%** |
| Logistic Regression | 83.3% |
| Support Vector Machine (SVM) | 83.3% |

The **Decision Tree classifier provided the best performance** of all tested models.

---

## Conclusion

This analysis reveals a clear trend of increased reliability and cost-efficiency in Falcon 9 launches, driven by reusable technology. The insights gathered emphasize the importance of efficient operational strategies. The predictive models, particularly the Decision Tree, demonstrate a strong capability to predict mission outcomes based on launch parameters.

### Recommendations
* **For SpaceX:** Continue investing in predictive analytics to further refine launch patterns and streamline operations.
* **Future Research:** Explore advanced materials for rocket durability and improved AI algorithms for flight path optimization.

---

## License

This project is open-source. Please feel free to fork, clone, and build upon this work.
