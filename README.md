# 🎸 Bringing AI to Music: Classifying Guitar Chords with a Convolutional Neural Network (CNN)! 🎶
The objective of this model is creating a CNN model that helps classify different guitar chords from this kaggle dataset: https://www.kaggle.com/datasets/fabianavinci/guitar-chords-v2

# 📊 Pipeline Overview
1. Audio Data Preprocessing:
Converted audio files to a consistent format and sample rate using librosa and ffmpeg.

Extracted MFCC (Mel-frequency Cepstral Coefficients) features, which are crucial for capturing the spectral properties of audio signals.

Converted the audio files to spectrogram in order to feed them to the CNN model.
2. Model Architecture:
   
Built a Convolutional Neural Network (CNN) using TensorFlow and Keras.

The model includes layers for feature extraction and classification, leveraging the CNN’s ability to identify patterns in MFCC data.
3. Model Training and Evaluation:

Trained the CNN on labeled datasets with guitar chords.

Achieved an impressive 95% validation accuracy, demonstrating the model’s ability to distinguish between chords like Am, C, G, and more. And 94% accuracy on testing dataset.

# Model Architecture
- Data Augmentation and Generators:
   Uses ImageDataGenerator to preprocess spectrogram images for training, validation, and testing.
   Rescales image pixel values and splits the training data into training and validation subsets.
- Builds a CNN model with three convolutional layers, max-pooling layers, and a dense layer for feature extraction and classification.
   Includes dropout regularization to reduce overfitting.
   Configures the output layer to classify into the number of chord classes based on the training dataset.
- Model Compilation:
   Compiles the model with the Adam optimizer, sparse categorical cross-entropy loss, and accuracy as the evaluation metric.
   Utilizes a lower learning rate for improved training stability.
