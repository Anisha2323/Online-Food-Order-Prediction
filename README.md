# Online Food Order Prediction

## Project Overview
This project uses Machine Learning classification techniques to analyze customer characteristics and predict online food ordering outcomes.

The objective is to identify patterns in customer demographics and socioeconomic characteristics that are associated with online food ordering behaviour.

## Dataset
- 388 original records
- 285 records after removing exact duplicate rows
- 12 columns after removing the redundant target duplicate column
- Target variable: `Output` (Yes/No)

## Data Preprocessing
- Removed duplicate records and redundant columns.
- Handled inconsistent whitespace in categorical values.
- Examined missing values and data distributions.
- Excluded Feedback due to potential post-outcome information leakage.
- Excluded PIN code and geographical coordinates from the initial model.

## Exploratory Data Analysis
Explored relationships between ordering outcomes and:
- Age
- Gender
- Marital Status
- Occupation
- Monthly Income
- Educational Qualifications
- Family Size

## Machine Learning Models
The following classification models were developed:
1. Dummy Classifier
2. Logistic Regression
3. Balanced Logistic Regression
4. Decision Tree Classifier

Stratified 5-fold cross-validation and GridSearchCV were used for model comparison and hyperparameter tuning.

## Final Model Performance

**Tuned Decision Tree Classifier**

| Metric | Score |
|---|---:|
| Accuracy | 73.68% |
| Macro F1-score | 61.57% |
| Recall (No) | 36% |
| Recall (Yes) | 86% |

## Key Findings
- Age was the most influential feature in the final Decision Tree.
- Family size and educational qualifications were also important.
- The model performed better at identifying Yes outcomes than No outcomes.
- Class imbalance remains a challenge.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Limitations
- The dataset is relatively small.
- The target classes are imbalanced.
- Model performance may vary with different data samples.
- Feature importance does not establish causal relationships.

## Future Improvements
- Collect more customer records.
- Explore additional relevant features.
- Evaluate other classification algorithms.
- Improve minority-class prediction performance.
