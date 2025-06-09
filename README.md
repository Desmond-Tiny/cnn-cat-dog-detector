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

# Model Architecture
- MobileNetV2 pretrained on ImageNet as the base model (with top layers removed).
- Added Global Average Pooling layer.
- Dropout layer with 0.3 rate to prevent overfitting.
- Dense layer with 128 units and ReLU activation.
- Final output layer with 1 neuron and sigmoid activation for binary classification.

## Training
- Optimizer: Adam
- Loss function: Binary crossentropy
- Metrics: Accuracy
- Number of epochs: 10
- Batch size: 32

- 
## Results

Confusion Matrix:

|           | Predicted Cats | Predicted Dogs |
|-----------|----------------|----------------|
| Actual Cats | 1176           | 74             |
| Actual Dogs | 28             | 1222           |

Classification Report:

| Class | Precision | Recall | F1-score | Support |
|-------|-----------|--------|----------|---------|
| Cats  | 0.98      | 0.94   | 0.96     | 1250    |
| Dogs  | 0.94      | 0.98   | 0.96     | 1250    |

Overall Accuracy: 96%

## Usage

```python
# Load the trained model
model = tf.keras.models.load_model('path_to_model.h5')

# Predict on new images
predictions = model.predict(image_batch)


