# adversarial-examples

The purpose of this project is dual: primarily, to build a CNN model that can accurately classify input images from the MNIST and CIFAR10 datasets; as an extension, to create adversarial examples that can trick the CNN into mis-classifying the input.

![Illusion](/aes/illusion.jpeg)

## 📗 Introduction

Adversarial examples are inputs to machine learning models that intentionally cause the model to make a mistake; in that sense they're like optical illusions for machines. In this implementation, we create adversarial examples for samples from the MNIST and CIFAR-10 datasets.

The **MNIST** database of *handwritten digits*, available [here](http://yann.lecun.com/exdb/mnist/), has a training set of 60,000 examples, and a test set of 10,000 examples. It is a subset of a larger set available from NIST. The digits have been size-normalized and centered in a fixed-size image. It is one of the most widely used databases for people who want to try learning techniques and pattern recognition methods on real-world data while spending minimal efforts on preprocessing and formatting.

The **CIFAR-10** dataset, available [here](https://www.cs.toronto.edu/~kriz/cifar.html), consists of 60000 32x32 _colour images_ in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images. The dataset is divided into five training batches and one test batch, each with 10000 images. The test batch contains exactly 1000 randomly-selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than another. Between them, the training batches contain exactly 5000 images from each class. The CIFAR-10 classes are:

| Class | Class ID (*Python index*) |
| ------------- | ------------- |
| Airplane  | 0  |
| Automobile  | 1  |
| Bird  | 2  |
| Cat  | 3  |
| Deer  | 4  |
| Dog  | 5  |
| Frog  | 6  |
| Horse  | 7  |
| Ship  | 8  |
| Truck  | 9  |

## 🔑 Prerequisites

Please make sure that you have **Python 3.8.3** or greater installed. The implementation might work with previous versions as well.

In addition, the following python libraries are required; please make sure they are installed and up-to-date.
* numpy
* keras
* tensorflow
* matplotlib
* tqdm

## 👟 Walkthrough

### 🔡 MNIST dataset

A CNN model trained on the MNIST dataset is provided with the `CNN_model_mnist.h5` file. A walkthrough for the creation of the adversarial examples is provided in the form of a Jupyter notebook: `MNIST.ipynb`.

If the user wishes to re-run the cells, it is suggested that they *skip cells in section **2.1. Model Training** since it takes quite some time to run*. Instead, the created model can be loaded from file by running cells in section **2.2. Loading Model from File**, and the user can resume from that point.

### 🐈 CIFAR-10 dataset

A CNN model trained on the CIFAR-10 dataset is provided with the `CNN_model_cifar.h5` file. A walkthrough for the creation of the adversarial examples is provided in the form of a Jupyter notebook: `CIFAR-10.ipynb`.

If the user wishes to re-run the cells, it is suggested that they *skip cells in section **2.1. Model Training** since it takes quite some time to run*. Instead, the created model can be loaded from file by running cells in section **2.2. Loading Model from File**, and the user can resume from that point.
