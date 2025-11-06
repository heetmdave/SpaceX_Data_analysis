# 🚀 SpaceX Falcon 9 Launch Analysis and Prediction

[cite_start]**Author:** Heet Dave [cite: 4, 231]
[cite_start]**GitHub Repository:** [https://github.com/heetmdave/SpaceX_Data_analysis](https://github.com/heetmdave/SpaceX_Data_analysis) [cite: 1]

---

## 📜 Executive Summary

[cite_start]This project examines historical launch data for the SpaceX Falcon 9 rocket[cite: 2, 24]. [cite_start]The primary goal is to analyze launch performance, identify key factors that influence mission success rates, and build a predictive model to forecast future launch outcomes[cite: 21]. [cite_start]By analyzing trends and building predictive models, this work aims to enhance the understanding of Falcon 9 reliability and help optimize future launch strategies[cite: 25].

---

## 📋 Table of Contents

* [Project Objective](#-project-objective)
* [Methodology](#-methodology)
    * [1. Data Collection & Wrangling](#1-data-collection--wrangling)
    * [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
    * [3. Predictive Analysis](#3-predictive-analysis)
* [🛠️ Technologies Used](#️-technologies-used)
* [📊 Key Results & Findings](#-key-results--findings)
* [🏆 Model Performance](#-model-performance)
* [Conclusion](#-conclusion)

---

## 🎯 Project Objective

The capstone project aims to:
* [cite_start]Analyze the historical launch performance of the SpaceX Falcon 9[cite: 42].
* [cite_start]Assess its reliability and efficiency over time[cite: 42].
* [cite_start]Develop predictive models to forecast the probability of mission success on future launches[cite: 42].
* [cite_start]Identify key factors (e.g., launch site, payload mass, orbit) that correlate with success[cite: 21].

---

## ⚙️ Methodology

The project followed a structured data science pipeline:

### 1. Data Collection & Wrangling

* **Data Sources:**
    * [cite_start]**SpaceX REST API:** Used to retrieve structured launch data, including flight numbers, payload mass, orbit, launch site, and landing outcomes[cite: 49, 51].
    * [cite_start]**Web Scraping:** Scraped Wikipedia pages to supplement the dataset and fill in missing details on payload mass and mission outcomes[cite: 50, 53].
* **Data Wrangling:**
    * [cite_start]Handled missing values by imputing the mean (e.g., for `PayloadMass`)[cite: 61, 62].
    * [cite_start]Cleaned the data by removing duplicates and standardizing formats[cite: 56].
    * [cite_start]Converted the target variable (launch outcome) into a binary indicator (0/1) for modeling[cite: 59].

### 2. Exploratory Data Analysis (EDA)

* **Trend & Correlation Analysis:**
    * [cite_start]Visualized relationships between attributes using scatter plots (e.g., Payload vs. Orbit) and bar charts[cite: 66].
    * [cite_start]Used `one-hot encoding` to convert categorical variables (like `Orbit` and `LaunchSite`) into numerical formats for analysis[cite: 69].
* **Interactive Visual Analytics:**
    * [cite_start]Used **Folium** to create interactive maps of launch sites[cite: 74, 179].
    * [cite_start]Employed **Plotly Dash** to build interactive dashboards for data exploration[cite: 74].
* **Database Analysis:**
    * [cite_start]Loaded the dataset into an **SQL** database to perform complex queries[cite: 152].
    * [cite_start]Answered specific questions, such as finding the total payload mass for NASA (CRS) launches or identifying boosters with successful drone ship landings within a specific payload range[cite: 154, 157].

### 3. Predictive Analysis

* **Model Selection:** Trained and evaluated three different classification models to predict launch success:
    1.  [cite_start]**Logistic Regression** [cite: 83]
    2.  [cite_start]**Support Vector Machine (SVM)** [cite: 83]
    3.  [cite_start]**Decision Trees** [cite: 83]
* [cite_start]**Hyperparameter Tuning:** Utilized **GridSearchCV** to find the optimal hyperparameters for each model to maximize performance[cite: 83].

---

## 🛠️ Technologies Used

* **Python**
* [cite_start]**Data Collection:** `requests` library [cite: 52]
* [cite_start]**Data Analysis:** SQL (SQLite)[cite: 167], Pandas
* [cite_start]**Data Visualization:** Matplotlib, Seaborn, `Folium` [cite: 74][cite_start], `Plotly Dash` [cite: 74]
* [cite_start]**Machine Learning:** Scikit-learn (for Logistic Regression, SVM, Decision Trees, and GridSearchCV) [cite: 83]

---

## 📊 Key Results & Findings

### EDA Insights
* [cite_start]**Success Trend:** The launch success rate generally increased from 2013 to 2017, dipped in 2018, and then increased again[cite: 89].
* [cite_start]**Highest Success Year:** 2019 was identified as the year with the highest success rate in the visualized data[cite: 106].
* [cite_start]**Best Orbits (Success Rate):** `ES-L1`, `GEO`, `HEO`, and `SSO` showed the highest success rates[cite: 95].
* [cite_start]**Best Orbits (High Payload):** `ISS`, `PO`, and `VLEO` were the most common orbits for high payload masses[cite: 96].

### SQL Query Highlights
* [cite_start]**Total NASA (CRS) Payload:** 619,967 KG [cite: 154]
* **Avg. [cite_start]Payload (F9 v1.1):** 2,534.66 KG [cite: 155]
* [cite_start]**First Ground Pad Success:** 2010-06-04 [cite: 156] (Note: This date appears to be the first *launch* in the dataset, not the first *ground pad success* which was later).
* [cite_start]**Successful Drone Ship Boosters (4-6k KG Payload):** `F9 FT B1022`, `F9 FT B1026`, `F9 FT B1021.2`, `F9 FT B1031.2` [cite: 157, 159-162]

---

## 🏆 Model Performance

After training and tuning, the models were evaluated based on their accuracy scores:

| Model | [cite_start]Accuracy [cite: 193] |
| :--- | :--- |
| **Decision Tree** | [cite_start]**88.9%** [cite: 199] |
| Logistic Regression | [cite_start]83.3% [cite: 196] |
| Support Vector Machine (SVM) | [cite_start]83.3% [cite: 203] |

[cite_start]The **Decision Tree classifier provided the best performance** of all tested models[cite: 207].

---

## 🏁 Conclusion

[cite_start]This analysis reveals a clear trend of increased reliability and cost-efficiency in Falcon 9 launches, driven by reusable technology[cite: 218]. [cite_start]The insights gathered emphasize the importance of efficient operational strategies[cite: 217]. The predictive models, particularly the Decision Tree, demonstrate a strong capability to predict mission outcomes based on launch parameters.

### Recommendations
* [cite_start]**For SpaceX:** Continue investing in predictive analytics to further refine launch patterns and streamline operations[cite: 223].
* [cite_start]**Future Research:** Explore advanced materials for rocket durability and improved AI algorithms for flight path optimization[cite: 226].

---

## 📄 License

This project is open-source. Please feel free to fork, clone, and build upon this work.
