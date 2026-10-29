# Crypto Price Direction Prediction

A course project comparing machine-learning models for the next 15-minute price direction across BTC, ETH, SOL, XRP, and DOGE market data.

## Workflow

The [main notebook](ML_Final_Project_Hitesh.ipynb) combines five Bybit CSV files, explores the data, creates return/volume/candle features, adds lag and rolling statistics, and compares classification approaches.

The target is 1 when the next close exceeds the current close, otherwise 0. Models include thresholded linear regression, logistic regression, KNN, decision trees, and Random Forest.

## Recorded results

| Model | Accuracy reported in the notebook |
| --- | --- |
| Logistic regression baseline | 52.12% |
| Selected Random Forest | 52.65% |

The reported improvement is **0.53 percentage points**. These are historical notebook results, not a fresh reproduction.

## Evaluation limits

The final 365 days form a chronological test period. However, Random Forest candidates are selected using that same test set, so the selected score is not an untouched final evaluation. Labels also cross the train/test boundary by one future step unless the boundary observation is purged.

A stronger evaluation would use a separate chronological validation period, purge overlapping labels, and reserve a final test period. Directional accuracy alone does not establish profitable trading after transaction costs.

## Run locally

```bash
python -m venv .venv
python -m pip install jupyter pandas numpy matplotlib scikit-learn
jupyter notebook
```

Activate the environment first, then open `ML_Final_Project_Hitesh.ipynb`. Replace the five absolute Windows paths in its loading cell with the matching repository CSV paths. Run cells in order; the full multi-asset feature matrix and model search can require substantial memory and time.

## Repository contents

The five `BYBIT_*USDT_15m.csv` files supply the data. PNG files capture exploratory plots, model comparisons, the confusion matrix, and feature importance. A consolidated dependency file is not currently included.
