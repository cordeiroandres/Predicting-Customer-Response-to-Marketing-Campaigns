# **Predicting Bank Term Deposit Subscription Using Machine Learning**

![Bank](https://miro.medium.com/v2/resize:fit:640/format:webp/0*MGHujWl6U9Y_h1oV.png)

## **Introduction**

In this project, we aim to predict whether a customer will subscribe to a bank term deposit based on their personal and marketing campaign data. This is a common problem in the banking sector, where identifying potential subscribers can help target marketing efforts more efficiently. By using machine learning algorithms, we can build predictive models to assist in this process.

The primary objective of this analysis is to develop and evaluate different machine learning models to predict whether a customer will subscribe to a bank term deposit based on a set of attributes captured during previous marketing campaigns. We explore Logistic Regression (LR), K-Nearest Neighbors (KNN), Support Vector Machine (SVM), and Decision Trees (DT), comparing their performance across various metrics such as accuracy, precision, recall, F1-score, and AUC-ROC.

## **Dataset Overview**

The dataset used for this project is the **Bank Marketing Dataset** from [Kaggle](https://www.kaggle.com/datasets/henriqueyamahata/bank-marketing/data). It contains information collected during direct marketing campaigns conducted by a Portuguese bank. The marketing campaigns were based on phone calls, and the objective was to get customers to subscribe to a term deposit. The dataset contains 41,188 rows and 21 columns, with the target variable being **`y`**, which indicates whether the client subscribed to a term deposit (`yes` or `no`).

### **Attributes:**
1. **Age**: Age of the customer.
2. **Job**: Type of job (e.g., 'admin.', 'technician', 'blue-collar').
3. **Marital**: Marital status (e.g., 'married', 'single').
4. **Education**: Level of education (e.g., 'primary', 'secondary', 'tertiary').
5. **Default**: Whether the customer has credit in default.
6. **Balance**: Average yearly balance in euros.
7. **Housing**: Whether the customer has a housing loan.
8. **Loan**: Whether the customer has a personal loan.
9. **Contact**: Contact communication type (e.g., 'cellular', 'telephone').
10. **Day**: Day of the month when the last contact was made.
11. **Month**: Last contact month of the year (e.g., 'may', 'jul').
12. **Duration**: Last contact duration, in seconds.
13. **Campaign**: Number of contacts performed during this campaign for this client.
14. **Pdays**: Number of days that passed since the client was last contacted from a previous campaign.
15. **Previous**: Number of contacts performed before this campaign.
16. **Poutcome**: Outcome of the previous marketing campaign (e.g., 'success', 'failure').
17. **y**: Target variable indicating whether the client subscribed to a term deposit ('yes', 'no').

### **Data Preparation:**
The dataset was preprocessed to handle missing values, encode categorical variables using one-hot encoding, and scale numerical features using standardization. Additionally, the data was split into training and testing sets to allow proper model evaluation.

---

## **Results**

We implemented and compared four machine learning models: **Logistic Regression (LR)**, **K-Nearest Neighbors (KNN)**, **Support Vector Machine (SVM)**, and **Decision Trees (DT)**. The following table summarizes the performance metrics of each model:

| Model | Accuracy | Precision | Recall  | F1-Score | AUC-ROC |
|-------|----------|-----------|---------|----------|---------|
| **LR**   | 0.8996   | 0.6245    | 0.5578  | 0.5893   | 0.7540  |
| **KNN**  | 0.8681   | 0.4918    | 0.6506  | 0.5602   | 0.7755  |
| **SVM**  | 0.8688   | 0.4743    | 0.1525  | 0.2308   | 0.5637  |
| **DT**   | 0.8763   | 0.5158    | 0.6836  | 0.5880   | 0.7942  |

### **Key Observations**:
- **Logistic Regression (LR)** performed the best in terms of **accuracy (0.8996)** and **precision (0.6245)**.
- **Decision Tree (DT)** performed best on **recall (0.6836)** and had the highest **AUC-ROC (0.7942)**, making it the best at distinguishing between customers who would and wouldn't subscribe.
- **Support Vector Machine (SVM)** had the lowest performance in terms of recall and F1-score, indicating challenges in detecting the positive class (i.e., subscribers).

### **Conclusion:**
The **Logistic Regression** model performed the best overall, providing a good balance between accuracy and precision, making it ideal for predicting whether a customer will subscribe to a term deposit. However, if higher recall is desired, **Decision Trees** could be a better option due to their ability to capture more positive cases.

![BankMarket](https://media.assettype.com/analyticsinsight%2Fimport%2Fwp-content%2Fuploads%2F2024%2F03%2FPredicting-Bank-Deposit-Subscriptions-with-ML-and-Analytics.jpg?w=768&auto=format%2Ccompress&fit=max)
---

## **Next Steps**
For future work, we could:
- Experiment with **ensemble methods** such as **Random Forests** or **Gradient Boosting** to improve model performance.


---

Feel free to clone the repository, explore the code, and run the models on your own!

