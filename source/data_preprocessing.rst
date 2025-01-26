Data Preprocessing
==================

This section outlines the preprocessing steps taken to clean and prepare the data for modeling.

Data Checks
-----------

1. **Check Missing Values**:
   - No missing values were found in the dataset.

2. **Check Duplicates**:
   - No duplicate entries were found.

3. **Data Types**:
   - The dataset contains 9 columns with appropriate data types.

Feature Engineering
-------------------

1. **Transformations**:
   - A binary target column (`y`) was created to represent whether the `Chance of Admit` is >= 0.75 (class 1) or < 0.75 (class 0):
     ```python
     df['y'] = (df['Chance of Admit '] >= 0.75).astype(int)
     ```

2. **Scaling**:
   - Standardization was applied to numerical features using `StandardScaler`.

---

