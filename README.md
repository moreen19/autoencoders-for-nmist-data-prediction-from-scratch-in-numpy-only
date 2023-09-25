# PREDICTION AND CLASSIFICATION WITH AUTOENCODERS AND CLASSIFIER(MLP)- MNIST DATA SET
Author:Moreen Owino

In this project i use a simple autoenencoder and a denoiser as feature extractors for the mnist data set efore using an mlp to classify the autoencoded test dataset digits.All these have been coded from scratch using python-numpy and no keras or pytorch.

In this project i use two different types of autoencoders i.e A simple basic two layer feedforward autoencoder and a denoising autoencoder as feature extractors for my mnist xtrain and x_test sets and use this lower dimensional output as input to my classifier together with the y_targets and use that to train my classifier the use the trained model to predict the digit labels of the encoded test set.

**Auto encoders:**

Autoencoders are a type of neural network that can learn to encode input data into a lower-dimensional representation, and then decode that representation back into the original input data. The goal of an autoencoder is to learn a compressed representation of the input data that captures the most important features and patterns, while discarding the less important details.

The basic architecture of an autoencoder consists of two parts: an encoder and a decoder. The encoder takes in the input data and produces a lower-dimensional representation (also known as a latent code) that captures the essential features of the input. The decoder then takes this representation and produces an output that is as close as possible to the original input.Autoencoders have many practical applications, such as dimensionality reduction, data compression, and image denoising. They can also be used as a generative model to generate new data points that are similar to the original data.

**Multi layer perceptrone(MLP):**

A multi-layer perceptron (MLP) is a type of artificial neural network that is commonly used for supervised learning tasks, such as classification or regression. MLPs consist of multiple layers of interconnected nodes (perceptrons) that process the input data and produce an output.

The input layer of an MLP receives the input data, and each node in the input layer represents a feature of the input. The hidden layers of the MLP perform a series of nonlinear transformations on the input data, with each layer transforming the output of the previous layer. The final layer of the MLP produces the output, which can be either a classification result or a continuous value for regression.Each node in an MLP typically applies a nonlinear activation function to the weighted sum of its inputs. This activation function introduces nonlinearity into the network, allowing it to model complex relationships between the input and output.

![image](https://github.com/moreen19/autoencoders-for-nmist-data-prediction-from-scratch-in-numpy-only/assets/97608840/68deaceb-ccac-4fa0-bd3e-696cecb7291a)

![image](https://github.com/moreen19/autoencoders-for-nmist-data-prediction-from-scratch-in-numpy-only/assets/97608840/fcedadaf-b771-413d-ad0a-20b18706b338)

## Discussion

From the output of the classifier the simple feed forward autoencoder seems to have produced the best output considering that it has a lower dimension than the original data sets.With encoder outputs of 39260000 and 39210000 it was able to achieve the same training accuracy of 99.998333 as the original 78460000 and 78410000 data sets over the same number of epochs.

The simple feed forward encoder outputs were obtained after only 10 epochs of training which suggests that with more training the results might have been even better than what was observed above.

The output from the denoising encoder which had the same lower dimensions of 39260000 and 39210000 did not perform very well and had a training accuracy of about 80% for the same number of epochs.Though this might be because i only trained the autoencoder over 10 epochs and did not give it enough training time so the results might have been better.

The project has showed that autoencoders can indeed be used as feature extractors for machine learning classification problems or for data preparation or denoising , since we see that the outputs of the trained encoders though having lower dimensions are able to achieve similar or maybe even better accuracy than the original data sets.

