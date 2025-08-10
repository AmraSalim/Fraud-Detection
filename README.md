# Introduction
This project focuses on building a machine learning-based system to detect fraudulent transactions in financial datasets. The workflow covers all key stages of the data science process, including data preprocessing, exploratory data analysis (EDA), model development, and evaluation. This project focuses on detecting fraudulent transactions using machine learning.
The dataset contains details about financial transactions and labels indicating whether they are fraudulent.
The primary goal is to build a predictive model that can identify potential fraud while handling class imbalance.

# Dataset Overview

Datase Link: https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download

This dataset comes from Kaggle and includes approximately 6.3 million records of financial transactions.

## Data Exploration
The dataset was loaded and inspected for structure, missing values, and class distribution.
Key steps included:
- Viewing the first few rows with `head()`
- Checking column data types and non-null counts using `info()`
- Counting the number of fraudulent vs. non-fraudulent transactions
- Checking for missing values
- Determining the total number of rows in the dataset

## Data Preprocessing
Before training the model, preprocessing was applied to handle categorical and numerical features:
- Categorical variables were encoded using `OneHotEncoder`
- Numerical variables were standardized using `StandardScaler`
- A `ColumnTransformer` was used to combine these steps into a single transformation pipeline

This ensured that all features were in a suitable format for model training.


## Model Building
The model chosen for this task was **Logistic Regression**, due to its interpretability and effectiveness in binary classification.
Parameters used:
- `class_weight='balanced'` to address the imbalance between fraudulent and non-fraudulent transactions
- `max_iter=1000` to ensure convergence during training

The preprocessing steps and the classifier were combined into a single `Pipeline` for streamlined training.

## Results & Evaluation
After training, the model was evaluated on the test set using:
- **Classification Report**: Precision, Recall, F1-score
- **Confusion Matrix**: To visualize true positives, false positives, true negatives, and false negatives

These metrics help determine the effectiveness of the fraud detection system, with particular focus on **Recall** for the fraud class.
