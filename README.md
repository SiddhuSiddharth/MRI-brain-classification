# Why MRI brain classification?

This process aims to classify based on nearly 280 MRI scanned images. The project aims to create model to classify whether the brain has tumor or not. The prerequisites are knowledge are Computer Vision, TensorFlow, Keras, Activation Functions, ANN and CNN.

The project was inspired from a lack of data that is currently available in the medical field. Creating models like this can tremendously help other data analysts to gather insights.

# Dataset

The Dataset contains nearly 280 MRI scanned images of human brains when and without brain tumour. The Dataset is taken from Kaggle and is gold rated. Although some of the images maybe of varying sizes ultimately we are reducing them down to 224 x 224 pixel width images for better processing. Here is the [link](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection) to the dataset.

![11 no.png](https://user-images.githubusercontent.com/98100916/218330032-7a2ec080-2723-4074-a5c1-4f0abe3ae3a0.png) ![37 no.png](https://user-images.githubusercontent.com/98100916/218330073-4672eb8e-88b9-47ac-9b97-4955e90e4e96.png)

These are 2 image samples from the No category.

### Why do we need computer vision?

Obviously in order to create a model we need numbers. Computer Vision helps us convert pixels into numbers by disintegrating them into simple RGB values and also resizes the images. In this situation we use computer vision to convert BGR values to grayscale and then resize all images.

# Artificial Neural Network

In this portion, we create an ANN, with 2 ReLu hidden layers and 1 softmax hidden layer and calculate loss functions in terms MAE and MSE. But we default to using MSE for the time being. The Flatten function in front of the dense layers is to resize the image every time we pass the input stream of vectors. This is the result obtained after 50 iterations.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/98100916/218331194-b0be6558-fc9c-4141-92e2-938be6988b4f.png">

# Convolutional Neural Network

The $R^2$ value of ANN is consistently high, usually ranging from 0.6 to 0.9 after multiple different sets of iterations. In order to reduce that we introduce CNN as an alternative. The main advantage of CNN is it provides better loss scores for the same no. of iterations. But the cost of 1 iteration is also large. At the end a graph is plotted of actual values vs predicted values for CNN.

<img width="400" alt="image" src="https://user-images.githubusercontent.com/98100916/218331526-226a8545-f9a4-4680-b21d-34104b0be8c2.png">

This is way better than ANN results.
