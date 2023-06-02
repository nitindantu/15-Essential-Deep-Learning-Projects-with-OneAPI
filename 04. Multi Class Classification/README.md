In this code, we're using the CIFAR-10 dataset, which consists of 50,000 training images and 10,000 test images belonging to 10 different classes. The code loads the dataset, preprocesses the images by normalizing pixel values, and performs one-hot encoding on the class labels.

Next, we define the model architecture using the Sequential API from Keras. The model consists of several convolutional layers, max pooling layers, and fully connected layers. The final layer uses the softmax activation function to output class probabilities for each image.

We then compile the model by specifying the optimizer, loss function, and evaluation metric. In this example, we use the Adam optimizer, categorical cross-entropy loss, and accuracy as the evaluation metric.

After compiling the model, we train it using the training data with a batch size of 64 and for 10 epochs. We also use 10% of the training data as a validation set for monitoring the model's performance during training.

Finally, we evaluate the trained model on the test data and print the test loss and accuracy.
