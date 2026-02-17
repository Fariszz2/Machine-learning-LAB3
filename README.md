# Machine Learning Lab – Exploratory Data Analysis (EDA)

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) was conducted to understand the structure quality and relationships within the house prices dataset before applying machine learning techniques.

## Jupyter Notebook
📓 **Notebook:**  
- [View Notebook on GitHub](./Lab3_EDA.ipynb)
- [View Notebook Rendered (nbviewer)](https://nbviewer.org/github/Fariszz2/Machine-learning-LAB3/blob/main/Lab3_EDA.ipynb)

### Data Inspection

The dataset was explored using:

- `df.shape` to determine the number of rows and columns.
- `df.head()` to preview the first few records.
- `df.columns` to review feature names.
- `df.dtypes` and `df.info()` to inspect data types and missing values.

This step helped distinguish between numerical and categorical variables.

---

### Data Cleaning and Preprocessing

Several preprocessing steps were applied to prepare the dataset for analysis:

- Converted **Price (in rupees)** to numeric format.
- Converted **Bathroom** columns to numeric values.
- Handled invalid entries (e.g., ">10") using `pd.to_numeric(..., errors='coerce')`.
- Managed missing values using `dropna()` where appropriate.

These steps ensured the dataset was properly formatted for numerical analysis and machine learning modeling.

---

### Univariate Analysis

To understand individual feature distribution, histogram were plotted for:

- **Price (in rupees)**

Observations:

- House prices show a right-skewed distribution.
- Most properties fall within a moderate price range.
- A small number of high-priced properties act as outliers.

---

### Bivariate Analysis

Scatter plots were used to analyze relationships between key features and house price:

- **Bathroom vs Price**

The analysis revealed positive relationships between property size, number of bathrooms, and price.

---

### Correlation Analysis

A correlation heatmap was generated for selected numerical features:

- Price (in rupees)
- Bathroom

This helped identify which features have stronger relationships with house price and are more suitable for regression modeling.

---

## Results

Based on the exploratory data analysis, the following key findings are identified:

### Key Findings

1. **Bathroom count shows moderate positive correlation with Price.**  
   Houses with more bathrooms generally have higher market value.

2. **Price distribution is right-skewed.**  
   A small number of luxury properties increase overall price variance.

3. **Data preprocessing was necessary.**  
   Some columns contained text-based numeric values and missing entries that required cleaning before analysis.

---
