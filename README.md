# Implementation of deep learning framework -- Unet, using Keras

The architecture was inspired by [U-Net: Convolutional Networks for Biomedical Image Segmentation](http://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/).

---
### Data augmentation

The data for training contains 30 512*512 images, which are far not enough to feed a deep learning neural network. I use a module called ImageDataGenerator in keras.preprocessing.image to do data augmentation.

See dataPrepare.ipynb and data.py for detail.


### Model

!(https://www.google.com/url?sa=i&url=https%3A%2F%2Ftowardsdatascience.com%2Funet-line-by-line-explanation-9b191c76baf5&psig=AOvVaw0jVPOES-DwkZZqGpDVBj8G&ust=1712640943405000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCJCdgezysYUDFQAAAAAdAAAAABAE))

This deep neural network is implemented with Keras functional API, which makes it extremely easy to experiment with different interesting architectures.

Output from the network is a 512*512 which represents mask that should be learned. Sigmoid activation function
makes sure that mask pixels are in \[0, 1\] range.

### Training

The model is trained for 5 epochs.

After 5 epochs, calculated accuracy is about 0.97.

Loss function for the training is basically just a binary crossentropy.


---
