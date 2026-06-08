# Data Mining Project – Crash Reporting Drivers Data

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Project-Data%20Mining-green)

## Overview
This project explores and prepares a real-world crash reporting dataset for data mining tasks. The notebook performs data understanding, exploratory data analysis (EDA), and preprocessing steps to clean and structure the data for potential machine learning applications.

The analysis focuses on identifying patterns in driver crash reports and preparing a reliable dataset for further modeling.

## Dataset
Dataset used in this project:

**Crash Reporting – Drivers Data**  
Source: https://catalog.data.gov/dataset/crash-reporting-drivers-data

The dataset contains driver-related information from reported traffic crashes, including vehicle characteristics, crash conditions, and driver attributes.

## Project Objectives
- Understand the structure and quality of the dataset
- Explore numerical and categorical variables
- Analyze feature distributions
- Detect class imbalance in potential target variables
- Clean and standardize categorical data
- Prepare the dataset for future machine learning models

## Key Observations
- The dataset includes both **numerical** and **categorical** features.
- The **Injury Severity** attribute is highly **imbalanced**, with most records belonging to non‑severe categories.
- Due to this imbalance, the variable was **not used as the target variable** in the analysis.
- Semantic data cleaning was performed to unify categorical labels (e.g., casing differences or synonymous labels).
- Only non‑statistical cleaning was done before splitting the dataset to **avoid data leakage**.

## Project Workflow

### 1. Library Import & Data Loading
The project uses common Python data science libraries:
- pandas
- numpy
- matplotlib
- scikit‑learn

The dataset is loaded and inspected to understand its structure.

### 2. Data Understanding
Initial inspection includes:
- dataset shape
- column types
- descriptive statistics
- previewing records

### 3. Exploratory Data Analysis (EDA)
EDA explores distributions and relationships within the dataset, including visualizations such as:

- Speed Limit distribution
- Vehicle Year distribution

These visualizations help identify patterns, outliers, and potential preprocessing needs.

### 4. Data Cleaning
Cleaning steps include:

- Standardizing categorical labels
- Removing inconsistencies in text-based categories
- Preparing columns for later modeling

These operations are purely semantic and do not rely on statistical properties or target information.

### 5. Data Preparation Considerations
To prevent **data leakage**:

- Only semantic cleaning is done before splitting
- Any statistical preprocessing should be applied **after train/test split** and only fitted on the training data.

## Repository Structure

```
.
├── DM_Project_1017.ipynb
├── Crash_Reporting_-_Drivers_Data.csv
└── README.md
```

## Requirements
Install the required Python libraries:

```
pip install pandas numpy matplotlib scikit-learn
```

## Running the Project
1. Clone the repository

```
git clone https://github.com/your-username/your-repo-name.git
```

2. Open the notebook

```
jupyter notebook DM_Project_1017.ipynb
```

3. Run the cells sequentially to reproduce the analysis.

## Authors
- Mohammadreza Tavafoghi — 40363031004
- Shayan Etminan — 40363031002

## Future Work
Possible extensions for this project include:

- Feature engineering
- Handling class imbalance
- Training classification models
- Model evaluation and comparison
- Building predictive crash severity models
