# Customer-Churn-Prediction-Model
The primary reason I chose this project is because customer retention is one of the biggest challenges for subscription and service-based industries like telecom, SaaS, and e-commerce. As an aspiring data scientist, I wanted to work on a classification problem where the goal is to predict a binary outcome whether a customer will stay or leave. 

2. How It Helps the Business:
   
Proactive Retention Strategies: It helps companies identify high-risk customers before they cancel their subscriptions, allowing businesses to offer them special discounts or better support.

Cost Efficiency: Acquiring a new customer costs significantly more than retaining an existing one. This model helps marketing and customer success teams focus their retention budget only on the customers who are most likely to churn.

Reducing Revenue Leakage: By predicting customer churn trends, companies can minimize customer loss and improve long-term revenue stability.

Step-by-Step Technical Execution:
5. Step 1: Data Collection & UnderstandingI used the benchmark Telco Customer Churn dataset from Kaggle, which contains customer demographic details, account tenure, services subscribed, and payment information.

6. Step 2: Data Cleaning & PreprocessingThe raw data contained non-numeric text columns and missing values in fields like TotalCharges.I handled missing values using median imputation and converted text data types into proper numeric types.Since machine learning models only understand numbers, I applied Label Encoding to convert categorical string columns (like contract type, payment method, and gender) into numeric formats. I also dropped unique identifier columns like customerID as they have no predictive value.
7. 
8. Step 3: Feature Selection & Train-Test SplitI separated the dataset into independent feature variables ($X$) containing customer metrics and the target variable ($y$) as Churn (0 for retained, 1 for churned).I split the dataset into an 80% training set and 20% testing set using Scikit-Learn's train_test_split to ensure unbiased model evaluation.
9. 
10. Step 4: Model Training (Machine Learning)I chose the Random Forest Classifier ensemble algorithm because it handles tabular data and complex non-linear feature interactions very well.I trained the model using the training data (model.fit(X_train, y_train)).
11. 
12. Step 5: Model Evaluation & Performance MetricsUnlike regression, classification models cannot be evaluated using MSE or $R^2$.
13. 
14. Instead, I evaluated my model on unseen test data using metrics like Accuracy Score, Precision, Recall, and Confusion Matrix via Scikit-Learn's classification_report.
