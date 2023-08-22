# Exercise Overview

The exercise report provides a comprehensive overview of deep learning concepts and practical applications. The theoretical part discusses the structure and calculations involved in MLPs, convolutional networks, and batch normalization layers. It also explains the gradients in a one-dimensional batch normalization layer. The practical section focuses on training a regularized LeNet5 Convolutional neural network using different hyperparameters and regularization techniques, such as dropout, batch normalization, and weight decay. The results are presented through convergence graphs and accuracy tables, highlighting the performance of each regularization method. The report concludes by emphasizing the importance of regularization in improving model accuracy and preventing overfitting.

Overall, the exercise report offers a valuable exploration of deep learning principles and their practical implementation, providing insights into both theoretical concepts and empirical results.

--- 

# Practical Part - Fashion MNIST Classification with LeNet5

This repository provides an implementation of the LeNet5 architecture for effectively classifying images from the Fashion MNIST dataset.

## Dataset
The Fashion MNIST dataset comprises grayscale images of size 28x28, representing various clothing items such as T-shirts, trousers, sneakers, etc. The dataset consists of 60,000 training images and 10,000 testing images.

## Model
The LeNet5 architecture is utilized for accurate image classification. It consists of three convolutional layers followed by a fully connected layer. The input to the network is a 28x28 image, and the output corresponds to one of the ten possible classes.

## Usage
Before running the code, ensure that the relevant paths are correctly set:
- Directory for models.
- Directory for plots (optional if you desire to visualize the convergence graphs we have saved).

Choose one of the following options for training/loading the model:
- Load a pre-trained model and test it (flag = 1).
- Train a new model (flag = 0).

Additionally, select the desired regularization method from the following options:
- 'Batch_Normalization'
- 'Dropout'
- 'Weight_Decay'
- 'Without_Regularization'

All modifications can be made within the 'For the Instructor' cell. After making the necessary changes, click on 'Run all' or use the ctrl+F9 command. Please note that the default parameters are as follows: batch size = 100, epochs = 60, learning rate = 1e-4. To modify these parameters, navigate to the 'Globals' cell.

## Results
The final accuracy of the model on both the train and test datasets is printed below each graph. The accuracy values for each regularization method are as follows:
- Without regularization: Train accuracy = 92.44% | Test accuracy = 89.27%
- Weight decay: Train accuracy = 91.35% | Test accuracy = 89.30%
- Dropout: Train accuracy = 90.07% | Test accuracy = 88.55%
- Batch normalization: Train accuracy = 95.16% | Test accuracy = 90.16%

