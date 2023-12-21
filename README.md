# Sad or Happy Image Classifier

This is a machine learning project to classify images as sad or happy. It uses a convolutional neural network (CNN) model trained on a dataset of sad and happy images.

## Dataset
The dataset consists of sad and happy images in separate folders. The images were preprocessed to resize them to 256x256 and normalize the pixel values. The dataset was split into 70% training, 20% validation and 10% test sets.

## Model
The model is a CNN with the following layers:

- Convolutional layer with 16 3x3 filters and ReLU activation
- Max pooling layer
- Convolutional layer with 32 3x3 filters and ReLU activation  
- Max pooling layer
- Convolutional layer with 16 3x3 filters and ReLU activation
- Max pooling layer
- Flatten layer
- Dense layer with 256 units and ReLU activation
- Output layer with a single unit and sigmoid activation

The model was trained for 20 epochs using the Adam optimizer and binary cross entropy loss.

## Usage
To classify a new image, resize it to 256x256 and pass it through the trained model to get a prediction 0-1. Values above 0.5 are classified as happy, below as sad.

The trained model is saved in the `models` folder as `imageclassifier.h5`. It can be loaded to make predictions on new images.

## Results
The model achieved 98% precision and 99.6% accuracy on the test set.

