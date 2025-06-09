# 🐾 Cats vs. Dogs Classifier using CNN

This project uses Convolutional Neural Networks (CNNs) to classify images of cats and dogs from the [Microsoft PetImages dataset](https://www.microsoft.com/en-us/download/details.aspx?id=54765). The dataset contains 25,000 images (12,500 cats and 12,500 dogs), which are used to train a deep learning model capable of binary classification.

## 📦 Dataset

The dataset includes:

- 12,500 cat images  
- 12,500 dog images  

All images vary in size and quality, and some corrupted files are removed during preprocessing.

## 🏃‍♂️ How to Run
Clone this repo or open it in Google Colab

Download and unzip the cats-and-dogs.zip dataset

Install the requirements (pip install -r requirements.txt)

Run the notebook to train and evaluate the model

## 🧠 Model Architecture

The CNN consists of:

- 3 Convolutional layers (with ReLU and `padding='same'`)  
- 1 Max Pooling layer  
- Fully connected (dense) layers  
- Final sigmoid output layer for binary classification  

```python
Conv2D(32, (3,3)) → ReLU  
Conv2D(32, (3,3)) → ReLU  
Conv2D(32, (3,3)) → ReLU  
MaxPool2D(2,2)  
Flatten  
Dense(64) → ReLU  
Dense(32) → ReLU  
Dense(1) → Sigmoid

