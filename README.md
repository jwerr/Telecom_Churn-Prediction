Introduction:
Customer churn, or the rate at which customers stop doing business with a company, is a critical metric for any telecom company. High churn rates can significantly impact profitability, making it essential for businesses to identify customers at risk of leaving. This project focuses on predicting customer churn in a telecom setting, using a dataset spanning four months. The objective is to build predictive models that can identify high-value customers likely to churn, allowing the company to take proactive measures to retain them.

We define high-value customers as those with significant recharge amounts in the first two months. By analyzing customer behavior patterns and service usage, we aim to pinpoint key indicators of churn and develop strategies to mitigate it. The results of this analysis will not only highlight the most significant predictors of churn but will also provide actionable insights for reducing customer attrition.

Understanding of Churn:
There are two main models of payment in the telecom industry - postpaid and prepaid.

In the Postpaid model, when customers want to switch to another operator, they usually inform the existing operator, and you directly know that this is an instance of churn.

However, in the Prepaid model, customers who want to switch to another network can simply stop using the services without any notice, and it is hard to know whether someone has actually churned or is simply not using the services temporarily.

Prepaid is the most common model in India and southeast Asia, while postpaid is more common in Europe in North America. This project is based on the Indian and Southeast Asian market.

Revenue-based churn: Customers who have not utilized any revenue-generating facilities such as mobile internet, outgoing calls, SMS etc. over a given period of time. One could also use aggregate metrics such as ‘customers who have generated less than INR 4 per month in total/average/median revenue’.

The main shortcoming of this definition is that there are customers who only receive calls/SMSs from their wage-earning counterparts.

Usage-based churn: Customers who have not done any usage, either incoming or outgoing - in terms of calls, internet etc. over a period. A potential shortcoming of this definition is that when the customer has stopped using the services for a while, it may be too late to take any corrective actions to retain them. For e.g., if you define churn based on a ‘two-months zero usage’ period, predicting churn could be useless since by that time the customer would have already switched to another operator.

In this project, the usage-based definition has been considered.

High-value Churn: Approximately 80% of revenue comes from the top 20% customers (called high-value customers). Thus, if we can reduce churn of the high-value customers, we will be able to reduce significant revenue leakage.

Here, high-value customer-level data has been analyzed of a leading telecom firm, built predictive models to identify customers at high risk of churn and identify the main indicators of churn.

Business Aspects
The dataset contains customer-level information for a span of four consecutive months - June, July, August and September.

The business objective is to predict the churn in the last (i.e. 9th) month using the data from the first three months.

Customers usually do not decide to switch to another competitor instantly, but rather over a period (especially applicable to high-value customers). In churn prediction, we assume that there are three phases of customer lifecycle:

The ‘good’ phase: In this phase, the customer is happy with the service and behaves as usual.

The ‘action’ phase: The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behavior than the ‘good’ months. Also, it is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point

The ‘churn’ phase: In this phase, the customer is said to have churned. You define churn based on this phase. Also, it is important to note that at the time of prediction, this data is not available to you for prediction. Thus, after tagging churn as 1/0 based on this phase, you discard all data corresponding to this phase.

Directory Tree:

├── data dictionary 
│   └── Data_Dictionary_Telecom_Churn_Case_Study.xlsx
├── datasets
│   ├── telecom_churn_data.csv
│   └── HVC_telecom_cleaned.csv
├── model
│   └── model.pkl
├── Telecom_Churn_Driving_Factors.py
├── Telecom_Churn_Prediction.py
├── requirements.txt
└── README.md
