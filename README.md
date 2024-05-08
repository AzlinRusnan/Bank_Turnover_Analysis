# <div align="center">BANK TURNOVER ANALYSIS</div>
![Intro](https://github.com/Pradnya1208/Telecom-Customer-Churn-prediction/blob/main/output/customer%20churn.jpeg?raw=true)

## What is Customer Churn 🤔?
**Click on the video to watch📺**

[![Watch the video](https://img.youtube.com/vi/InOB1wXEkC8/0.jpg)](https://www.youtube.com/watch?v=InOB1wXEkC8)

## Overview:

This project focuses on analyzing bank turnover to identify key factors contributing to customer churn in the banking sector. By leveraging data-driven insights, we aim to propose strategies to improve customer retention and enhance service delivery.

## Objectives

- **Understand Customer Behavior**: Analyze historical data to understand why customers leave the bank.
- **Predictive Modeling**: Develop models to predict potential churn to enable proactive retention strategies.
- **Actionable Insights**: Provide actionable recommendations based on the analysis to reduce turnover rates.

## Dataset:
 [Bank Customer Churn](https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn/data)

## Data Description

The dataset used in this analysis contains the following key attributes:

- CustomerId, Surname: Identifiers and names, generally not useful for prediction.
- CreditScore, Geography, Gender, Age: Demographic information.
- Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary: Financial and account-related details.
- Exited: This is the target variable indicating whether a customer has churned (1) or not (0).
- Complain, Satisfaction Score, Card Type, Point Earned: Additional customer satisfaction and engagement metrics.

## Implementation:

**Libraries:** sklearn, Matplotlib, pandas, seaborn, and NumPy

## Glimpses of EDA:

### 1. Displaying Customer Turnover Distribution
>![Customer Turnover Distribution](images/Distribution.png)
>The dataset shows a significant difference between the number of customers who have left the bank ("Yes") and those who have stayed ("No").

### 2. Displaying Customer Turnover by Gender
>![Customer Turnover by Gender](images/Gender.png)
>**Insight:**
>
>According to the Gender bar graph above, female customer leading the percentage of turnover (11.4%) from the bank compared to male(9.0%).
>
>**Recommendation:**
>
>Customer Research: Conduct surveys, focus groups, and interviews with female customers to understand their specific concerns, preferences, and needs. This >research can reveal insights into why they may be more likely to turn from bank.
>Monitoring and Feedback: Regularly monitor the effectiveness of these strategies through ongoing feedback mechanisms and adjust them as necessary to ensure they >continue to meet the needs of female customers effectively

### 3. Displaying Customer Turnover by Number of Product
>![Customer Turnover by Number of Product](images/Product.png)
>**Note:**
>
>Banks offer a wide range of products and services to meet the financial needs of their customers, ranging from basic banking services to more complex financial >solutions. For example here's a list of products from Maybank (https://www.maybank.com/en/products-and-services.page):
>
>1. Wealth Management
>2. Insurance & Takaful 
>3. Consume and Digital Solutions
>4. Etc..
>
>**Insight:**
>
>The majority of customers hold either one or two products, while fewer customers have more than two products.
>The highest turnover occurs among customers with only one product.
>
>**Recommendation:**
>
>Customer Research: Conduct surveys, focus groups, and interviews with female customers to understand their specific concerns, preferences, and needs. This >research can reveal insights into why they may be more likely to turn from bank.
>Monitoring and Feedback: Regularly monitor the effectiveness of these strategies through ongoing feedback mechanisms and adjust them as necessary to ensure they >continue to meet the needs of female customers effectively.

### 4. Displaying Customer Turnover by Active Member or Not
>![Customer Turnover by Active Member or Not](images/Isactivemember.png)
>**Insight:**
>1. IsActiveMember: Indicates active membership status (1 = Active, 0 = Inactive).
>2. Active members show a significantly lower turnover rate compared to inactive members, highlighting the importance of engagement in customer retention strategies.
>
>**Recommendation:**
>
>It is a loss if a bank loses its customer. Below are the few suggestions that can keep customer running away from a bank:

>1. Loyalty Programs: Implementing loyalty programs that reward customers for their business can increase retention. Rewards could be in the form of better rates, >lower fees, or even non-banking perks.
>2. Community Engagement: Banks that actively engage with their community, such as sponsoring local events or supporting local businesses, can build goodwill and >strong local customer base.

### 5. Displaying Customer Turnover by Satisfaction Score
>![Customer Turnover by Satisfaction Score](images/SatisfactionScore.png)
> **Note:**
>
>The visualization for "Customer Turnover by Satisfaction Score" shows the distribution and impact of satisfaction scores on customer churn. The percentages >indicate how each satisfaction score segment contributes to the overall customer churn and retention with score 5 is the perfect score and 1 is the lowest score.

>**Insights:**
>
>Satisfaction score of 2 appear to have higher churn rates, suggesting that less satisfied customers are more likely to leave. This relationship can guide >strategies to improve customer retention by focusing on enhancing satisfaction levels.

### 6. Visualizing Customer Turnover by Balance.
>![Customer Turnover by Balance](images/Balance.png)
>**Insights:**
>
>Over 3,000 customers have a zero account balance. These customers are more likely to deactivate their accounts. When excluding zero values, the balance >distribution approximates a normal distribution.
>
>**Recommendations:**
>
>1. For customers with low or zero balances, strategies to engage them might be developed to prevent account dormancy and potentially convert them into more active, >profitable customers.
>
>2. Analyzing the needs of different segments might reveal opportunities for new financial products or services, especially targeted at high-balance customers who >show a higher propensity to turnover.

### 7. Visualizing Customer Turnover by Age.
>![Customer Turnover by Age](images/Age.png)
>**Insights:**
>1. Customers who exited are typically older than those who stayed. The distribution for those who exited is skewed towards older ages, while the distribution for >those who stayed is more concentrated in the younger age range.
>
>2. Notably, the peak for customers who exited (Yes) is much higher around ages 45 to 60, suggesting this age group is at higher risk of churning.
>
>3. The median age of customers who exited is higher than those who stayed. This is evident from the position of the median line in each box.
>
>4. Customers who stayed have a narrower interquartile range (IQR), mostly concentrated between the ages of 30 and 40. In contrast, the age range for those who >exited is broader, with a lower quartile near 40 and an upper quartile extending to around 55.

### 8. Correlation Matrix
>![Correlation Matrix](images/CorrMatrix.png)
>
>**Insight:**
>
>The correlation matrix above highlights several important relationships:

>1. Age: Shows a moderate positive correlation with Exited, suggesting that older customers are more likely to exit.
>2. IsActiveMember: Has a negative correlation with Exited, confirming that active members are less likely to leave.
>3. Balance: Has a small positive correlation, indicating a slight tendency for customers with higher balances to exit, which might be counterintuitive and >warrants further investigation.
>4. NumOfProducts: Interestingly, there's a negative correlation here; customers with more products are slightly less likely to exit, which might suggest that >diversified services could help in retention.

## Few glimpses of Model Prediction:
### Importance Variables in the Model Prediction
>![Customer Turnover Distribution](images/Var.png)
>The key factors that significantly influence the deactivation of customers banking facilities are:- Age, Complain, Credit Score and IsActiveMember

## Conclusion:
>**Key-Points:**
>1. Model Performance: The logistic regression model provided a reasonable baseline performance with turnover customers, which is evident from the low recall and
>F1 score for the positive class.
>2. Feature Importance: The feature importance analysis from the logistic regression model can provide insights into which factors are most influential in predicting customer turnover. Important features may include customer age, account balance, number of products, credit score, and activity level. Understanding these can help inform strategies to retain customers.
>3. Business Insights: Active membership appears to be a strong indicator of retention, suggesting that efforts to engage customers could reduce turnover. Older >customers were more likely to turnover, highlighting a potential area to explore tailored retention strategies. The presence of a credit card did not show a >strong correlation with turnover, suggesting that simply having a credit card isn't a deciding factor in customer retention.
>   
>**Strategic Recommendations:**
>1. Investigate the reasons behind the turnover of older customers and consider offering products or services that might be more appealing to them.
>2. Enhance customer engagement and satisfaction, perhaps by improving customer service or offering loyalty programs, as active members are less likely to turnover.
>3. Consider a more detailed analysis of the customers with high balances who exited to understand if there are specific services or products that are not meeting
>   their needs.

## More project details on EDA & Results:
**Click here:**
[Bank Turnover Analysis](https://colab.research.google.com/drive/1T8MYyxysA7KzMLcFFeGgJyYvb5Yci3bA#scrollTo=lkCi_np54J5R))

# <div align="center">Enjoy 👍</div>
