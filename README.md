# MNIST Dataset
#### **Hand-written Digit Classification with a Convolutional Neural Network**

Dataset Source: http://yann.lecun.com/exdb/mnist/

Implementing a CNN and training it on MNIST dataset. 

The CNN model has the following architecture: 

<pre>Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 14, 14, 16)        416       
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 14, 14, 32)        4640      
_________________________________________________________________
batch_normalization (BatchNo (None, 14, 14, 32)        128       
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 7, 7, 32)          9248      
_________________________________________________________________
batch_normalization_1 (Batch (None, 7, 7, 32)          128       
_________________________________________________________________
dropout (Dropout)            (None, 7, 7, 32)          0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 7, 7, 64)          18496     
_________________________________________________________________
batch_normalization_2 (Batch (None, 7, 7, 64)          256       
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 4, 4, 64)          36928     
_________________________________________________________________
batch_normalization_3 (Batch (None, 4, 4, 64)          256       
_________________________________________________________________
dropout_1 (Dropout)          (None, 4, 4, 64)          0         
_________________________________________________________________
flatten (Flatten)            (None, 1024)              0         
_________________________________________________________________
dense (Dense)                (None, 256)               262400    
_________________________________________________________________
batch_normalization_4 (Batch (None, 256)               1024      
_________________________________________________________________
dropout_2 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 10)                2570      
=================================================================
Total params: 336,490
Trainable params: 335,594
Non-trainable params: 896</pre>

After training for 23 epochs, it obtained ``99.38%`` accuracy on the test set.

The trained model is available in ``./trained_model/model.h5`` file.

Learning curves is as follows:

![learning_curves](https://user-images.githubusercontent.com/77887540/235900916-62065606-4fc8-4914-8978-49bfe25f74d5.png)

