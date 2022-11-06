## Vehicle Image Dataset Classification 🚗🎇

Implementation with ⇾
- Decision Trees (at various depths and sample leafs)
- Random Forect Classifier (with best decision tree parameters and at various estimators)
- Keras Sequential Model
    - Convolutional 2D (A filter or a kernel in a conv2D layer “slides” over the 2D input data, performing an elementwise multiplication. As a result, it will be summing up the results into a single output pixel.) (dim1, dim2, dim3, dim4) ex. (None, 64, 64, 3) - Learning a total of 32 layers (32, (3,3) - Convolutional 2d layer applies a filter to an input to create a feature map that summarizes the presence of detected features in the input (CNN for short, is a specialized type of neural network model designed for working with two-dimensional image data) (https://machinelearningmastery.com/convolutional-layers-for-deep-learning-neural-networks/)
    - flatten (dim1, dim2*dim3*dim4) ex. (None, 123008) - flattening multi-dimensional input into a single dimension
    - Multiple dense layers to reduce dimensionality until (none, 1) as the problem is not multi-label classification 




We use ReLU in hidden layer to avoid vanishing gradient problem and better computation performance , and Softmax function use in last output layer
ReLU helps to prevent the exponential growth in the computation required to operate the neural network


Dense layer is the regular deeply connected neural network layer. It is most common and frequently used layer. Dense layer does the below operation on the input and return the output. output = activation(dot(input, kernel) + bias)

Dense Layer is simple layer of neurons in which each neuron receives input from all the neurons of previous layer, thus called as dense. Dense Layer is used to classify image based on output from convolutional layers.


A dense layer also referred to as a fully connected layer is a layer that is used in the final stages of the neural network. This layer helps in changing the dimensionality of the output from the preceding layer so that the model can easily define the relationship between the values of the data in which the model is working.
