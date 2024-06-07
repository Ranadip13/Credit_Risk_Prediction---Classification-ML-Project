# Credit_Risk_Prediction---Classification-ML-Project
This project is based on The German Credit Risk dataset. The goal is to predict if this loan credit would be a risk to the bank or not? In simple terms, if the loan amount is given to the applicant, will they pay back or become a defaulter?
Given the numerous applications that need to be processed daily, having a predictive model in place would be beneficial. Such a model can assist executives by providing early insights into the approval or rejection of new loan applications, helping them perform their tasks more efficiently.

In the case study below, a step-by-step approach to creating a Machine Learning predictive model for such scenarios will be discussed. This flow can be used as a template to solve any supervised ML classification problem.
The flow of the case study is as below:
- Reading the data in python
- Defining the problem statement
- Identifying the Target variable
- Looking at the distribution of Target variable
- Basic Data exploration
- Visual Exploratory Data Analysis for data distribution (Histogram and Barcharts)
- Feature Selection based on data distribution
- Outlier treatment
- Missing Values treatment
- Visual correlation analysis
- Statistical correlation analysis (Feature Selection)
- Selecting final predictors for ML
- Converting data to numeric for ML
- Splitting the data into Training and Testing sample
- Standardization / Normalization of data (if required)
- Sampling and K-fold cross validation
- Trying multiple classification algorithms
- Selecting the best Model
- Deploying the best model in production

Data description: The business meaning of each column in the data is as below
- GoodCredit: Whether the issued loan was a good decision or bad
- checkingstatus: Status of existing checking account.
- duration: Duration of loan in months
- history: Credit history of the applicant
- purpose: Purpose for the loan
- amount: Credit amount
- savings: Savings account/bonds
- employ: Present employment since
- installment: Installment rate in percentage of disposable income
- status: Personal status and sex
- others: Other debtors / guarantors for the applicant
- residence: Present residence since
- property: Property type of applicant
- age: Age in years
- otherplans: Other installment plans
- housing: Housing
- cards: Number of existing credits at this bank
- job: Job
- liable: Number of people being liable to provide maintenance for
- tele: Is the Telephone registered or not
- foreign: Is the applicant a foreign worker

Following the above steps, various classification machine learning algorithms were tried, including Logistic Regression, Decision Trees, Random Forest, AdaBoost, XGBoost, KNN, Support Vector Machines (SVM), and Naive Bayes, and their average accuracies were calculated. In this case, multiple algorithms produced similar average accuracy. Therefore, any one of them could be chosen. SVM was selected as the final model due to its fast performance on this high-dimensional data.

The final step is to deploy the model. To deploy the model, the following steps are followed.
1. Train the model using 100% data available
2. Save the model as a serialized file which can be stored anywhere
3. Create a python function which gets integrated with front-end (like Tableau) to take all the inputs and returns the prediction
