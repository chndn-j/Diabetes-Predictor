# 🩺 Diabetes Prediction Model

A machine learning web app that predicts whether a patient is likely to have diabetes, based on key diagnostic measurements. The app is built with **Streamlit** and served through a trained scikit-learn model.

## Overview

This project trains a classification model on the Pima Indians Diabetes dataset and wraps it in a simple, interactive Streamlit interface. Users enter a patient's medical details and get an instant prediction along with a confidence score.

## Features

- Interactive web form for entering patient data
- Instant diabetes prediction (Diabetic / Not Diabetic)
- Prediction confidence percentage
- Clean, centered UI built with Streamlit

## Project Structure

```
Diabetes-Prediction-Model/
├── Diabetes_Prediction.ipynb   # Notebook: data exploration, training, and model export
├── app.py                      # Streamlit web app for making predictions
├── diabetes.csv                # Dataset used for training
├── diabetes_model.pkl          # Trained model (saved with joblib)
└── README.md
```

## Dataset

The model is trained on the **Pima Indians Diabetes Dataset**, which includes the following features:

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| Blood Pressure | Diastolic blood pressure (mm Hg) |
| Skin Thickness | Triceps skinfold thickness (mm) |
| Insulin | 2-hour serum insulin (mu U/ml) |
| BMI | Body mass index |
| Diabetes Pedigree Function | Likelihood of diabetes based on family history |
| Age | Age in years |

The target variable indicates whether the patient has diabetes (1) or not (0).

## How It Works

1. `Diabetes_Prediction.ipynb` loads and explores `diabetes.csv`, trains a classification model, and exports it as `diabetes_model.pkl` using `joblib`.
2. `app.py` loads the saved model and presents a Streamlit form where users can input the eight medical features.
3. On clicking **Predict Diabetes**, the app runs the input through the model and displays the result with a confidence score.

## Getting Started

### Installation

```bash
git https://github.com/chndn-j/Diabetes-Predictor.git
cd Diabetes-Prediction-Model
pip install streamlit numpy joblib scikit-learn pandas
```

### Run the App

```bash
streamlit run app.py
```

Then open the local URL shown in your terminal (usually `http://localhost:8501`).

## Usage

1. Launch the app.
2. Enter the patient's medical details: Pregnancies, Glucose, Blood Pressure, Skin Thickness, Insulin, BMI, Diabetes Pedigree Function, and Age.
3. Click **Predict Diabetes**.
4. View the result — 🔴 *Likely Diabetic* or 🟢 *Not Diabetic* — along with the model's confidence percentage.

## Retraining the Model

To retrain or experiment with the model, open `Diabetes_Prediction.ipynb` in Jupyter and re-run the notebook. It will regenerate `diabetes_model.pkl`, which `app.py` automatically picks up.

## Disclaimer

This tool is built for educational and demonstration purposes only. It is **not** a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare provider for medical concerns.
