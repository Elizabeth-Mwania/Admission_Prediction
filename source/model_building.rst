Model Building
==============

Algorithms Used
---------------

- **XGBoost**: Chosen for its accuracy and scalability.

Training and Evaluation
-----------------------

1. **Train-Test Split**:
   - 80% training, 20% testing.
2. **Metrics**:
   - Accuracy: 90%
   - F1 Score: 0.8857

Hyperparameter Tuning
---------------------

Best parameters:
- `colsample_bytree`: 0.9
- `learning_rate`: 0.1
- `max_depth`: 5
- `n_estimators`: 100
- `subsample`: 0.8
