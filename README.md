# PYTHON PROJECT

## BANK MARKETING CAMPAIGN ANALYSIS

### 1. Problem Statement

#### Context

A Portuguese banking institution has been running direct marketing campaigns to promote their term deposit products. The campaigns are conducted primarily through phone calls, where potential clients are contacted and encouraged to subscribe to a term deposit. Despite the extensive effort put into these campaigns, the bank struggles with a low conversion rate, making it crucial to identify the factors that influence a client's decision to subscribe to the term deposit.

#### Objective

The primary objective is to develop a predictive model that can identify potential clients who are more likely to subscribe to a term deposit based on their demographic and transactional information. By accurately predicting the likelihood of subscription, the bank can optimize its marketing efforts, reduce costs, and improve the overall efficiency of its campaigns.

#### Specific Goals

1. **Identify Key Factors**: Determine which factors (e.g., age, job type, education level) significantly influence the likelihood of a client subscribing to a term deposit.
2. **Predict Subscription Probability**: Develop a machine learning model to predict the probability that a given client will subscribe to a term deposit.
3. **Optimize Marketing Strategy**: Use the insights gained from the model to tailor marketing strategies, focusing on clients with a higher predicted probability of subscription.
4. **Increase Conversion Rates**: Improve the overall conversion rate of the marketing campaigns by targeting the right clients, thereby maximizing the return on investment (ROI) for the bank's marketing efforts.

#### Challenges

1. **Imbalanced Dataset**: The dataset may have an imbalance between the number of clients who subscribe and those who do not, which can affect the performance of the predictive model.
2. **Data Quality**: Ensuring the data is clean, consistent, and free of missing values is essential for building an accurate model.
3. **Feature Engineering**: Identifying and creating relevant features that capture the underlying patterns in the data is crucial for improving model performance.
4. **Model Interpretability**: While achieving high predictive accuracy is important, the model should also be interpretable to provide actionable insights to the bank's marketing team.

#### Expected Outcome

By leveraging the predictive model, the bank aims to:

- Enhance the efficiency of its marketing campaigns by focusing efforts on clients who are more likely to subscribe.
- Increase the subscription rate for term deposits, contributing to higher revenue.
- Gain deeper insights into client behavior and preferences, enabling more personalized marketing approaches in the future.

Ultimately, the goal is to create a data-driven marketing strategy that not only boosts the bank's performance but also enhances customer satisfaction by offering relevant financial products to the right clients.

### 2. Dataset Information

The data is related to direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required to determine if the product (bank term deposit) would be ('yes') or not ('no') subscribed.

#### Variable Information

##### Input Variables

| **Variable** | **Description** | **Type** | **Values** |
|--------------|-----------------|----------|------------|
| age | Age of the client | numeric | - |
| job | Type of job | categorical | "admin.", "unknown", "unemployed", "management", "housemaid", "entrepreneur", "student", "blue-collar", "self-employed", "retired", "technician", "services" |
| marital | Marital status | categorical | "married", "divorced", "single" (note: "divorced" means divorced or widowed) |
| education | Education level | categorical | "unknown", "secondary", "primary", "tertiary" |
| default | Has credit in default? | binary | "yes", "no" |
| balance | Average yearly balance, in euros | numeric | - |
| housing | Has housing loan? | binary | "yes", "no" |
| loan | Has personal loan? | binary | "yes", "no" |
| contact | Contact communication type | categorical | "unknown", "telephone", "cellular" |
| day | Last contact day of the month | numeric | - |
| month | Last contact month of the year | categorical | "jan", "feb", "mar", ..., "nov", "dec" |
| duration | Last contact duration, in seconds | numeric | - |
| campaign | Number of contacts performed during this campaign and for this client (includes last contact) | numeric | - |
| pdays | Number of days that passed by after the client was last contacted from a previous campaign (-1 means client was not previously contacted) | numeric | - |
| previous | Number of contacts performed before this campaign and for this client | numeric | - |
| poutcome | Outcome of the previous marketing campaign | categorical | "unknown", "other", "failure", "success" |

##### Output Variable (Desired Target)
- **deposit**: (binary) - Has the client subscribed a term deposit? ("yes", "no").

### 3. Tasks Completed

#### Exploratory Data Analysis (EDA)

1. **Missing Values Check**:
   - Verified that the dataset has no missing values, ensuring data completeness for analysis.

2. **Features with One Unique Value**:
   - Identified that there are no features with only one unique value, confirming that all features provide some variation in the data.

3. **Categorical Feature Exploration**:
   - Listed and explored categorical features including job, marital status, education, default status, housing loan status, personal loan status, contact type, month of contact, and outcome of previous campaigns.
   
4. **Categorical Feature Distribution**:
   - Visualized the distribution of categorical features using bar plots.

5. **Relationship between Categorical Features and Target Variable**:
   - Analyzed the relationship between each categorical feature and the target variable (`deposit`) using count plots.

6. **Numerical Feature Exploration**:
   - Listed numerical features including age, balance, day, duration, campaign, previous contacts, and pdays.
   
7. **Discrete and Continuous Numerical Features**:
   - Identified that all numerical features are continuous due to their large number of unique values.

8. **Distribution of Continuous Numerical Features**:
   - Plotted the distribution of continuous numerical features using histograms.
     
9. **Relation between Continuous Numerical Features and Target Variable**:
   - Analyzed the relationship between continuous numerical features and the target variable (`deposit`) using box plots.

10. **Outliers in Numerical Features**:
    - Detected outliers in numerical features using box plots.

11. **Correlation between Numerical Features**:
    - Calculated and visualized the correlation matrix of numerical features.

12. **Dataset Balance Check**:
    - Verified that the dataset is relatively balanced with approximately 52.6% `no` and 47.4% `yes` responses for the target variable (`deposit`), using a count plot.

#### Preprocessing

1. **Feature Engineering**:
   - Dropped less significant features such as `default` and `pdays`.
   - Encoded categorical features using one-hot encoding.
   - Converted binary features (`housing`, `loan`, `deposit`) into numerical format.

2. **Data Splitting**:
   - Split the dataset into training and testing sets for model validation.

#### Modeling

1. **Logistic Regression Model**:
   - Trained a Logistic Regression model using the preprocessed dataset.
   - Evaluated the model using accuracy, confusion matrix, and classification report.

2. **Model Evaluation**:
   - Achieved an accuracy of approximately 80.8%.
   - Visualized the confusion matrix in both raw counts and percentages for clear understanding.
   - Presented the classification report in a tabular format for detailed performance metrics.

### 4. Summary

The tasks completed provide a comprehensive analysis and modeling framework to predict the likelihood of clients subscribing to a term deposit. The findings and visualizations offer actionable insights for the bank's marketing strategy.

