# Enhancing-Risk-Prediction-in-Cardiovascular-Health
Enhancing Risk Prediction in Cardiovascular Health: A Comprehensive Discriminant Analysis of Mr. John Hughes' MHR Dataset Using SMOTE

# Project Description
The aim of this project is to conduct a discriminant analysis for Mr. John Hughes' MHR data set. Discriminant Analysis is a statistical technique used in data analysis and machine learning to determine which variables or features discriminate between two or more groups or categories.
From the dataset we can deduce that we have 6 independent variables and 1 dependent variable which includes; 
Age, Systolic Blood Pressure, Diastolic Blood Pressure, BS, Body Temperature, and Heart Rate 
Dependent variable is Risk Level
The primary objective of Discriminant Analysis is to find a combination of variables that best separates the different groups while minimizing variation within each group. This combination, known as the discriminant function, can be used to classify new observations into one of the predefined groups.
There are two types of discriminate analysis; Linear Discriminant Analysis (LDA) and Quadratic Discriminant Analysis (QDA).
In this analysis, we will utilize the SMOTE technique to achieve class balance for the dependent variable.

# Insights from the Pandas Profile Report
The Pandas profiling report offers valuable data insights, which can be beneficial for your data analysis process, including Linear Discriminant Analysis (LDA) and Quadratic Discriminant Analysis (QDA). In the analysis of the MHR dataset, some key observations were made:
- The dependent variable (RiskLevel) exhibits an unequal distribution of observations across its classes, with 406, 336, and 272 instances in the Low-risk, Mid-risk, and High-risk classes, respectively. This imbalance could pose challenges as it may lead the model to be biased toward the majority class, potentially reducing its effectiveness in predicting the minority class. To address this issue, we will apply the SMOTE technique to balance the dataset.
- It is evident that there is a high correlations between certain variables in the dataset, Age, Systolic Blood Pressure, Diastolic Blood Pressure. High correlations can affect the assumptions of Discriminant Analysis, particularly in the case of LDA and QDA. Multicollinearity can pose challenges for accurately estimating discriminant functions because it becomes complex to differentiate the influence of each variable from the others.

# Insights from the Confusion Matrix from LDA
The confusion matrix assesses the performance of Linear Discriminant Analysis in predicting high, low, and medium risks. The results are as follows:
- High Risk: The model accurately classified 37 cases as high risk but misclassified 4 as low risk and 14 as medium risk.
- Low Risk: For the low-risk category, the model correctly classified 42 cases but incorrectly classified 3 as high risk and 36 as medium risk. Notably, it performed poorly in identifying low risks, as it wrongly categorized 36 as medium risk.
- Medium Risk: In the medium-risk category, the model correctly classified 31 cases but misclassified 10 as high risk and 31 as low risk.

# Insights from the Classification Report LDA
The linear classification report offers a concise overview of the model's performance:
- Accuracy: With an accuracy of 54%, the model exhibited subpar classification accuracy, indicating that it struggled to correctly categorize instances.
- Precision: The model's precision rates for the different risk levels are 0.74 (74%) for high risk, 0.58 (58%) for low risk, and 0.38 (38%) for medium risk. This suggests that the model excelled in correctly identifying high-risk instances but was less precise in classifying low and medium-risk cases.
- Recall: The recall values for the risk categories are 0.67 (67%) for high risk, 0.52 (52%) for low risk, and 0.46 (46%) for medium risk. These scores indicate that the model was relatively effective at capturing high-risk instances but struggled with low and medium-risk classifications.
- F1 Score: The F1 score, which combines precision and recall, is not provided in the report. This metric offers a balanced perspective on the model's performance by considering false positives and false negatives.
In summary, the model's performance across various metrics suggests that it faced challenges in accurately classifying, detecting, and assigning instances to the different risk levels. There is room for improvement in its classification capabilities.

# Insights from the Confusion Matrix from QDA
- High Risk Evaluation: The QDA model accurately identified 39 instances as high risk. However, it made 12 misclassifications, erroneously categorizing them as low risk, and 4 misclassifications as medium risk.
- Low Risk Evaluation: In the low-risk category, the QDA model successfully classified 67 instances correctly. Nevertheless, it made 4 misclassifications, incorrectly labeling them as high risk, and 10 misclassifications as medium risk.
- Medium Risk Evaluation: When it comes to medium risk, the QDA model correctly classified 16 instances. However, it struggled in distinguishing between this category and others, with 10 instances mistakenly categorized as high risk and 41 instances as low risk. This indicates a suboptimal performance in classifying medium-risk cases.

# Insights from the Classification Report QDA
The linear classification report offers a concise overview of the model’s
- Accuracy Analysis: The model achieved an accuracy of 60%, indicating the proportion of correctly classified instances. This accuracy level suggests that the model faced challenges in classification and didn't perform exceptionally well.
- Precision for Risk Levels: Precision values of 0.74, 0.56, and 0.53 were observed for the "High," "Low," and "Medium" risk categories, respectively. This implies that the model correctly predicted 74% of high-risk cases, 56% of low-risk cases, and 53% of medium-risk cases.
- Recall for Risk Levels: Recall values of 0.71, 0.83, and 0.24 were found for the "High," "Low," and "Medium" risk categories, indicating that 71% of high-risk instances, 83% of low-risk instances, and 24% of medium-risk instances were correctly identified by the model.
- F1 Score and Comparative Analysis: The F1 score, which combines precision and recall, is not explicitly provided in the report. 
However, the general assessment in the summary suggests that the model performed better than Linear Discriminant Analysis (LDA) in terms of classifying, detecting, and assigning classes. This implies that the model showed improvements in classification over the LDA model, indicating a relatively more effective performance.

# Insights From the Optimized LDA and QDA Reports
- Precision
In comparison to the QDA model, the LDA model had an overall accuracy of roughly 54%. This shows that in this case LDA provides a greater overall classification accuracy.  QDA performs better in specific classes, such as "high risk" and "mid risk," achieving higher precision and recall ratings, even though its total accuracy is lower than LDA’s.
- Recall and accuracy
For the majority of the classes, the LDA model demonstrated improved precision and recall. This suggests that LDA is better at distinguishing between positive and negative events. The accuracy and recall numbers of the QDA model tend to vary more between classes, indicating that its performance might not be as consistent. In terms of precision and recall, QDA performs better in some classes, such as "high risk" and "mid risk," whereas LDA performs better in other classes.
- Model Complexity
All classes are presumed to have the same covariance, or homoscedasticity, by LDA. This assumption results in a simpler model when compared to QDA, which assumes that each class has a unique covariance (heteroscedasticity). If the data is consistent with the underlying theory, the simplicity of LDA may be advantageous. QDA, on the other hand, is a more adaptable model because it does not assume the same covariance. It may be more prone to overfitting when working with smaller amounts of data, but it may also be able to capture more complex connections in the data.

# Recommendations 
- I suggest considering the utilization of Quadratic Discriminant Analysis (QDA) due to its superior performance compared to Linear Discriminant Analysis (LDA). QDA demonstrates higher accuracy, precision, recall, and F1 score, making it a more favorable choice.
- Even though QDA outperforms LDA, I recommend conducting further feature engineering to enhance its overall performance. This process may involve incorporating pertinent features and eliminating irrelevant ones to optimize the model's predictive capabilities.







