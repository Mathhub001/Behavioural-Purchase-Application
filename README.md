# Behavioural-Purchase-Application

README: Backend and Frontend for Purchase Prediction
Backend: Model Training and Saving
This script preprocesses the dataset, trains a Random Forest model, and saves both the model and the scaler for use in the frontend.

Dataset:

The dataset (PurchaseData.csv) contains features:
Age: Numeric (e.g., 23, 35).
Gender: Categorical (Male, Female).
Income: Numeric (e.g., 45000, 80000).
Browsing_Hours: Numeric (e.g., 1.5, 3.0).
Cart_Abandonment: Categorical (Yes, No).
Purchase: Target variable (0 = Not Purchased, 1 = Purchased).
Preprocessing:

Categorical variables (Gender, Cart_Abandonment) are one-hot encoded.
Missing values are dropped.
Features are scaled using StandardScaler.
Model Training:

A RandomForestClassifier is trained on 70% of the data.
Performance metrics include accuracy, confusion matrix, and classification report.
Saving Artifacts:

Trained model: random_forest_model.joblib
Scaler: scaler.joblib
Run Instructions:

Place PurchaseData.csv in the script directory.
Execute the script to train and save the model:
python backend.py



Frontend: Tkinter GUI for Predictions
This Tkinter-based GUI collects user input, preprocesses it, and makes predictions using the saved model.

Inputs:

Age: Numeric (e.g., 23, 35).
Gender: Dropdown (Male, Female).
Income: Numeric (e.g., 45000).
Browsing Hours: Numeric (e.g., 2.5).
Cart Abandonment: Dropdown (Yes, No).
Workflow:

Inputs are collected through text fields and dropdown menus.
Data is preprocessed using the saved scaler.joblib.
The random_forest_model.joblib predicts whether a purchase was made (Purchased or Not Purchased).
Run Instructions:

Ensure random_forest_model.joblib and scaler.joblib are in the script directory.
Run the GUI script:
python frontend.py
GUI Components:

Input fields: For numeric and categorical data.
Dropdowns: For Gender and Cart Abandonment.
Predict button: Generates a prediction and displays it in a pop-up.

Dependencies
Install required Python libraries:

pip install numpy pandas scikit-learn joblib tkinter

File Structure
bash
Copy code
project/
├── backend.py                 # Model training script
├── frontend.py                # Tkinter GUI script
├── PurchaseData.csv           # Dataset
├── random_forest_model.joblib # Trained model
├── scaler.joblib              # Trained scaler
