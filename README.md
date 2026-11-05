# 🌍 AQI Prediction and Classification Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)
![Domain](https://img.shields.io/badge/Domain-Environmental%20Data%20Science-green)

## 📌 Project Overview

**AQI Prediction and Classification Using Machine Learning** is a data science and machine learning project designed to analyze historical air pollution data, predict numerical Air Quality Index (AQI) values, and classify air quality into different pollution categories.

The project uses historical air quality measurements from multiple Indian cities and applies five machine learning algorithms to understand the relationship between atmospheric pollutants and AQI.

It combines Exploratory Data Analysis (EDA), regression, classification, data visualization, and model evaluation to generate meaningful environmental insights.

The system performs two major prediction tasks:

- **AQI Prediction (Regression):** Estimates numerical AQI values using pollutant concentrations.
- **AQI Classification (Classification):** Classifies air quality into Good, Satisfactory, Moderate, Poor, Very Poor, and Severe categories.

## 🎯 Problem Statement

Air pollution is a major environmental concern that affects human health and environmental sustainability. Pollution levels vary across cities and time periods due to pollutants such as PM2.5, PM10, NO2, and CO.

Analyzing large historical pollution datasets manually makes it difficult to identify pollution trends, estimate AQI values, and determine the severity of air pollution.

This project aims to develop a machine learning-based system that analyzes historical air pollution measurements, predicts numerical AQI values, and classifies air quality into predefined pollution categories.

The project also compares multiple machine learning algorithms to identify the best-performing models for AQI prediction and classification.

## 🎯 Project Objectives

- Analyze historical air pollution data from Indian cities.
- Perform data cleaning and preprocessing.
- Explore pollutant distributions and statistical relationships.
- Identify city-wise and monthly pollution trends.
- Predict numerical AQI values using regression algorithms.
- Classify air quality into six AQI categories.
- Compare machine learning algorithms using evaluation metrics.
- Identify the strongest pollutant correlation with AQI.
- Generate meaningful insights from environmental data.

## 📂 Dataset Information

**Dataset:** City Day Air Quality Dataset

**File:** `city_day.csv`

The dataset contains historical air pollution measurements recorded across 25 Indian cities.

| Dataset Information | Details |
|---|---|
| Original Records | 29,531 |
| Records After Cleaning | 16,626 |
| Original Columns | 16 |
| Number of Cities | 25 |
| Time Period | 2015–2020 |
| Regression Target | AQI |
| Classification Target | AQI_Bucket |

### Important Dataset Features

| Feature | Description |
|---|---|
| City | Name of the city |
| Date | Date of observation |
| PM2.5 | Fine particulate matter |
| PM10 | Particulate matter |
| NO2 | Nitrogen dioxide |
| CO | Carbon monoxide |
| AQI | Numerical Air Quality Index |
| AQI_Bucket | Air quality classification |

The machine learning models use four primary pollutant features:

`PM2.5`, `PM10`, `NO2`, and `CO`.

## ⚙️ Technologies and Libraries Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and preprocessing |
| NumPy | Numerical computations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine learning algorithms |
| Jupyter Notebook | Development and experimentation |

## 🤖 Machine Learning Algorithms

A total of **5 machine learning models** are implemented in this project.

### 1. Regression Models

Regression algorithms predict continuous numerical AQI values.

| Model | Input Features | Prediction |
|---|---|---|
| Simple Linear Regression | PM2.5 | Numerical AQI |
| Polynomial Regression | PM10 and PM10² | Numerical AQI |
| Multiple Linear Regression | PM2.5, PM10, NO2, CO | Numerical AQI |

**Simple Linear Regression**

Estimates AQI using PM2.5 as the single independent variable and learns a linear relationship between the pollutant and AQI.

**Polynomial Regression**

Uses PM10 and its squared term to model a quadratic relationship between PM10 concentration and AQI. The polynomial degree used is 2.

**Multiple Linear Regression**

Uses four pollutant measurements simultaneously to estimate AQI and understand their combined relationship with air quality.

### 2. Classification Models

Classification algorithms predict categorical AQI labels.

| Model | Input Features | Prediction |
|---|---|---|
| Logistic Regression | PM2.5, PM10, NO2, CO | AQI Category |
| Decision Tree Classifier | PM2.5, PM10, NO2, CO | AQI Category |

**Logistic Regression**

Calculates the probability of an observation belonging to each AQI category and selects the most probable category.

**Decision Tree Classifier**

Uses feature-based decision rules and threshold conditions to classify air quality into different pollution categories.

### AQI Categories

The classification models predict six categories:

1. Good
2. Satisfactory
3. Moderate
4. Poor
5. Very Poor
6. Severe

## 📊 Exploratory Data Analysis (EDA)

The project performs multiple analytical visualizations to understand pollution patterns.

### Visualizations Included

- AQI Distribution Histogram
- Top 10 Cities by Average AQI
- Monthly Average AQI Trend
- Pollutant Correlation Heatmap
- Regression Model R² Comparison
- Regression Model RMSE Comparison
- Actual vs Predicted AQI
- Polynomial Regression Curve (PM10 vs AQI)
- Classification Accuracy Comparison
- Logistic Regression Confusion Matrix
- Decision Tree Confusion Matrix
- Decision Tree Structure Visualization

## 📈 Model Evaluation Metrics

### Regression Evaluation

| Metric | Purpose |
|---|---|
| R² Score | Measures explained variation |
| MAE | Measures average absolute prediction error |
| MSE | Measures average squared prediction error |
| RMSE | Measures the square root of mean squared error |

### Classification Evaluation

| Metric | Purpose |
|---|---|
| Accuracy | Measures overall correct predictions |
| Precision | Measures correctness of positive predictions |
| Recall | Measures identification of actual positive cases |
| F1-Score | Balances precision and recall |
| Log Loss | Evaluates predicted class probabilities |
| ROC-AUC | Evaluates class discrimination ability |

## 🏆 Model Performance and Results

Based on the current experiment:

### Regression Results

| Model | R² Score | MAE | RMSE |
|---|---:|---:|---:|
| Simple Linear Regression | 0.6310 | 33.64 | 62.75 |
| Polynomial Regression (PM10) | 0.6612 | 33.07 | 60.12 |
| Multiple Linear Regression | **0.8835** | **22.38** | **35.25** |

**Best Regression Model: Multiple Linear Regression**

It achieves the highest R² score and the lowest MAE and RMSE among the three regression models.

### Classification Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 77.12% | 76.63% | 77.12% | 76.38% |
| Decision Tree | **77.96%** | **77.51%** | **77.96%** | **77.58%** |

**Best Classification Model: Decision Tree Classifier**

It achieves the highest classification accuracy and F1-score in the experiment.

*Note: These are experimental results from the current dataset, preprocessing and train-test split. Re-run the updated code to reproduce the results.*

## 🔍 Key Project Insights

The project generates seven important analytical insights:

1. **Highest AQI City:** Ahmedabad – Average AQI of 363.73.
2. **Lowest AQI City:** Aizawl – Average AQI of 35.05.
3. **Most Common AQI Category:** Satisfactory.
4. **Highest Pollution Month:** January – Average AQI of 195.12.
5. **Strongest Pollutant Correlation:** PM10 – Correlation of 0.800.
6. **Best Regression Model:** Multiple Linear Regression – R² of 0.8835.
7. **Best Classification Model:** Decision Tree – Accuracy of 77.96%.

These findings are calculated from the cleaned historical dataset and do not represent current pollution conditions.

## 🧹 Data Preprocessing

The following preprocessing operations are performed:

- Loading the CSV dataset using Pandas.
- Converting the Date column into datetime format.
- Converting pollutant measurements into numerical values.
- Removing duplicate records.
- Removing records with missing values in required columns.
- Extracting Month and Year from the Date column.
- Separating independent and dependent variables.
- Applying StandardScaler for Logistic Regression.

## 🔄 Machine Learning Workflow

1. Dataset Loading
2. Data Cleaning
3. Exploratory Data Analysis
4. Feature Selection
5. Train-Test Splitting (80:20)
6. Regression Model Training
7. Classification Model Training
8. Model Evaluation
9. Model Comparison
10. Prediction Visualization
11. Final Insight Generation

## 📁 Project Structure

```text
AQI-Prediction-and-Classification/
│
├── city_day.csv
│
├── aqi_prediction.py
│
├── README.md
│
└── requirements.txt
```

*Adjust the filenames if your actual repository uses different names.*

## 💻 Installation and Execution

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AQI-Prediction-and-Classification.git
```

### 2. Navigate to the project directory

```bash
cd AQI-Prediction-and-Classification
```

### 3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Alternatively:

```bash
pip install -r requirements.txt
```

### 4. Run the project

```bash
python aqi_prediction.py
```

Make sure that `city_day.csv` is located in the correct project directory.

## 📦 Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
```

## 🚀 Future Enhancements

- Integrate additional pollutant features such as SO2, O3, NH3 and other relevant measurements.
- Experiment with Random Forest, XGBoost and Gradient Boosting algorithms.
- Implement hyperparameter optimization.
- Apply cross-validation for more reliable evaluation.
- Handle class imbalance using appropriate sampling or class weighting.
- Develop time-series models for future AQI forecasting.
- Build an interactive dashboard using Streamlit.
- Integrate live air quality data through an external API.
- Deploy the prediction system as a web application.

## ⚠️ Project Limitations

- The current models use only four pollutant features.
- Missing observations are removed rather than imputed.
- The dataset has imbalanced AQI categories.
- The current implementation uses random train-test splitting.
- The project predicts AQI from supplied pollutant measurements rather than forecasting future pollutant concentrations.
- It does not currently provide real-time pollution monitoring.

## 🎓 Learning Outcomes

Through this project, I explored:

- Data preprocessing and exploratory data analysis.
- Statistical analysis and correlation.
- Supervised machine learning.
- Regression and classification techniques.
- Model evaluation and comparison.
- Data visualization using Python.
- Environmental data analysis.

## 👨‍💻 Author

**Nossam Nithin**

Machine Learning | Data Science | Python | Data Analytics

Interested in developing data-driven solutions using machine learning, statistical analysis and data visualization.

## ⭐ Acknowledgement

This project was developed as a machine learning and data science project using historical air quality data to explore pollution patterns and demonstrate AQI prediction and classification techniques.

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

**Project:** AQI Prediction and Classification Using Machine Learning

**Domain:** Data Science | Machine Learning | Environmental Analytics

**Language:** Python
