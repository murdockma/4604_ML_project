## Vehicle Image Dataset Classification 🚗🎇

Implementation with ⇾
- Decision Trees (at various depths and sample leafs)
- Random Forect Classifier (with best decision tree parameters and at various estimators)
- Keras Sequential Model
    - Conv2d: Using Convolutional 2d layer, learning a total of 32 layers with a 3x3 kernel size (i.e., 2D width and height of the filter). Input shape of (64, 64, 3), which is the dimensions of our image data. This layer essentially transforms our input (image) into an abstract representation that the densely connected layers can then use to generate a classification. Rectified linear activation function (reLU) is used to isolate the features by outputting 0 for negative inputs, indicating the pixel values which are not important.
    - Flatten: Dense layers can only deal with one dimensional data, so we need to convert our multidimensional feature map with the flatten layer in order to get the one dimensional shape required for the dense layers.
    - Dense x 3: Multiple dense layers to reduce dimensionality until shape is binary, since our predictions are considered binary classification (Vehicle or Non-Vehicle). ReLU is used in hidden layers primarily for better computational performance and is one of the most commonly used activation functions for hidden layers in CNN. Softmax is used in last dense layer which allows us to generate a probability distribution in order to understand which classification is more likely. The dense layers are the regular deeply connected layers that perform the operation activation(dot(input, kernal) + bias).
