# 🎙️ Speech Emotion Recognition (SER)

This project focuses on **detecting human emotions from speech** using deep learning. The model learns emotional cues such as tone, pitch, and energy from audio signals to classify them into predefined emotional states.

---

## 🧠 Overview

This repository implements a **hybrid CNN + LSTM architecture** for **Speech Emotion Recognition (SER)** on the [RAVDESS Emotional Speech Audio Dataset](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio).  
It extracts key acoustic features — **MFCC**, **Chroma**, and **Mel Spectrograms** — to capture both spectral and temporal characteristics of speech.

---

## 🏗️ Model Architecture

The SER model is composed of:

1. **Feature Extraction**
   - Mel-Frequency Cepstral Coefficients (MFCCs)
   - Chroma Features
   - Mel Spectrograms

2. **Deep Learning Pipeline**
   - **CNN Layers** → capture spatial feature maps from spectrograms.  
   - **LSTM Layers** → model temporal dependencies in speech signals.  
   - **Dense Layers** → classify emotion from learned features.  

3. **Output Classes (8 Emotions):**
   - Neutral  
   - Calm  
   - Happy  
   - Sad  
   - Angry  
   - Fearful  
   - Disgust  
   - Surprised  

---

## 📊 Results

| Metric | Score |
| --- | --- |
| **Training Accuracy** | 98.3% |
| **Validation Accuracy** | 86.5% |
| **Best Validation Loss** | 0.6761 |
| **Best Epoch (Early Stopping)** | 29 / 100 |

Early stopping was used to minimize overfitting by monitoring validation loss.

**Model Insight:**  
The CNN effectively captures emotional nuances in spectrograms, while the LSTM models the time-series emotion flow, resulting in robust recognition performance.

---

## 🖼️ Visualizations

Training and validation metrics:

<p align="center">
  <img src="images/training_accuracy_loss.png" alt="Training Accuracy and Loss" width="70%"/>
</p>


## 🚀 How to Run

```bash
🧩 Step 1️⃣ — Clone the Repository
---------------------------------
git clone https://github.com/sarthakkhurana815/Speech-Emotion-Recognition.git
cd Speech-Emotion-Recognition


🧩 Step 2️⃣ — Create and Activate Environment
---------------------------------------------
python -m venv venv
source venv/bin/activate    # Mac/Linux
.\venv\Scripts\activate     # Windows


🧩 Step 3️⃣ — Install Dependencies
---------------------------------
pip install -r requirements.txt


🧩 Step 4️⃣ — Run the Notebook
------------------------------
# Open the Jupyter Notebook
jupyter notebook SER.ipynb

# Or open it directly in VS Code
# Run all cells to:
# - Preprocess the dataset
# - Extract audio features
# - Train and evaluate the CNN+LSTM model


🧩 Tech Stack
--------------
Category           Tools
-------------------------------------
Language           Python
Deep Learning      TensorFlow, Keras
Audio Processing   Librosa
Data Handling      NumPy, Pandas
Visualization      Matplotlib, Seaborn
Dataset            RAVDESS


📁 Project Structure
--------------------
Speech-Emotion-Recognition/
│
├── SER.ipynb                  # Main Jupyter notebook
├── requirements.txt           # Dependencies
├── README.md                  # Documentation
├── data/                      # Audio dataset (RAVDESS)
├── features/                  # Extracted MFCCs and spectrograms
└── models/                    # Saved model weights


🌱 Future Improvements
----------------------
1️⃣ Integrate attention mechanisms to enhance temporal feature learning
2️⃣ Experiment with transformer-based architectures (Wav2Vec2, HuBERT)
3️⃣ Build a Streamlit app for real-time emotion detection
