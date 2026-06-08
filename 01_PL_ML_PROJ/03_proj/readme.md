
# Why this project is best for your topics

| Topic                 | How you will practice it                                     |
| --------------------- | ------------------------------------------------------------ |
| EDA workflow          | Full dataset inspection, cleaning notes, target analysis     |
| Profiling             | Dataset overview, missing values, data types, summary stats  |
| Univariate analysis   | Distribution of tenure, MonthlyCharges, TotalCharges         |
| Bivariate analysis    | Churn vs contract, churn vs payment method, churn vs charges |
| Target distribution   | Churn class balance                                          |
| Class balance         | Check percentage of churned vs non-churned customers         |
| Pair plots            | Numerical relationships by churn                             |
| Correlation matrix    | Numeric feature relationships                                |
| Distribution plots    | Histograms, KDE plots, boxplots                              |
| Hypothesis generation | Identify possible churn drivers                              |
| Matplotlib            | Basic figure/axes plots                                      |
| Seaborn               | Countplots, boxplots, heatmaps, pairplots, facet grids       |
| Plotly                | Interactive churn dashboard charts                           |

# Project structure

```text
03_telco_churn_eda_visualisation/
│
├── data/
│   ├── raw/
│   │   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   └── processed/
│       └── telco_churn_clean.csv
│
├── notebooks/
│   └── 01_telco_churn_eda.ipynb
│
├── outputs/
│   ├── figures/
│   │   ├── churn_distribution.png
│   │   ├── monthly_charges_distribution.png
│   │   ├── correlation_heatmap.png
│   │   └── churn_by_contract.png
│   └── reports/
│       └── eda_report.html
│
├── README.md
└── requirements.txt
```

# Notebook section structure

```text
01_data_importing
02_data_reviewing
03_data_cleaning_for_eda
04_target_distribution_and_class_balance
05_univariate_analysis
06_bivariate_analysis
07_correlation_analysis
08_pairplots_and_multivariate_analysis
09_visualisation_with_matplotlib
10_visualisation_with_seaborn
11_interactive_visualisation_with_plotly
12_hypothesis_generation
13_final_eda_summary
```

# Detailed section plan

```text
01_data_importing
- Import pandas, numpy, matplotlib, seaborn, plotly
- Load the raw CSV
- Set display options
```

```text
02_data_reviewing
- Check shape
- Check columns
- Check first rows
- Check data types
- Check missing values
- Check duplicated rows
- Check basic descriptive statistics
```

```text
03_data_cleaning_for_eda
- Convert TotalCharges to numeric
- Handle missing/blank TotalCharges values
- Standardize categorical values if needed
- Create clean copy of the dataset
- Save processed CSV
```

```text
04_target_distribution_and_class_balance
- Count Churn values
- Calculate churn percentage
- Plot churn distribution
- Explain whether the dataset is balanced or imbalanced
```

```text
05_univariate_analysis
- Analyze numerical columns: tenure, MonthlyCharges, TotalCharges
- Plot histograms
- Plot boxplots
- Analyze categorical columns: Contract, PaymentMethod, InternetService, gender
- Plot countplots
```

```text
06_bivariate_analysis
- Compare Churn with Contract
- Compare Churn with InternetService
- Compare Churn with PaymentMethod
- Compare Churn with tenure
- Compare Churn with MonthlyCharges
- Use grouped tables and visual charts
```

```text
07_correlation_analysis
- Select numerical columns
- Calculate correlation matrix
- Create seaborn heatmap
- Explain which variables are positively or negatively related
```

```text
08_pairplots_and_multivariate_analysis
- Create pairplot for numerical variables
- Use Churn as hue
- Look for visible separation between churned and non-churned customers
```

```text
09_visualisation_with_matplotlib
- Create basic bar chart
- Create histogram using figure/axes API
- Customize title, labels, figure size
```

```text
10_visualisation_with_seaborn
- Countplot for categorical features
- Boxplot for numerical feature vs Churn
- Heatmap for correlation matrix
- Facet grid for distributions by Churn
```

```text
11_interactive_visualisation_with_plotly
- Interactive churn distribution
- Interactive MonthlyCharges vs tenure scatter plot
- Interactive bar chart for churn by contract type
- Add hover information
```

```text
12_hypothesis_generation
- Write 5–7 possible hypotheses from EDA
Example:
  1. Month-to-month contract customers may churn more often.
  2. Higher monthly charges may be linked to higher churn.
  3. Longer-tenure customers may churn less often.
  4. Electronic check users may have higher churn.
```

```text
13_final_eda_summary
- Summarize what was explored
- List main visual insights
- List possible next steps for modeling
```

# Minimal requirements.txt

```text
pandas
numpy
matplotlib
seaborn
plotly
jupyter
```

# Final recommendation

Use the **simple Kaggle Telco Customer Churn dataset** first:

```text
https://www.kaggle.com/datasets/blastchar/telco-customer-churn
```

It is better than a very large dataset because your goal is not “big data hero mode.” Your goal is to learn clean EDA thinking: inspect, visualize, compare, explain, and generate hypotheses.
