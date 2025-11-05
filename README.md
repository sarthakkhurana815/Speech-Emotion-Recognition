# Speech Emotion Recognition (SER)
This project uses a deep learning model to classify emotions from audio speech files. It is built with TensorFlow/Keras and uses a hybrid **CNN+LSTM architecture**.

- **Model**: A 2D Convolutional Neural Network (CNN) for feature extraction from spectrograms, followed by a Long Short-Term Memory (LSTM) network to understand the sequence and context of the audio.
- **Dataset**: [RAVDESS Emotional Speech Audio](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio). The model was trained on 2,880 audio files covering 8 distinct emotions.
- **Features**: MFCC, Chroma, and Mel Spectrograms.
- **Final Result**: The model achieved a **86.5% validation accuracy** after implementing Early Stopping to prevent overfitting.

---

## 📈 Results

The model was trained for 100 epochs with an Early Stopping callback monitoring validation loss. The training stopped automatically at epoch 29, which had the best performance.

| Metric | Score |
| --- | --- |
| **Validation Accuracy** | 86.5% |
| **Training Accuracy** | 98.3% |
| **Best Validation Loss** | 0.6761 |

The gap between the training and validation accuracy indicates some overfitting (common for this dataset size), which was successfully managed by the Early Stopping callback to save the best-generalized model.

![Training Accuracy and Loss Plots](image_5fac41.jpg)

---

## 🚀 How to Run

**1. Create the Environment:**
Create and activate a Python virtual environment.
```bash
python -m venv venv
source venv/bin/activate  # On Mac/Linux
.\venv\Scripts\activate    # On Windows