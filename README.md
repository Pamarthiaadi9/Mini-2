# Emotion Recognition from EEG with LSTM & Transformer
This project deploys a strong deep learning model for emotion classification based on EEG signals. It leverages the strength of LSTM networks and multi-head self-attention Transformers to classify emotions into three categories: positive, negative, and neutral. The model is 97.89% accurate, demonstrating its ability to capture both short-term and long-range patterns in brain activity.

# Overview
Emotions are central to human-computer interaction and cognitive computing. Facial expression or voice-based traditional emotion detection is not always accurate. EEG signals, representing electrical activity in the brain, give more insight into the emotional state of a person.

# This project suggests a hybrid deep model that:

Employes LSTM to learn temporal (time) patterns.

Employes Transformers to learn global contextual features.

Categorizes EEG signals into positive, neutral, or negative emotions with high accuracy.
# The data is from Kaggle and contains:

2132 EEG recordings

2549 features per recording

EEG recordings from 2 subjects (1 male and 1 female)

Recorded while viewing emotional video clips

Raw signals preprocessed to derive:

Time-domain features (mean, std, RMS, etc.)

Frequency-domain features (PSD, dominant freq, etc.)

Time-frequency features (wavelet, STFT)

EEG recorded at 150Hz with 32 channels.
# Model Architecture
1. LSTM Layer
Captures local temporal features

Uses return_sequences=True for sequence output

2. Transformer Block
Applies Multi-Head Self-Attention to LSTM output

Learns global relationships between EEG features

Includes:
Attention masking

Feed Forward Neural Network (FFN)

Residual connections

Layer normalization

3. Global Average Pooling
Reduces transformer output to a compact feature vector

4. Dense Layer + Softmax
Final classification layer

# Outputs probabilities for each emotion class

# Results
Metric	Value

Accuracy	97.89%

Precision	97.85%

Recall	97.87%

F1-Score	97.85%

Cohen’s Kappa	96.83%
