# convolutional-neural-network-EMINST
# EMNIST Letter Classification Project

## Overview
This project explores various deep learning models for classifying letters in the EMNIST dataset, comparing performance with the MNIST dataset, and applying transfer learning to the Binary Alpha Digits dataset.

## Models and Results

### Base Models
1. Simple Dense Architecture (Francis Chollet)
   - EMNIST accuracy: 89%
   - MNIST accuracy: 98%

2. Simple MNIST ConvNet (Francis Chollet)
   - EMNIST accuracy: 93%
   - MNIST accuracy: 99%

### Custom Models

#### Model 1
- Architecture: 2 convolutional layers, flattening layer, fully connected layers
- Features: Data augmentation, BatchNormalization, MaxPooling
- Callbacks: TensorBoard, Early Stopping
- Validation Accuracy: 94.37%

#### Model 2
- Architecture: More Conv2D and Dense layers compared to Model 1
- No data augmentation
- Validation Accuracy: 94%

#### Model 3
- Architecture: 2 convolutional layers (32, 64 filters), 2 dense layers
- Features: BatchNormalization, Data Augmentation, MaxPooling, Early Stopping, Regularization, Dropout
- Validation Accuracy: 91%

#### Model 4
- Identified as the best performing model
- Provides better and more consistent results compared to other models

## Optimization Methods Tested
- Weight Initialization
- Activation Functions
- Optimizers
- Batch Normalization
- Data Augmentation
- Regularization (L1 and L2)
- Dropout
- Early Stopping
- Pooling

## Transfer Learning
- Dataset: Binary Alpha Digits
- Approach: Reshaped to 64x64, added dense layers, unfroze some layers
- Features: Batch normalization, data augmentation (Random Rotation)
- Validation Accuracy: 74% (using base model from Part 2)

## Brand New Binary AlphaDigits Model
- Validation Accuracy: 88%

## Transfer Learning on Binary AlphaDigits
- Validation Accuracy: 91%

## Conclusions
1. Model 4 emerged as the best performing model among custom architectures.
2. Optimization methods showed small improvements when applied individually.
3. Combining multiple optimization methods with complex architectures (like Model 4) is necessary for significant accuracy improvements.
4. Transfer learning proved effective, achieving higher accuracy (91%) compared to training a brand new model (88%) on the Binary AlphaDigits dataset.
5. Using pretrained models with transfer learning can save computational resources and time while maintaining or improving accuracy.
