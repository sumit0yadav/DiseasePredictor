
---

# Medical Diagnosis System

This repository contains code for a Medical Diagnosis System that predicts diseases based on input symptoms. The system combines predictions from Support Vector Machine (SVM), Naive Bayes, and Random Forest classifiers to enhance accuracy.

## Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Usage](#usage)
- [Model Training](#model-training)
- [Prediction Function](#prediction-function)
- [Saved Models and Data](#saved-models-and-data)
- [License](#license)

## Introduction

This system uses machine learning models to predict diseases based on symptoms. The models include SVM, Naive Bayes, and Random Forest classifiers. The combined model offers more accurate predictions.

## Requirements

Ensure you have the necessary dependencies installed. You can install them using:

```bash
pip install numpy pandas scipy matplotlib seaborn scikit-learn joblib
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/medical-diagnosis-system.git
cd medical-diagnosis-system
```

2. Run the main script:

```bash
python main_script.py
```

3. Follow the instructions in the script to input symptoms and receive disease predictions.

## Model Training

The script includes code for training SVM, Naive Bayes, and Random Forest models. The training data is loaded from `Training.csv`, and models are evaluated using k-fold cross-validation.

## Prediction Function

The repository includes a prediction function, `predictDisease(symptoms)`, that takes a string of symptoms as input and returns predictions from individual models as well as the final combined prediction.

Example:

```python
predictions = predictDisease("Itching,Skin Rash,Nodal Skin Eruptions")
print(predictions)
```

## Saved Models and Data

Trained models (`final_rf_model.joblib`, `final_nb_model.joblib`, `final_svm_model.joblib`) and additional data (`data_dict.joblib`) are saved for future use. You can load them using joblib:

```python
import joblib

final_rf_model = joblib.load('final_rf_model.joblib')
final_nb_model = joblib.load('final_nb_model.joblib')
final_svm_model = joblib.load('final_svm_model.joblib')
data_dict = joblib.load('data_dict.joblib')
```

## License

This project is licensed under the [MIT License](LICENSE).

---

