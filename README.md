# **TelConnect Churn Prediction & Retention Optimization**

## **Project Overview**
This project aims to **predict customer churn** for TelConnect and develop a **cost-effective retention strategy** using machine learning. The goal is to shift from a **reactive** approach (responding only when customers cancel) to a **proactive** strategy that targets high-risk customers before they leave.

## **Dataset**
- **Source:** TelConnect's customer database
- **Size:** 7,043 customer records
- **Features:**
  - **Demographics:** Gender, senior citizen status, dependents
  - **Account Info:** Tenure, contract type, payment method
  - **Services:** Phone, internet, streaming, security options
  - **Churn Label:** Whether the customer left TelConnect

## **Data Preprocessing**
- Handled **missing values** (median for numerical, mode for categorical)
- **One-Hot Encoding** for categorical variables
- **Train-Test Split (80%-20%)** with stratification

## **Exploratory Data Analysis (EDA)**
- **High churn risk:** Customers on **month-to-month contracts** and **short tenure**
- **Feature correlation:** Contract type, tenure, and payment method were the strongest predictors of churn
- **Churn visualization:** Identified patterns in service usage and customer demographics

## **Machine Learning Models**
Trained and evaluated multiple models:
- **Logistic Regression** (Baseline)
- **Random Forest** (Ensemble Model)
- **XGBoost** (Boosting Model)
- **AdaBoost** (Best trade-off between accuracy & efficiency)

### **Model Performance Comparison**
| Model              | Accuracy | ROC AUC | Precision (Churn) | Recall (Churn) |
|-------------------|----------|---------|------------------|--------------|
| Logistic Regression | 78.2%   | 0.71    | 0.61             | 0.51         |
| Random Forest      | 80.5%   | 0.83    | 0.64             | 0.52         |
| XGBoost           | 80.0%   | 0.84    | 0.65             | 0.53         |
| **AdaBoost**      | **80.0%** | **0.80** | **0.66**         | **0.50**     |

## **Feature Importance**
Top churn predictors across models:
- **Contract Type:** Short-term contracts have the highest churn
- **Tenure:** New customers are more likely to churn
- **Payment Method:** Electronic check users churn the most

## **Retention Strategy & Cost-Benefit Analysis**
### **StreamFlix Voucher Cost Analysis**
- **Cost per voucher:** $30
- **Avg. monthly revenue per customer:** $65
- **Avg. retention period for saved customers:** 6 months
- **Optimal threshold selection** balances true positives (retained customers) and false positives (unnecessary vouchers)

### **Recommendations for TelConnect**
✔ **Implement a proactive retention strategy** using AdaBoost churn predictions  
✔ **Target high-risk customers** before they call to cancel  
✔ **Optimize retention incentives:** Offer StreamFlix selectively to maximize ROI  
✔ **Explore alternative offers:** Discounted long-term contracts, proactive tech support  
✔ **Conduct A/B Testing:** Compare voucher effectiveness with other retention strategies  

## **Next Steps**
- Deploy **AdaBoost model** for real-time churn prediction
- Develop **targeted retention messaging** based on model insights
- Monitor **retention rates & net savings** for further optimization

