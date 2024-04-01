# voice-gender-recognition
## Project Overview

This project focuses on recognizing gender from voice recordings using machine learning techniques. It leverages signal processing to extract meaningful features from audio files, which are then used to train a RandomForestClassifier for gender classification. Key features include audio file conversion, noise reduction, and feature extraction.

## Installation

Ensure you have Python installed on your system. This project requires the following Python libraries:

- librosa
- noisereduce
- pydub
- scikit-learn

To install the required libraries, run:

``` python
pip install librosa noisereduce pydub scikit-learn
```

## Setup

1. Clone this repository to your local machine.

2. Ensure you have ffmpeg installed, as pydub uses it for audio format conversion.

## Usage

1. Mount Google Drive (if using Google Colab):
```python
from google.colab import drive
drive.mount('/content/drive')
```
2. Prepare Your Dataset: Place your .m4a voice recordings in two separate folders within your dataset directory - one for Males and one for Females.

3. Run the Feature Extraction and Model Training:

- Update the dataset_dir variable to point to your dataset's location.
- Execute the script to preprocess audio files, extract features, and train the RandomForest model.

## Features
- Audio Conversion: Converts .m4a files to .wav for consistent processing.
- Noise Reduction: Applies noise reduction to clean audio signals.
- Feature Extraction: Extracts a comprehensive set of features including MFCCs, Chroma, Mel-Spectrogram, Spectral Contrast, and Tonnetz.
- Dataset Balancing: Balances the dataset to ensure an even distribution of classes.
- Model Optimization: Uses RandomizedSearchCV to find optimal hyperparameters for the RandomForestClassifier.
- Evaluation: Evaluates the model on a test set and prints a classification report.

## Contributing
Contributions to this project are welcome! Here are some ways you can contribute:

Adding more feature extraction techniques.
Implementing alternative machine learning models.
Enhancing the noise reduction process.
To contribute, please fork the repository, make your changes, and submit a pull request.

## License
This project is open-source and available under the MIT License.



