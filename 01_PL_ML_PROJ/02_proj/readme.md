
# Titanic Data Quality & Healing Pipeline

## Introduction

This project explores the **Titanic - Machine Learning from Disaster** dataset from Kaggle using core concepts from  **Data Quality and Data Healing** . The main goal of this project is to consolidate the second-week knowledge topics, including missing value analysis, imputation strategies, outlier detection, duplicate detection, data type correction, consistency validation, data completeness, validity checks, profiling tools, and data pipeline outputs.

The dataset contains passenger information such as age, sex, passenger class, fare, cabin, embarkation port, family-related columns, and survival status. These variables make the dataset useful for practicing real-world data cleaning because it contains missing values, mixed data types, categorical variables, possible outliers, and columns that require validation.

In this project, I will analyze the raw dataset step by step: first by reviewing the structure and quality of the data, then by identifying missing values, duplicates, invalid values, and outliers, and finally by applying appropriate cleaning and validation strategies. The project is designed not only to clean the dataset, but also to explain why each cleaning decision was made.

The final purpose of this project is to build practical intuition for preparing raw data for machine learning workflows. Instead of blindly dropping or filling values, this project focuses on understanding data problems, choosing suitable treatment methods, documenting decisions, and saving a clean, ML-ready dataset.

# Why this project is best for these topics

| Topic                          | How it will be practiced                                                         |
| ------------------------------ | -------------------------------------------------------------------------------- |
| Data importing                 | Load the Titanic dataset from CSV and inspect the raw file                       |
| Data reviewing                 | Check shape, columns, data types, first rows, and summary statistics             |
| Missing value analysis         | Identify missing values in columns such as Age, Cabin, and Embarked              |
| Missing percentage             | Calculate how much data is missing in each column                                |
| MCAR / MAR / MNAR intuition    | Explain possible reasons why values are missing                                  |
| Mean imputation                | Test mean imputation for numerical columns where appropriate                     |
| Median imputation              | Use median imputation for skewed numerical columns or outlier-sensitive features |
| Mode imputation                | Use mode imputation for categorical columns with few missing values              |
| KNN imputation                 | Practice a more advanced imputation method for numerical features                |
| Iterative imputation           | Optional advanced method for estimating missing values using other features      |
| Outlier detection with IQR     | Detect possible outliers in Fare and Age using the IQR rule                      |
| Outlier detection with z-score | Detect extreme numerical values using standard deviation logic                   |
| Mahalanobis distance           | Optional multivariate outlier detection for numerical columns                    |
| Outlier treatment              | Decide whether to keep, cap, transform, or remove outliers                       |
| Duplicate detection            | Check full duplicate rows and duplicate passenger IDs                            |
| Data type correction           | Convert incorrect data types and prepare columns for analysis                    |
| Consistency validation         | Check whether categorical values are consistent and expected                     |
| Validity checks                | Verify logical rules such as Age >= 0 and Fare >= 0                              |
| Completeness checks            | Measure how complete the dataset is before and after cleaning                    |
| Referential integrity idea     | Understand whether ID-like columns are unique and reliable                       |
| Data profiling                 | Generate an automated profiling report using ydata-profiling                     |
| Great Expectations             | Optional: create formal validation rules for important columns                   |
| CSV pipeline                   | Save the cleaned dataset as a CSV file                                           |
| JSON pipeline                  | Save the cleaned dataset as a JSON file                                          |
| Parquet pipeline               | Save the cleaned dataset as a Parquet file                                       |
| ML-ready dataset               | Produce a clean dataset that can later be used for modeling                      |

# Project structure

```text
02_titanic_data_quality_healing/
│
├── data/
│   ├── raw/
│   │   └── train.csv
│   └── processed/
│       ├── titanic_clean.csv
│       ├── titanic_clean.json
│       └── titanic_clean.parquet
│
├── notebooks/
│   └── 01_titanic_data_quality_healing.ipynb
│
├── outputs/
│   ├── figures/
│   │   ├── missing_values_barplot.png
│   │   ├── age_distribution_before_after.png
│   │   ├── fare_boxplot_outliers.png
│   │   └── data_quality_summary.png
│   └── reports/
│       ├── profiling_report.html
│       └── data_quality_report.html
│
├── README.md
└── requirements.txt
```

