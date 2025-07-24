# 🧠 Fashion-MNIST Classification with Keras

This repository contains an image classification project using the [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset and Keras.  
The goal is to train a neural network that can recognize clothing items such as shoes, bags, shirts, and more.

---

## 👕 About the Dataset

Fashion-MNIST is a popular benchmark dataset for machine learning.  
It includes 70,000 grayscale images of fashion products from 10 categories.

- 📦 **Classes**:
  - `0` T-shirt/top  
  - `1` Trouser  
  - `2` Pullover  
  - `3` Dress  
  - `4` Coat  
  - `5` Sandal  
  - `6` Shirt  
  - `7` Sneaker  
  - `8` Bag  
  - `9` Ankle boot  

- 🖼️ **Image Size**: 28x28 pixels  
- 🌑 **Color Mode**: Grayscale  
- ✂️ **Split**:  
  - 60,000 training images  
  - 10,000 test images  

---

## 🧠 Model Overview

The model is built using the `Sequential` API in Keras:

```python
model = keras.Sequential([
    layers.Flatten(input_shape=(28, 28)),
    layers.Dense(128, activation='relu'),
    layers.Dense(64, activation='relu'),
    layers.Dense(10, activation='softmax')
])
