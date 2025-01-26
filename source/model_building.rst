Model Building
==============

Algorithms Used
---------------

- **XGBoost**: Chosen for its accuracy and scalability.

Training and Evaluation
-----------------------

1. **Train-Test Split**:

   - 80% training, 20% testing.

   .. code-block:: python

      X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

   - Train the XGBoost model.

   .. code-block:: python

      model = xgb.XGBClassifier(use_label_encoder=False, eval_metric='logloss')
      model.fit(X_train, y_train)

2. **Metrics**:

   - Make predictions.

   .. code-block:: python

      y_pred = model.predict(X_test)

   - Evaluate performance.

   .. code-block:: python

      accuracy = accuracy_score(y_test, y_pred)
      f1 = f1_score(y_test, y_pred)

   - Results:
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