# Notebook section structure

```text
01_data_importing
02_data_reviewing
03_missing_value_analysis
04_imputation_strategies
05_outlier_detection
06_duplicates_and_consistency
07_data_type_correction
08_data_quality_assessment
09_data_profiling
10_data_pipeline_outputs
11_final_cleaning_summary
```

# Detailed section plan

```text
01_data_importing
- Import pandas, numpy, matplotlib, seaborn, scipy, and scikit-learn
- Load the raw Titanic train.csv file
- Set display options
- Check whether the dataset was loaded correctly
```

```text
02_data_reviewing
- Check dataset shape
- Check column names
- Check first rows
- Check data types
- Check missing values
- Check duplicated rows
- Check basic descriptive statistics
- Separate numerical and categorical columns
```

```text
03_missing_value_analysis
- Count missing values for each column
- Calculate missing value percentage
- Visualize missing values with a bar plot
- Identify columns with high, medium, and low missingness
- Discuss whether missingness may be MCAR, MAR, or MNAR
- Decide which columns should be imputed, transformed, or dropped
```

```text
04_imputation_strategies
- Apply median imputation for Age
- Apply mode imputation for Embarked
- Create a has_cabin feature from the Cabin column
- Compare mean vs median imputation for numerical columns
- Test KNN imputation as an advanced option
- Compare how imputation changes summary statistics
```

```text
05_outlier_detection
- Use boxplots to inspect Age and Fare
- Detect outliers with the IQR method
- Detect outliers with the z-score method
- Optionally test Mahalanobis distance for multivariate outliers
- Decide whether each outlier should be kept, capped, transformed, or removed
- Explain that not every outlier is automatically an error
```

```text
06_duplicates_and_consistency
- Check full duplicate rows
- Check whether PassengerId is unique
- Check repeated names if needed
- Check categorical values in Sex, Embarked, and Pclass
- Check invalid values such as negative Age or negative Fare
- Check whether family-related columns contain valid values
```

```text
07_data_type_correction
- Convert categorical columns to category type if appropriate
- Ensure numerical columns have correct numerical types
- Convert Survived and Pclass into categorical or integer formats depending on use
- Create clean feature names if needed
- Prepare a cleaned dataframe for saving
```

```text
08_data_quality_assessment
- Create a data quality checklist
- Measure completeness before and after cleaning
- Measure duplicate count before and after cleaning
- Record invalid value checks
- Record outlier treatment decisions
- Build a small summary table with issue, column, action, and reason
```

```text
09_data_profiling
- Generate a ydata-profiling report
- Save the profiling report as HTML
- Optionally create Great Expectations validation rules
- Validate important rules such as unique PassengerId, non-negative Age, and valid categories
```

```text
10_data_pipeline_outputs
- Save the cleaned dataset as CSV
- Save the cleaned dataset as JSON
- Save the cleaned dataset as Parquet
- Compare CSV, JSON, and Parquet in simple words
- Explain which format is most useful for this project and why
```

```text
11_final_cleaning_summary
- Summarize what data quality issues were found
- Explain what was cleaned or transformed
- List the imputation strategies used
- List the outlier treatment decisions
- Explain why the dataset is now cleaner and more ML-ready
- Mention possible improvements for future work
```

# Minimal requirements.txt

```text
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
ydata-profiling
pyarrow
jupyter
```

# Dataset reference

```text
Dataset: Titanic - Machine Learning from Disaster
Source: Kaggle
Link: https://www.kaggle.com/competitions/titanic
Main file: train.csv
Optional file: test.csv
```

# Final recommendation

Use the **Titanic - Machine Learning from Disaster** dataset first:

```text
https://www.kaggle.com/competitions/titanic
```

This dataset is small, famous, and beginner-friendly, but still realistic enough for data cleaning practice. It contains missing values, categorical variables, numerical variables, possible outliers, and useful validation checks. The goal is not to build the best survival prediction model yet. The goal is to learn how to turn raw data into a clean, validated, and well-documented dataset.
