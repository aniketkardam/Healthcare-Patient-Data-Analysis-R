# Healthcare Patient Data Analysis Using R

## Project Overview

This project analyzes healthcare patient data using R to identify patterns in patient demographics, clinical variables, treatment costs, and hospital stays.

The analysis focuses on:

- Data visualization
- Correlation analysis
- Simple linear regression
- Healthcare interpretation
- Managerial recommendations

## Business Problem

ABC Multi-Specialty Hospital wants to understand patient demographics, relationships among clinical variables, and factors that may help predict important healthcare outcomes.

## Objectives

1. Analyze patient demographics and disease distribution.
2. Visualize important clinical variables.
3. Identify relationships between numerical healthcare variables.
4. Build regression models to understand predictive relationships.
5. Translate statistical findings into healthcare insights.

## Tools & Technologies

- R
- RStudio
- ggplot2
- corrplot
- ggcorrplot
- Base R
- Linear Regression

## Analysis Performed

### 1. Data Visualization

The project includes:

- Patient distribution by gender
- Disease distribution
- Blood pressure distribution
- Treatment cost by disease
- Age vs Blood Pressure
- Hospital stay density

### 2. Correlation Analysis

A correlation matrix was created using numerical variables.

The analysis identifies:

- Strongest positive correlation
- Strongest negative correlation
- Weak relationships
- Healthcare significance of correlations

Both `corrplot` and `ggcorrplot` were used for visualization.

### 3. Regression Analysis

Three simple linear regression models were developed:

#### Model 1: Blood Pressure ~ Age

Predicting Blood Pressure using Age.

#### Model 2: Treatment Cost ~ Hospital Stay

Predicting Treatment Cost using Hospital Stay.

#### Model 3: Blood Sugar ~ Weight

Predicting Blood Sugar using Weight.

For each model, the project examines:

- Regression equation
- Slope coefficient
- R²
- p-value
- Statistical significance
- Prediction for a new observation
- Healthcare interpretation

## Key Healthcare Questions

The analysis addresses questions such as:

- Is Age strongly related to Blood Pressure?
- Is Hospital Stay related to Treatment Cost?
- Which variables have weak relationships?
- Which variable appears most influential?
- Which factors may help predict healthcare outcomes?

## Project Structure

```text
Healthcare-Patient-Data-Analysis-R/
│
├── README.md
├── R/
│   └── Regression_Assignment.R
├── Data/
│   └── correlation_regression_dataset.csv


One more important point: **don’t upload only the `.R` file.** Your GitHub will look substantially stronger if it contains the dataset, analysis script, generated plots, and a professional README.

Also, your current script has `ggcorrplot(cor_matrix, lab = TRUE...)` before `library(ggcorrplot)` and `install.packages("ggcorrplot")`. :contentReference[oaicite:5]{index=5} That should be cleaned up before GitHub. `install.packages()` generally should **not** be inside the analysis script; installation is a one-time setup step.

A cleaner beginning would be:

```r
# Load required libraries
library(ggplot2)
library(corrplot)
library(ggcorrplot)

# Load dataset
regression <- read.csv("Data/correlation_regression_dataset.csv")

# View dataset
head(regression)
str(regression)
summary(regression)
├── Output/
│   └── Analysis visualizations
└── .gitignore
