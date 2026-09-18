# User Behavior Analytics End-to-End Project

<div align="center">

  <img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/FastAPI-0.100%2B-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/scikit--learn-ML-FF9900?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
  <img src="https://img.shields.io/badge/Status-ML%20Project-4B8BBE?style=for-the-badge" alt="Project Status" />

  <h3>Predicting user behavior with data-driven insights and deployed ML inference</h3>

</div>

An end-to-end machine learning project that analyzes user behavior using app and device usage data, builds predictive features, trains a classification model, and serves predictions through a FastAPI web application.

## Overview

This repository demonstrates a complete ML workflow from raw data to deployment:

- Data cleaning and preprocessing
- Exploratory data analysis (EDA)
- Feature engineering and feature selection
- Model training and evaluation
- Model persistence and reuse
- REST API deployment with FastAPI
- Frontend interaction for prediction input/output

## Project Goals

The project aims to classify or predict user behavior patterns based on metrics such as:

- device model
- operating system
- app usage time
- screen-on time
- battery drain
- number of apps installed
- data usage

## Tech Stack

- Python
- FastAPI
- scikit-learn
- pandas
- NumPy
- Plotly
- Seaborn
- Matplotlib
- HTML/CSS/JavaScript

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   │   └── user_behavior_dataset.csv
│   └── processed/
│       ├── 01_clean_data.csv
│       ├── 03_feature_engineering.csv
│       ├── 04_feature_selection.csv
│       └── final_data.csv
├── deployment/
│   ├── main.py
│   ├── static/
│   │   ├── css/
│   │   └── js/
│   └── templates/
│       └── index.html
├── modeling/
│   └── models.py
├── notebook/
│   ├── 00_exploration.ipynb
│   ├── 01_clean data.ipynb
│   ├── 02_analytics.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_feature_selection.ipynb
│   ├── 05_preprocessing.ipynb
│   ├── 06_test_models.ipynb
│   └── 07_test_final_model.ipynb
├── reports/
├── saved-model/
├── script/
│   ├── cleaning.py
│   ├── config.py
│   ├── feature.py
│   ├── feature_selection.py
│   ├── preprocessing.py
│   ├── saving.py
│   └── visualization.py
├── requirements.txt
├── setup.py
├── README.md
└── .gitignore
```

## Pipeline Overview

The project follows this workflow:

1. Load raw user behavior dataset
2. Clean and normalize the data
3. Engineer additional behavioral features
4. Encode categorical fields
5. Select important features
6. Train a classification model
7. Evaluate model performance
8. Save the trained model
9. Serve predictions via FastAPI
10. Provide a frontend interface for user interaction

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/itsthemaverick/ML-End-2-End
cd "User Behavior"
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
```

On Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Run the Application

Start the FastAPI app:

```bash
uvicorn deployment.main:app --reload
```

Then open the app in your browser at:

```text
http://127.0.0.1:8000
```

## API Usage

The app exposes a prediction endpoint at:

```text
POST /predict
```

Example request body:

```json
{
  "f1": 12,
  "f2": 1,
  "f3": 180,
  "f4": 5,
  "f5": 250,
  "f6": 16,
  "f7": 800
}
```

This request is mapped to the model features and returns a predicted class.

## Model Notes

The project stores model artifacts in the `saved-model/` folder and uses a serialized model for inference. Feature engineering logic is also repeated at prediction time to keep input data consistent with the training pipeline.

## Notebooks

The notebooks under `notebook/` are useful for exploring the data, testing features, and validating different model approaches during development.

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Commit and push
5. Open a pull request

## License

This project does not currently include a license file. If you plan to share it publicly, consider adding an appropriate license such as MIT.

## Final Note

This repository is a practical example of an end-to-end ML deployment workflow, combining data science, model training, and web-based inference in a single project structure.
"# ML-End-2-End" 
