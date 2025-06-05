# Multimodal Object Prediction Model - Deep Learning Approach (TensorFlow)

## Project Overview

This project is a deep learning model based on multimodal data, specifically designed to predict the status or grade of objects. The model integrates numerical and image features using the TensorFlow deep learning framework to achieve precise object classification.

## Model Features

- **Multimodal Fusion**: Simultaneous processing of numerical and image data to enhance prediction accuracy
- **Automated Feature Extraction**: Automatically extracts key features via image preprocessing
- **High-Accuracy Classification**: Utilizes TensorFlow models to classify objects into different levels
- **Visualization Analysis**: Provides visualizations for feature importance and sensitivity analysis

## System Requirements

- Python 3.8
- Required dependencies are listed in the `requirements.txt` file

## Installation Guide

1. Clone the repository locally:

```bash
git clone https://github.com/qwerfgb/Level-Of-Research-Object-Prediction-Model-TensorFlow.git
cd Level-Of-Research-Object-Prediction-Model-TensorFlow
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

## Data Input

The model requires two types of input data, both in Excel format:

1. **Numerical Feature Data**: Contains quantitative indicators related to the objects
2. **Image Feature Data**: Extracted from raw images using `data/PreprocessImage.py`

### Image Preprocessing Pipeline

Raw image data should be organized into separate folders based on object levels, with folder names representing class labels. Use `data/PreprocessImage.py` to extract image features:

1. Read images from labeled folders
2. Extract image features
3. Save features to an Excel file for model input

## Project Structure

```
Level-Of-Research-Object-Prediction-Model-TensorFlow/
│
├── data/                          # Data processing module
│   ├── __init__.py                # Initialization file
│   └── PreprocessImage.py         # Image feature extraction script
│
├── model/                         # Model definition module
│   ├── __init__.py                # Initialization file
│   └── FunctionalAPI.py           # TensorFlow classification model
│
├── README.md                      # Project documentation
└── requirements.txt               # Dependency list
```

## Output Results

Upon training completion, the model will generate the following outputs:

1. Training and validation accuracy and loss curves
2. Detailed classification report (accuracy, precision, recall, F1-score)
3. Feature importance rankings and visualization charts
4. Feature sensitivity analysis

## Notes

- Python version must be 3.8
- All required dependencies are listed in the `requirements.txt` file
- During preprocessing, images must be organized into folders according to their corresponding object levels
- Extracted feature Excel files must conform to the expected input format
- Label values should be integers from 1 to n, indicating the different object levels
