
# Student Performance Statistical Analysis

## Introduction

This project explores the **Students Performance in Exams** dataset from Kaggle using core concepts from  **Statistics and Probability** . The main goal of this project is to consolidate the first-week knowledge topics, including descriptive statistics, probability distributions, correlation analysis, hypothesis testing, the Central Limit Theorem, statistical power, and the bias-variance tradeoff.

The dataset contains information about students’ exam scores in math, reading, and writing, as well as categorical features such as gender, parental level of education, lunch type, and test preparation course. These variables make the dataset useful for practicing both numerical and categorical analysis.

In this project, I will analyze the dataset step by step: first by summarizing the data with descriptive statistics, then by exploring distributions and relationships between variables, and finally by applying statistical tests to answer simple research questions. The project is designed not only to calculate statistical values, but also to interpret them clearly and explain when each method should be used.

The final purpose of this project is to build practical intuition for data analysis and prepare for machine learning topics where statistics are used for feature understanding, model evaluation, and decision-making.

# Why this project is best for these topics

| Topic                        | How it will be practiced                                                                                           |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Descriptive statistics       | Calculate mean, median, mode, variance, standard deviation, range, percentiles, quartiles, and IQR for exam scores |
| Measures of center           | Compare mean, median, and mode for math, reading, and writing scores                                               |
| Measures of spread           | Analyze how widely exam scores are distributed using variance, standard deviation, range, and IQR                  |
| Percentiles and quartiles    | Identify score positions such as Q1, median, Q3, and high-performing students                                      |
| Outlier analysis             | Use boxplots and IQR to check whether some exam scores are unusually low or high                                   |
| Probability distributions    | Explore whether exam scores look approximately normally distributed                                                |
| Normal distribution          | Compare score histograms with the bell-shaped distribution idea                                                    |
| Binomial distribution        | Treat pass/fail status as success/failure and analyze proportions                                                  |
| Poisson distribution         | Discuss where event-count distributions could be used, even if the dataset is not mainly count-based               |
| PDF and CDF intuition        | Explain density and cumulative probability using score distributions                                               |
| Pearson correlation          | Measure linear relationships between math, reading, and writing scores                                             |
| Spearman correlation         | Measure monotonic relationships between ranked scores or ordinal-style variables                                   |
| Point-biserial correlation   | Measure the relationship between a binary variable, such as pass/fail, and a continuous score                      |
| Feature-target relationships | Explore which variables are related to exam performance                                                            |
| Hypothesis testing           | Use statistical tests to compare groups and answer simple research questions                                       |
| t-test                       | Compare average scores between two groups, such as test preparation completed vs not completed                     |
| ANOVA                        | Compare average scores across 3+ groups, such as parental education levels                                         |
| Chi-square test              | Test relationships between categorical variables, such as lunch type and pass/fail status                          |
| p-value interpretation       | Practice explaining whether a result is statistically significant                                                  |
| Confidence intervals         | Estimate likely ranges for average exam scores                                                                     |
| Central Limit Theorem        | Simulate repeated samples and show how sample means become more normal                                             |
| Sampling distributions       | Visualize the distribution of sample means                                                                         |
| Statistical power            | Simulate how sample size affects the ability to detect group differences                                           |
| Bias-variance tradeoff       | Train simple models with different complexity levels to show underfitting and overfitting                          |

# Project structure

```text
01_student_performance_statistics/
│
├── data/
│   ├── raw/
│   │   └── StudentsPerformance.csv
│   └── processed/
│       └── student_performance_clean.csv
│
├── notebooks/
│   └── 01_student_performance_statistics.ipynb
│
├── outputs/
│   ├── figures/
│   │   ├── score_distributions.png
│   │   ├── score_boxplots.png
│   │   ├── correlation_heatmap.png
│   │   ├── clt_sampling_distribution.png
│   │   └── bias_variance_plot.png
│   └── reports/
│       └── statistics_report.html
│
├── README.md
└── requirements.txt
```

# Notebook section structure

```text
01_data_importing
02_data_reviewing
03_basic_data_cleaning
04_descriptive_statistics
05_distribution_analysis
06_correlation_analysis
07_hypothesis_testing
08_confidence_intervals
09_clt_and_sampling_distribution
10_statistical_power_simulation
11_bias_variance_tradeoff
12_final_learning_summary
```

# Detailed section plan

```text
01_data_importing
- Import pandas, numpy, matplotlib, seaborn, scipy, and scikit-learn
- Load the StudentsPerformance.csv file
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
```

```text
03_basic_data_cleaning
- Rename columns into snake_case format
- Check categorical values
- Create average_score column
- Create pass/fail column if needed
- Save a cleaned version of the dataset
```

```text
04_descriptive_statistics
- Calculate mean, median, and mode for math, reading, writing, and average scores
- Calculate variance and standard deviation
- Calculate min, max, and range
- Calculate percentiles and quartiles
- Calculate IQR
- Interpret what these statistics say about student performance
```

```text
05_distribution_analysis
- Plot histograms for math, reading, writing, and average scores
- Plot KDE curves if needed
- Create boxplots for score columns
- Check skewness
- Compare score distributions with the Normal distribution idea
- Explain PDF and CDF intuition using exam scores
```

```text
06_correlation_analysis
- Select numerical columns
- Calculate Pearson correlation
- Calculate Spearman correlation
- Create a correlation heatmap
- Create scatter plots between score columns
- Use point-biserial correlation for binary pass/fail vs continuous score
- Explain feature-target relationships
```

```text
07_hypothesis_testing
- Use a t-test to compare two groups
Example: average score of students who completed test preparation vs those who did not

- Use ANOVA to compare 3+ groups
Example: average score across parental education levels

- Use chi-square test for categorical variables
Example: test preparation course vs pass/fail status

- Interpret p-values clearly
- Explain whether the result is statistically significant
```

```text
08_confidence_intervals
- Calculate confidence interval for average math score
- Calculate confidence interval for average reading score
- Calculate confidence interval for average writing score
- Explain what a confidence interval means in simple words
```

```text
09_clt_and_sampling_distribution
- Take repeated random samples from exam scores
- Calculate the mean of each sample
- Plot the sampling distribution of the mean
- Show how the sampling distribution becomes more normal as sample size increases
- Explain the Central Limit Theorem
```

```text
10_statistical_power_simulation
- Simulate two groups with different average scores
- Change sample size and effect size
- Observe when the test detects a difference
- Explain why larger samples usually give higher statistical power
```

```text
11_bias_variance_tradeoff
- Create a simple prediction task using exam-related features
- Train simple models with different complexity levels
- Show underfitting with a too-simple model
- Show overfitting with a too-complex model
- Explain model complexity and regularisation intuition
```

```text
12_final_learning_summary
- Summarize what statistical methods were practiced
- List the most important insights from the dataset
- Explain which methods were useful and why
- Mention what can be improved or extended later
```

# Minimal requirements.txt

```text
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
jupyter
```

# Dataset reference

```text
Dataset: Students Performance in Exams
Source: Kaggle
Link: https://www.kaggle.com/datasets/spscientist/students-performance-in-exams
File: StudentsPerformance.csv
```

# Final recommendation

Use the **Students Performance in Exams** dataset first:

```text
https://www.kaggle.com/datasets/spscientist/students-performance-in-exams
```

This dataset is small, clean, and beginner-friendly, which makes it ideal for practicing Statistics and Probability. The goal is not to build a complicated machine learning system yet. The goal is to understand how to inspect data, summarize it, compare groups, test assumptions, interpret statistical results, and explain findings clearly.
