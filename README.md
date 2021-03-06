# Image-Classification-Deep-Learning
Implemented ***Convolutional Neural Network*** with ***Keras*** for image classification of dogs vs cats (Kaggle Cats &amp; Dogs dataset)

I used Kaggle API to directly load the train and test images and I created the notebook in Google Colab to make use of the GPU that they offered.

Initially, I started with a basic convolutional neural network, where I had 2 blocks of convolution and pooling layers, and then I had the dense neural network. I fitted this model to tha training data and it gave me an accuracy of around 82% on the validation dataset. The test data gave me a log loss of 0.89 .

So the basic CNN model wasn't good enough to classify images very well. I tried other variations of the basic CNN by increasing the neurons, and the number of layers and also using kernel reguarizers. Then I used a pretrained model - ***resnet***. The core idea of ResNet is introducing a so-called “identity shortcut connection” that skips one or more layers. My intial block was the resnet and the next few layers were a dense network consisting of 3 dense layers. I used early stopping method along with kernel regularizer to prevent overfitting of the model to the training data. Relu was used as the activation function.

This model performed very well and gave me an accuracy of around 98% on the validation data and a loss of 0.0593. On the test data, I got a great performance as well. The **log loss score** on the test dataset after uploading on Kaggle is ***0.09***.
