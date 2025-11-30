# DS3000 Final Project — Flood Detection from Satellite Imagery (SEN12FLOOD)

## Group 3 — DS3000: Introduction to Machine Learning

**Members:**
- Raco Ahmed  
- Mohammed Sidahmed  
- Mikaail Sukkurwala  
- Tony Karunakkal  

## Project Overview

This project uses the **SEN12FLOOD** dataset to classify satellite image patches
as **flooded vs. non-flooded**. We apply both traditional machine learning models
and deep learning architectures to evaluate how well they detect flooded areas
from multi-spectral satellite imagery.

This repository is the official code submission for the DS3000 course project.

**Dataset link (Kaggle):**  
https://www.kaggle.com/datasets/rhythmroy/sen12flood-flood-detection-dataset

## Repository Structure

- `notebook/main.ipynb`  
  Main project notebook. Contains:
  - data loading & preprocessing
  - baseline models (Logistic Regression, KNN, Decision Tree, Random Forest)
  - neural network models (MLP and CNN)
  - evaluation (accuracy, precision, recall, F1, ROC-AUC & confusion matrices)

- `results/`  
  Saved figures and tables generated from the notebook (e.g., model comparison plots).

- `requirements.txt`  
  Python dependencies used in this project.

> **Note:** The SEN12FLOOD dataset is **not** stored in this repository due to size.
> It must be downloaded separately from Kaggle.

## How to Run the Notebook

1. Open the notebook in Google Colab:
   - Go to **Google Colab → File → Open notebook → GitHub**
   - Enter this repository URL:  
     `https://github.com/racoahmed/DS3000-Final-Project`
   - Open `notebook/main.ipynb`

2. Download and unzip the SEN12FLOOD dataset into your Google Drive.

3. **Mount Google Drive and set the dataset path**

   In the first code cell of the notebook, run:

   python
   from google.colab import drive
   drive.mount('/content/drive')

   Make sure the SEN12FLOOD data is located at:
   `/content/drive/MyDrive/DS3000 Final Project/archive/SEN12FLOOD`

   If it is in a different folder, update the configuration line in the notebook:
   `DATASET_PATH = '/content/drive/MyDrive/DS3000 Final Project/archive/SEN12FLOOD`

4. Run all cells (**Runtime → Run all**). The notebook will train:
   - Logistic Regression
   - KNN (with k-tuning)
   - Decision Tree
   - Random Forest
   - MLP
   - CNN

   and output performance metrics and plots.

> **Please view `notebook/main.ipynb` for the implementation of all models and all figures/tables/results.**
