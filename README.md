# ❤️ Heart Disease Prediction AI

<img src="docs/assets/heart_banner.png" alt="Heart AI Banner" width="100%">

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![Flask](https://img.shields.io/badge/Flask-Web_App-lightgrey.svg)](https://flask.palletsprojects.com/)
[![Accuracy](https://img.shields.io/badge/Model_Accuracy-88.33%25-brightgreen.svg)]()

This project leverages **Advanced Machine Learning** to predict the likelihood of heart disease in patients based on 14 medical attributes. Using the **Random Forest** algorithm, we achieve high-precision results to aid in early diagnosis and health management.

---

## 🚀 Project Overview

Heart disease remains one of the leading causes of mortality globally. This AI-powered solution analyzes critical health metrics to provide a rapid risk assessment. The study was conducted on the UCI Heart Disease dataset, focusing on 14 specific clinical attributes.

### 📋 Data Dictionary
| Attribute | Medical Description |
|:---|:---|
| **age** | Age of the patient (years) |
| **sex** | Gender (1=Male, 0=Female) |
| **cp** | Chest pain type (Typical, Atypical, Non-anginal, Asymptomatic) |
| **trestbps** | Resting blood pressure (mm Hg) |
| **chol** | Serum cholesterol (mg/dl) |
| **fbs** | Fasting blood sugar > 120 mg/dl (1=True, 0=False) |
| **restecg** | Resting ECG results |
| **thalach** | Maximum heart rate achieved |
| **exang** | Exercise induced angina (1=Yes, 0=No) |
| **oldpeak** | ST depression induced by exercise |
| **slope** | Slope of peak exercise ST segment |
| **ca** | Number of major vessels (0-3) colored by flourosopy |
| **thal** | Thalassemia (Normal, Fixed defect, Reversable defect) |
| **num** | Target: Diagnosis of heart disease (0=Healthy, 1-4=Disease) |


### 🌟 Key Features
- **High-Precision Prediction**: Achieves **88.33% accuracy** in binary classification (Sick vs. Healthy).
- **Comprehensive Feature Analysis**: Identifies top risk factors like Chest Pain type (cp) and Thalassemia (thal).
- **Interactive Web Interface**: A sleek Flask-based UI for real-time patient data input.
- **Robust Preprocessing**: Handles missing values and data normalization for reliable results.

---

## 📊 Performance & Insights

![Accuracy Dashboard](docs/assets/accuracy_dashboard.png)

The project involved training a **Random Forest Classifier** with hyperparameter tuning (optimizing the number of trees). Data preprocessing included handling hidden missing values (marked as '?') and feature scaling via `StandardScaler`.

* **Raw Dataset**: 303 patients
* **Cleaned Dataset**: 297 patients
* **Test Split**: 20% (60 patients)


| Classification Type | Model Used | Accuracy | Precision | Recall | F1-Score |
|:---:|:---:|:---:|:---:|:---:|:---:|
| **Binary (Healthy/Sick)** | **Random Forest** | **88.33%** | 0.86 | 0.88 | 0.87 |
| **Multi-class (Risk levels)** | Random Forest | 60.00% | 0.54 | 0.60 | 0.56 |

### 🔍 Top Risk Indicators
Based on our model's **Feature Importance** analysis, these are the strongest predictors:

![Feature Importance Chart](docs/assets/feature_importance.png)

1. **Chest Pain type (cp)**: Often the highest indicator of clinical risk.
2. **Number of major vessels (ca)**: Crucial diagnostic metric from fluoroscopy.
3. **Thalassemia (thal)**: A significant genetic factor in our dataset.

---

## 🔧 Installation & Usage

### 1. Environment Setup
```bash
# Clone the repository
git clone <repository-url>
cd ML-Heart-Disease-Prediction

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Running the Analysis
To dive into the research and model training pipeline:
```bash
jupyter notebook heart_disease_analysis.ipynb
```

### 3. Launching the Web App
```bash
python app.py
```
Visit `http://localhost:5000` to interact with the prediction engine.

---

## 📂 Project Structure

```text
ML-Heart-Disease-Prediction/
├── assets/                  # Images and banners
├── data/                    # Dataset (heart_disease.csv)
├── models/                  # Saved .pkl model files
├── templates/               # Web UI components
├── heart_disease_analysis.ipynb  # Core ML research
└── app.py                   # Flask Application
```

## 🛠️ Built With
- **Algorithms**: Random Forest, Logistic Regression
- **Libraries**: Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
- **Web Framework**: Flask

---

> [!NOTE]
> This tool is for educational purposes and should not be used as a substitute for professional medical advice.
