# Salary Prediction App
This project uses machine learning to predict employee salaries based on various factors such as years at the company, satisfaction level, and average monthly hours worked. The application is built using Python, leveraging libraries like Pandas, Scikit-Learn, and Streamlit for building the model and interactive web interface.

## Overview
The **Salary Prediction App** takes inputs from the user through an interactive Streamlit interface and uses pre-trained machine learning models to predict an employee’s salary. The model is trained using a dataset that contains information about employees' job titles, departments, satisfaction levels, hours worked, and more.

The following steps were taken to build the project:
1. **Data Cleaning**: The dataset was cleaned by removing unnecessary columns and handling missing or duplicate values.
2. **Data Visualization**: Various visualizations were created to show trends in the dataset, such as salary by job title, gender count, and department-wise salary averages.
3. **Feature Scaling**: The features were standardized using Scikit-learn’s `StandardScaler`.
4. **Model Training**: Several machine learning models (Linear Regression, Support Vector Regression, and Random Forest Regressor) were trained to predict the salary based on the cleaned dataset.
5. **Hyperparameter Tuning**: GridSearchCV was used to find the best parameters for the Support Vector Regressor and Random Forest models.
6. **Deployment**: The model is deployed using **Streamlit**, allowing users to interactively input data and receive salary predictions.

## About the Project

### Data Preprocessing:
The dataset was loaded and preprocessed using the following steps:
- Dropped the `Employee_ID` column.
- Checked for missing values and duplicates.
- Cleaned noisy data and ensured that only relevant information was kept for analysis.

### Data Visualization:
Visualizations were created to gain insights into the dataset:
- **Gender Count**: A pie chart of the distribution of male and female employees.
- **Average Salary by Job Title**: A line plot showing the average salary across different job titles.
- **Salary by Department & Promotion**: Grouped average salary by department and promotion status over the last 5 years.
  
### Model Training:
Three machine learning models were used for salary prediction:
1. **Linear Regression**: A simple regression model to predict salaries based on the features.
2. **Support Vector Regression (SVR)**: A more complex model using a hyperparameter grid search to tune the best parameters.
3. **Random Forest Regressor**: An ensemble learning model also optimized through grid search.

### Hyperparameter Tuning:
- GridSearchCV was employed to optimize the Support Vector Regressor and Random Forest Regressor models by testing multiple hyperparameters like the number of estimators, maximum depth, and kernel types.

### Model Evaluation:
The models were evaluated using:
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

### Deployment with Streamlit:
The project is deployed using Streamlit, which provides an interactive web interface where users can input the following parameters:
- Years at the company
- Satisfaction level
- Average monthly hours worked

Upon clicking the "Predict Salary" button, the model predicts the salary based on the input values and displays the result to the user.

## Requirements

To run this project locally, the following Python libraries are required:

- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `joblib`
- `streamlit`

You can run the file code using the following command:

```bash
streamlit run app.py
