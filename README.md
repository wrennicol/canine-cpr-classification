# Canine CPR Classification

Predicts whether CPR succeeds in a canine patient using Logistic Regression, KNN, and Random Forest, and finds which variables matter most.

**Tools:** Python, pandas, NumPy, scikit-learn

## Data
158 dogs, 55 successful outcomes (about 35%). Data file: `data/CPCR_finalx.xls`

## What I did
- Wrote logistic regression from scratch (IRLS) and found that `arrh4` and `arrh6` caused unstable coefficients, so I removed them
- Compared three models on a 75/25 train/test split

## Results

| Model | Test accuracy | F1 |
|---|---|---|
| Logistic Regression | 65% | 0.53 |
| Random Forest | 70% | 0.71 |
| KNN | 75% | 0.73 |

**Most important variables (Random Forest):** rounds of epinephrine, duration of CPR, dog's weight.

**Limitations:** the test set is small (about 40 dogs) and the models overfit somewhat, so the differences between models are not conclusive.
