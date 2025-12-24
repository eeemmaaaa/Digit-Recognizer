# Digit-Recognizer (MNIST)
Learn computer vision fundamentals with the famous MNIST data.

## Project Overview
This project builds a Convolutional Neural Network(CNN) to identify digits(0-9) from the dataset of handwritten images.
The goal is to practice a complete deep learning workflow, including data preprocessing, model training, training, validation, and performance analysis.

## Dataset
The dataset comes from the Kaggle Digit Recognizer competition and is based on the MNIST dataset of handwritten images.

- Training set: includes images and corresponding digit labels
- Test set: unlabeled images used for final prediction submission

## Data Preprocessing
The following preprocessing steps were applied before model training:

- Separated features and labels to prevent data leakage
- Normalized pixel values by dividing by 255.0
- Reshape input data into '(28, 28, 1)' to match CNN input requirements
- Visualized sample images to verify preprocessing correctness

## Model Architecture
A CNN model was contructed with the following components:

  - **Conv2D layers** to automatically learn local patterns such as edges and shapes
  - **MaxPooling2D layers** to reduce spatial dimensions and computional cost
  - **Flatten layer** to convert 3D feature maps into a 1D feature vector
  - **Dense layers** to combine learned features and perform classification
  - **Dropout layer** to reduce overfitting and improve generalization

The final output layer uses softmax activation to classify images into 10 digit categories.

## Model Training & Validation
- The dataset was split into training and validation sets(80/20 split).
- The model was trained for 3 epochs using the Adam optimizer
- Sparse categorical cross-entropy was used as the loss function
- Model performance was evaluated using accuracy and loss on both training and validation sets
- Training curves were plotted to analyze learning behavior and detect overfitting

## Results
During training, both training and validation accuracy increased steadily, while loss decreased across epochs.
The model achieved high validation accuracy, indicating good generalization on unseen data.

## What I Learned
Through this project, I gained hands-on experience with:

- CNN-based image classification
- Image data preprocessing and normalization
- Designing and training convolutional neural networks
- Interpreting accuracy and loss curves during training
- Understanding overfitting and regularization techniques such as dropout
