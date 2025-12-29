# Handwritten Digit Recognition with Convolutional Neural Networks
This project explores the fundamentals of computer vision through handwritten digit recognition using convolutional neural networks (CNNs).

## Project Motivation
Handwritten digit recognition is a foundational computer vision task that illustrates how convolutional neural networks extract hierarchical visual features.
This project focuses on understanding the full CNN workflow rather than maximizing leaderboard performance.

## Dataset & Task Definition
The project uses the MNIST handwritten digit dataset.

- **Task type:** Multiclass image classification (0–9)
- **Input:** 28×28 grayscale images
- **Output:** Digit class label

## Methodology
An end-to-end CNN workflow was implemented to ensure correct data handling and model evaluation.
Image preprocessing included pixel normalization and reshaping to match convolutional input requirements.
Intermediate visual checks were performed to verify data integrity before model training.

The overall pipeline consisted of:
- Image normalization and tensor reshaping
- Visual inspection of preprocessed samples
- CNN model construction
- Training–validation split and learning curve analysis

## Model Architecture
A CNN model was contructed with the following components:

  - **Conv2D layers** to automatically learn local patterns such as edges and shapes
  - **MaxPooling2D layers** to progressively reduce spatial dimensions and computional cost
  - **Flatten layer** to convert 3D feature maps into a 1D feature vector representation
  - **Dense layers** to combine learned features for classification
  - **Dropout layer** to reduce overfitting and improve generalization

The final output layer uses softmax activation to classify images into 10 digit categories.

## Model Training & Evaluation
- The dataset was split into training and validation sets(80/20 split).
- The model was trained for 3 epochs using the Adam optimizer
- Sparse categorical cross-entropy was used as the loss function
- Model performance was evaluated using accuracy and loss on both training and validation sets
- Learning curves were plotted to analyze learning behavior and detect overfitting

## Results
During training, both training and validation accuracy increased steadily, while loss decreased across epochs.
The model achieved high validation accuracy, indicating good generalization on unseen data.

## Key Takeaways
This project strengthened practical understanding of:

- CNN-based image classification
- Image data preprocessing and normalization for deep learning
- Designing and training convolutional neural networks
- Interpreting training dynamics using accuracy and loss curves
- Regularization techniques such as dropout
