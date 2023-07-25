# Health-Insurance-Cross-sell-Prediction
Insurance is an agreement by which an individual obtains protection against any losses from an insurance company against the risks of damage, financial losses, damage, illness, or death in return for the payment of a specified premium. In this project, we have an insurance details dataset which contains a total of 381109 rows and 12 features. We have a categorical dependent variable Response which represents whether a customer is interested in vehicle insurance or not. As an initial step, we checked for the null and duplicate values in our dataset. As there were no null and duplicate values present in our dataset, so data cleaning was not required. Further, we normalized the numerical columns for bringing them on the same scale.

In Exploratory Data Analysis, we categorized the Age as YoungAge, MiddleAge, OldAge.Then we categorized Region_Code and Policy_Sales_Channel to extract some valuable information from these features. We explored the independent features using some plots.

For Feature selection, we used Kendall's rank correlation coefficient for numerical features and for categorical features, we applied the Mutual Information technique.

For Model prediction, we used supervised machine learning algorithms like Decision tree Classifier, AdaBoost, LightGBM, BaggingRegressor, NaiveBayes and Logistic regression. Then applied hyperparameter tuning techniques to obtain better accuracy and to avoid overfitting.

Problem Statement
Our client is an Insurance company that has provided Health Insurance to its customers now they need your help in building a model to predict whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.

An insurance policy is an arrangement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee.

For example, you may pay a premium of Rs. 5000 each year for a health insurance cover of Rs. 200,000/- so that if, God forbid, you fall ill and need to be hospitalised in that year, the insurance provider company will bear the cost of hospitalisation etc. for upto Rs. 200,000. Now if you are wondering how can company bear such high hospitalisation cost when it charges a premium of only Rs. 5000/-, that is where the concept of probabilities comes in picture. For example, like you, there may be 100 customers who would be paying a premium of Rs. 5000 every year, but only a few of them (say 2-3) would get hospitalised that year and not everyone. This way everyone shares the risk of everyone else.

Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called ‘sum assured’) to the customer.

Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

Now, in order to predict, whether the customer would be interested in Vehicle insurance, you have information about demographics (gender, age, region code type), Vehicles (Vehicle Age, Damage), Policy (Premium, sourcing channel) etc.

List of Machine Learning Models we are train and evaluate for our data set

Decision Tree Gaussian Naive Bayes AdaBoost Classifier Bagging Classifier LightGBM Logistic Regression

Tuning Methods

HalvingRandomizedSearchCV GridSearchCV RandomizedSearchCV

Evaluation Metrics

Accuracy Score Precision Recall F1 Score ROC AUC Score Log Loss

Plots

At the end of every model's hyper-parameter tuning, there is one ROC Curve which shows the ROC Scores and Parallel Coordinates Plot which shows all the combinations of hyper-parameters used for tuning the model to get the best parameters.

Conclusion
Starting from loading our dataset, we initially checked for null values and duplicates. There were no null values and duplicates so treatment of such was not required. Before data processing, we applied feature scaling techniques to normalize our data to bring all features on the same scale and make it easier to process by ML algorithms.

Through Exploratory Data Analysis, we categorized Age as YoungAge, MiddleAge, and OldAge, then we categorized the Region_Code as Region_A, Region_B, Region_C. We categorized the Policy_Sales_Channel into channel_A, channel_B, channel_C. Further, we observed that customers belonging to youngAge are more interested in vehicle response. We observed that customers having vehicles older than 2 years are more likely to be interested in vehicle insurance. Similarly, customers having damaged vehicles are more likely to be interested in vehicle insurance.

For Feature Selection, we used Kendall's rank correlation coefficient for numerical features and for categorical features, we applied the Mutual Information technique. Here we observed that Previously_Insured is the most important feature and has the highest impact on the dependent feature and there is no correlation between the two numeric features

Further, we applied Machine Learning Algorithms to determine whether a customer would be interested in Vehicle Insurance. For the Naive Bayes algorithm, we got an accuracy score of 68% and after hyperparameter tuning, the accuracy score increased to 72%. Similarly, for Decision Tree Classifier, AdaBoost, BaggingClassifier, LightGBM accuracy score was obtained around 82%-87%. So, we selected our best model as the model with an accuracy score of 85% considering precision and recall as we have an unequal number of observations in each class in our dataset, so accuracy alone can be misleading.

That’s it! We reached the end
