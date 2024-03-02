# PRODIGY_ML_03
ML Internship at [Prodigy InfoTech](https://prodigyinfotech.dev) 

Task - 03

# support vector machine (SVM) to classify images of cats and dogs
This repository contains code on support vector machine (SVM) to classify images of cats and dogs from the Kaggle dataset.

## Algorithm:

1. **Data Preparation:**
   - The script extracts the contents of two zip files ("cat vs dog train.zip" and "cat vs dog test.zip") containing training and testing images, respectively.
   - The extracted images are stored in the directories specified by `train_dir` and `test_dir`.

2. **Data Augmentation:**
   - ImageDataGenerator is used for data preprocessing and augmentation. It rescales pixel values to the range [0,1] and applies shear, zoom, and horizontal flip transformations to augment the training dataset.

3. **Loading Data:**
   - Flow from Directory is used to load and augment images from the specified directories for both training and testing datasets.

4. **CNN Model Architecture:**
   - A Sequential model is used to build the CNN.
   - Convolutional layers (`Conv2D`) with rectified linear unit (ReLU) activation are used to capture image features.
   - MaxPooling layers reduce the spatial dimensions of the feature maps.
   - A Flatten layer converts the 2D feature maps to a 1D vector.
   - Dense layers with ReLU activation introduce non-linearity, and the final Dense layer uses a sigmoid activation for binary classification.

5. **Model Compilation:**
   - The model is compiled with the Adam optimizer, binary crossentropy loss function (suitable for binary classification), and accuracy as the evaluation metric.

6. **Model Training:**
   - The `fit` function is used to train the model on the training dataset for a specified number of epochs (10 in this case).
   - The validation dataset (`test_generator`) is used to monitor the model's performance during training.

7. **Model Evaluation:**
   - After training, the model is evaluated on the test dataset using the `evaluate` method.
   - The test accuracy is printed.

## Usage:
1) Dataset from Kaggle [Cat vs Dog]( https://www.kaggle.com/c/dogs-vs-cats/data).
2) Used Jupiter Notebook for Python Coding.

## Techniques:
The following techniques are implemented in this project:
- support vector machine (SVM)
