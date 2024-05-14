# Fetal Health Classification

## Abstract

Classify fetal health in order to prevent child and maternal mortality.

## Context

Reduction of child mortality is reflected in several of the United Nations' Sustainable Development Goals and is a key indicator of human progress. The UN expects that by 2030, countries will end preventable deaths of newborns and children under 5 years of age, with all countries aiming to reduce under‑5 mortality to at least as low as 25 per 1,000 live births.

Parallel to the notion of child mortality is, of course, maternal mortality, which accounted for 295,000 deaths during and following pregnancy and childbirth (as of 2017). The vast majority of these deaths (94%) occurred in low-resource settings, and most could have been prevented.

In light of what was mentioned above, Cardiotocograms (CTGs) are a simple and cost-accessible option to assess fetal health, allowing healthcare professionals to take action to prevent child and maternal mortality. The equipment itself works by sending ultrasound pulses and reading its response, thus shedding light on fetal heart rate (FHR), fetal movements, uterine contractions, and more.

## Data

This dataset contains 2126 records of features extracted from Cardiotocogram exams, which were then classified by three expert obstetricians into three classes:

- Normal
- Suspect
- Pathological

## Project Overview

The goal of this project is to develop a classification model that can accurately predict the health status of a fetus based on features extracted from Cardiotocogram exams. The classification will help in early detection and prevention of potential health risks for both the child and the mother.

## Steps to Follow

### 1. Load and Understand the Dataset

- Load the dataset using pandas.
- Display the first few rows to understand the structure of the data.

### 2. Data Preprocessing

- Check for missing values.
- Define the feature matrix `X` and the target vector `y`.
- Split the dataset into training and testing sets.

### 3. Exploratory Data Analysis (EDA)

- Perform basic statistical analysis.
- Visualize data distribution and relationships using seaborn and matplotlib.

### 4. Feature Engineering

- Standardize features using `StandardScaler`.

### 5. Model Selection and Training

- Initialize and train a Logistic Regression model.
- Make predictions and evaluate model performance using accuracy, precision, recall, and F1-score.

### 6. Model Evaluation and Fine-Tuning

- Use Grid Search for hyperparameter tuning.
- Perform cross-validation to validate the model.

## Files

- `fetal_health.csv`: The dataset used for this project.
- `fetal_health.ipynb`: Jupyter Notebook containing the entire code for data preprocessing, EDA, model training, and evaluation.
- `deploy.py`: Flask application for deploying the model.
- `model.pkl`: Trained model saved as a pickle file.
- `requirements.txt`: List of dependencies required for the project.

## Usage

### Running the Jupyter Notebook

1. Open `fetal_health.ipynb` in Jupyter Notebook or JupyterLab.
2. Execute the cells step by step to preprocess data, train the model, and evaluate it.

### Deploying the Model with Flask

1. Ensure you have `model.pkl` and `deploy.py` in the same directory.
2. Install dependencies using:

```python
pip install -r requirements.txt
```

3. Run the Flask application:

```python
python app.py
```

4. The Flask server will start, and you can make POST requests to the `/predict` endpoint to get predictions.

## Dependencies

- Flask==2.0.3
- scikit-learn==1.0.2
- pandas==1.4.2
- numpy==1.22.3

## License

This project is licensed under the MIT License.

## Acknowledgements

Special thanks to the creators of the dataset and the United Nations for their efforts in improving child and maternal health worldwide.

Ayres de Campos et al. (2000) SisPorto 2.0 A Program for Automated Analysis of Cardiotocograms. J Matern Fetal Med 5:311-318 ([link](https://onlinelibrary.wiley.com/doi/10.1002/1520-6661%28200009/10%299:5%3C311::AID-MFM12%3E3.0.CO;2-9))
