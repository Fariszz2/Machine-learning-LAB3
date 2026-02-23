# Machine Learning Lab – Exploratory Data Analysis (EDA)

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) was conducted to understand the structure quality and relationships within the house prices dataset before applying machine learning techniques.

## Jupyter Notebook
📓 **Notebook:**  
- [View Notebook on GitHub](./Lab3_EDA.ipynb)
- [View Visualizations Notebook on GitHub](./Lab3_Matplotlib_Seaborn.ipynb)
- [View Notebook Rendered (nbviewer)](https://nbviewer.org/github/Fariszz2/Machine-learning-LAB3/blob/main/Lab3_EDA.ipynb)
- [View Visualizations Notebook Rendered (nbviewer)](https://nbviewer.org/github/Fariszz2/Machine-learning-LAB3/blob/main/Lab3_Matplotlib_Seaborn.ipynb)

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

## 📊 Visualizations Implemented

### 1. Price Distribution
- Histogram with KDE curve
- Log transformation applied for skewness analysis

**Output Insight:**
- Property prices are right-skewed
- Majority of properties are concentrated in lower-to-mid price ranges
- Few high-value outliers exist

---

### 2. Carpet Area vs Price (Scatter & Joint Plot)

**Output Insight:**
- Strong positive correlation between carpet area and price
- Larger properties tend to cost more
- Some large-area properties priced lower (possible location effect)

---

### 3. Price by Furnishing Type (Boxplot)

**Output Insight:**
- Furnished properties generally have higher median prices
- Semi-furnished properties dominate the dataset
- Outliers exist in all furnishing categories

---

### 4. Bathrooms vs Price

**Output Insight:**
- Price increases with number of bathrooms
- Clear upward trend
- Properties with more bathrooms belong to higher price segments

---

### 5. Top Locations (Bar Plot)

**Output Insight:**
- Certain locations dominate listings
- Indicates market concentration in specific areas

---

### 6. Pairplot (Feature Relationships)

Analyzed relationships between:
- Price
- Carpet Area
- Super Area
- Bathroom

**Output Insight:**
- Strong linear relationship between area features and price
- Bathroom count moderately correlated with price
- Area features highly correlated with each other

---

### 7. Correlation Heatmap

**Output Insight:**
- Carpet Area strongly correlated with Price
- Super Area also positively correlated
- Bathrooms show moderate positive correlation
- Some multicollinearity exists between area columns

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 👨‍💻 Author

fariszz
