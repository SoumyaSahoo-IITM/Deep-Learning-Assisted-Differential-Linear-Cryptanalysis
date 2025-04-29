# Supplementary Material for "Deep Learning Assisted Differential-Linear Cryptanalysis: A Study on Salsa, ChaCha \& Forr\'o"

## Overview
This repository contains the supplementary material for the paper titled *"Deep Learning Assisted Differential-Linear Cryptanalysis: A Study on Salsa, ChaCha \& Forr\'o."* 

The models are implemented using the Google Colab  with a T4 GPU.

## Directory Structure
- **Salsa/**
  - `salsa_dataset.ipynb`: To create dataset for differential model. 
  - `salsa_diff_model_linear_data.ipynb`: For training the differential model and filtering the data needed for linear model .
  - `salsa_encryption.ipynb`: Encryption function.
  - `salsa_linear_model.ipynb`: For training the linear model.
  
- **ChaCha/**
  - `chacha_dataset.ipynb`: To create dataset for differential model. 
  - `chacha_diff_model_linear_data.ipynb`: For training the differential model and filtering the data needed for linear model .
  - `chacha_encryption.ipynb`: Encryption function.
  - `chacha_linear_model.ipynb`: For training the linear model.
  
- **Forro/**
  - `forro_dataset.ipynb`: To create dataset for differential model. 
  - `forro_diff_model_linear_data.ipynb`: For training the differential model and filtering the data needed for linear model .
  - `forro_encryption.ipynb`: Encryption function.
  - `forro_linear_model.ipynb`: For training the linear model.
  
- **Data/**
  - `Diff_salsa_100000_3round.csv`: Dataset generated for training the differential model of Salsa. 
  - `lin_filtered_data_salsa.csv`:  Filtered dataset needed for training linear model of Salsa.
  
  - `Diff_chacha_100000_2round.csv`: Dataset generated for training the differential model of ChaCha. 
  - `lin_filtered_data_chacha.csv`:  Filtered dataset needed for training linear model of ChaCha.
  
  - `Diff_forro_100000_2round.csv`: Dataset generated for training the differential model of forro. 
  - `lin_filtered_data_forro.csv`:  Filtered dataset needed for training linear model of forro.






## Requirements
- [Google Colab](https://colab.research.google.com/): You need to use Google Colab to run the neural models. We have used Google Colab T4 GPU for our neural models.

## Usage


1. **Running the Models**:
   To run our neural models, save the files for a specific cipher in Google Drive and then open them in a new notebook in Google Colab:

   **For example, to run the Salsa model:**
   - Open `salsa_dataset.ipynb` and run the code using T4 GPU. The code will generate a dataset `Dataset_salsa_100000_3round.csv` and it will be saved in Google Drive itself. 
   - Open `salsa_diff_model_linear_data.ipynb` and run. It will call the generated dataset and train the differential model and depending the accuracy of the differential model, it will generate the required the dataset for linear model. Download the generated linear dataset and save it in Google Drive.
   - Open `salsa_linear_model.ipynb` and run. It will call the linear dataset and train the linear model. 
 

2. **Modifying Parameters**:  
    You can modify the hyperparameters in the models to test different configurations.
