# Implementation of deep learning framework -- Unet, using Pytorch

The architecture was inspired by [U-Net: Convolutional Networks for Biomedical Image Segmentation](http://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/).

---
### Data augmentation

The data for training contains 30 512*512 images, which are far not enough to feed a deep learning neural network. 

### Model

![UNET_architecture](https://github.com/shubhampundhir/UNet/assets/56575094/bed931a6-da03-4848-b176-423f39c052fc)
This deep neural network is implemented with Pytorch, which makes it extremely easy to experiment with different interesting architectures.

Output from the network is a 512*512 which represents mask that should be learned. Sigmoid activation function
makes sure that mask pixels are in \[0, 1\] range.

### Training

The model is trained for 5 epochs.

After 5 epochs, calculated accuracy is about 0.97.

Loss function for the training is basically just a binary crossentropy.


---
