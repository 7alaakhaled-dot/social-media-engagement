# Online Shopper Purchase Prediction

Predicting whether an online shopping session ends in a purchase, plus a side analysis of Instagram post performance.

## Projects
1. **shoppers.ipynb (main project):** classification on the UCI Online Shoppers Purchasing Intention dataset (12,330 sessions).
2. **analysis.ipynb (side analysis):** Instagram Analytics dataset. No predictive signal was found in pre-posting features (accuracy about 25%, same as random guessing for 4 classes).

## Approach (shoppers)
- Explored the data and found imbalanced classes (about 15.5% buyers).
- Compared Logistic Regression, Random Forest and Gradient Boosting with 5-fold cross-validation.
- Tuned Gradient Boosting and the decision threshold.
- Tested the model without PageValues, which partly leaks the target.

## Key results (test set)
| Setting | Precision | Recall | F1 (buyers) |
|---|---|---|---|
| Threshold 0.5 | 0.74 | 0.60 | 0.66 |
| Threshold 0.30 | 0.61 | 0.73 | 0.67 |
| Without PageValues | 0.33 | 0.49 | 0.39 |

## Limitations
Results are correlations, not causes. PageValues leaks part of the target. The model predicts purchase during a session, not before it.

## Data
Not included in this repo. Download from Kaggle:
- Online Shoppers Purchasing Intention Dataset (Akash Patel)
- Instagram Analytics Dataset (Kundan Sagar Bedmutha)

## Tools
Python, pandas, scikit-learn, matplotlib