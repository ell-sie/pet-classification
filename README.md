# Dog Breed Classification using Convolutional Neural Networks

This project aims to classify dog breeds using Convolutional Neural Networks (CNNs). CNNs are powerful tools for image classification, capable of learning spatial hierarchies of features, starting from simple patterns like edges and moving to more complex patterns as the layers get deeper. This hierarchical feature learning is particularly well-suited to image classification, where the visual features of an image can vary widely [2].

## Libraries Used

- numpy and pandas for data manipulation
- matplotlib for data visualization
- tqdm for progress tracking
- keras for building and training neural networks
- sklearn for preprocessing data and evaluating models

## Dataset

The dataset used is the "Dog Breed Identification" dataset, consisting of images of various dog breeds. It contains a total of  10,222 images belonging to  120 dog breeds. For this project, a subset of five dog breeds was selected: Scottish Deerhound, Maltese Dog, Afghan Hound, Entlebucher, and Bernese Mountain Dog.

## Model Implementation

- **Baseline Model:** A simple CNN model was implemented without any optimization techniques.
- **Optimized Model:** An optimized CNN model was implemented using three regularization techniques: L1 regularization, L2 regularization, and a combination of both.

## Training and Evaluation

The dataset was split into training, validation, and test sets. Both models were trained using the training set and evaluated on the validation and test sets. Model performance metrics such as accuracy were recorded during training and evaluated after training completion.

## Implementation Details

- **Data Preprocessing:** The labels data was loaded into a dataframe and inspected. The number of images per breed was also counted.
- **Data Augmentation:** To increase the diversity of the training set and reduce overfitting, data augmentation was applied using the `ImageDataGenerator` from Keras.
- **Model Architecture:** The model consists of several convolutional layers, max pooling layers, and dense layers. The convolutional layers are used to detect features in the images, while the dense layers are used for classification. The model uses L1 and L2 regularization to prevent overfitting.
- **Training:** The model was trained for  20 epochs with a batch size of  84. The training process was monitored using the accuracy metric on both the training and validation sets.
- **Evaluation:** After training, the model's performance was evaluated on the test set to assess its ability to generalize to new, unseen data.

## Next Steps

- Further optimize the model architecture to improve performance.
- Experiment with different regularization techniques and data augmentation strategies.
- Apply the model to new datasets or expand the current dataset for better generalization.