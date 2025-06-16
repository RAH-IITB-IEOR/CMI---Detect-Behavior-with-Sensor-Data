# Exploratory Data Analysis (EDA) and Feature Engineering Steps

---

## 1. Exploratory Data Analysis (EDA)

-   **Initial Assessment:** Load and inspect raw data for structure, size, and data types.
-   **Feature Analysis:**
    -   Identify and summarize numerical and categorical features.
    -   Check for constant or duplicate columns.
-   **Visualization:**
    -   Plot histograms, box plots, and density plots for numerical features to understand distributions.
    -   Use count plots and bar charts for categorical features to analyze frequency and cardinality.
-   **Missing Values:**
    -   Visualize missing data patterns (e.g., heatmaps).
    -   Quantify missingness per feature.
-   **Outlier Detection:**
    -   Use box plots, scatter plots, and z-score/IQR methods to detect outliers.
-   **Data Cleaning:**
    -   Identify and address inconsistent, duplicate, or erroneous entries.
-   **Correlation Analysis:**
    -   Generate correlation matrices to identify relationships between features.
-   **Goal:** Develop a comprehensive understanding of the dataset to inform preprocessing and modeling decisions.

---

## 2. Handling Missing Values

-   **Imputation Techniques:**
    -   Mean, median, or mode imputation for numerical features.
    -   Most frequent or constant value imputation for categorical features.
    -   Advanced methods: KNN imputation, regression imputation, or using model-based approaches.
-   **Strategy Selection:**
    -   Choose imputation method based on feature distribution and presence of outliers.
    -   Consider dropping features or samples with excessive missingness.

---

## 3. Handling Imbalanced Dataset

-   **Assessment:**
    -   Analyze class distribution for target variable.
-   **Balancing Techniques:**
    -   Oversampling (e.g., SMOTE, ADASYN) or undersampling.
    -   Generate synthetic samples or use class weighting in algorithms.
    -   Stratified sampling for train-test splits.

---

## 4. Treating Outliers

-   **Detection:**
    -   Use statistical methods (z-score, IQR) and visualizations.
-   **Treatment:**
    -   Cap or floor outliers (winsorization).
    -   Remove extreme outliers if justified.
    -   Transform features (e.g., log, square root) to reduce impact.

---

## 5. Scaling the Data

-   **Standardization:** Transform features to have zero mean and unit variance.
-   **Normalization:** Scale features to a fixed range (e.g., [0, 1]).
-   **When to Scale:** Apply scaling after splitting data into train/test sets to avoid data leakage.

---

## 6. Converting Categorical Features into Numerical Features

-   **Encoding Techniques:**
    -   Label encoding for ordinal features.
    -   One-hot encoding for nominal features.
    -   Target encoding or frequency encoding for high-cardinality features.
-   **Considerations:** Avoid introducing multicollinearity or data leakage during encoding.

---

## 7. Feature Selection

-   **Purpose:** Reduce dimensionality, improve model performance, and prevent overfitting.
-   **Techniques:**
    -   Filter methods: Correlation analysis, chi-square test, ANOVA.
    -   Wrapper methods: Recursive Feature Elimination (RFE), K-nearest neighbors.
    -   Embedded methods: Feature importance from tree-based models (e.g., Extra Trees, Random Forest).
    -   Advanced: Genetic algorithms, LASSO regularization.
-   **Evaluation:** Validate selected features using cross-validation and model performance metrics.
