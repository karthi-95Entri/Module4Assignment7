# Crowdfunding Classification – Model Building

## Project Overview

This project explores a crowdfunding dataset and builds classification models to predict whether a campaign is successful using the `IsSuccessful` target column. The work is organized into data preprocessing, model building, evaluation, cross-validation, hyperparameter tuning, and model comparison.

## Dataset

- **File:** `crowdfunding.csv`
- **Target column:** `IsSuccessful`
- **Dataset URL:**  
  https://raw.githubusercontent.com/karthi-95Entri/M4A7Classification-Algorithms-Model-Building/refs/heads/main/crowdfunding.csv

The notebook loads the dataset from the repository URL. If you run it in Google Colab and use a local copy instead, upload `crowdfunding.csv` before reading it.

## Project Tasks

### Task 1 – Data Exploration and Preprocessing
- Load and inspect the dataset.
- Check missing values and duplicate rows.
- Encode categorical variables.
- Select features and the target variable.
- Split data into training and testing sets.
- Apply feature scaling where appropriate.

### Task 2 – Classification Model Building
The notebook builds and evaluates these classifiers:
- Random Forest
- K-Nearest Neighbors (KNN)
- Decision Tree
- Gaussian Naive Bayes
- Support Vector Machine (SVM)

### Task 3 – Model Evaluation
Models are evaluated using classification metrics such as:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report

### Task 4 – Cross-Validation and Hyperparameter Tuning
- Use cross-validation to assess model stability.
- Tune model parameters with `GridSearchCV`.
- Compare candidate configurations.

### Task 5 – Model Comparison and Selection
- Compare model metrics.
- Identify the best-performing model using the evaluation results.
- Review training versus testing accuracy to consider generalization.

## Tools and Libraries

- Python
- pandas
- NumPy
- scikit-learn
- Matplotlib
- Seaborn

## How to Run in Google Colab

1. Open `M4A7Classification_Algorithms_Model_Building.ipynb` in Google Colab.
2. Run the notebook cells in order from top to bottom.
3. The notebook reads the dataset from the URL above, so a separate upload is not normally required when that URL is accessible.
4. If you prefer to upload the CSV manually, use:

   ```python
   from google.colab import files
   uploaded = files.upload()
   ```

   Then load it with:

   ```python
   import pandas as pd
   df = pd.read_csv("crowdfunding.csv")
   ```

5. If the Colab runtime is restarted, rerun the cells that import libraries and define variables such as `df`, `X`, and `y`.

## Important Notes

- Make sure the target column is named exactly `IsSuccessful`.
- Run notebook cells in order; later cells may depend on variables created earlier.
- Fit preprocessing steps only on training data when evaluating a model, then apply the fitted transformations to test data. This helps prevent data leakage.
- Use the held-out test set for final evaluation. A score calculated on the same data used for fitting or tuning may overstate how well the model performs on unseen campaigns.
- Report the results produced by your latest complete notebook run; results can differ depending on preprocessing, split strategy, and hyperparameters.

## Repository

GitHub repository:  
https://github.com/karthi-95Entri/M4A7Classification-Algorithms-Model-Building

## Conclusion

This project demonstrates a typical machine-learning classification workflow for crowdfunding campaign success: inspect and prepare the data, train multiple classifiers, tune model parameters, and compare models with evaluation metrics. The final model should be selected based on performance on unseen test data and not accuracy alone.
