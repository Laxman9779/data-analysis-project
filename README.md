Machine Learning Assignment

Dataset

This project uses the Adult Income Dataset. The objective is to clean the dataset, perform exploratory data analysis, build machine learning models, compare their performance, and develop an LLM-powered feature.

---

Part 1 – Data Acquisition, Cleaning and Exploratory Data Analysis

Data Cleaning:-

* Loaded the dataset using pandas.
* Checked the first five rows, data types, and dataset shape.
* Calculated missing values and missing percentage for every column.
* Filled missing numeric values using the median because the dataset contains skewed distributions and outliers. The median is more robust than the mean in such cases.
* Removed duplicate records.
* Corrected data types where required.
* Converted repetitive categorical columns into the category data type to reduce memory usage.

Exploratory Data Analysis:-

The following analyses were performed:

* Descriptive statistics
* Skewness analysis
* IQR-based outlier detection
* Correlation analysis
* Pearson correlation
* Spearman correlation
* Grouped aggregation

Visualizations

The following plots were created:

* Line Plot
* Bar Chart
* Histogram
* Scatter Plot
* Box Plot
* Correlation Heatmap

Outlier Analysis

Outliers were detected using the Interquartile Range (IQR) method. The outliers were retained because they may contain important information and can be handled appropriately during model training instead of being removed.

Skewness Interpretation

Positive skew indicates that the distribution contains a longer right tail, while negative skew indicates a longer left tail. Since skewed distributions are affected by extreme values, the median was preferred over the mean for missing value imputation.
 
Correlation Analysis

Both Pearson and Spearman correlation matrices were computed. Pearson measures linear relationships, whereas Spearman captures monotonic relationships. The comparison helps identify relationships that may not be strictly linear.

Output

The cleaned dataset was saved as:

* cleaned_data.csv

---

Part 2 – Supervised Machine Learning

Data Preprocessing

* Loaded cleaned_data.csv.
* Selected features and target.
* Applied one-hot encoding to categorical variables.
* Used train-test split with random_state=42.
* Applied StandardScaler using only the training data to avoid data leakage.

Regression Models

The following regression models were trained:

* Linear Regression
* Ridge Regression

Evaluation metrics:

* Mean Squared Error (MSE)
* R² Score

The coefficients were analysed to identify the most influential features.

Classification Model

A Logistic Regression classifier was trained.

The following metrics were evaluated:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC Curve
* Area Under the Curve (AUC)

The ROC curve was plotted and AUC was calculated to evaluate classification performance.

Decision Threshold Analysis :-

Prediction probabilities were evaluated using thresholds from 0.30 to 0.70.

Precision, Recall and F1-score were calculated at each threshold to identify the best operating point.

Regularization:-

Logistic Regression models with different regularization strengths were compared.

The effect of parameter C on model performance was analysed.

## Bootstrap Analysis

Bootstrap sampling was performed to estimate the confidence interval of the AUC difference between Logistic Regression models with different regularization strengths.
