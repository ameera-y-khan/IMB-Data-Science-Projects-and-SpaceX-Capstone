# SpaceX Falcon 9 First Stage Landing Prediction

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange.svg)
![Plotly Dash](https://img.shields.io/badge/Dashboard-Plotly%20Dash-brightgreen.svg)
![Folium](https://img.shields.io/badge/Geospatial-Folium-green.svg)

## Executive Summary
The commercial launch price of a SpaceX Falcon 9 rocket is around **$62 million**, whereas other providers cost upwards of $165 million. Much of this savings is due to SpaceX's ability to reuse the first stage. 

The primary goal of this capstone project is to predict whether the Falcon 9 first stage will land successfully. By determining the likelihood of a successful landing, we can estimate the true cost of a rocket launch for prospective competitors or stakeholders.

---

## Project Workflow & Notebook Directory

This repository contains the full end-to-end Data Science pipeline across the following notebook stages:

| File Name | Description |
| :--- | :--- |
| `jupyter-labs-spacex-data-collection-api-v2.ipynb` | **Data Collection (API):** Requests launch data directly from the official SpaceX API endpoints. |
| `jupyter-labs-webscraping.ipynb` | **Data Collection (Web Scraping):** Scrapes historical Falcon 9 launch records from Wikipedia using BeautifulSoup. |
| `labs-jupyter-spacex-Data wrangling.ipynb` | **Data Wrangling:** Cleans raw dataset, handles missing values, and assigns landing classification labels (`0` or `1`). |
| `edadataviz.ipynb` | **EDA & Visualization:** Analyzes relationships between payload mass, flight number, launch site, and outcome using Seaborn/Matplotlib. |
| `jupyter-labs-eda-sql-coursera_sqlite.ipynb` | **EDA with SQL:** Runs SQL queries using SQLite to query launch metrics, total payloads, and landing statistics. |
| `lab_jupyter_launch_site_location.ipynb` | **Geospatial Analysis:** Creates interactive maps using `Folium` to plot launch sites, success ratios, and proximity to coastlines/railways. |
| `spacex-dash-app.py` | **Interactive Dashboard:** A Plotly Dash web application built to analyze payload ranges and launch site performance interactively. |
| `SpaceX_Machine Learning Prediction_Part_5.ipynb` | **Machine Learning:** Trains, hyperparameter-tunes (via `GridSearchCV`), and evaluates classification algorithms. |

---

## Machine Learning Model Results

Four classification models were trained and hyperparameter-tuned using 10-fold Cross-Validation (`GridSearchCV`) on standard-scaled features:

* **Logistic Regression**
* **Support Vector Machine (SVM)**
* **Decision Tree Classifier**
* **K-Nearest Neighbors (KNN)**

### Results Summary
* **Training Validation Accuracy:** ~`84.64%` (identical across tuned models)
* **Test Set Accuracy:** **`83.33%`** across all four models (correctly predicting 15 out of 18 test samples).

> **Conclusion:** Due to the compact test sample size ($N = 18$), all tuned algorithms performed equally well in distinguishing successful landings vs. non-landings, with the main area of error being a few false positives.

---

## Tech Stack & Libraries Used

* **Programming Language:** Python 3.11
* **Data Wrangling & Analysis:** Pandas, NumPy
* **Data Scraping & APIs:** Requests, BeautifulSoup4
* **Database & Querying:** SQLite3, SQL Magic
* **Visualization:** Matplotlib, Seaborn, Folium, Plotly Dash
* **Machine Learning:** Scikit-Learn

---

##  How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/ameera-y-khan/Testrepo.1.git](https://github.com/ameera-y-khan/Testrepo.1.git)
   cd Testrepo.1
