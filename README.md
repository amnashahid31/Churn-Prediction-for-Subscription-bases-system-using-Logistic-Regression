**AI Fellowship (2024)
SayabiDevs**


**Final Project Report
AI-Based Predictive Analytics Platform**



**Domain Chosen: General Public / e-commerce
System Name: Churn Prediction for Subscription-based system**



**Link for Dataset:** https://www.kaggle.com/datasets/safrin03/predictive-analytics-for-customer-churn-dataset


**1. Data Preparation**

**Data Loading:** The dataset is loaded from a CSV file named “train.csv”.
**Handling Missing Values:** Numerical columns such as ‘AccountAge’ , ‘MonthlyCharges’, ‘TotalCharges’, and others are filled with the median value to handle missing data.
**Encoding Categorical Data:** Binary categorical columns (e.g., ‘PaperlessBilling’, ‘MultiDeviceAccess’) are converted into 0s and 1s. Other categorical variables (e.g., ‘SubscriptionType’, ‘PaymentMethod’) are encoded using LabelEncoder for machine learning purposes.
**Scaling Numerical Data:** Numerical features are standardised using ‘StandardScaler’ to ensure all values are on the same scale.


**2. Model Selection: Logistic Regression**

Logistic Regression is selected for the churn prediction problem because it is well-suited for binary classification tasks. In this case, weare predicting whether a customer will churn (leave the service) or not churn (stay), which is a binary outcome (yes/no, true/false)
**Splitting Data:** The dataset is split into a training set (80%) and a test set (20%).
**Model Training:** A Logistic Regression model is chosen to predict customer churn. The model is trained on the training set using ‘LogisticRegression’ from scikit-learn (library).
**Model Prediction:** The trained model is used to predict churn on the test dataset.


**4. Performance Evaluation**

**Accuracy:** The model achieves an accuracy of (0.824) 82.4% on the test set.
**Confusion Matrix:** The confusion matrix shows how well the model distinguishes between churn and non-churn customers.
**Precision, Recall, F1-Score:** These metrics are computed to evaluate the model's predictive performance for the churn class:
**Precision:** 0.562 (indicates the total true churn predictions)
**Recall:** 0.114 (indicates actual churn cases which are predicted correctly)
**F1-Score:** 0.190 (it is the harmonic mean of precision and recall)


**5. Model Export**

The trained logistic regression model is saved as a pickle file (logreg.pkl) for further use, such as deploying it in a production environment or using it as part of an API.


**6. Web Application**

**UI Interface:** The user interface (UI) is built using Streamlit. The app takes two inputs:
**a. Account Age:** The number of months the user has been subscribed.
**b. Monthly Charges:** The monthly subscription cost.
**Logic for Churn Prediction:** Once the user enters the values and clicks the ‘Predict’ button, the application gathers the input, transforms it into a dataframe, and uses the preloaded model to make a prediction on whether the customer is likely to churn.


**7. Technology Stack:**

We used Streamlit over the MERN stack for churn prediction application. It is because we needed rapid development, simplicity, and the seamless integration with machine learning models. Streamlit is able to create an interactive UI with minimal code and without needing extensive backend setup

**Business UseCase:**
This model can help the business identify at-risk customers who may churn, allowing the implementation of targeted retention strategies.

**Issues Faced:**
Due to the use of a new technology, Streamlit, there were some issues in the creation of the UI interface for the platform. This made it difficult to run the platform as required although the Machine learning part is complete in all aspects.



