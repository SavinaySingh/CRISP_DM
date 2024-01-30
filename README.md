# Part D: Final Report

## CRISP-DM Approach
The structured approach followed for these experiments, from the phase of problem definition to model deployment, is CRISP-DM (Cross-Industry Standard Process for Data Mining).
<div align="center">
<img width="500" alt="image" src="https://github.com/SavinaySingh/CRISP_DM/assets/21008903/682eb976-02b8-44a3-8d09-3f51a33bea8c">
</div>

There are six successive phases in this process (Hotz, 2023):

### 1. Business Understanding
#### 1.1 Business Problem
The primary objective is to forecast the likelihood of an existing customer buying a new car using their service record features and other parameters. The results aim to benefit car companies by:

a. Developing and executing retention tactics targeting customers likely to repurchase.
b. Improving inventory management by understanding which models have a higher chance of being resold.
c. Enhancing customer satisfaction through improvements in certain aspects of car service.

Accurate predictions provide essential insights for optimizing marketing strategies, minimizing unnecessary expenses, and staying ahead of the competition.

#### 1.2 Project Goals
The project consists of six experiments:

a. Experiment 1: Focuses on determining the importance of service in building customer loyalty.
b. Experiment 2: Analyzes top features predicting the likelihood of an existing customer buying a new car.
c. Experiment 3: Predicts the probability of a purchase using under-sampled data and logistic regression.
d. Experiment 4: Compares multiple classification techniques.
e. Experiment 5: Optimizes hyperparameters of the most accurate model from Experiment 4.
f. Experiment 6: Develops an Explainable Model to understand feature contributions.

### 2. Data Understanding
#### 2.1 Data Collection
The dataset includes information on customers who repurchased a car, along with service history. Seventeen input parameters, all categorical, such as age band, gender, and car model, are used for analysis.

#### 2.2 Data Exploration
Exploration involves checking for missing values, outliers, and studying relationships between features and outcomes.

### 3. Data Preparation
#### 3.1 Data Cleaning
Handling missing data, removing columns with excessive missing values, and transforming textual labels into numerical categories using a label encoder.

#### 3.2 Data Transformation
Feature scaling through standardization and balancing the dataset using the SMOTE technique.

### 4. Modelling
#### 4.1 Model Selection
Logistic regression, chi-square test, and various classification algorithms are utilized in different experiments.
<div align="center">
<img width="500" alt="image" src="https://github.com/SavinaySingh/CRISP_DM/assets/21008903/e59b6c6f-c15e-4b6f-b76d-75b3416b121d">
</div>

### 5. Evaluation
#### 5.1 Model Performance
Performance metrics for testing data include accuracy, precision, recall, and F1 score.

| Experiment | Accuracy | Precision (Will not buy) | Precision (Will Buy) | Recall (Will not buy) | Recall (Will Buy) | F1 Score |
|------------|----------|--------------------------|----------------------|------------------------|---------------------|----------|
| 1          | 77.5%    | 0.99                     | 0.09                 | 0.77                   | 0.84                | 0.87     |
| 2          | 77.9%    | 1.00                     | 0.10                 | 0.78                   | 0.88                | 0.87     |
| 3          | 76.3%    | 0.99                     | 0.09                 | 0.76                   | 0.85                | 0.87     |
| 4          | 98.6%    | 1.00                     | 0.81                 | 0.99                   | 0.85                | 1.00     |
| 5          | 99%      | 1.00                     | 0.76                 | 0.99                   | 0.87                | 0.99     |
| 6          | 98.9%    | 1.00                     | 0.75                 | 0.99                   | 0.89                | 0.99     |

### 6. Deployment
The model is currently deployed as a Python script, taking user input to predict the likelihood of an existing customer buying a new car. Deployment steps include exporting the model, setting up a CI/CD pipeline, deploying on a cloud-based platform, testing, monitoring, and continuous improvement.

## Encountered Issues
1. Data privacy threats: Potential misuse of repurchase data for targeted marketing without explicit customer permission.
2. Data Quality Issues:
   - Small dataset: May lead to biased models.
   - Imbalanced dataset: Bias towards the majority class may impact minority class predictions.
   - High missing values: Features like age_band with high missing values were removed.

## Modelling Issues
1. Risk of overfitting: Small training data increases the risk.
2. Features not showing high correlation: Selected features showed low correlation with the target outcome.

## Future Scope
Address ethical issues, such as bias, transparency, privacy, and accountability. Future steps include careful consideration of these factors.

## Conclusion
The project, following the CRISP-DM methodology, conducted six experiments predicting the likelihood of customers buying new cars. The final model, achieved through these experiments, demonstrates high performance, offering valuable insights for car companies.

## References
- Hotz, N. (2023, January 19). What is CRISP DM? Data Science Process Alliance. [Link](https://www.datascience-pm.com/crisp-dm-2/)
- Patiegm. (2018, October 30). Datasci_Resources/CRISP-DM analysis template.ipynb. GitHub. [Link](https://github.com/patiegm/Datasci_Resources/blob/master/CRISP-DM%20Analysis%20Template.ipynb)
