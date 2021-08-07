# Covid_detection_XRAY
## Convolutional Neural Network
CNN is one of the most popular algorithm for image processing and predictions.The role of CNN is to reduce the images into a form which is easier to process and yet getting good prediction results.It consisits of a number of layers and a feed forward neural network at the end for classification.


![alt text](https://miro.medium.com/max/2000/1*vkQ0hXDaQv57sALXAJquxA.jpeg)


* Convolutional Layer - This layer builds the convolution feature matrix which captures the features of the input image matrix, preserving the spatial and temporal dependencies of the pixels (which could not captured if we just flattened the image matrix and fed it to the FFNN). This convolution operation is done using the kernel/filter matrix which shifts through the whole image and calcutes the matrix multiplication of the kernel and the image matrix and constructs the feauture matrix. The filter/kernel has the same number of color channels as the image and lesser dimensions. The feature matrix can have the same,higher or lower dimensions than the image matrix based on the type of padding.
  * Valid Padding  : reduced dimensions
  * Same Padding  : same/increased dimensions

* Pooling layer - This layer further reduces the dimensions of the feature matrix to make computations easier. After passing through this layer, we get an even smaller matrix. It only extracts the dominant features from the convolutional feature matrix. There are two types of pooling called max and average pooling. if the pooling filter extracts the maximum value from the window then it is called max pooling and if it takes the aversge then the latter. This also reduces the noice.

* ReLu Layer - Rectified Linear Unit is an activation function. It transforms the negative values to 0 and keeps the positive values. This layer can be placed before of after the pooling operation because of commutative rule. 

All these layers form a single layer in CNN. Depending upon the complexity, we can increase the number of these layers to capture more and more features. We train this CNN and the FFNN under the supervised learning model with the X-RAY dataset taken from kaggle and github. Once the parameters are set, we test the model. We get the final feature matrix from CNN and flatten it before passing it to the feed-forward neural network. In the FFNN, we are using sigmoid activation function for the classification purpose.

# Data Pre-processing
The Normal X-RAY images have been taken from kaggle and the infected ones are taken from a github repository. The dataset is divided into train,test and validation parts. We have used shutil python library for file operations. 70 % -> train dataset, 20 % -> test dataset, 10% -> validation dataset

#### The model got 95% test accuracy




