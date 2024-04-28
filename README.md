# Health-Care-Decision-Tree-Model
Orchestrated a refined data purification and outlier remediation process, elevating the data landscape. Developed a sophisticated decision  tree model, finessing the intricacies through hyperparameter tuning.

## Dataset Exploration and Preprocessing

The code starts by importing the necessary libraries, including Pandas for data manipulation and Matplotlib/Seaborn for data visualization.

### Data Loading and Inspection
- The dataset is loaded into a Pandas DataFrame named `df`. [1]
- The `df.info()` function is used to inspect the dataset, which shows that there are 303 non-null samples with 14 features, including `age`, `sex`, `cp` (chest pain type), `trestbps` (resting blood pressure), `chol` (serum cholesterol), `fbs` (fasting blood sugar), `restecg` (resting electrocardiographic results), `thalach` (maximum heart rate achieved), `exang` (exercise induced angina), `oldpeak` (ST depression induced by exercise relative to rest), `slope` (the slope of the peak exercise ST segment), `ca` (number of major vessels colored by fluoroscopy), `thal` (a blood disorder called thalassemia), and `target` (the predicted attribute - 0 for no disease, 1 for disease). [1]

### Missing Data Handling
- The `df.isnull().sum()` function is used to check for any missing values in the dataset, which shows that there are no missing values. [1]

### Duplicate Data Handling
- The `df.duplicated().sum()` function is used to check for any duplicate rows in the dataset, which shows that there is 1 duplicate row. [1]
- The `df.drop_duplicates(inplace=True)` function is used to remove the duplicate row. [1]

### Exploratory Data Analysis
- The `df` DataFrame is displayed, showing the cleaned dataset with 302 rows and 14 columns. [1]
- Boxplots are generated for each feature in the dataset using the `sns.boxplot()` function from the Seaborn library. This helps to visualize the distribution and outliers of each feature. [1]

The boxplots provide valuable insights into the distribution and outliers of each feature in the dataset. For example, the boxplots can reveal the following:

- **Age**: The age distribution appears to be relatively wide, with some older patients in the dataset.
- **Sex**: The dataset includes both male (coded as 1) and female (coded as 0) patients.
- **Chest Pain Type (cp)**: The dataset includes patients with different types of chest pain, with the majority having a chest pain type of 1 or 3.
- **Resting Blood Pressure (trestbps)**: The resting blood pressure values are distributed across a wide range, with some high values indicating potential hypertension.
- **Serum Cholesterol (chol)**: The cholesterol levels are also distributed across a wide range, with some high values indicating potential hypercholesterolemia.
- **Fasting Blood Sugar (fbs)**: The fasting blood sugar values are mostly low, with a few higher values.
- **Resting Electrocardiographic Results (restecg)**: The resting electrocardiographic results show different patterns, with most patients having a value of 0 or 1.
- **Maximum Heart Rate Achieved (thalach)**: The maximum heart rate achieved during the test is distributed across a wide range, with some lower values indicating potential heart rate issues.
- **Exercise Induced Angina (exang)**: Most patients did not experience exercise-induced angina, with a few having this condition.
- **ST Depression (oldpeak)**: The ST depression values are distributed across a range, with some higher values indicating potential heart problems.
- **Slope of the Peak Exercise ST Segment (slope)**: The slope of the peak exercise ST segment is mostly distributed between 1 and 2, with a few outliers.
- **Number of Major Vessels Colored by Fluoroscopy (ca)**: Most patients have 0 or 1 major vessels colored by fluoroscopy, with a few having higher values.
- **Thalassemia (thal)**: The thalassemia values are mostly distributed between 2 and 3, with a few outliers.
- **Target (target)**: The target variable, which represents the presence or absence of heart disease, is roughly balanced, with 165 patients having heart disease (target = 1) and 137 patients not having heart disease (target = 0).

The exploratory data analysis provides a comprehensive understanding of the dataset, highlighting the distribution and characteristics of each feature. This information can be valuable for subsequent feature engineering, model selection, and interpretation of the results.
