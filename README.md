# Uber Fare Prediction Analysis

## Machine Learning Project

This project presents an end-to-end machine learning analysis of Uber trip data. The objective is to understand the factors influencing fare amounts and develop a predictive model capable of estimating fares for new trips.

## Project Objectives

- Load and inspect the Uber fare dataset
- Clean and preprocess the data
- Perform exploratory data analysis (EDA)
- Engineer useful geographic and datetime features
- Train and compare multiple regression models
- Evaluate model performance using RMSE, MAE, and R²
- Identify the best-performing model
- Generate fare predictions for new Uber trips
 ## Dataset

The dataset used in this project is the **Uber Fares Dataset** obtained from Kaggle.

- **Source:** [Uber Fares Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/uber-fares-dataset)
- **File:** `uber.csv`
- **Records:** 200,000 trips
- **Features:** Fare amount, pickup datetime, pickup and drop-off coordinates, and passenger count

The dataset is not included in this repository. To reproduce the analysis, download `uber.csv` from the Kaggle link above and place it in the `data` folder before running the notebook.

## Data Cleaning

The preprocessing stage included:

- Checking missing values
- Removing invalid and unrealistic records
- Validating passenger counts
- Restricting coordinates to appropriate geographic boundaries
- Preparing datetime information for analysis and modelling

## Exploratory Data Analysis

Exploratory analysis was performed to understand:

- Fare distributions
- Passenger patterns
- Geographic trip characteristics
- Relationships between trip distance and fare
- Temporal patterns in Uber trips

## Feature Engineering

Additional features were created to improve predictive performance, including:

- Haversine trip distance
- Year
- Month
- Day of week
- Hour
- Geographic location indicators
- Distance/proximity to major NYC landmarks and airports

## Machine Learning Models

The following regression models were evaluated:

1. Linear Regression
2. Random Forest
3. XGBoost

Model performance was compared using:

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

## Model Results

XGBoost achieved the best predictive performance among the evaluated models and was selected as the final model.

The analysis showed that trip distance was the strongest predictor of fare amount, while geographic and airport-related features also contributed to prediction performance.

## Example Prediction

The final model was tested on a new trip from Midtown Manhattan to JFK Airport.

**Predicted Fare: $57.74**

This demonstrates that the trained model can generate fare estimates from new trip information.

## Key Findings

- Trip distance is the strongest factor influencing Uber fare amounts.
- XGBoost achieved the best predictive performance among the evaluated models.
- Location-related features, including proximity to major NYC airports, contribute to fare prediction.
- Data cleaning and feature engineering improved the quality of the modelling dataset.
- The final model can generate predictions using pickup, drop-off, datetime, and passenger information.

## Business Recommendations

- Use trip distance and geographic information as key inputs when estimating fares.
- Incorporate airport and high-demand location indicators into pricing systems.
- Regularly retrain the model with newer trip data to account for changing travel and pricing patterns.
- Monitor prediction errors and unusual trips to maintain model reliability.
- The trained model can serve as the foundation for a fare-estimation application or deployment system.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

## Project Workflow

Data Loading → Data Validation → Data Cleaning → Exploratory Data Analysis → Feature Engineering → Model Training → Model Evaluation → Model Selection → Fare Prediction

## Repository Contents

- `Uber_Fare_Prediction_Analysis.ipynb` — Complete analysis, visualizations, feature engineering, model training, evaluation, and prediction workflow.

## Final Outcome

This project demonstrates an end-to-end machine learning workflow covering data validation, cleaning, exploratory analysis, feature engineering, model training, evaluation, model selection, and prediction.

## 👤 Author

**Chuks Spencer Eze**

Data Science & Machine Learning Enthusiast

The final XGBoost model was selected for its superior holdout performance and successfully generated a fare prediction for a new trip.
