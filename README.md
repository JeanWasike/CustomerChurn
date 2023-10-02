# CustomerChurn
An ML project to predict customer churn in a telecom company.

Question:  Imagine you're working with Sprint, one of the biggest telecom companies in the USA. They're really keen on figuring out how many customers might decide to leave them in the coming months. Luckily, they've got a bunch of past data about when customers have left before, as well as info about who these customers are, what they've bought, and other things like that. So, if you were in charge of predicting customer churn, how would you go about using machine learning to make a good guess about which customers might leave? What steps would you take to create a machine learning model that can predict if someone's going to leave or not?

# Solution
To predict customer churn, the following steps are followed:

## Step 1: Data Collection
Since the use case company is Sprint, based in the USA, we need to work with data of a telecom company based in the USA. The sample dataset used was [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) from Kaggle. It contained information about customers, their phone services and uses, charges and whether they churned or not, hence it was relevant for the question at hand.
The overview of the data is shown below:
add image

## Step 2: Data Preparation
This phase includes preparing the data obtained for use by the machine learning model. It is implemented through the following steps.

### Data Preprocessing
This step involves checking the data for any missing values and replacing them in the case where the dataset is small or deleting the rows if the dataset is large. Since our dataset has 5000+ values, it would be easier to delete the rows with missing values. However, the data contained no missing values hence no need.
add image

### Feature and Labels Selection
This stage involves selecting the columns that are relavent to the prediction and dropping the columns that are not relevant for the task at hand. In our case, the selected featires for the prediction of customer churning were 'id','gender', 'SeniorCitizen', 'Partner', 'Dependents', 'tenure', 'PhoneService', 'MultipleLines', 'InternetService', 'PaymentMethod', 'MonthlyCharges', 'TotalCharges'.  The rest were dropped.
Afterwards, the columns were separated into  features and labels as X and y respectively.

### Label Encoding
Since come of the data values in the columns are categorical in nature, there is need for encoding them to a form that the model will be able to work with. This is done using label encoding. Some of the columns that needed encoding were 'gender', 'SeniorCitizen', 'Partner', 'Dependents', 'PhoneService', 'MultipleLines', 'InternetService', 'PaymentMethod'.

### Splittling into Train and Test Sets
This is the final step in data preparation where we split the data into training tests and testing sets. This will allow the model to be trained on the training sets and be evaluated with the testing data which will be new to it. This provides an easy way to assess the perfromance of the data to new data. The spli was in the ration 80:20.

## Step 3: Model Development
In this phase, the model will be built, trained and tested.

### Exploratory Data Analysis
This is the step where the nature of the data is observed and analyzed so as to identify the best model for use. In this case, the number of customers who churned within the dataset was represented using a pie chart.

add image

### Model Selection
The model selected for this task was Logistic Regression since it is a classification problem.  The model was trained and tested with an accuracy of 79% which was fairly good.
add image

# Conclusion
From the above steps, a machine elarning model was able to be built and trained for the task of predicting whether a customer will churn or not. 



