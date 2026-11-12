# Holiday booking prediction (Random Forest)

Predicts whether a customer completes a holiday booking, using British Airways booking data (Forage job simulation). The model is tuned for recall: it tries not to miss real buyers, and accepts more false alarms in return.

## Data

`customer_booking.csv`: 50,000 bookings, 13 features plus the target `booking_complete`.
Only 14.8% of rows are bookings that completed (1,480 of 10,000 in the test split), so the classes are imbalanced.

Features include passengers, sales channel, trip type, purchase lead time, length of stay, flight day and hour, route, booking origin, and extras (baggage, seat, meals).

## Method

1. Encode text columns (`LabelEncoder`), map weekdays to 1 to 7.
2. 80/20 train/test split, `random_state=42`.
3. Random Forest with `GridSearchCV` (108 settings, 3-fold, scored on recall), with class weights to handle the imbalance.

Best settings: `max_depth=10`, `min_samples_leaf=4`, `min_samples_split=10`, 200 to 300 trees, balanced class weights.

## Results (test split of 10,000)

| | Precision | Recall | F1 |
|---|---|---|---|
| No booking | 0.93 | 0.71 | 0.81 |
| Booking | 0.30 | 0.71 | 0.42 |

Overall accuracy: **70.8%**.

How to read it: the model finds about 7 in 10 real buyers (recall 0.71), but only 3 in 10 people it flags actually buy (precision 0.30). Accuracy alone would hide this, which is why recall was the tuning goal.

## Next steps

- Try gradient boosting (XGBoost, LightGBM) and compare.
- Pick the decision threshold from the cost of a missed buyer versus a wasted offer.
- Check feature importance before adding features.

## Run it

```bash
pip install pandas scikit-learn matplotlib seaborn
jupyter notebook v25f8fd49c5.ipynb
```

The notebook reads the file from a Kaggle path. Change the path to the local `customer_booking.csv`.

Also in this repo: `Predicting Holiday Bookings Using Random Forest.pdf` (slides).
