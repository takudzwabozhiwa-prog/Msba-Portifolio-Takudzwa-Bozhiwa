# Track 3: Deployment and Real-World Use of Churn Predictions

## Do you need churn predictions instantly or is overnight OK and why?
Overnight predictions are sufficient because customer churn does not usually happen instantly and retention actions such as marketing campaigns or outreach can be planned in advance. Running predictions overnight allows the company to process all customers efficiently and update risk scores regularly.

## Would this churn prediction run on a schedule or on demand, and where would results be saved?
This churn prediction would run on a scheduled basis, such as weekly or daily scoring, depending on business needs. The results would be saved in a database table that includes customer_id and churn_probability. This table could be used by dashboards or CRM systems to help business teams identify high-risk customers.

## What software approach would you use at a high level?
A scheduled Python process would be used to run the model automatically. This could be implemented using a scheduled job that loads new customer data, applies the trained XGBoost model, and saves the predictions to a database or dashboard system.

## What would you monitor so you trust this model over time?

### Data quality check
Monitor for missing values, unexpected data formats, or sudden drops in data volume.

### Input stability check
Monitor whether key input features change significantly over time, which could indicate changes in customer behavior or data collection.

### Outcome check
Monitor model performance metrics such as accuracy or churn rate trends to ensure the model continues to provide reliable predictions.
