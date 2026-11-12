# Customer Churn Prediction & Business Insights

Predicts which telecom customers are likely to leave (churn), explains why, and turns the findings into retention recommendations.

- **Data:** IBM Telco Customer Churn dataset, 7,043 customers, 21 columns
- **Analysis:** data cleaning, EDA with Pandas and Matplotlib, SQL analysis with SQLite
- **Models:** Logistic Regression, Decision Tree, Random Forest (Scikit-learn), with class weights for the imbalanced target
- **Evaluation:** precision, recall, F1 and confusion matrix

## Key findings

| Churn driver | Group | Churn rate |
|---|---|---|
| Contract | Month-to-month | 42.7% |
| Contract | Two year | 2.8% |
| Tenure | 0-12 months | 47.4% |
| Payment | Electronic check | 45.3% |

## Model results (test set, 1,409 customers)

| Model | Precision | Recall | F1 |
|---|---|---|---|
| Logistic Regression | 0.507 | 0.786 | 0.616 |
| Decision Tree | 0.500 | 0.807 | 0.618 |
| **Random Forest** | **0.518** | **0.797** | **0.628** |

Random Forest catches about 80% of churners. Recall was prioritised because a missed churner costs more than a retention offer sent to a loyal customer.

## Recommendations

1. Move month-to-month customers to annual plans with a discount.
2. Run an onboarding and loyalty programme for customers in their first year.
3. Encourage automatic payment instead of electronic checks.
4. Score customers weekly and send the high-risk list to the retention team.

## How to run

Open `Customer_Churn_Prediction.ipynb` in Google Colab or Jupyter and run all cells. The dataset downloads automatically.
