# Dysarthria Classification with CNN

This repository contains the notebook implementation for **Dysarthria Classification** using **Convolutional Neural Networks (CNN)**. The project involves preprocessing raw audio files, converting them into log-mel spectrograms, training a CNN model for classification, and evaluating the model's performance. The dataset used in this project, along with the code (notebook), is also available on [Kaggle](https://www.kaggle.com/datasets/mirabuhuraira/).

## Dataset

The dataset used in this project is downloaded from the official Torgo database. The repository contains the following datasets:

1. **Organized Audio Files (torgodataset(Organized))**: This dataset organizes the audio files into two main folders: *Male* and *Female*, each containing subfolders for *Dysarthria* and *NotDysarthria*. The folders are further divided into session folders, each containing files captured with arraymic and headmic microphones.

2. **Log-mel Spectrograms (torgoimages)**: The log-mel spectrograms of the audio files from the previous datasets are available in this folder. There are two subfolders, one for patients with dysarthria and another for those without.

3. **Dataset CSV File**: The dataset also includes a **CSV file** containing metadata for the audio files. This file has four columns:
   - **`gender`**: Gender of the speaker (`M` or `F`).
   - **`mictype`**: Type of microphone used (`headmic` or `arraymic`).
   - **`path`**: File path to the corresponding audio sample.
   - **`label`**: Classification label (`Dysarthria` or `NotDysarthria`).

    You can use this CSV file to generate **spectrograms, MFCCs, and waveform plots** for classification using CNN.

The datasets can be downloaded from the [Kaggle page](https://www.kaggle.com/datasets/mirabuhuraira).

## Model

The model used in this project is a **Convolutional Neural Network (CNN)**, which is effective for analyzing spatial hierarchies in images. The network learns features from the log-mel spectrograms and classifies the audio samples as either Dysarthria or NotDysarthria.

### Architecture:
- **Input**: Log-mel spectrogram images
- **Convolutional Layers**: Several convolutional layers with ReLU activations
- **Fully Connected Layers**: Dense layers for final classification
- **Output**: Binary classification (Dysarthria vs. NotDysarthria)

## Evaluation

After training the model, it is evaluated using various classification metrics:

- **Accuracy**: Measures the percentage of correct predictions
- **Precision**: Measures the number of correct positive predictions divided by the total predicted positives
- **Recall**: Measures the number of correct positive predictions divided by the total actual positives
- **F1-Score**: The harmonic mean of precision and recall
