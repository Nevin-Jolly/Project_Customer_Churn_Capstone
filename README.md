# Final Capstone — Predicting Customer Churn

## Project
**Predicting Customer Churn: A Data-Driven Analysis of Subscription Customer Behaviour Using Machine Learning**

## Dataset
LMS-provided Project 4 Telco Customer Churn dataset.

- Raw observations: 7,043
- Variables: 21
- Target: `Churn`
- Churn rate: 26.54%

## Workflow
1. Problem definition
2. Dataset understanding
3. Data cleaning
4. Data preprocessing
5. EDA
6. Statistical analysis
7. Feature engineering
8. Logistic Regression baseline
9. Random Forest model
10. Model evaluation
11. Findings
12. Discussion
13. Limitations
14. Conclusion and recommendations

## Key Model Results
| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.806 | 0.657 | 0.559 | 0.604 | 0.842 |
| Random Forest | 0.763 | 0.537 | 0.783 | 0.637 | 0.842 |

## Main Findings
- Month-to-month contracts have the highest observed churn.
- Churned customers have substantially shorter tenure.
- Churned customers have higher average monthly charges.
- Internet service and payment method are useful segmentation variables.
- Random Forest provides stronger recall/F1 performance than the Logistic Regression baseline.

## Files
- `Final_Capstone_Customer_Churn_Report.pdf` — final research-style PDF report
- `Final_Capstone_Customer_Churn_Report.docx` — editable report version
- `Customer_Churn_Capstone_Analysis.ipynb` — reproducible notebook
- `P_4_WA_Fn-UseC_-Telco-Customer-Churn.csv` — original LMS dataset
- `Telco_Customer_Churn_Cleaned.csv` — cleaned dataset
- `plots/` — report figures
- `README.md` — project documentation

## Running the Notebook
Place the notebook and original CSV in the same folder and run all cells in Jupyter Notebook or Google Colab.

## Why Random Forest is the final model

Logistic Regression is retained as an interpretable baseline. Random Forest is selected for the final retention-screening use case because it produces substantially higher recall (78.34% vs 55.88%) and a higher F1-score (63.70% vs 60.40%). Accuracy is lower for Random Forest (76.30% vs 80.55%), so the choice is not based on accuracy alone. Recall is prioritized because missing an actual churner (a false negative) can mean missing a retention opportunity.

ROC-AUC is approximately the same for both models (0.842), so the main practical distinction in this analysis is the classification threshold behaviour reflected by recall, precision and F1-score.
