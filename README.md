
# Customer Churn Prediction

This project involves building a machine learning model to predict customer churn using a dataset from a bank. The target variable is 'Exited', which indicates whether the customer has exited the bank or not. The goal is to classify customers as 'churned' or 'not churned' based on their attributes.

## Project Workflow

1. **Data Preprocessing:**
   - Dropping irrelevant columns such as 'RowNumber' and 'CustomerId'.
   - Handling class imbalance using Random Oversampling (ROS).
   - Feature scaling using `StandardScaler` for numeric features and encoding categorical variables using `OneHotEncoder`.

2. **Model Building:**
   - Two models were built:
     - **Logistic Regression**: To establish a baseline.
     - **Random Forest Classifier**: Tuned using GridSearchCV for improved performance.
   - The final Random Forest model was selected as the best model after tuning.

3. **Model Evaluation:**
   - Models were evaluated using accuracy, recall, and precision metrics.
   - A confusion matrix was plotted to visualize model performance.

4. **Saving the Model:**
   - The best model (Random Forest Classifier) was saved using `joblib` for future use.

5. **Predictions:**
   - The saved model was used to make predictions on the test data.
   - A comparison of actual vs predicted values was saved to a CSV file.

## Project Files
- `Churn_Modelling.csv`: The dataset used for this project.
- `Customer_Churn_Prediction.ipynb`: Jupyter file script containing the complete code for this project.
- `saved_models/best_random_forest_model.pkl`: The saved Random Forest model after hyperparameter tuning.
- `predicted_output/predicted_vs_actual.csv`: The output file comparing actual and predicted values.

## Requirements

To run this project, install the required dependencies by using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your_username/churn-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd churn-prediction
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Python script:
   ```bash
   python churn_prediction.py
   ```

## Results
- The final model achieved an accuracy of over 85% on the test set.
- The confusion matrix and comparison of actual vs predicted values are stored in the output files.

