# Smartphone Addiction Prediction
Binary classification of smartphone addiction based on usage behavior, comparing KNN, Decision Tree, and a neural network (MLP).

## Dataset
7,500 records, 12 features (screen time, sleep hours, notifications, stress level, etc.). Target: `addicted_label` (70.8% positive class). ID and addiction-level columns were excluded to avoid target leakage.

## Methods
- Preprocessing: median/mode imputation, standard scaling, one-hot encoding
- Models: KNN, Decision Tree, ANN (MLP 64-32)
- Validation: stratified 5-fold CV and repeated hold-out (5 split ratios x 5 repeats)

## Results (5-fold CV)
| Model | Accuracy | F1-Score | Train time |
|---|---|---|---|
| Decision Tree | 93.56% | 93.62% | 0.05 s |
| ANN (MLP) | 93.07% | 93.09% | 15.84 s |
| KNN | 88.87% | 88.81% | 0.22 s |

## Tech Stack
Python, Pandas, NumPy, scikit-learn, Matplotlib, Seaborn

## Files
`smartphone-addiction-prediction.ipynb` - full analysis and results
