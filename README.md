🎙️ Speech Emotion Recognition (SER)

This project focuses on detecting human emotions from speech using deep learning. The model learns emotional cues such as tone, pitch, and energy from audio signals to classify them into predefined emotional states.

🧠 Overview

This repository implements a hybrid CNN + LSTM architecture for Speech Emotion Recognition (SER) on the RAVDESS Emotional Speech Audio Dataset
.
It extracts key acoustic features — MFCC, Chroma, and Mel Spectrograms — to capture both spectral and temporal characteristics of speech.

🏗️ Model Architecture

The SER model is composed of:

Feature Extraction

Mel-Frequency Cepstral Coefficients (MFCCs)

Chroma Features

Mel Spectrograms

Deep Learning Pipeline

CNN Layers → capture spatial feature maps from spectrograms.

LSTM Layers → model temporal dependencies in speech signals.

Dense Layers → classify emotion from learned features.

Output Classes (8 Emotions):

Neutral

Calm

Happy

Sad

Angry

Fearful

Disgust

Surprised

📊 Results
Metric	Score
Training Accuracy	98.3%
Validation Accuracy	86.5%
Best Validation Loss	0.6761
Best Epoch (Early Stopping)	29 / 100

Early stopping was used to minimize overfitting by monitoring validation loss.

Model Insight:
The CNN effectively captures emotional nuances in spectrograms, while the LSTM models the time-series emotion flow, resulting in robust recognition performance.

🖼️ Visualizations

Training and validation metrics:

🚀 How to Run
1️⃣ Clone the Repository
git clone https://github.com/<your-username>/Speech-Emotion-Recognition.git
cd Speech-Emotion-Recognition

2️⃣ Create and Activate Environment
python -m venv venv
source venv/bin/activate  # Mac/Linux
.\venv\Scripts\activate   # Windows

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Run the Notebook

Open SER.ipynb in Jupyter or VS Code and execute all cells to:

Preprocess the dataset

Extract audio features

Train and evaluate the CNN+LSTM model

🧩 Tech Stack
Category	Tools
Language	Python
Deep Learning	TensorFlow, Keras
Audio Processing	Librosa
Data Handling	NumPy, Pandas
Visualization	Matplotlib, Seaborn
Dataset	RAVDESS
📁 Project Structure
Speech-Emotion-Recognition/
│
├── SER.ipynb                  # Main Jupyter notebook
├── requirements.txt           # Dependencies
├── README.md                  # Documentation
├── data/                      # Audio dataset (RAVDESS)
├── features/                  # Extracted MFCCs and spectrograms
└── models/                    # Saved model weights

🧩 Future Improvements

Integrate attention mechanisms to enhance temporal feature learning

Experiment with transformer-based architectures (Wav2Vec2, HuBERT)

Build a Streamlit app for real-time emotion detection