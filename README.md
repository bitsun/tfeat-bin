# tfeat-bin
shallow convolutional neural network based binary local descriptor

This is the pytorch implementation of training a shallow convolutional neural network based binary local descriptor.

TFeat descriptor models proposed in BMVC 2016 paper "Learning local feature descriptors with triplets and shallow convolutional neural networks" is a very successful learning-based local descriptor. It is proved that a simple shallow convolutional neural network is enough for near-duplicate image recognition. However in practice, especially in the context of large image retrieval, it is desirable to compress the learned local descriptor further, preferably with a single visual word id or some binary string. Not surprisingly, simply adding a sign function after the last activation layer works quite well. The reason is that, the activation function tanh stops learning when the activation output is nearly saturated, and this is extactly what binarization want to achieve.
